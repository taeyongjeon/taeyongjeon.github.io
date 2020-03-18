---
title: 유튜브 다운로더 youtube-dl
date: 2020-02-21 00:00
categories:
- [프로그래밍, 리눅스]
mathjax: true
---

# 설치
sudp pip3 install youtube-dl
sudo apt-get install ffmpeg

# 옵션
-f : 파일 형식을 지정합니다. "best", "mp4", "webm", "flv" 등.
-x : 영상을 mp3 등 음악 파일로 받습니다.
--audio-format "mp3" : 파일 형식을 지정합니다. "aac" "best" "flac" "mp3" 등. 반드시 -x 옵션과 같이 써야 합니다.

예시
* youtube-dl https://www.youtube.com/watch?v=KMU0tzLwhbE
    * 기본 형태.

* youtube-dl -f best https://www.youtube.com/watch?v=KMU0tzLwhbE
    * 받을 수 있는 최고화질로 영상을 받습니다.

* youtube-dl -f best[height=720] https://www.youtube.com/watch?v=KMU0tzLwhbE
    * 720p 화질로 영상을 받습니다. 영상 화질이 720p가 없는 경우 다운로드가 실패합니다.

* youtube-dl -f mp4 https://www.youtube.com/watch?v=KMU0tzLwhbE
    * mp4 형식으로 파일을 받습니다.

* youtube-dl -x --audio-format aac https://www.youtube.com/watch?v=KMU0tzLwhbE
    * aac 파일(오디오)로 다운로드합니다.
    * aac가 mp3보다 음질, 용량 면에서 더 좋다고 합니다.

# 참고문헌
[Youtube-dl: Python not found (18.04)](https://askubuntu.com/questions/1037666/youtube-dl-python-not-found-18-04)
[ffprobe or avprobe not found. Please install one](https://stackoverflow.com/questions/30770155/ffprobe-or-avprobe-not-found-please-install-one)
[acc 256이 mp3 320보다 음질이 더 좋습니다.](https://www.clien.net/service/board/cm_iphonien/11726569)
