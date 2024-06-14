# Node.js  

`nvm`은 `node.js` 매니저라고 생각하면 된다.

1. google에 nvm 검색 후  Git 링크로 접속 > installing and updating 에 공유된 코드 중 첫번째 'curl -o- https://~' 로 시작되는 코드 복사해서 터미널에서 설치
1. vs code 의 터미널에서   
   - nvm ls : nvm list 확인  
   - nvm install <u>12.14.1</u> : <u>12.14.1</u> 버전 확인  
   - nvm use <u>12.14.1</u> : <u>12.14.1</u> 버전 사용  
   - node --version : node 버전 확인  
   - nvm uninstall <u>12.21.1</u> : <u>12.21.1</u> 버전 삭제
   - nvm --help : 설명서


`npm`은 `node.js`의 패키지 매니저 (`node.js` 설치하면 자동 설치)

3. vs code 의 터미널에서
   - npm init -y : 프로젝트 내에서 package.json 생성
   - npm install <u>parcel-bundler</u> <u>-D</u> : 개발용 의존성 패키지 설치
   - npm i(install) <u>lodash</u> : 일반 의존성 패키지 설치

***

# 유의적 버전  

node --version / npm --version  
➡️ v<u>12</u>.<u>14</u>.<u>1</u> : Major / Minor / Patch  
➡️ <u>^</u>12.14.1 : major 버전 안에서 가장 최신 버전으로 업데이트 가능  

npm install <u>lodash</u>@<u>12.14.0</u> : 버전 설치  
npm install : node_modules 패키지 설치  
npm run build : dist 폴더 설치

***

# npm 프로젝트 버전 관리 (.gitignore)

루트 경로에서 .gitignore 파일 생성 (버전 관리하지 않을 무시할 내용)  
➡️ <span style="color:orange;">해당 폴더는 git에 업로드 해도 올라가지 않음</span>



