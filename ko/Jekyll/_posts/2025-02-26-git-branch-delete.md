---
title: "Git 브랜치 삭제하기"
excerpt: 
tags: Github 깃허브 Git 깃 branch 브랜치 
header:
  teaser: https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png
---

브랜치를 삭제하는 방법을 알아보자.

# 로컬 브랜치

## 로컬 브랜치 목록 확인하기

우선 로컬 브랜치 목록을 확인해보자.

```
git branch
```

## 브랜치 전환하기

로컬 브랜치를 삭제하기 위해서 삭제할 브랜치가 아닌 브랜치로 전환해야 한다.

```
git checkout <branch name>
```
위의 명령어를 통해 `branch name`브랜치로 전환할 수 있다.

예시 - main 브랜치로 전환하기
```
git checkout main
```


## 로컬 브랜치 삭제하기


```
git branch -d <branch name>
```

`-d`는 `--delete`의 약자로 `삭제`의 의미를 담은 플래그이다.

예시 - test 브랜치 삭제하기
```
git branch -d test
```

### 에러 1: 작업 중인 브랜치
현재 작업 중인 브랜치는 삭제할 수 없다. 

만일 아래의 에러를 만났다면, 작업 중인 브랜치를 삭제하려 시도한 것이다.
```
error: Cannot delete branch '<branch name>' checked out at '<repository path>'
```
`브랜치 전환하기`를 참고하여 다른 브랜치로 이동하고 다시 시도해 보자.

### 에러 2: 기록되지 않은 커밋
삭제하고자 하는 브랜치가 가진 커밋이 다른 브랜치나 저장소에 저장되어 있지 않다면, 실수로 커밋 기록이 손상되는 것을 막기 위해 에러가 발생한다. 

만일 아래의 에러를 만났다면, 브랜치에 기록되지 않은 커밋이 존재하는 것이다.
```
error: The branch '<branch name>' is not fully merged.
```
정말로 삭제하기를 원한다면, `-d` 대신 `-D`를 사용해보자.

`-D`는 `--delete --force`의 약자로 `강제 삭제`의 의미를 담은 플래그이다.

# 원격 브랜치

## 원격 브랜치 목록 확인하기
원격 브랜치의 목록을 확인해보자.
```
git branch -a
```
`-a`는 `--all`의 약자로 `모두`의 의미를 담은 플래그이다. 로컬과 원격 브랜치 모두를 확인할 수 있다.

```
git branch -r
```
`-r`는 `--remotes`의 약자로 `원격`의 의미를 담은 플래그이다. 원격 브랜치를 확인할 수 있다.

## 원격 브랜치 삭제하기
저장소 이름은 기본적으로 `origin`이다.
```
git push <storage name> -d <branch name>
```

예시 - test 브랜치 삭제하기
```
git push origin -d test
```

### 저장소 이름을 모를 때
```
git remote
```
저장소 이름을 보여준다.

# 총정리
## 목록확인
로컬: `git branch` / 원격: `git branch -r`
## 삭제하기
로컬: `git branch -d <branch name>` / 원격: `git push <storage name> -d <branch name>`