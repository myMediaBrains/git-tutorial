# README.md

## Quick setup

| no   | 구분                             |      | 액션                                                         |
| ---- | -------------------------------- | ---- | ------------------------------------------------------------ |
| 1    | 전제조건                         | 1    | GitHub 에 new remote repository  **“git-tutorial”** 생성     |
|      |                                  | 2    | root 폴더에 **README.md**  생성                              |
|      |                                  | 3    | root 폴더에 현재 빈 파일인 **.gitignore** 생성               |
| 2    | git 저장소 생성                  | 1    | git init                                                     |
|      |                                  | 2    | git add README.md                                            |
|      |                                  | 3    | git commit -m “first commit”                                 |
|      |                                  | 4    | git branch -M main                                           |
|      |                                  | 5    | git remote add origin git@github.com:myMediaBrains/git-tutorial |
|      | GitHub remote repository 에 push | 6    | git push -u origin main                                      |



| 구분    | no   | 명령                                                         | 비고                          |
| ------- | ---- | ------------------------------------------------------------ | ----------------------------- |
| Setup   | 1    | git config \--global user.name “myMediaBrains”               | account 설정                  |
|         |      | git config \--global user.email “my.media.brains@gmail.co”   |                               |
|         | 2    | git init                                                     | git 저장소 초기화             |
|         | 3    | git remote add origin https://github.com/myMediaBrains/tutorial.git | git 의  GitHub endpoint  지정 |
|         | 4    | git clone https://github.com/myMediaBrains/tutorial.git      | GitHub 파일을 로컬로 복제     |
| SSH Key | 1    | ssh-keygen                                                   | 개인키 및 공개키 생성         |
|         | 2    | ~/.ssh/id_rsa.pub                                            | 공개키 내용 copy              |
|         | 3    | GitHup > Profile > Settings > SSH and GPG keys > New SSH key > Title / Key | Key 에 공개키 내용 paste      |
|         | 4    | Clone or download > Clone with HTTPS > Use SSH 버튼 클릭     |                               |
|         | 5    | git remote set-url origin git@github.com:myMediaBrains/tutorial.git | origin의 Remote URL 변경방법  |
|         | 6    | git remote show origin                                       | origin의 Remote URL 변경 체크 |
|         |      |                                                              |                               |

