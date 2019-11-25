# Github actions

- Github에서 준비한 ci/cd 서비스
- CI/CD를 잘 모른다면 [https://github.com/features/actions](https://github.com/features/actions) 를 참고한다
- Test, build, jenkins 등의 용어에 익숙하다면 금방 적응할 수 있고
- 잘 모른다면 test, build와 같은 걸 command line으로 진행하고 이걸 대신 github 서버에서 진행하다고 생각하면 쉽다.

## golang development environment

- Windows 10 1903 (build 18362.476)
- go version
  - go version go1.13.4 windows/amd64
- Understanding GOPATH
  - work space root 경로로 그 경로 하위에는 반드시 src, bin의 폴더가 위치해 있어야 한다.
  - [https://golang.org/doc/code.html#Workspaces](https://golang.org/doc/code.html#Workspaces)
  - 이것 때문에 초반 세팅에 좀 고생했는데 gopath 자체를 src 폴더 바로 직전까지 세팅하면 편하다.

## Why github actions

- 이건 purpose 문서에도 쓴 내용인데, github actions가 얼마나 잘 진행되는지 해보려고 하는 것과
- 맨날 하는 unity, .net core 말고 golang, dart 같은 것도 잘 되는지 해보려고 한다.

## Next step

- golang에서 unit test 하는 방법에 대하 조사하고 적용한 뒤에 github actions에 적용해 본다.
- golang에서 web server 구축하는 방법에 대해 조사하고 적용한 뒤에 github actions에 적용해 본다.

## Github packages

- 고작 hello world 찍은 것 뿐이므로 package delivery는 나중에 고민해 보도록 한다.
- 지금 드는 생각은 golang은 npm 기반이 아니므로 docker를 사용하고 그 container를 클라우드 서비스 쪽에 push 하지 않을까 싶다.

## Review

- 하나의 CI 단위를 workflow라고 부르는데 이 스크립트를 만드는 절차에 대한 문서가 상당히 잘 되어 있다.
  - [https://help.github.com/en/actions/automating-your-workflow-with-github-actions/configuring-workflows](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/configuring-workflows)
- 준비된 template에서 찾을 수 없으면 market place에서 누군가 잘 만들어 놓은 스크립트를 참고하거나 그대로 가져와서 약간 수정해서 쓸 수도 있다.
  - [https://github.com/marketplace?type=actions](https://github.com/marketplace?type=actions)
- Microsoft가 github를 인수하고 난 뒤에 생긴 서비스라 그 동안 Azure pipeline에서 잘 써왔던 서비스를 github에 맞게 적용했을 거라 생각했는데 그 예상이 맞았다.
- 계속 써보고 별 문제가 없거나 괜찮다고 느껴지면 별도의 CI 서비스를 돌릴 필요가 없을 듯 하다.
