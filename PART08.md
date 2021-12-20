[← 뒤로](./README.md)

# <img src="./assets/icon-git-1.jpg" alt /> Git 버전 관리 에센셜 PART 08

Git을 사용해 프로젝트 버전 관리하는 방법을 살펴봅니다. CLI와 GUI 환경에서 Git을 사용하는 방법을 비교해봅니다.

<a href="https://bit.ly/GIT_ESSENTIAL" target="_blank"><img src="./assets/00-COVER.jpg" alt /></a>


<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> 원격 저장소 가져오기

`fetch` 명령을 사용해 원격 저장소의 수정 내용을 로컬 저장소로 가져올 수 있습니다. 이는 `pull` 명령과 유사하지만 조금 다른 점이 있습니다. 바로 병합 여부인데 `pull`은 `fetch` + `merge` 즉 수정된 내용을 자동으로 병합하는 방식이고 `fetch`는 수동으로 병합하는 방식입니다. 

#### CLI 명령어 환경 —

`fetch` 명령을 사용해 원격 저장소의 수정 내용을 로컬 저장소로 가져올 수 있습니다.

```sh
$ git fetch origin <브랜치명>
```


#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>

<!-- ----------------------------------------------------------------------- -->
## <img src="./assets/icon-git-2.png" alt /> 임시 저장소로 이동하기

`fetch` 명령을 실행하면 원격 저장소의 내용을 로컬 저장소로 가져올 때 임시로 FETCH_HEAD라는 이름의 브랜치를 생성해 주게 됩니다. 이때 해당 브랜치의 수정 내용을 확인하기 위해 임시 저장소로 이동할 수 있습니다.  

#### CLI 명령어 환경 —

`checkout` 명령을 사용해 임시로 생성한 FETCH_HEAD 브랜치의 내용을 조회할 수 있습니다. 

```sh
$ git checkout FETCH_HEAD
```

다시 master 브랜치로 이동하고 싶을 때 `checkout` 명령을 사용할 수 있습니다. 

```sh
$ git checkout master
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>
<!-- ----------------------------------------------------------------------- -->

## <img src="./assets/icon-git-2.png" alt /> 임시 저장소 병합하기

`fetch` 명령을 실행하여 로컬로 가져온 임시 저장소 FETCH_HEAD 브랜치의 수정된 내용을 로컬 저장소에 반영하기 위해 `merge` 명령을 사용할 수 있습니다. 이때 주의할 점은 master 브랜치로 이동 후 `merge`을 이용해 병합해야 합니다. 

#### CLI 명령어 환경 —

`merge` 명령을 사용해 임시로 생성한 FETCH_HEAD 브랜치의 내용을 master 브랜치에 병합할 수 있습니다. 

```sh
$ git checkout master
$ git merge origin/master
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>
<!-- ----------------------------------------------------------------------- -->
