# AI-Research-by-Raspberry-Pi
AI Research by Raspberry Pi

라즈베리파이 OS 및 Tensorflow 설치
===
20201102 김현빈

# 서론
본 보고서를 작성은 이미 설치과정을 모두 완료한 후 작성한 보고서로 그 과정의 사진 없이 과정만을 설명하여 설치 시 참고할 수 있도록 한다.
##설치과정
1. SD 카드 초기화
라즈베리 OS 설치를 위해서는 32G 이상의 메모리가 권장되어 SD카드를 포맷해주는 과정이 필요한데 초기 상태의 SD카드는 별도의 포맷 과정이 필수는 아닌 것 같습니다.

1-1. SD카드 포맷 방법 
>    >
https://www.sdcard.org/downloads/formatter/sd-memory-card-formatter-for-windows-download/

위 링크를 참조하여 라이선스 계약 문서 페이지 최하단 Accept 버튼을 통해 포맷 프로그램 설치 후 포맷 진행


포맷 프로그램 실행 창
참고: 32GB 기준 SDHC (High Capacity)
     64GB 기준 SDXC (eXtended Capacity)
2. 라즈베리OS 설치
https://www.raspberrypi.com/software/

위 링크를 참조하여 라즈베리 OS 설치


Download for Windows 버튼을 눌러 설치 진행.

설치된 Imager 프로그램 실행화면 구성

설치 과정

1. 저장소 선택 버튼을 눌러 OS를 설치할 SD카드를 선택.

2. 운영체제 OS 선택 버튼을 눌러 Raspberry Pi OS (other) 선택.

3. Raspberry Pi OS (64-bit) 선택

4. 쓰기 버튼 클릭


설치 확인 과정
설치가 완료된 SD카드를 안전하게 제거 후 라즈베리파이에 SD 카드를 삽입한 후 태블릿과 라즈베리 파이를 연결한다.

태블릿과 라즈베리파이가 연결된 모습

태블릿에 전원을 연결한 후 초기설정 
(유저네임, 비밀번호 및 와이파이 연결과정 –저는 해당 과정을 이미 완료하여 사진자료 X) 





설정 완료 후 초기화면 
---
@참고@ 
가상키보드:
CMD창에서 sudo apt-get install matchbox-keyboard를 입력 후 설치 후 좌측 상단 라즈베리마크 버튼을 클릭 후 보조도구로 들어가면 “가상키보드”를 사용할 수 있다.

하지만 사용하는데 있어 매끄러운 느낌을 받지는 못하여 저는 별도의 블루투스 키보드를 연결하여 사용 중.

WIFI 연결 오류:
처음 설정시는 정상적으로 와이파이를 잡았었는데 재부팅시 와이파이 목록이 전혀 안뜨거나 목록이 표시되더라도 연결시 무한 로딩 현상이 발생하여 찾아본 결과 지역을 KR ->GB 로 변경하면 해결 됨. 다른 방법도 존재함, 
---





TensorFlow

부팅된 라즈베리 OS의 우측 상단 Cmd 창을 열어 
1. pip install tensorflow-aarch64 –f http://tf.kmtea.eu/whl/stable.html 입력 후 설치

2. sudo pip3 install numpy 입력 후 numpy라이브러리 설치

3. import tensorflow as tf 입력 후 에러확인



참고자료
1.https://cafe.naver.com/vl/4373 - 텐서플로우 설치 및 에러확인 과정.
2.https://blog.naver.com/handzfree/221570847486 - 가상키보드
3.https://miinsun.tistory.com/28 -와이파이 오류 해결
4.https://zifmfmphantom.tistory.com/113 -라즈비안 설치 과정 및 SD카드 포멧














