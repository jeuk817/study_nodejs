# npm이란?
참고 : https://m.blog.naver.com/magnking/220961896609  

- Node Packaged Manager의 약자
- npm이란 Node.js로 만들어진 pakage(module)을 관리해주는 툴
- npm 명령어로 기존에 공개된 모듈들을 설치하고 사용할 수 있다.

## 어떻게 사용하는가?
- 예전에는 npm을 따로 설치해야했지만 지금은 node.js를 설치하면 내장되어 있다.

- 모듈 다운로드 하는법 :
    1. 터미널에 'npm install 모듈'과 같은 명령어를 입력하면 다운로드 된다.
    2. 반대로 삭제하는 법은 'npm uninstall 모듈'
    3. 1번처럼 일일이 설치하는 방법 외에 package.json에 기록하여 한꺼번에 관리할 수 도 있다.
        - 우선 package.json생성 : 'npm init'
        - package.json안에서 중요한 부분은 'script'와 'dependecies'다.
        - "script" : run 명령어를 통해서 실행할 것들을 적어둔다.
        - "dependencies" : 는 함께 설치할 모듈들을 적어둔다. 예) "webpack" : "2.2.1"
        - 이렇게 package.json 파일에 정리해두면 배포할 때 해당 프로그램 개발에 사용했던 모듈들을 그대로 같이 설치할 수 있다. 명령어) 'npm install'
        - package.json을 생성한 이후 외부 모듈을 다운로드 할 경우 '--save'옵션을 주면 자동으로 package.json에 기록된다. 예) 'npm install nconf --save'
        - 반대로 package.json의 dependencies의 목록에 직접 추가하여 'npm update'명령어로 외부모듈을 설치할 수 있다.
