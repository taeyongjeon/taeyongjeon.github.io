---
title: 리눅스 우분투 Git 사용법
date: 2020-02-07 23:51:20
tags:
categories:
- [프로그래밍, 리눅스]
---

## 설치

```bash
sudo apt install git
```

## 설정
```bash
git config --global user.name John Doe
git config --global user.email johndoe@example.com

vim ~/.gitconfig # 잘 설정되었는지 확인한다.
```

만약 정보를 잘못 입력했다면 다음 명령어로 일괄 삭제할 수 있다.
```bash
git config --global --unset-all user.name
git config --global --unset-all user.email
```

## 원격 -> 로컬 최초 다운로드 : clone
mkdir 명령어로 폴더를 만들 필요가 없다.
주소는 각 리포지토리에서 Clone or download를 누르면 복사할 수 있다.
```bash
git clone https://github.com/facebook/react-native.git
```

## 원격 <-> 로컬 일상작업 : pull / commit / push
여러 사람들이 함께 개발한다면 git pull로 변경사항이 없는 지 업데이트한다.
```bash
git pull
username 입력
비밀번호 입력
```

코드를 수정했다면 원격 저장소에 add, commit, push로 올릴 수 있다.
```bash
git add filename.txt
git commit -m "update filename.txt" # -m은 commit 코멘트 작성 옵션.
git push
username 입력
비밀번호 입력
```

## 기타 : SSH Key 인증 : pull, push 때 username과 비밀번호 안 물어보게 하기
1. 먼저 공개키를 생성한다.
```bash
ssh-keygen -t rsa -C "johndoe@gmail.com"
엔터
엔터
cd ~/.ssh
cat id_rsa.pub
출력되는 내용을 전부 복사한다.
rm id_rsa.pub # 공개 키는 삭제한다.
```
1. [Settings - SSH and GPG Keys](https://github.com/settings/keys)로 이동한다.
1. Title은 아무거나 입력, keys는 방금 복사한 내용을 붙여넣기한 뒤 Add SSH Key 클릭.
1. 설정은 모두 끝났고 다음 작업을 수행하면 된다.
    1. 아직 clone되지 않은 리포지토리
        1. Clone or download를 누르고 Use SSH를 눌러 나오는 링크를 복사한다.
        1. 이걸로 git clone git@github.com:facebook/react-native.git
        1. 이제 pull, push 등이 별도 인증이 필요없어진다.
    1. 이미 clone된 리포지토리
        1. Clone or download를 누르고 Use SSH를 눌러 나오는 링크를 복사한다.
        1. 해당 폴더 이동 후 git remote set-url origin git@github.com:facebook/react-native.git
        1. 이제 pull, push 등이 별도 인증이 필요없어진다.

## 참고자료
[SSH KEY로 Github 인증하기](https://zeddios.tistory.com/120)
