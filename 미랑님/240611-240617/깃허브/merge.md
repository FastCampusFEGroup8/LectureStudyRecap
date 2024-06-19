# merge


## 오늘의 퀘스트 : 병합된 브랜치를 그대로 두고 main 브랜치에 병합하기

발생한 문제 : main 브랜치에서 merge 작업을 했더니 내가 의도하지 않은 다른 파일까지 포함해서 merge 되었다.  

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1ecad111-2392-448b-842b-55303bf43fd8/440696db-14f6-4d21-8f17-5ad927598d8a/Untitled.png)

기존 파일인 미랑, 한빈, 리드미 파일을 제외하고 나머지 파일들은 모두 아래 사진과 같이 로컬 폴더에서 가져와진 거였다. 어떻게 가져와졋는지도 의문인데 자칫 개인정보와 관련된 문제가 발생할 수 있어 빠르게 해결이 필요한 부분이었다.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1ecad111-2392-448b-842b-55303bf43fd8/21cf7d82-95f2-4f94-9a3a-7fff93d9acbe/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1ecad111-2392-448b-842b-55303bf43fd8/78ada6e0-9c02-4a7a-bdfa-da10edf3fc10/Untitled.png)

- 로컬에 저장된 저 파일들이 어떻게 해서 생겨난 것인지 파악해야 한다.
- 해당 파일들을 지워도 되는 것인지, 삭제하면 안 된다면 어떻게 머지 할 때 해당 파일들이 병합되지 않도록 할 수 있는지 방법을 찾아야 한다.

 

## 해결 시도

- 처음엔 이전 단계로 되돌리는 방법을 시도해봤다. 하지만 main 브랜치는 여전히 머지된 상태로 남아있는 것이 문제였다.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1ecad111-2392-448b-842b-55303bf43fd8/9d8dc782-c537-4ccc-ac14-f36786f2a2c2/Untitled.png)

- 함께 작업 중인 한빈님과 상황 공유를 먼저 해보기로 했다. 일단 한빈님께서 해당 리포지토리를 관리하고 계셨기 때문에 한빈님은 내 브랜치의 변경사항을 한빈님의 브랜치로 pull하고 그 뒤 자신의 브랜치를 main에 push 하려고 했다. 그런데 잘못해서 나처럼 한빈 브랜치를 main 브랜와 merge 해버렸다고 하셨다.
- 한빈님의 브랜치에 저 정체를 알 수 없는 파일들을 먼저 삭제했다. 그리고 나서 로**컬에서 쓸모 없는 파일들이 삭제된 브랜치를 원격의 main 브랜치에 강제로 push 함으로서 해결할 수 있었다.**