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

### git bash에서 계정 설정

1. 깃 계정정보 등록(유저명, 이메일)

- 초기설정하면 더 이상 안해도 됨

```bash
# git hub 유저명 입력
git config --global user .name "Chosukhyun"`

# git hub 이메일 입력
git config --global user .email "asa950@naver.com"`
```





2. 등록된 계정정보 확인하기

```bash
# git hub 유저네임과 이메일 확인하기
git config --global --list
```





3. 등록한 계정정보 삭제하기

```bash
# git hub 유저네임 삭제하기
git config --global --unset user .name

# git hub 이메일 삭제하기
git config --global --unset user .email
```

- 삭제한 이메일이나 유저네임은 다시 계정정보를 등록해야 함



### <상향식> git init ~ push 

1. 일반폴더(TIL) 생성 후, TIL폴더 bash창에서 `git init` 입력

- `git init`입력하면 터미널 창의 폴더명 옆에 `~/(master)`표시가 됨

- `git init`을 입력한 폴더가 __repository__ 역할을 하게 해줌
- __유의사항__ 
  - <u>처음 1회만 설정</u>하면 됨
  - <u>__홈폴더(users)에서 입력하면 안됨__</u>
  - `git init`한 폴더의 <u>__하위폴더에서 절대 입력하면 안됨__</u> (__상위폴더__가 `~/(master)`인지 확인하기)

```bash
# 일반폴더(TIL)을 git이 respository로 생성
git init 

# 파일의 상태를 보여주는 명령어
git status
 - 현재 파일상태는 untracked 상태 : 파일을 git이 관리하고 있지 않음
```



2. `git add `

- 파일 상태가 `added`로 __Staging Area__로 파일이 올라옴을 의미
- __staging area__로 올라와서, __Tracked__상태로 git이 파일을 관리하는 상태가 됨

```bash
# 파일을 added상태로 만듬
git add 파일명

# 폴더 내의 모든 파일을 __staging area__로 올라옴
git add .

# 파일의 상태를 확인
git status
 - Untracked : 단 한 번도 git이 관리하지 않았음을 의미(git add 입력 전 상태)
 - Added : 파일이 repository에 추가 된 상태
 - Tracked : git이 파일을 추적하는 상태
```



3. commit 기록

- Staging Area로 올린 파일을 commit으로 저장소에 기록했다는 것을 의미

```bash
# commit 기록하기
git commit -m "커밋의 이유 입력"

# commit변경사항의 내역을 한 줄로 보여줌
git log --oneline
 - 빠져나가기 : "q" 입력
```



__↓ Remote 원격저장소(깃헙 내의 repository)와 길 만들기__



4. remote 저장소 ↔ local 저장소와 연결

```bash
# 두 저장소 간 연결하는 길 생성
git remote add origin [깃허브의 원격 url]

# 저장소가 연결되었는지 확인
git remote -v
```



5. local 저장소의 변경사항을 remote 저장소로 밀어(push)올리기

```bash
# commit을 remote저장소(git hub) 올리기
git push origin master
```



### <하향식> git clone과 pull

#### git clone

__`Ex 상황)`__  내 컴퓨터가 아닌 외부 컴퓨터로 작업하는 경우, 

- __파일을 git hub에서 local저장소로 가져오기__ 
  - git hub의 repository를 local로 복제하기(remote 저장소와 연결)
  - clone하면 자동으로 길이 생성 되므로 `git init`을 할 필요가 <u>없음</u>
  - <u>__주의할 점__</u> : `git init`된 저장소에서는 `git clone` <u>__입력 금지__</u>

```bash
# 홈폴더(Suk Hyun Cho폴더)의 bash창에서 입력해서 저장소(repository) 형성
git clone [remote저장소 url]
 - clone은 git hub의 respository를 복제
```



#### pull

- remote저장소의 파일을 <u>__나의 local 저장소__</u>로 내려받기

```bash
# 원격저장소에 있는 파일의 같은 버전을 내려받을 수 있음
git pull origin master
- remote저장소에서 내려받은 파일을 가지고 외부컴퓨터로 작업하고 다시 git hub으로 올리는 방식으로 작업 가능
```



#### __`정리`__

- __분산버전관리__ → git hub은 협업을 위한 기본적인 툴
  - git hub(remote repository)을 기준으로 하여 local repository에서 push와 pull을 하며 같은 버전의 파일을 공유하는 것
  - 한 저장소에서 push와 pull 가능

---

## 5. README.md생성하여 git hub에 올리기

---

## 6. `.gitignore` 생성하기



## 

---

## ※ conflict 오류

### 1) conflict 발생 원인

### 2) 해결 과정



