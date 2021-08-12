# README.md

## Quick setup

| no  | 구분                             |     | 액션                                                            |
| --- | -------------------------------- | --- | --------------------------------------------------------------- |
| 1   | 전제조건                         | 1   | GitHub 에 new remote repository **“git-tutorial”** 생성         |
|     |                                  | 2   | root 폴더에 **README.md** 생성                                  |
|     |                                  | 3   | root 폴더에 현재 빈 파일인 **.gitignore** 생성                  |
|     |                                  | 4   | git config \--global user.name “myMediaBrains”                  |
|     |                                  | 5   | git config \--global user.email “my.media.brains@gmail.co”      |
| 2   | git 저장소 생성                  | 1   | git init                                                        |
|     |                                  | 2   | git add README.md                                               |
|     |                                  | 3   | git commit -m “first commit”                                    |
|     |                                  | 4   | git branch -M main                                              |
|     |                                  | 5   | git remote add origin git@github.com:myMediaBrains/git-tutorial |
|     | GitHub remote repository 에 push | 6   | git push -u origin main                                         |

## SSH 설정

| no  | 구분                                                                              | 설명                               |
| --- | --------------------------------------------------------------------------------- | ---------------------------------- |
| 1   | $ git version                                                                     | git 설치 확인                      |
| 2   | $ cd ~/.ssh                                                                       | id_rsa 및 id_rsa.pub 파일 확인     |
| 3   | $ ssh-keygen -t rsa -C “my.media.brains@gmail.com”                                | 새로운 개인키 및 공개키 생성       |
|     |                                                                                   | 물어보는 질문은 디폴트로 엔터      |
| 4   | $ cd ~/.ssh                                                                       | id_rsa 및 id_rsa.pub 파일 확인     |
| 5   | $ vi id_rsa.pub                                                                   | 내용 copy                          |
| 6   | GitHub > Profile 아이콘 > Settings > SSH and GPG keys > New SSH key > Title & Key | Key 에 copy 한 id_rsa.pub 를 paste |

# [GitHub 사용법 총 정리](https://www.lainyzine.com/ko/article/summary-of-how-to-use-github-for-developers/)

## GitHub 계정 생성 및 셋업

