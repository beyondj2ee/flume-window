flume-window
============

Flume 배포 버전은 기본적으로 Linux 버전으로 배포가 됩니다.
만약 window 환경에서 사용을 하려면 
소스를 받아서 다시 빌드/패키징 과정을 거쳐야 합니다.

하지만 Flume을 빌드 하기 위해서는 
자바 와 메이븐에 익숙할 필요가 있습니다.
그래서 제가 메이븐으로 window 환경에 맞는
버전으로 빌드/패키징 되어진 버전을 만들었습니다.

Flume Packaging Version : 1.4.0


(1) <strong>선행 조건</strong>

- JDK 1.6 이상 설치

(2) 패키지 다운로드

- C:/flume 디렉토리 생성
- git clone https://github.com/beyondj2ee/flume-window.git 또는
Github 오른쪽 메뉴에 "Download Zip" 다운로드 후 압축 해제

![ScreenShot](http://beyondj2ee.pbworks.com/w/file/fetch/67630145/%EC%9D%B4%EB%AF%B8%EC%A7%80%203%21%40%23.png)

(3) 환경 변수 설정

clone 또는 압축 해제된 디렉토리 기준으로 환경 변수를 추가 합니다.
![ScreenShot](http://beyondj2ee.pbworks.com/w/file/fetch/67630181/%EC%9D%B4%EB%AF%B8%EC%A7%80%201%21%40%23.png)

(4) Flume 실행 하기

"How to Run.txt" 파일의 내용을 복사 해서 실행 한다.

java -Xmx20m -Dlog4j.configuration=file:///%FLUME_HOME%\conf\log4j.properties -Dflume.root.logger=DEBUG,console -cp "%FLUME_HOME%\lib\*" org.apache.flume.node.Application -f %FLUME_HOME%\conf\flume.conf -n agent

아래의 그림처럼 출력되면 설치가 완료.
※ 자세한 설정은 http://flume.apache.org/FlumeUserGuide.html 참고

![ScreenShot](http://beyondj2ee.pbworks.com/w/file/fetch/67630203/%EC%9D%B4%EB%AF%B8%EC%A7%80%202%21%40%23.png)





