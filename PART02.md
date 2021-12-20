[← 뒤로](./README.md)

# <img src="./assets/icon-git-1.jpg" alt /> Git 버전 관리 에센셜 PART 02

Git을 사용해 프로젝트 버전 관리하는 방법을 살펴보겠습니다. CLI와 GUI 환경에서 Git을 사용하는 방법을 비교해보겠습니다.

<a href="https://bit.ly/GIT_ESSENTIAL" target="_blank"><img src="./assets/00-COVER.jpg" alt /></a>



<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> Git 환경 설정하기

Git을 사용하기 위해서는 로컬 컴퓨터에 사용자 정보를 등록해야 합니다. 등록해야 하는 사용자 정보는 사용자 "ID"와 사용자의 "이메일 주소" 입니다. 여기서는 Github 계정에 가입할 때 설정한 "ID"와 사용자의 "이메일 주소"를 CLI 명령어로 등록해 보도록 하겠습니다.


#### CLI 명령어 환경 —

`config` 명령을 사용해 글로벌(`--global`) 옵션 플래그를 사용하여 Git의 글로벌 사용 환경을 설정합니다.
Git 환경 설정은 사용자 이름과 이메일 주소를 설정하는 것으로 Git은 커밋할 때마다 이 정보를 사용합니다.
필요한 경우 환경 설정은 언제든지 다시 수정할 수 있습니다.

```sh
$ git config --global user.name <"사용자 ID">
$ git config --global user.email <"이메일 주소">
```


<!-- ----------------------------------------------------------------------- -->



#### GUI 그래픽 환경 —

VSCode에서는 설정할 수 없습니다.

<br>

<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> VS Code를 기본 에디터로 설정하기

Git에서 사용하는 기본 에디터를 Visual Studio Code(VS Code)로 설정하는 방법을 살펴보겠습니다.

#### CLI 명령어 환경 —

기본 에디터를 Visual Studio Code로 지정합니다.

```sh
$ git config --global core.editor "code --wait"
```

#### GUI 그래픽 환경 —

VSCode에서는 설정할 수 없습니다.

<br>

<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> Git 환경 설정 값 확인하기

사용자 "ID"와 사용자의 "이메일 주소" 그리고 기본 에디터 등 Git 환경 설정 값을 확인해보겠습니다.

#### CLI 명령어 환경 —

현재 Git에 설정된 값들을 확인하려면 `config --list` 명령을 사용합니다.

```sh
$ git config --list
```

명령이 실행되면 현재 Git config 설정 값이 출력됩니다.

```sh
$ git config --list
  credential.helper=osxkeychain
  core.excludesfile=/Users/seulbinim-imac/.gitignore_global
  filter.lfs.process=git-lfs filter-process
  filter.lfs.required=true
  filter.lfs.clean=git-lfs clean -- %f
  filter.lfs.smudge=git-lfs smudge -- %f
  user.name=seulbinim
  user.email=seulbinim@gmail.com
  core.editor=code --wait
  core.repositoryformatversion=0
  core.filemode=true
  core.bare=false
  core.logallrefupdates=true
  core.ignorecase=true
  core.precomposeunicode=true
  remote.origin.url=https://github.com/seulbinim/git-study.git
  remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
```

#### GUI 그래픽 환경 —

VSCode에서는 설정할 수 없습니다.

<br>

<!-- ----------------------------------------------------------------------- -->
## <img src="./assets/icon-git-2.png" alt /> Git 글로벌 환경 설정 파일 에디터로 열기

사용자 "ID"와 사용자의 "이메일 주소" 그리고 기본 에디터 등 Git 글로벌 환경 설정(`.gitconfig`) 파일을 에디터에서 열 수 있습니다.

#### CLI 명령어 환경 —

Git에 설정된 글로벌 설정 파일을 에디터로 열려면 `config --global -e` 명령을 사용합니다.

```sh
$ git config --global -e
```

#### GUI 그래픽 환경 —

VSCode에서는 설정할 수 없습니다.

<br>

<!-- ----------------------------------------------------------------------- -->
