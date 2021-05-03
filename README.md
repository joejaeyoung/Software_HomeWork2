Git 사용법 in 소공
=========

###  Repository 주소 : https://github.com/joejaeyoung/Software_HomeWork2

<br>


## 1단계 작업환경 설정
### config
- 현재 파일이 아무것도 설정되어 있지 않음
- commit 할 때마다 내 이름을 명시할 수 있도록 설정하고 싶음
-  이를 위해 config 명령어 사용
    - git 환경의 최초 설정을 위해 사용하며
    - 사용자 정보 또한 설정할 수 있다.
    - git에서 사용할 텍스트 편집기 또한 명시 가능하다.
- 자주 사용할 것 같은 명령어는 아래 사항들이다.
    - git config --global user.name "이름"
    - git config --global user.email "이메일"
    - git config --global core.editor vim    

![config](https://user-images.githubusercontent.com/68009715/116853624-55ee7d00-ac31-11eb-97a7-230baa698875.JPG)

### clone
- 현재 깃허브에만 내 프로젝트 작업환경(빈 Reposiotry)가 있음
- 위 Repository를 내 git사용 환경으로 가져오고 싶음
- 이를 위해 clone 명령어 사용
    - github에 먼저 레포지토리를 생성한 후 내 작업환경으로 가져오고 싶을 때 사용
- git clone "Repository 주소"

![clone](https://user-images.githubusercontent.com/68009715/116854114-2429e600-ac32-11eb-9a47-f271e08dc3d1.JPG)

## 2단계 작성한 파일 깃허브에 올리기
### status
- 내 작업환경(Linux Ubuntu)에서 과제1파일인 md파일을 일부분 작성함
- 이를 git을 통해 github에 올려 백업해두고 싶음
- 이를 위해 status 명령어 사용
- status 명령어는 현재 파일이 스테이지 위에 있는지 아래에 있는지 혹은 변동사항이 있는지 확인해줌
- git status 

![status-1](https://user-images.githubusercontent.com/68009715/116854496-b5995800-ac32-11eb-9ce1-95ae4a7e269e.JPG)

### add
- 일부분 작성한 과제1파일이 스테이지 아래에 있는 상태임을 확인함
- 이 파일을 후에 커밋하기 위해 스테이지 위에 올리고 싶음
- 이를 위해 add 명령어 사용
- add 명령어는 스테이지 아래에 있는 파일을 스테이지 위로 올림
- git add 파일이름
- add 이후 파일이 잘 스테이지 위로 올라갔는지 확인하기 위해 status 명령어와 같이 사용

![add](https://user-images.githubusercontent.com/68009715/116854912-69024c80-ac33-11eb-8c07-630e6b503123.JPG)

### commit
- github에 올리고 싶은 파일이 현재 스테이지 위에 올라가 있음
- 파일 이름을 바꿀 예정이 없기 때문에 지금 올린 파일에 대해 부연 설명(1/3을 진행했다는 진행사항)을 덧붙이고 싶음
- 이를 위해 commit 명령어 사용
- commit은 현재 repository 의 변동사항, 변동시간, 버전등 history를 명시함
- 자주 쓸 것 같은 commit 옵션
    - git commit -m "메세지"  
        - vim에서 별도로 작성할 필요없이 한 문장(인라인)형식으로 commit메세지 작성
    - git commit -a 
        -  한번이라도 add된 파일을 별도의 add명령어 사용없이 add commit 한번에 수행
    - git commit -am "메세지"
        - 위의 두 옵션을 합쳤다
    >-a, -am옵션은 깃을 잘 다루기 전까진 사용하지 않을 것 같다.
    
![commit](https://user-images.githubusercontent.com/68009715/116855720-cf3b9f00-ac34-11eb-8af1-30270e4f6330.JPG)
    
### push
- 현재 파일이 커밋을 통해 과제 1/3진행했다는 것을 알 수 있게 됨
- 이제 이 파일을 github에 올리고 싶음
- 이를 위해 push 명령어 사용
- push는
    - 리모트 저장소에서 로컬 브랜치를 서버로 전송한다.
    - 자동으로 전송되지 않기 때문에 사용자가 직접 push 해야한다.
    - 내가 작업한 내용, 브랜치를 모두 다 공유하지 않고 일부분을 다른 사용자들에게 숨기거나 공개할 수 있다.
- git push "파일 이름"    
![push1](https://user-images.githubusercontent.com/68009715/116856942-f004f400-ac36-11eb-8e6a-a1b5547d75a8.JPG)

- push 후 직접 깃허브를 확인해보면 잘 올라간 것을 확인할 수 있다.
![push1후 깃허브 확인](https://user-images.githubusercontent.com/68009715/116856985-014e0080-ac37-11eb-9f84-60fb09c392ab.JPG)

## 3단계 작성한 파일 추가 관리(2단계 반복+a)
### log
- 처음 작성한 파일에 수정해야할 부분이 생김
- vim으로 파일 수정 후 2단계반복(커밋 두번째)
- 내가 지금까지 수정한 기록들을 보고싶음
- 이를 위해 log 명령어 사용
- log는 커밋 히스토리를 시간순으로 보기 위해 사용
    - git log --pretty=oneline 옵션들을 사용
        - 각 커밋을 한 라인으로 요약하여 출력
        
![log -1](https://user-images.githubusercontent.com/68009715/116862338-8fc68000-ac3f-11eb-8ff5-fea175ba3caf.JPG)


![git log--pretty=oneline](https://user-images.githubusercontent.com/68009715/116862414-ab318b00-ac3f-11eb-94af-cd3a496510d6.JPG)

### reset --hard(커밋 세번째 후 취소)
- 1.vi로 이미지 관련 내용을 추가함
- 2.add * 명령어를 통해 바로 올리려 했음
- 3.작업 디렉토리에 올라가면 안되는 파일이 존재했음
- 4.잘못된 두개의 파일을 커밋함
- 5. status를 사용해 확인해보니 잘못된 파일도 커밋함
- 커밋을 전으로 돌리고 잘못한 커밋을 없애고 싶음
- 이를 위해 reset --hard를 사용하려함
    - 커밋을 전으로 돌리기 위해 log를 통해 커밋의 위치를 알아냄
    - reset --hard 명령어를 통해 커밋을 돌림
    
![reset --hard](https://user-images.githubusercontent.com/68009715/116862996-95709580-ac40-11eb-98bb-ac6ccf42b5c1.JPG)

### tag(세번째 커밋)
- 1.커밋을 전으로 돌렸음
- 2.vi로 기존의 이미지 관련 내용을 추가한 후 2단계 반복
- 방금 푸쉬한 내용에 관련하여 이미지 파일 내용을 추가했다는 태그를 달고 싶음
- 이를 위해 tag명령어 사용
- 태그 종류
    - Lightweight 태그
        - git tag 이름
            - 특정 커밋을 가리키는 역할만 함
    - Annotated 태그
        - git tag -a 태그이름
            - 만든 사람, 이메일, 날짜, 메세지 저장

- git tag -a 이름 -m "관련내용"
    - Annotated 태그 생성을 주로 쓸 것 같다.
- git tag
    - 태그를 보여주는 명령어와 같이 쓸 것 같다.
- git show 태그이름
    - 태그한 내용을 자세히 보여주는 명령어와 같이 쓸 것 같다.
- tag를 따로 푸쉬하지는 않았다.

![tag1](https://user-images.githubusercontent.com/68009715/116864348-ad491900-ac42-11eb-9616-da20de1e6493.JPG)


## 4단계 브랜치 관리
### branch
- master브랜치에서 계속 작업하고 있었음
- master브랜치가 아닌 새로운 브랜치develop을 만든 후
- 원본은 두고 develop에서 무언가 새로운 내용을 추가 하고 싶음
- branch를 통해 develop 브랜치 생성
- branch 브랜치이름 을 통해 브랜치 생성

![branch-1](https://user-images.githubusercontent.com/68009715/116866923-17fc5380-ac47-11eb-9f75-88ef88beee46.JPG)

### checkout
- 현재 head는 master를 가리키고 있음
- head를 새로 만든 브랜치를 가리키게하고 새로 만든 브랜치에서 작업하고 싶음
- checkout 사용을 통해 head를 옮김
- git checkout 브랜치명

![checkout](https://user-images.githubusercontent.com/68009715/116867270-c7392a80-ac47-11eb-98c3-1edec3cb4202.JPG)

### merge 커밋4
- 1.기존의 과제파일에 백틱내용을 추가하기 위해
- 2.과제파일 수정후 commit(백틱내용 추가)만 함
- develop브랜치에서 수정한 파일의 내용이 검증되어서
- master 브랜치에 merge하고 싶음
1. master브랜치로 checkout
2. 브랜치별 커밋상황 확인
    -git log --branches --decorate --graph
    
 ![log --graph](https://user-images.githubusercontent.com/68009715/116875523-08383b80-ac56-11eb-80e7-9291c7896121.JPG)
3. merge 명령어 사용
    - git merge develop
    - 두개의 브랜치에 있는 모든 작업내역을 포함하는 방법.
    - 커밋의 색이 같아지면 두 브랜치가 모두 저장소의 모든 작업 내역을 포함하고 있다는 뜻임
    
![merge](https://user-images.githubusercontent.com/68009715/116868109-2481ab80-ac49-11eb-8f69-13fb8d0861ca.JPG)
    
4. merge후 develop에서 개발했던 내용 + 이미지 파일 내용 추가
  - master에서 add, commit한 내역
  
![master add, commit](https://user-images.githubusercontent.com/68009715/116874886-01f58f80-ac55-11eb-92e6-242dbad51f39.JPG)  
  - 추가 후 커밋 푸쉬한 내역
  
![log --graph](https://user-images.githubusercontent.com/68009715/116874470-58ae9980-ac54-11eb-9711-e03327bea557.JPG)


## 5단계 다른 사람과 공동작업 상황 및 기타 사항
### init
1. 다른사람이 개발에 참여하는 상황을 만들기 위해
2. 새로운 디렉토리 생성 후 git init 사용
- init
    - .git이라는 하위 디렉토리를 만듬.
    - 아직 프로젝트의 어떤 파일도 관리하지 않음
    
![gitinit](https://user-images.githubusercontent.com/68009715/116873705-13d63300-ac53-11eb-9d0d-bd75d5957329.JPG)

### remote
- 현재 작업중인 디렉토리에 리모트 저장소를 저장함
- git remote add 이름 주소 를 통해 생성할 수 있다

![init, remote](https://user-images.githubusercontent.com/68009715/116873774-323c2e80-ac53-11eb-9592-d76ea5996cdc.JPG)
- 리모트 저장소 확인

![remote저장소확인](https://user-images.githubusercontent.com/68009715/116874832-e9857500-ac54-11eb-8e86-17addb9e33f5.JPG)

### pull
- 현재는 리모트 저장소만 디렉토리에 저장되어 있는 상태
- 기존의 개발 진행 상황을 가져와 이어서 하고 싶음
- pull 명령어 사용
- 기존의 작업환경을 저장한 깃허브, 리모트 저장소에서 pull을 통해 최신 진행사항을 받아와서 local의 master브랜치와 merge해줌


![pull](https://user-images.githubusercontent.com/68009715/116873964-7e876e80-ac53-11eb-8407-1d5bad83ad39.JPG)

### rebase 커밋5~8
   1. branch 생성
  - 현재 local의 master에는 기존의 과제 1 제출물이 존재
  - master브랜치에는 기존의 과제1 제출물만 완성시킬 예정
  - develop 브랜치를 새로 만들어 기존의 과제 1 제출물 파일에 github에 올린 md 파일 설명법을 올릴 예정(소공 과제1)
  
  - develop 브랜치 생성 및 checkout
  
  ![dir branch checkout](https://user-images.githubusercontent.com/68009715/116874975-20f42180-ac55-11eb-86f2-cf3d308e2f96.JPG)
 
 2. master 브랜치에서 기존의 파일에 새로운 내용 추가 1 커밋5
  - 2단계 반복
 
 ![dir master변경](https://user-images.githubusercontent.com/68009715/116875084-4d0fa280-ac55-11eb-8aaa-282e59995480.JPG)

3. master 브랜치에서 기존의 파일에 새로운 내용 추가 2 커밋 6
  - 2단계 반복
  
  ![dir master변경2](https://user-images.githubusercontent.com/68009715/116875182-78928d00-ac55-11eb-99ba-ae53c61d714a.JPG)

4. develop 브랜치에서 기존의 파일에 새로운 내용 추가 1 커밋 7
  - 1.기존의 master 브랜치에서 develop 브랜치로 checkout
  
  ![dir branch checkout](https://user-images.githubusercontent.com/68009715/116875334-af68a300-ac55-11eb-83a8-d233f27365fe.JPG)
  - 2.develop 브랜치에서 2단계 반복
  
  ![dir developqusrud](https://user-images.githubusercontent.com/68009715/116875374-c5766380-ac55-11eb-9280-70cd1664cc24.JPG)

5. develop 브랜치에서 기존의 파일에 새로운 내용 추가 2 커밋 8
  - 1.develop 브랜치에서 2단계 반복
  
  ![dir develop 변경 2](https://user-images.githubusercontent.com/68009715/116875442-e8a11300-ac55-11eb-8be4-1874f1718050.JPG)
  
6. 현재 커밋상태 확인

![git log](https://user-images.githubusercontent.com/68009715/116875551-12f2d080-ac56-11eb-8bd4-5ac141d0ac6a.JPG)

- 두개의 브랜치끼리의 작업을 합치고 싶어 rebase 명령어 사용
- commit의 흐름을 한줄로 만들 수 있음
- 순서대로 개발한 것 처럼 보이게 됨


- 첫 리베이스 시도 실패

![rebase 실패1](https://user-images.githubusercontent.com/68009715/116875812-7da40c00-ac56-11eb-9266-d5f89729cefa.JPG)

- 수정 후 다시 리베이스 시도

![수정후 다시 rebase](https://user-images.githubusercontent.com/68009715/116875895-9b717100-ac56-11eb-9a28-7d4a78dcdf30.JPG)

- 떨어져있는 master, develop 브랜치의 작업현황을 합침

![마지막rebase](https://user-images.githubusercontent.com/68009715/116875963-b8a63f80-ac56-11eb-8f7f-c1080c5a916a.JPG)

- rebase 후 커밋상황 확인

![rebase 후 커밋상황](https://user-images.githubusercontent.com/68009715/116876008-c3f96b00-ac56-11eb-8ad4-38704993b096.JPG)

- 마지막 완성파일 push

![마지막 push](https://user-images.githubusercontent.com/68009715/116876178-015df880-ac57-11eb-8dbd-cce73e3a358a.JPG)

|명령어 | 이름|
| --- | --- |
|   config  |    O     |
|   clone   |    O     |  
|   status  |    O     | 
|    add    |    O     |
|   commit  |    O     |
|    push   |    O     |
|    log    |    O    |
|reset --hard|    O   |
|    tag   |    O     |
|  branch  |    O     |
| checkout |    O     |
| pull     |    O     |
|   merge  |    O     |
|   init   |    O     |
|  remote  |    O     |
|  rebase  |    O     |

