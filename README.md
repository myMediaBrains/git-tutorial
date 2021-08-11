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

## GitHub 저장소 생성 및 개발 환경

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
|     |                                         |                       |
|     |                                         |                       |
|     |                                         |                       |
|     |                                         |                       |

GitHub 계정을 생성하고 초기 셋업을 마쳤으면 이제 저장소를 만들고 코딩에 푹 빠져들 시간입니다. 😎

Git이 처음이라면, 먼저 로컬 시스템에서 사용할 사용자 이름과 이메일을 설정행야합니다. 이 정보는 커밋할 때 함게 기록되며 GitHub에서도 GitHub 사용자를 매칭할 때 사용합니다.

```
$ git config --global user.name "Your Name"
$ git config --global user.email you@example.com
```

빠르게 두 줄을 실행해주면 됩니다(이름과 이메일은 변경해주세요). 아래 글에서 이름과 이메일 설정에 대해서 더 자세히 살펴봅니다. 🧐

- [Git/GitHub의 커밋 사용자 이름과 이메일 설정하는 방법](https://www.lainyzine.com/ko/article/how-to-set-git-repository-username-and-email/)

이제 저장소를 만들어볼 차례입니다. GitHub에서 저장소를 만들고 로컬 Git 저장소와 연동하는 방법을 소개합니다.

- [GitHub에서 새로운 저장소 생성하는 방법](https://www.lainyzine.com/ko/article/how-to-create-a-new-remote-git-repository-on-github/)
- [GitHub 원격 저장소와 로컬 Git 저장소 연동하는 방법](https://www.lainyzine.com/ko/article/how-to-link-github-remote-repository-and-local-git-repository/)

위의 글만 이해해도 GitHub의 기초적인 사용은 가능합니다만, 저장소를 초기화하는 `git init`과 원격 저장소를 복제해오는 `git clone`에 대해서 더 자세히 알고 싶다면 다음 글을 클릭 클릭, 함께 공부해요.

- [git init 사용법: Git 저장소를 초기화하는 방법](https://www.lainyzine.com/ko/article/git-init-how-to-initialize-git-repository/)
- [git clone 사용법: 원격 Git 저장소 복제](https://www.lainyzine.com/ko/article/git-clone-command/)

테스트로 만든 저장소를 삭제하고 싶나요? 아니면 더 이상 GitHub에서 코드를 공개하고싶지 않나요? GitHub 저장소를 삭제하는 방법을 소개합니다.

🔥 **주의: 한 번 삭제하면 되돌릴 수 없어요.** 🔥

- [Git 저장소와 원격 GitHub 저장소를 삭제하는 방법](https://www.lainyzine.com/ko/article/how-to-remove-git-repository-and-github-repository/)

## GitHub 단체(Organization)

GitHub은 개인 계정으로도 사용할 수 있지만, 본격적인 협업을 위해서는 단체(Organization) 계정을 만들어 사용합니다. 협업을 위해 단체를 만드는 방법을 소개합니다. 🤼‍♀️

- [GitHub에서 협업 용 단체(Organization) 만드는 방법](https://www.lainyzine.com/ko/article/how-to-create-an-organization-for-collaboration-on-github/)

GitHub 단체를 만들거나, 단체에 초대 받더라도 단체 멤버 외에는 내가 멤버라는 것을 알 수 없습니다. 특정 단체에 소속되어있는지 여부를 공개하려면 추가 설정이 필요합니다.

- [GitHub 단체(Organization) 멤버 여부 공개하는 방법](https://www.lainyzine.com/ko/article/how-to-disclose-whether-you-are-a-member-of-the-github-organization/)

## GitHub 활용

GitHub을 개인 프로젝트에서도 쓰고, 회사에서도 쓰고, 계정도 여러 개 가지고 계신가요? 프로 개발자군요! 👨‍💻

프로 개발자 분을 위한 저장소 별로 프로필을 다르게 설정할 수 있는 팁입니다. 🍯

- [Git 저장소 별로 사용자 이름과 이메일 다르게 설정하는 방법](https://www.lainyzine.com/ko/article/how-to-set-a-different-username-and-email-for-each-git-repository/)

단순히 커밋에 기록하는 사용자 이름과 이메일을 다르게 하는 것이 아니라, 연동하고자 하는 GitHub 계정을 변경하는 방법은 다음 글에서 다룹니다. GitHub 계정을 완전히 변경하는 경우와 특정 저장소의 GitHub 계정만 변경하는 경우를 나눠서 설명합니다.

- [개발 환경에서 사용중인 GitHub 계정 변경하는 방법](https://www.lainyzine.com/ko/article/how-to-change-the-github-account-used-by-the-development-environment/)

한 두개 저장소만 사용할 때는 위의 팁으로 충분합니다만, 상시적으로 멀티 어카운트를 사용하시는 프로 개발자 분들께 아래 글을 바칩니다. 디렉터리 별 사용자 프로필 셋업과 프로젝트 별 SSH 설정도 소개합니다. 👩‍🚒🧛‍♀️🥷

- [GitHub 멀티 어카운트를 사용할 때 유용한 Git 설정](https://www.lainyzine.com/ko/article/useful-git-settings-when-using-github-multi-account/)

가끔 GitHub 상태가 이상한 것 같은데, 나만 그런 걸까요? 현재 GitHub 상태를 확인할 수 있는 몇 가지 방법들을 함께 살펴봅니다.

- [GitHub 장애 상황을 확인하는 방법](https://www.lainyzine.com/ko/article/how-to-check-github-outage-status/)

GitHub의 사용자 이름은 고유한 값으로 특정 사용자를 식별하는 ID로서 사용됩니다. 권장하지는 않습니다만, 원한다면 이 사용자 이름을 변경하는 것도 가능합니다. ID를 바꾸는 방법과 ID 변경시 생기는 부작용에 대해서 알아봅니다.

- [GitHub의 계정 이름 변경하는 방법](
