# README.md

## Quick setup

| no   | 구분                             |      | 액션                                                         |
| ---- | -------------------------------- | ---- | ------------------------------------------------------------ |
| 1    | 전제조건                         | 1    | GitHub 에 new remote repository  **“git-tutorial”** 생성     |
|      |                                  | 2    | root 폴더에 **README.md**  생성                              |
|      |                                  | 3    | root 폴더에 현재 빈 파일인 **.gitignore** 생성               |
|      |                                  | 4    | git config \--global user.name “myMediaBrains”               |
|      |                                  | 5    | git config \--global user.email “my.media.brains@gmail.co”   |
| 2    | git 저장소 생성                  | 1    | git init                                                     |
|      |                                  | 2    | git add README.md                                            |
|      |                                  | 3    | git commit -m “first commit”                                 |
|      |                                  | 4    | git branch -M main                                           |
|      |                                  | 5    | git remote add origin git@github.com:myMediaBrains/git-tutorial |
|      | GitHub remote repository 에 push | 6    | git push -u origin main                                      |

## SSH 설정

| no   | 구분                                                         | 설명                               |
| ---- | ------------------------------------------------------------ | ---------------------------------- |
| 1    | $ git version                                                | git 설치 확인                      |
| 2    | $ cd ~/.ssh                                                  | id_rsa 및 id_rsa.pub 파일 확인     |
| 3    | $ ssh-keygen -t rsa -C “my.media.brains@gmail.com”           | 새로운 개인키 및 공개키 생성       |
|      |                                                              | 물어보는 질문은 디폴트로 엔터      |
| 4    | $ cd ~/.ssh                                                  | id_rsa 및 id_rsa.pub 파일 확인     |
| 5    | $ vi id_rsa.pub                                              | 내용 copy                          |
| 6    | GitHub > Profile 아이콘 > Settings > SSH and GPG keys > New SSH key > Title & Key | Key 에 copy 한 id_rsa.pub 를 paste |

