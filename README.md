# SpeechAuth

Account authentication with speech authentication app

## Motivation

- 로그인 인증을 하는 방법은 여러가지이고 방법 또한 다양하다.
  - 전통적인 id, pw 입력 방식
  - 공인인증서 방식
  - 잠금 비밀번호 6자리 입력
  - 홍채 인식
  - 지문 인식
  - 휴대폰 인증 -> 인증번호 문자 전송
  - 2FA(Two factor authentication)
    - OTP를 이용한 pw 입력 (숫자, 문자+숫자 조합 등 다양)
    - Authentication app을 이용한 approve check
- 여러 앱을 통해 이런 인증 방식을 사용하다 보니 한번 쯤 만들어 보고 싶다는 생각이 들어서 토이 프로젝트 레벨로 만들어 보려 한다.
- 위에 나열한 걸 다 구현할 건 아니고 휴대폰 인증앱에서 특별히 음성 인식 기능을 넣어 pw를 말하고 인식된 text를 사용해서 인증하게 만들어 보려 함.
- 그러므로 2FA 기법을 따라가되 인증 방법이 speech text 방식.
- 아무도 이런 방식으로 만든 사람이 없으므로 재미있을 수도 있다. 흐흐.

## Skills

- Web front는 사실 로그인 하고 인증하는 화면만 필요하므로 담백하게 javascript + 필요한 라이브러리 조합으로 진행
- Server의 경우 그냥 node.js로 하면 재미 없으므로 go language로 일단 진행, 뭔가 막히면 다른 대안으로 빠르게 갈아타는 것으로 진행, 하지만 그 다른 대안이 node.js는 아닐 것!
- 인증앱 역시 android native로 하면 재미 없으므로 핫하다는 flutter를 사용
- CI의 경우는 회사에서 쓰던 jenkins, azure devops로 하면 재미 없으므로 Github actions를 사용
  - 이 때 회사에서는 경우 시간내서 맛보기로만 했던 unit test code 잘 작성해 보기

## Purpose

- 인증 방식에 대한 걸 실제 구현함으로써 implementation level에서 이해도 높임
- Dart, Go 언어 등 마이너한 언어를 습득하고 기존 언어들과 비교 분석 리포트 작성
- Language level을 넘어서 새로 경험해 봐야할 framework들 github actions 사용 경험
- 입만 터는 멘토의 모습 말고 정말 뭔가 하는 모습의 모범적인 멘토의 모습을 보여주기 위함
