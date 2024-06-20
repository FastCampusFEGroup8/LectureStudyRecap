## 깃허브 사용법 숙지

### 깃 초기화

저장소를 만들고 싶은 디렉토리로 이동해서 위 명령어를 입력해 깃을 초기화 한다.

```
git init
```

### 작업

작업 트리에서 깃의 상태를 확인할 수 있는 명령어.

```
git status
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

### 기타 깃 명령어

1. 브랜치 생성

```
//git branch [브랜치명]
git branch test
```

2. 해당 브랜치로 이동

```
// git checkout [브랜치명]
git checkout test
```

3. 브랜치를 생성하고 해당 브랜치로 바로 이동

```
// git branch -b [브랜치명]
git branch -b test
```

4. 원하는 브랜치로 이동했는지 확인

```
git branch
```

5. 모든 브랜치 확인

```
git branch -a
```

6. 원하는 브랜치로 push 하여 원격 서버에 전송

```
// git push origin [브랜치명]
git push origin test
```

7. 브랜치 삭제

```
// git branch -d [브랜치명]
git branch -d test
```

8. 현재 브랜치에 다른 브랜치 수정사항 병합

```
// git merge [다른 브랜치명]
git merge test2
```
