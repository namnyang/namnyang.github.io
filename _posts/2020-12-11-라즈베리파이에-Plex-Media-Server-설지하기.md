이번 포스트에서는 라즈베리파이에 Plex Media Server를 설치해봅시다



###### Plex Media Server 

Plex Media Server는 영상을 스트리밍으로 볼 수 있게 해주는 서버입니다

RPI3는 약간 버거울 수 있지만 RPI4부터는 원활하게 동영상 시청이 가능합니다



## Plex Media Server 설치

일단 업그레이드 부터!

```terminal
sudo apt-get update
sudo apt-get upgrade
```

Repository를 추가합니다

```terminal
sudo apt-get install apt-transport-https
curl https://downloads.plex.tv/plex-keys/PlexSign.key | sudo apt-key add -
echo deb https://downloads.plex.tv/repo/deb public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list
```

Repository list를 업데이트 하고, Plex Media Server를 설치합니다

```terminal
sudo apt-get install plexmediaserver
```

설치 중에 옵션을 물어보면 Y를 선택해 줍니다



만약 이런 경고가 나온다면, `systemctl daemon-reload`를 실행해 줍니다

```
Warning: The unit file, source configuration file or drop-ins of plexmediaserver.service changed on disk. Run 'systemctl daemon-reload' to reload units.
```



## Plex Media Server 접속

웹 브라우저에서 `http://라즈베리파이IP:32400/web/index`에 접속하면 됩니다



## 유지보수(?)

#### 부팅시 자동실행

만약 라즈베리파이를 재부팅한 후 Plex Media Server가 자동으로 실행되지 않는다면 service 상태를 확인해 보고

```terminal
systemctl status plexmediaserver
```

Fail 메세지가 나오면 오류 메세지를 보고 오류를 해결하면 됩니다

#### 업데이트

나중에 새로운 버전이 출시되면 deb파일을 다운받은 뒤

아래 명령어로 설치하시면 됩니다

```terminal
sudo dpkg -i plexmediaserver*.deb
```

