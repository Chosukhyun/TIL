# 2일차 정리

# git hub

## 1. git hub setting 하기

- __[Git Hub](https://github.com/) 사이트에 접속하기__
- 로그인 후, `Settings` 클릭
- `Repositories` 클릭 후, `Repository default branch`에 `"master"`입력 후 `update` 클릭




---

## 2. git hub에서 Repository 생성하기

- __좌측 상단 문어 고양이 __ 클릭 후, `New`버튼 클릭
- `Repository name`에 이름 만들고 설정 클릭 후, `Create Repository` 클릭하여 생성

---

## 3. git 명령어

1. 깃 계정정보 등록(유저명, 이메일)

- 초기설정하면 더 이상 안해도 됨

- `git config --global user .name "유저명"`
- `git config --global user .email "이메일"` 





2. 등록된 계정정보 확인하기

- `git config --global --list`





3. 등록한 계정정보 삭제하기

- `git config --global --unset user .name`
- `git config --global --unset user .email`
  - 삭제한 이메일이나 유저네임은 다시 계정정보를 등록해야 함





4. `git init`

- `git init`입력하면 터미널 창의 폴더명 옆에 `~/(master)`표시가 됨

- `git init`을 입력한 폴더가 __repository__ 역할을 하게 해줌
- __유의사항__ 
  - <u>처음 1회만 설정</u>하면 됨
  - <u>__홈폴더(users)에서 입력하면 안됨__</u>
  - `git init`한 폴더의 <u>__하위폴더에서 절대 입력하면 안됨__</u> (__상위폴더__가 `~/(master)`인지 확인하기)



5. `git add 파일명`

- 파일 상태가 `added`로 __Staging Area__로 파일이 올라옴을 의미
- __staging area__로 올라와서, __Tracked__상태로 git이 파일을 관리하는 상태가 됨
- `git add .`: 폴더 내의 모든 파일을 __staging area__로 올라옴



6. `git status`

- 파일의 상태를 확인
  - Untracked : 단 한 번도 git이 관리하지 않았음을 의미
  - Tracked : git이 파일을 추적하는 상태
  - 

---

## 4. TIL repository 연결(remote - local) 

### 1) `Remote Respository`란?

### 2) `Local Respository`란?

### 3) Remote ↔ Local 연결하기

---

## 5. README.md생성하여 git hub에 올리기

---

## 6. `.gitignore` 생성하기

---

## 7. clone, pull

### 1)clone과 pull의 차이

### 2) pull ↔push

---

## ※ conflict 오류

### 1) conflict 발생 원인

### 2) 해결 과정



