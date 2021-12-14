# playtimeboost
AWS(Amazon Web Services)와, ASF(ArchiSteamFarm)를 이용해 가상 윈도우에서 24/7 플레이타임부스트를 가능하게합니다.

<hr/>

참조:
- [1] https://github.com/JustArchiNET/ArchiSteamFarm/releases/tag/5.2.0.10 - ASF

- [2] https://kwonsaw.tistory.com/323 - AWS 가상 윈도우서버 구축

- [3] https://github.com/Jessecar96/SteamDesktopAuthenticator/releases/tag/1.0.10 - 자동 2FA

<hr/>
STEP 1 AWS 서버 구축 ( 해외결제가 지원되는 카드가 필요하다.)

- [1] [AWS 회원가입](https://aws.amazon.com/ko/free/?trk=fa2d6ba3-df80-4d24-a453-bf30ad163af9&sc_channel=ps&sc_campaign=acquisition&sc_medium=ACQ-P|PS-GO|Brand|Desktop|SU|Core-Main|Core|KR|KR|Text&ef_id=Cj0KCQiA2NaNBhDvARIsAEw55hg6XgL93SNEdE7REvQvuF-HlfhInFwqRsxZGSU9E5pis5cOWERkL-gaAo1TEALw_wcB:G:s&s_kwcid=AL!4422!3!563761819834!e!!g!!aws&ef_id=Cj0KCQiA2NaNBhDvARIsAEw55hg6XgL93SNEdE7REvQvuF-HlfhInFwqRsxZGSU9E5pis5cOWERkL-gaAo1TEALw_wcB:G:s&s_kwcid=AL!4422!3!563761819834!e!!g!!aws&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)
- [2] Amazon Machine Image(AMI) 선택 ![12](https://user-images.githubusercontent.com/46117865/145716377-03d439e6-6099-4257-8134-314e96122b15.png)
- [3] 인스턴스 유형 선택 ![13](https://user-images.githubusercontent.com/46117865/145716379-b4de601e-0ba9-43a7-9520-3a7eb6294c52.png)
- [4] 생성 ![16](https://user-images.githubusercontent.com/46117865/145716555-014faf82-bcaf-4ea5-99f5-32fdfaec7cbc.png)
- [5] 생성된 aws 를 우클릭 후, 연결을 눌러서 RDP 클라이언트를 받아야한다. ![15](https://user-images.githubusercontent.com/46117865/145716445-59b5f566-9551-400f-ae6d-5156de766e70.png)
- [6] 다운로드 받은 원격파일 (EC2~ 로 시작함) 을 실행하고, 암호키를 입력하라는 창이 뜬다. RDP 클라이언트를 다운받는곳 에서 암호 가져오기 탭을 연 후, 암호키(blabla.pem)를 메모장으로 열어서 입력한 후 해독하기 버튼을 통해 얻은 암호를 EC2 파일에 넣어주면 된다. 
- [7] WINDOW 10 기반의 가상서버가 만들어졌다. 가상서버에서 먼저 [이것](https://kwonsaw.tistory.com/322)을 해주길바람.


STEP 2 [ASF](https://github.com/JustArchiNET/ArchiSteamFarm/releases/tag/5.2.0.10) 설정 (반드시 가상윈도우 에서 해야한다.)
- [1] [이것](https://justarchinet.github.io/ASF-WebConfigGenerator/#/) 으로 자신의 계정 PROFILE 을 만든다.
- [2] ASF 를 압축해제 한 후 ASF 를 한번 실행하여 폴더내에 생성된 CONFIG 폴더에 자신의 프로필 파일을 넣어준다.
- [3] ASF 파일을 실행한 후 UI html 파일을 열어준다 ![17](https://user-images.githubusercontent.com/46117865/145717185-76f4e4ac-9808-43c3-be47-418e83f6d680.png)
- [4] SETTINGS 에서 STEAM ID 와 PW 를 설정 해 주고 GamesPlayedWhileIdle 에서 플레이타임 부스트를 하고싶은 게임의 APP ID 를 찾아서 등록해준다.
- [5] DONE

STEP 3 So how does it work?
> aws 에서 ASF 를 켜두면 24/7 가동한다. 이게 끝임. 게임을 껏다 켜도 AUTORESTART 기능으로 인해 관리를 안해주어도 계속 돌릴수있음. 
autorestart 과정에서 2fa 인증이 필요한데, 이게 restart 할때마다 계속 입력해주어야함. STEP 3 에서는 이것을 자동화 하는 방법을 서술할거임.
>[참조](https://github.com/JustArchiNET/ArchiSteamFarm/wiki/Two-factor-authentication)
