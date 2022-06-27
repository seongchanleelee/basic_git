

<h1>git과 git저장소



<h3>git

- git == 파일의 상태(변화)를 파악하고 기록하는 시스템

- git 장점
  - 모든 파일의 변화된 내용을 추적함
  - 같은 파일에 대한 각기 다른 버전을 보관 가능
  - 한 파일로 다른 에디터들과 함께 작업가능

<h3>git 저장소
    
</h3>

- git 저장소 == 클라우드에 있는 깃 제공자.
- 리모트 레포지터리를 관리(운영)하는 사이트(시스템)



<h3>사용법



- git init
  - 제일 처음에 프로젝트를 올릴때 git init으로 초기화를 시켜줌

```bash
git init
```



- git add .
  - git 변경내용을 add시켜줌 (뒤에 .은 모든 파일을 뜻함)
  - 하나의 파일의 변경사항만 올리고 싶다면 add 뒤에 파일이름을 작성

```bash
git add .
git add index.html
```



- git status
  - git에서 add되거나 add 되지 않은 상태의 파일을 확인

```bash
git status
```



- git commit
  - 변경된 사항의 history를 만듬

```bash
git commit -m"first commit"
```



- git remote
  - 내가 만든 repository로 내가 작성한 소스코드를 보낼 연결고리를 만듬

```bash
git remote add origin git@github.com seongchanleelee/first-project.git

// 연결고리 확인법
git remote -v
```



- git push
  - 연결된 repository에 변경사항을 보냄
  - 가장 마지막에 들어가는 단어는 branch명을 뜻함

```bash
git push origin master
```



- git pull
  - 협업에디터의 변경사항을 내 local repository에 받아오고 싶을때 사용

```bash
git pull
```



- git clone
  - git주소를 알고 프로젝트를 다운받아야 하는 상황이 있을때 사용

```bash
git clone #복사된 html주소#
```



<h3>branch

- 특정 commit을 가리키는 포인터 역할
- git push시 HEAD가 되는 branch(ex)main, master)에 한번에 올리게 되면 기능 세분화의 어려움은 물론, 오류가 났을 시 빠른 복구가 어려울 수 있다.

<hr>

- git branch
  - branch를 생성하는 명령어

```bash
git branch {branch_name}
git branch freshman
```



- git checkout {branch_name}
  - HEAD가 가리키는 branch를 옮겨줌

```bash
git checkouot freshman
```



- git log
  - 현재 HEAD가 어떤 branch를 가리키는지 확인함

```bash
git log
```



- git merge
  - 현재 가리키고 있는 포인터(위 예제에선 freshman)와, merge 뒤에 작성한 branch명에서의 커밋을 합칠때 사용된다.

```bash
git merge {branch_name}

git merge master
```



- merge시 conflict문제
  - 동일 라인(동일 선상의 커밋)이 서로 다른 코드를 가지게 되는 경우 합칠 때 충돌이 발생
  - conflict 에러 발생시 충돌이 일어난 파일에 들어가 본인이 작성한 코드와 다른 branch에서 작성된 코드를 잘 정리후 add commit 하면 된다.

