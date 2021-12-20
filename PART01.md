[← 뒤로](./README.md)

# <img src="./assets/icon-git-1.jpg" alt /> Git 버전 관리 에센셜 PART 01

Git을 사용해 프로젝트 버전 관리하는 방법을 살펴봅니다. CLI와 GUI 환경에서 Git을 사용하는 방법을 비교해봅니다.

<a href="https://bit.ly/GIT_ESSENTIAL" target="_blank"><img src="./assets/00-COVER.jpg" alt /></a>


<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> Git 워크플로우

Git을 사용해 프로젝트 버전을 관리하는 흐름을 표현하면 다음과 같습니다.

```sh
                 - add →        - commit →                 - push →
+-------------------+---------------+-------------------------+-------------------+
| Working directory | Index (Stage) | Local repository (HEAD) | Remote repository |
+-------------------+---------------+-------------------------+-------------------+
               ← restore -      ← reset -                  ← fetch -
```


<!-- ----------------------------------------------------------------------- -->


## <img src="./assets/icon-git-2.png" alt /> Git 버전 확인

`--version` 옵션 플래그를 사용하면 설치 된 `git` 버전이 출력됩니다.

```sh
$ git --version
```


<!-- ----------------------------------------------------------------------- -->
