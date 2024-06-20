## 깃허브 사용법 숙지

### 깃 초기화

저장소를 만들고 싶은 디렉토리로 이동해서 위 명령어를 입력해 깃을 초기화 한다.

```
git init
```

### 작업

작업 트리에서 깃의 상태를 확인할 수 있는 명령어.

```
git staus
```

![자료1](/LectureStudyRecap/승민님/240618-240624/image/gitstauts.png)

1. 메인 브런치에 있다.
2. 아직 커밋할 파일이 없다.
3. 현재 커밋할 파일이 없다.<br>

### 스테이징

작업 트리에 있는 파일을 스테이지에 올리기 위한 명령어.<br>
스테이지에 올리기 위한 파일 이름만 써도 되지만, (.)을 사용하면 untrcked file들을 한번에 스테이지에 올려준다.

```
git add .
git add test.md
```

### 커밋

```
git commit -m "add: test.md"
```

### 로컬 저장소를 원격 저장소와 연결

```
git remote -v
```

현재 로컬 저장소와 연결된 레포지토리의 주소를 보여준다.<br>
연결되어 있지 않다면 아무것도 나오지 않는다.<br>

### 원격 저장소의 등록

레포지토리와 연결시키기 위한 명령어는

```
// git remote [name] [레포지토리 주소]

//스터디 그룹 레포지토리
git remote add origin https://github.com/FastCampusFEGroup8/LectureStudyRecap.git

// toy-project 1 레포지토리
git remote add origin https://github.com/devcamp-intranet-1/toy-prj-1-serverless.git
```

레포지 토리를 연결시키고 다시 remote -v 를 해보면 연결된 레포지토리 주소를 확인할 수 있다.

### 원격 저장소의 연결 해제

삭제된 후 따로 삭제 성공 여부를 알려주지 않으므로 다시 -v 을 이용해 연결된 원격 저장소 목록을 확인하면 된다.

```
// git remote remove [name]
git remote remove origin
```

### 원격 저장소 사용

로컬에서 작업한 내용을 원격 저장소로 보내기 위해서 우선 작업 내용을 커밋한다.<br>
그 후 다음 명령어를 통해 push 해주면 원격 저장소에 해당 작업 내용이 기록되어 있는 것을 확인할 수 있다.

```
// git push [name] [branch]
git push origin main
```
