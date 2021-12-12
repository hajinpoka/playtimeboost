# playtimeboost
AWS(Amazon Web Services)와, ASF(ArchiSteamFarm)를 이용해 가상 윈도우에서 24/7 플레이타임부스트를 가능하게합니다.
<hr/>
참조:
- [1] https://github.com/JustArchiNET/ArchiSteamFarm/releases/tag/5.2.0.10 - ASF

- [2] https://kwonsaw.tistory.com/323 - AWS 가상 윈도우서버 구축

- [3] https://github.com/Jessecar96/SteamDesktopAuthenticator/releases/tag/1.0.10 - 자동 2FA
<hr/>
STEP 1, AWS 서버 구축 ( 해외결제가 지원되는 카드가 필요하다.)

- [1] [AWS 회원가입](https://aws.amazon.com/ko/free/?trk=fa2d6ba3-df80-4d24-a453-bf30ad163af9&sc_channel=ps&sc_campaign=acquisition&sc_medium=ACQ-P|PS-GO|Brand|Desktop|SU|Core-Main|Core|KR|KR|Text&ef_id=Cj0KCQiA2NaNBhDvARIsAEw55hg6XgL93SNEdE7REvQvuF-HlfhInFwqRsxZGSU9E5pis5cOWERkL-gaAo1TEALw_wcB:G:s&s_kwcid=AL!4422!3!563761819834!e!!g!!aws&ef_id=Cj0KCQiA2NaNBhDvARIsAEw55hg6XgL93SNEdE7REvQvuF-HlfhInFwqRsxZGSU9E5pis5cOWERkL-gaAo1TEALw_wcB:G:s&s_kwcid=AL!4422!3!563761819834!e!!g!!aws&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)
- [2] Amazon Machine Image(AMI) 선택 ![12](https://user-images.githubusercontent.com/46117865/145716377-03d439e6-6099-4257-8134-314e96122b15.png)
- [3] 인스턴스 유형 선택 ![13](https://user-images.githubusercontent.com/46117865/145716379-b4de601e-0ba9-43a7-9520-3a7eb6294c52.png)
- [4] 생성 ![14](https://user-images.githubusercontent.com/46117865/145716381-a04ae880-9a8a-4578-b1d9-d758a02068a7.png)
- [5] 생성된 aws 를 우클릭 후, 연결을 눌러서 RDP 클라이언트를 받아야한다.