| no  | 구분                              | 설명                                                                                                                                                       |
| --- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [github.com](https://github.com/) | Sign up                                                                                                                                                    |
| 2   | username, emai, password          |                                                                                                                                                            |
| 3   | email 인증                        | [GitHub Two Factor 인증(OTP) 활성화하는 방법](https://www.lainyzine.com/ko/article/github-activate-two-factor-authentication/)                             |
| 4   | SSH 등록                          | [GitHub 접속 용 SSH 공개키와 개인키 만들기](https://www.lainyzine.com/ko/article/creating-ssh-key-for-github/)                                             |
| 5   | 유료계정                          | [GitHub 개인 계정의 유료 Pro 플랜 구독하는 방법](https://www.lainyzine.com/ko/article/how-to-subscribe-to-the-pro-plan-in-your-github-personal-account/)   |
|     |                                   | [GitHub 개인 계정의 Pro 플랜 구독 취소하는 방법](https://www.lainyzine.com/ko/article/how-to-unsubscribe-to-the-pro-plan-in-your-github-personal-account/) |

## GitHub 저장소 생성

| no  | 구분                                                         | 설명                   |
| --- | ------------------------------------------------------------ | ---------------------- |
| 1   | $ git config --global user.name "myMediaBrains”              | username               |
| 2   | $ git config --global user.email “my.media.brains@gmail.com” | email                  |
| 3   | $ code ~/.gitconfig                                          | 상기 명령으로 자동생성 |

~/.gitconfig

```tsx
[user]
	name = myMediaBrains
	email = my.media.brains@gmail.com
[init]
	defaultBranch = main
```

| no  | 구분                                    | 설명                  |
| --- | --------------------------------------- | --------------------- |
| 4   | $ mkdir git-tutorial && cd git-tutorial | 프로젝트 폴더         |
| 5   | $ git init                              | 초기화                |
| 6   | $ touch .gitignore                      | node_modules 추가     |
| 7   | $ git add .                             | 모든 파일을 add       |
| 8   | $ git commit -m ‘Initialize repository’ | git repository 초기화 |
| 9   | $ git show                              | commit 정보 출력      |

## 저장소 별 git 사용자 및 이메일 정보 설정하기

- \--global 설정보다 우선한다.

| no  | 구분                                         | 설명 |
| --- | -------------------------------------------- | ---- |
| 1   | $ mkdir another-git && cd anther-git         |      |
| 2   | $ git init                                   |      |
| 3   | $ touch .gitignore                           |      |
| 4   | $ git config user.name “mckriskr”            |      |
| 5   | $ git config user.email “mckriskr@gmail.com” |      |
| 6   | $ touch README.md                            |      |
| 7   | $ git add .                                  |      |
| 8   | $ git commit -m ‘Add README.md’              |      |
| 9   | $ git show                                   |      |

## 주요 git 명령어

| no  | 구분                                       | 설명                                                            |
| --- | ------------------------------------------ | --------------------------------------------------------------- |
| 1   | $ git config user.name                     | 사용자 정보 확인                                                |
|     | $ git config user.email                    |                                                                 |
| 2   | $ git config \--global \--unset user.name  | 사용자 정보 삭제                                                |
|     | $ git config \--global \--unset user.email |                                                                 |
|     | $ git config \--unset user.name            |                                                                 |
|     | $ git config \--unset user.email           |                                                                 |
| 3   | $ rm -rf .git                              | 로컬에서 git 저장소 삭제 : 복구방법 없으니 주의                 |
| 4   | $ cd [GIT_REPO]                            | 소스 코드는 그대로 두고 git 저장소 정보 및 설정을 삭제하는 경우 |
|     | $ git checkout main                        |                                                                 |
|     | $ rm -rf .git                              |                                                                 |
|     | $ git status                               | git 저장소 삭제 확인                                            |

## git - GitHub 연결 방법

| no  | 연결방법            | 설명                                                      |
| --- | ------------------- | --------------------------------------------------------- |
| 1   | https 사용하는 경우 | 코드를 push 할 때 GitHub ID 와 Password 로그인 해야 한다. |
| 2   | SSH 사용하는경우    | 먼저 SSH 공개키와 개인키를 만들고, 셋업해야 한다.         |

본 문서는 SSH 프로토콜 사용을 전제한다.

**<u>시나리오 #1: git 저장소 초기화 > GitHub 로 push 하기</u>**

| no  | 구분                                                                  | 설명                                                                   |
| --- | --------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 1   | $ echo ‘# literate-engine’ >> README.md                               | README.md 파일 생성                                                    |
| 2   | $ git init                                                            |                                                                        |
| 3   | $ git status                                                          | git status 확인                                                        |
| 3   | $ git add README.md                                                   |                                                                        |
| 4   | $ git commit -m “first commit”                                        |                                                                        |
| 5   | $ git branch -M main                                                  | 현재 branch 를 강제로 main branch 로 이동                              |
|     |                                                                       | 기존 branch는 삭제된다.                                                |
|     | $ git branch                                                          | main 확인                                                              |
|     | $ git log                                                             | commit 내용, author, date 등 정보 표시                                 |
| 6   | $ git remote add origin git@github.com:myMediaBrains/git-tutorial.git | git 과 GitHub를 연결한다.                                              |
|     |                                                                       | GitHub 원격저장소의 이름은 관습적으로 origin을 사용한다.               |
|     | $ git remote -v                                                       | 로컬 git 저장소에 등록된 원격저장소 목록을 확인                        |
| 7   | $ git push -u origin main                                             | -u 는 원격저장소의 이름을 대신하는 것이고, main 은 git 의 branch 이다. |

**<u>시나리오 #2: 비어있는 GitHub 저장소 > git 으로 복제하기</u>**

| no  | 구분                                                      | 설명                              |
| --- | --------------------------------------------------------- | --------------------------------- |
| 1   | GitHub repository 생성                                    | git-tutorial repository 새로 생성 |
| 2   | $ git clone git@github.com:myMediaBrains/git-tutorial.git |                                   |
| 4   | $ cd git-tutorial                                         |                                   |
| 5   | $ git staus                                               |                                   |
| 6   | $ git log                                                 |                                   |
| 7   | $ git remote -v                                           |                                   |
| 8   | $ git branch -M main                                      |                                   |

**<u>시나리오 #3: 기존 git 저장소가 있는 경우</u>**

| no  | 구분                                                                  | 설명 |
| --- | --------------------------------------------------------------------- | ---- |
| 1   | $ git remote add origin git@github.com:myMediaBrains/git-tutorial.git |      |
| 2   | $ git branch -M main                                                  |      |
| 3   | $ git push -u origin main                                             |      |

## clone 사용법

| 구분                  |                                         | 설명                                                                         |
| --------------------- | --------------------------------------- | ---------------------------------------------------------------------------- |
| clone 방법            | https 형식                              | https://github.com/myMediaBrains/git-tutorial.git                            |
|                       | ssh 형식                                | git@github.com:myMediaBrains/git-tutorial.git                                |
| 명령어                | http                                    | $ git clone https://github.com/myMediaBrains/git-tutorial.git                |
|                       | ssh                                     | $ git clone git@github.com:myMediaBrains/git-tutorial.git                    |
| clone한 저장소 확인   |                                         | $ git remote -v                                                              |
| 오픈소스 클론 방법    | clone                                   | $ got clone https://github.com/ethereum/go-ethereum.git                      |
|                       | git 저장소 이동                         | $ cd go-ethereum                                                             |
|                       |                                         | read 할 수 있지만, write 권한은 없다. 따라서, push 작업 불가능               |
| private clone         | https                                   | id와 password 를 입력해야 한다.                                              |
|                       | ssh                                     | ssh 가 설정되어 있으면, 별도의 인증이 필요없다.                              |
| 특정 브랜치만 clone   |                                         | $ git clone \--branch [TAG] {REPO_URL}                                       |
| shallow clone         | 최신 변경만이 반영된 소스 코드만을 복제 | $ git clone \--depth=1 https://github.com/ethereum/go-ethereum.git           |
| 이미 기존 폴더가 존재 | 에러 발생 > 다른 디렉토리 만들 수 있음  | $ git clone https://github.com/myMediaBrains/git-tutorial.git git-tutorial-2 |
| permission denied     | ssh 확인 후 안되면 재설정               | $ ssh -T git@github.com                                                      |
