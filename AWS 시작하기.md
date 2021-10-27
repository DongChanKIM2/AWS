# AWS 시작하기



1. 사용 인스턴스 OS 선택
   - Amazon Linux VS Ubuntu
     - 선택한 것은 Amazon Linux, 그 이유로는 AWS  에서 가장 강력하게 밀고 있는 OS 이기 때문에 한 번 사용해볼만 함!
2. EC 2 생성
   1. 태그 추가 및 SSH 접근
   2. 키 발급: EC2의 키는 비대칭키 방식의 개인key를 저장해줘야합니다. 만약 기존에 발급해 사용하는 key가 있다면 해당 key를 기반으로 EC2를 생성해줘도 무관합니다.

3. EC2 인스턴스 SSH 프로토콜로 접속
   1. EC2 인스턴스 연결 후 SSH 클라이언트 에서 지시사항대로 수행하면 됩니다.
   2. 발급받은 key로 퍼블릭 IPV4 주소, ec2 주소로 접속할 수 있습니다.
4. EC2 인스턴스 HTTP, HTTPS 프로토콜로 접속
   1. 보안그룹에서 http, https 프로토콜 추가
   2. EC2 인스턴스에서 방금 생성한 보안그룹 추가해주기

5. ec2 ssh로 node.js 설치

   https://docs.aws.amazon.com/ko_kr/sdk-for-javascript/v2/developer-guide/setting-up-node-on-ec2-instance.html

6. ec2 ssh로 git 설치

   1. git 을 설치하기 위해 git이 의존하고 있는 라이브러리 먼저 설치

   참고지식: var directory란 도대체 뭔가? Linux 및 Unix 계열의 루트 디렉터리의 표준 하위 디렉토리로 주로 작업하는 데이터를 기록할 파일들을 저장하는 곳

   http://www.linfo.org/var.html

   





Linux 명령어 정리:

- curl: 서버로 데이터를 보내거나 받을 수 있는 명령어로 HTTP, HTTPS 외의 다양한 프로토콜에서 사용가능
  - -o: remote에서 받아온 데이터를 콘솔에 출력해줌
- wget: 파일 다운로드

- chown: sudo chown 관리할 유저명 폴더명
- ls -al: 소유권자 그룹 식별자
- sudo mkdir / / : 현재 디렉토리가 기준이 아니라 홈 디렉토리를 기준으로 생성됨
- sudo 자체가 홈 디렉토리를 기준으로 실행되는 듯 sudo chown 또한 홈 기준