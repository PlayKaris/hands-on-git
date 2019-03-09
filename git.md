#  GIT config 설정
------------------------

## 1. 커밋할 때 입력되는 사용자의 이메일과 이름정보를 등록하는 방법

```git config --global user.name "hunvely"```

```git config --global user.email "example@example.com"```

## 2. git config 설정 학인

```git config --list```


# GIT 기본 명령어
-----------------

## 1. 폴더를 하나 만들고 폴더 안에서 명령을 실행

```git init```

## 2. 저장소 GIT에서 받아오기

```git clone 원격저장소 경로```

## 3. 변경된 파일 Stage에 추가

```git add <파일이름>```

```git add *```

## 4. Stage > Head로 커밋방법

```git commit -m "설명"```

## 5. 변경 내용 발행(push)하기

```git push origin master```

## 6. 원격 저장소 연결

```git remote add origin <원격 서버 주소>```

## 7. GIT 원격 저장소 확인

```git remote -v```

## 8. GIT 원격 저장소 변경

```git remote set-url origin <원격 서버 주소>```

# 브런치 만들기
--------------

## 1. 브런치 생성

```git checkout -b new_branch```

## 2. 브런치 변경

``` git checkout master```

## 3. 브런치 삭제

```git branch -d new_branch```

## 4. 브런치 원격저장소로 Push

```git push origin <브런치 이름>```

# 갱신과 병합
-------------

## 1. 로컬 저장소를 원격저장소랑 싱크 맞추기

```git pull```

## 2. 다른 브런치에 변경내용을 현재 브런치에 병합

```git merge <브런치 이름>```
