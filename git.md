# GIT config 설정

### 1. 커밋할 때 입력되는 사용자의 이메일과 이름정보를 등록하는 방법 
#### 모든 프로젝트에 적용(--global)  
```git config --global user.name "hunvely"```  
```git config --global user.email "example@example.com"```  
#### 로컬 프로젝트에 적용(--local)
``` git config --local user.name "hunvely"```  
``` git config --local user.email "example@example.com"```  

### 2. git config 설정 확인  
```git config --list```

<br/>
<br/>

# GIT 기본 명령어

### 1. 폴더를 하나 만들고 폴더 안에서 명령을 실행  
```git init```

### 2. 저장소 GIT에서 받아오기  
```git clone 원격저장소 경로```

### 3. 변경된 파일 Stage에 추가  
```git add <파일이름>```  
```git add *```

### 4. Stage > Head로 커밋방법  
```git commit -m "설명"```

### 5. 변경 내용 PUSH 하기
#### 기존 PUSH  
```git push origin master```  
#### 강제 PUSH (+)
```git push origin +master```  

### 6. 원격 저장소 연결  
```git remote add origin <원격 서버 주소>```

### 7. GIT 원격 저장소 확인  
```git remote -v```

### 8. GIT 원격 저장소 변경  
```git remote set-url origin <원격 서버 주소>```

### 9. 원격 저장소에 있는 소스를 가져와 자동 병합
```git pull ```<br/>
```git pull origin master```

<br/>
<br/>

# 브런치 만들기

### 1. 브런치 생성  
```git checkout -b new_branch```

### 2. 브런치 변경  
``` git checkout master```

### 3. 브런치 삭제  
```git branch -d new_branch```

### 4. 브런치 원격저장소로 Push  
```git push origin <브런치 이름>```

<br/>
<br/>

# 갱신과 병합

### 1. 로컬 저장소를 원격저장소랑 싱크 맞추기  
```git pull```

### 2. 다른 브런치에 변경내용을 현재 브런치에 병합  
```git merge <브런치 이름>```

<br/>
<br/>

# Reset

### hard 옵션 : 지정한 커밋 이후의 기록이 모두 지워짐
```git reset hard <되돌릴 커밋>```
### soft 옵션 : 지정한 커밋 이후의 기록이 지워지지 X, (인덱스)스테이지에도 초기화 되지 않음
```git soft hard <되돌릴 커밋>```
### mixed 옵션 : 지정한 커밋 이후의 기록이 지워지지 X, (인덱스)스테이지에는 초기화 됨
```git mixed hard <되돌릴 커밋>```

<br/>
<br/>

# Revert 

### 지정한 커밋 이후의 기록이 모두 지워짐
```git revert <되돌릴 커밋> ```

### 되돌릴 커밋이 여러개일 때 범위 지정 가능
```git revert 2664ce8..15413dc ```

<br/>
<br/>

## Reset / Revert 차이

### Reset

```
1. 이후의 이력을 모두 삭제함.
2. 원격레포지토리에 PUSH를 한 상태에서 Reset을 사용하면 Reset을 하기 이전으로 되돌리기 전에는 push을 하지 못함.
   이유 : Git은 각각의 커밋이 부모를 바라보고 있기 때문에 중간 커밋을 삭제하면 2가지 분기가 나타나기 때문.
```

### Revert
```
1. Revert는 범위를 지정해서 중간에 있는 커밋만 삭제할 수 있음
2. 이미 PUSH가 된 커밋이라면 Revert를 사용해야함
```

