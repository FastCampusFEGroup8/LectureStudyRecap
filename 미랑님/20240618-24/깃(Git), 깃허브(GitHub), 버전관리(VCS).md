### Git
컴퓨터 파일의 변경사항을 추적하고 여러 사용자들 간에 해당 파일 작업을 조율하기 위한
대표적인 버전 관리 시스템(VCS, Version Control System)


### bash 기본 기호
`$` : 
`-` 또는 `--` : 플래그


### 초기 세팅
- 로컬에 깃 설지
- 깃허브 레포지토리 생성
- git bash 또는 코드 에디터 터미널에서 깃허브의 원격 저장소와 로컬 저장소 연결  

> git init을 시작으로 내가 로컬 환경에 만든 저장소를 연결하고 그 안의 변경사항을 추적한다.
추적할 파일을 선택하면 스테이지(stage) 영역에 추가된다.  
해당 변경사항에 대한 버전을 생성하하는 것을 커밋(commit)이라고 한다.  
이러한 버전들, 즉 커밋을 저장하고 관리하는 곳이
원격(remote) 환경에 만든 레포지토리(repository)다.  
원격 환경은 대표적으로 깃허브가 있다.


### 초기 세팅에 필요한 명령어
- 깃 버전 확인  
```
$ git version
```
</br>


- 현재 프로젝트에서 변경 사항 추적(버전관리) 시작
```
$ git init
```
</br>


- 개행문자(Newline) 설정 : 줄바꿈 처리 방법  
```
$ git config --global core.autocrlf true
```
> config 구성 옵션
> --global : 전역 옵션, 전체 영역에서 사용
> .autocrlf 자동으로 crlf를 운영체제에 맞게 변환
</br>


- 커밋(버전 생성)을 위한 사용자(로컬) 정보 등록  
```
$ git config --global user.name '깃허브 아이디'
$ git config --global user.email '이메일 주소'
```
가급적 깃허브 사용자명과 맞추는 것이 좋다.
</br>


- 구성 확인, q 키로 빠져나오기
```
$ git config --global --list
```
</br>


- 버전 관리 상태
```
$ git status
```
</br>


- 버전관리할 파일 지정
> 전체 : `.`  
> 특정 파일 : 파일명 입력
```
$ git add
```
</br>


- 커밋 및 메시지 입력
```
$ git commit -m '커밋 메세지'
```
</br>


- 커밋 기록 확인, q 키로 빠져나오기
```
$ git log
```
</br>


- 로컬에 원격 저장소를 연결
로컬에서의 저장소 별칭은 통상적으로 origin 사용
```
$ git remote add origin 레포지토리 주소
```
</br>


- 원격저장소 origin의 브랜치 main에 커밋 내역 업로드
```
$ git push origin main
```
</br>


