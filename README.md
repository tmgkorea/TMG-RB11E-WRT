설치방법
winscp 혹은 ftp 프로그램을 이용해서 무선통신모듈로 디렉토리를 카피한다

powershell 또는 다른종류의 터미널 프로그램을 통해서 마스터 또는 클라이언트 모듈에 접속한다.

자동실행
app_info 파일을 /root 경로에 카피한다.

ap의 경우
cp m.init.d/app_daemon /etc/init.d
chmod +x /etc/init.d/app_daemon

client의 경우
cp c.init.d/app_daemon /etc/init.d
chmod +x /etc/init.d/app_daemon

웹 GUI 적용
cp -r luci-static /www/luci-static

커널 업데이트
sysupgrade -F -c -v tmgk-snapshot-*squahfs-sysupgrade.bin
