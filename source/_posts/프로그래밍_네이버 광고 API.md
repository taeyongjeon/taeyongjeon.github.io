---
title: 네이버 광고 API
date: 2020-01-19 15:27:56
tags:
categories:
- [프로그래밍, Python]
---
<iframe width="640" height="360" src="https://www.youtube.com/embed/LjG7-5kbevo" frameborder="0" gesture="media" allowfullscreen=""></iframe>

* 이번 주말을 즐겁게 보내게 해 준 노래.

## API 개요
* 구글 API, 페이스북 API, 트위터 API 그리고 네이버 API는 REST API이다.
* API는 프로그램을 다루는 환경을 말한다. 키보드와 마우스로 컴퓨터를 다루면 키보드, 마우스는 API이다.
* REST는 API가 사용되는 형태를 말한다. 즉, "컴퓨터의 API"라고 하면 "키보드, 마우스, 모니터, 프린터...등의 컴퓨터를 다루는 수단들"이라 할 수 있다. REST API는 "REST의 규칙을 따르는 수단들"을 말한다.
* REST의 규칙이란 다음을 말한다. 첫재, 자원 식별자(URI, URL아님)로 접속할 수 있을 것. 둘째, HTTP Method(GET, POST 등)를 접속 수단으로 쓸 것. 셋째, 서버는 요청에 대해 JSON, XML, TEXT등의 방법으로 대한 응답(Representation)할 것.
* 예로, https://www.facebook.com/youtube/ 라는 링크는 REST API가 아니다. 그러나 https://graph.facebook.com/youtube/ 라는 링크는 REST API이다(자세한 정보를 보려면 토큰이 필요하다.). 왜냐하면 별도의 URI인 graph로 접속하며, HTTP 메소드로 주고받고(쉽게 말하자면 웹 브라우저로 들어갈 수 있다는 뜻이다), JSON 파일로 답신하기 때문이다.
## 네이버 광고 API 개요
* 네이버 공개 API와 별개의 API이다.
* 네이버 API와 달리 헤더가 좀 더 복잡하다.

## 실제 코드 구현
### 1) 헤더 만들기 : 연관키워드 API(RelKwdStat)
```python
import hashlib
import hmac
import base64
import time

# X-API-KEY : 네이버 광고 - 도구 - API 사용 관리 메뉴에서 "엑세스라이선스"의 값.
x_api_key = "0100040080618b186cb85dadee1530d97b60f2ab23b4f276400f282f60de1908671b58d46c"

# X-CUSTOMER : 네이버 광고 - 도구 - API 사용 관리 메뉴에서 "CUSTOMER_ID"의 값.
x_customer = "1234567"

# X-Timestamp : 현재 시간 * 1000을 반올림한 자연수 값.
x_timestamp = str(round(time.time() * 1000))

# secret_key : 네이버 광고 - 도구 - API 사용 관리 메뉴에서 "비밀키"의 값.
# 각 API 문서 상단에는 HTTP request가 있고, 이 때의 요청방식이 method이다.
# GET /keywordstool에서 GET은 method, /keywrodstool은 uri이다.
secret_key = "AQAAAACL9gAB059HwcGtmSLe1fLx39CeoPPUGW8kqkTehLogeg=="
method = "GET"
uri = "/keywordstool"

# X-Signature
# : X-Timestamp, method, uri 값을 점(.)으로 연결한 뒤 HmacSHA256 알고리즘으로 암호화한 후 Base64로 인코딩한 값.
sign = "%s.%s.%s" % (x_timestamp, method, uri)
signature_encrypted = hmac.new(
    secret_key.encode(), sign.encode(), hashlib.sha256
).digest()
x_signature = base64.b64encode(signature_encrypted).decode()

headers = {
    "X-API-KEY": x_api_key,
    "X-CUSTOMER": x_customer,
    "X-Timestamp": x_timestamp,
    "X-Signature": x_signature,
}

print("X-API-KEY:%s" % x_api_key)
print("X-CUSTOMER:%s" % x_customer)
print("X-Timestamp:%s" % x_timestamp)
print("X-Signature:%s" % x_signature)
```

### 2) 파라미터 만들기 : 연관키워드 API(RelKwdStat)
```python
params = {"hintKeywords":"마스크,마스크시트"}
```
* 네이버 광고 API는 무엇이 필수이고 무엇이 필수가 아닌지 가르쳐주지 않는다. 그래서 POSTMAN 등으로 API를 테스트해볼 필요가 있다.
* 연관키워드 API(RelKwdStat)의 경우 필수 파라미터는 키워드뿐이다.

### 3) GET 요청하기
```python
import requests
import json

BASE_URL = "https://api.naver.com" # 네이버 광고 API의 기본 URL이다.
uri = "/keywordstool"
request_url = BASE_URL + uri

response = request.get(request_url,headers=headers,params=params)

keyword_info = json.loads(response.text)

print(keyword_info)
```

## 맺으며
* 위와 같은 방식대로 다른 코드도 구현할 수 있겠다.
* 이미 완성된 리포지토리가 있으니 필요한 경우 참고자료의 링크를 참고하면 된다.

## 참고자료
* [REST란? REST API란? RESTful이란? heejeong Kwon](https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html)
* [헤더에 관한 대부분의 코드는 이곳을 참고했다](https://github.com/devkingsejong/python-PowerNad)
* [Access Key Id와 맵핑되는 SecretKey로 암호화한 서명 / HMAC 암호화 알고리즘은 HmacSHA256 사용](https://docs.ncloud.com/ko/apigw/apigw-2-5.html)
