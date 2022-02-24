# 1.CLI 기초

## 1) CLI(Command Line Interface) 란?

- 터미널을 통해 사용자와 컴퓨터가 상호작용 하는 것

- 디렉토리를 만드는 데에도 GUI 보다 과정이 간소화 됨





## 2) Git Bash

- `Git Bash`란?
  - UNIX 계열 운영체제의 CLI환경

- `Git Bash` 사용이유
  1) Window에서도 UNIX계열 운영체제의 터미널 명령어를 사용하기 위함
  2) 개발 시장에서 UNIX계열 운영체제가 더 많이 사용되기 때문
  3) UNIX계열 운영체제의 터미널 명령어를 연습하기 위함
  4) __버전관리에 용이__: 변경사항들과 최종 레포트만 저장함





## 3) 경로

- __루트 디렉토리__(Root Directory, `/`)
  - 모든 파일과 폴더를 담고 있는 최상위 폴더
  - Windows의 경우, 보통 __`C 드라이브`__를 의미 함



- __홈 디렉토리(Home Directory, `~`)__
  - `Tilde`라고 부르며, 현재 로그인 된 사용자의 홈 폴더를 의미
  - Window의 경우 __`C:/사용자(Users)/현재 사용자 계정`__을 의미함

---

- __절대 경로__

  - 루트 디렉토리 부터 목적지점 까지 거치는 경로를 전부 작성한 것

  - 윈도우 바탕화면의 절대경로

    __`C:/Users/asa95/Desktop`__



- __상대경로__
  - 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것
  - 현재 작업하고 있는 디렉토리가 `C:/Users`라고 하면
  - 바탕화면의 상대경로는 `asa95/Desktop`이 됨
  - 현재 작업하고 있는 디렉토리가 변경되면 상대 경로도 변경됨
  - `./` : 현재 작업하고 있는 폴더를 의미
  - `../` : 현재 작업하고 있는 폴더의 부모 폴더를 의미





## 4) Git Bash 

- **Git Bash CLI창 열기**
  - 홈 디렉토리에서 마우스 오른쪽 클릭하여 `'git bash here'`를 클릭



### 터미널 명령어

1. __`mkdir 폴더명`__

   - make directory
   - 새 폴더를 생성하는 명령어
   - 폴더 이름 사이에 공백 넣으려면 `"파일명"`형식으로 입력

   ```bash
   mkdir folder
   
   mkdir "hello world"
   ```

   

2. __`touch 파일명`__

   - 파일을 생성하는 명령어
   - 띄어쓰기로 구분하여 **여러 파일을 한꺼번에 생성 가능**
   - **숨김파일**을 만들려면, `.`을 **파일명 앞**에 붙여야 함

   ```bash
   touch a.txt
   
   touch a.txt b.txt c.txt
   
   touch .happy.txt



3. __`pwd`__

   - 현재 파일의 작업위치  찾을 때 사용

   ```bash
   pwd #/c/Users/asa95

4. __`ls`__

   - list segments
   - <u>현재 작업 중인 디렉토리의 폴더/파일의 리스트를 보여주는 명령어</u>
   - `-a` : __all__옵션, <u>숨김파일</u> 까지 모두 보여줌
   - `-l` : __long__옵션. 용량, 수정 날짜 등 파일 정보를 자세히 보여줌

   ```bash
   # 기본사용
   ls
   
   # all 옵션
   ls -a
   
   # long 옵션
   ls -l
   
   # all, long 옵션 같이 적용
   ls -a -l
   
   #여러 옵션 축약
   ls -al



5. __`cd `__

   - change directory
   - __현재 작업 중인 디렉토리__를 <u>변경</u>
   - `cd 폴더명` : `cd`뒤에 쓰여진 폴더로 디렉토리 변경
   - `cd`, `cd ~` : __홈 디렉토리__로 이동
   - `cd ..` : 내 디렉토리의 __부모 디렉토리(상위 디렉토리)__로 이동
   - `cd -` : 바로 __이전 디렉토리__로 이동<u>(뒤로 가기)</u>


   ```bash
   #디렉토리의 위치를 폴더test로 이동
   cd test

   #절대 경로 통한 디렉토리 변경
   cd c/users/asa95/Desktop

   #상대 경로 통한 디렉토리 변경
   cd ../parent/child
   ```


6. __`mv `__

   - move

   - 1. 파일/폴더를 다른 폴더 내로 이동하는 명령어

        `mv "이동시킬 파일명" "파일을 이동시킬 폴더명"`

     2. <u>이동시킬 폴더가 없으면</u>, 파일/폴더명이 __변경__됨

        `mv "파일명" "변경할 파일명"`

   ```bash
   # text파일을 happy폴더 안에 이동
   mv text.txt happy
   
   # text.txt파일명을 a.txt로 변경
   mv text.txt a.txt



7. __`rm`__

   - remove
   - 폴더/파일을 삭제하는 명령어
   - <u>__주의__</u> : `rm`사용하여 제거 시, 폴더/파일이 `영구 삭제` 됨으로 복구가 불가
   - `rm -r 폴더명/` : recursive옵션. 재귀적으로 __폴더__의 하단 내역 지울 때 사용
   - `rm -rf 폴더명/` : __강제 삭제__ 옵션(왠만하면 사용 추천 안함)
   - `*(asterisk, wildcard)`를 이용해 `rm *.txt` 입력하면 __txt파일 전체를 지움 __

   ```bash
   # a.txt파일을 삭제
   rm a.txt
   
   # bag라는 폴더를 삭제
   rm -r bag
   
   # bag 폴더를 강제 삭제
   rm -rf bag
   ```



8. __`start`__

   - window에서 현재 작업 중인 폴더/ 파일 여는 명령어
   - 다른 위치의 파일을 열려면 `cd 이동할 폴더명`을 입력하여 디렉토리의 위치를 파일이 저장된 위치로 바꾼 후 `start 파일명`을 입력

   

```bash
# animal 폴더 열기
start animal

# cat.txt 파일 열기
start cat.txt
```



9. 단축키
   - `↑, ↓ 방향키` : 이전 작성했던 명령어 조회
   - `tab` : 폴더/파일 이름 자동완성
   - `ctrl + a/e` : 커서가 맨 앞으로 이동, 커서가 맨 뒤로 이동
   - `ctrl + l` : 터미널 화면을 청소 (위로 올리면 작성내역 보기 가능)
   - `shift + insert` : 붙여넣기
   - `ctrl + insert` : 복사

---

---



# 2. Visual Studio Code

## 1) vscode 열기

- `방법 1`
  1. 작업할 폴더test를 생성하고, 폴더 내에서 마우스 우클릭
  2. `Code(으)로 열기`를 클릭하여 vscode 열기

- `방법 2`
  			1. `git bash`창에서 작업할 폴더 test로 이동`cd test` 입력
    			1. `code .`을 입력하면 자동으로 열림

## 2) 터미널 열기

1. `ctrl +(백틱,esc키 밑) ` 입력
   - 혹은 `vscode 화면 상단 → Terminal → New Terminal`
2. 터미널 창의 `powershell → Git Bash` 로 바꾸기
   - powershell 옆의 `∨` 클릭
   - `select default profile` 클릭
   - `Git Bash`  클릭하여 터미널 변경하기
   - 기존 터미널을 삭제 후 단축키로 다시 열면 Git Bash로 기본 터미널이 설정됨

## 3) vscode에서 Git Bash 

### 1. git 초기설정

> 이름과 이메일을 설정하지 않을 경우 `git commit -m "커밋의 이유 작성"`을 입력 시 `"Author indentity unknown"` 오류가 발생함

 1) `CLI`에 __이름__과 __이메일__ 설정

- 누가 커밋 기록을 남겼는지 확인하기 위함

```bash
git config --global user.name "이름"
git config --global user.email "메일 주소"
```




2. 작성자가 올바르게 설정되었는지 확인

```bash
$ git config --global -l
or
$ git config --global --list
```



- 이름/이메일 설정값을 취소할 경우
  - `git config --global --unset user "이름" 또는 "이메일 주소"` 입력

```bash
git config --global --unset user "이름" 또는 "이메일"
```



### 2. git 의 3공간

- __Working Directory ▷ Staging Area ▷ Commits__
  - __Working Directory__ : 파일 생성하고 작성 후 저장만 하고, S.A에 올라가지 않은 상태
  - __Staging Area__ : 파일을 git의 관리 하에 둠
  - __Commits__ : 파일을 git hub으로 올림





# 3. 마크 다운

- `__Typora__` 설치하기

## 1) 마크다운과 마크업

- 마크업: html, 개발자 도구로 확인 가능(F12)
- 마크다운 : 경량화된 마크업 언어(태그 필요x)

## 2) 마크다운 문법

1. 제목 :`#`(1~6까지 가능)

- `#` 1개가 제일 큼

```markdown
#
##
###
####
#####
######
```

2. 목록 

- 순서가 없는 목록 : `-`, `*`, `+`

- 순서가 있는 목록 : `1.`, `2.`, `3.`을 통해 작성

  - 목록 뒤에는 꼭 띄어쓰기를 하고 입력해야 함
  - `Tab`키는 __들여쓰기__
  - `Shift + Tab`을 통해 __내어쓰기__

  

3. 강조 : 글자의 __스타일링__

- *기울임* : `*글자*`, `_글자_` 혹은 `Ctrl + i`
- __굵게__ : `**글자**`, `__글자__`
  - ***기울이고 굵게*** : `***글자***`, `___글자___`
- ~~취소선~~ : `~~글자~~`
- <u>밑줄</u> : `<u>글자</u>`, `Ctrl +u`



4. 코드(code)

- 인라인 코드 : 백틱(`)으로 묶어주기
- 코드블록 : 백틱 3개(```)로 묶어주기
- 백틱3개(```) + python처럼 코드 언어를 작성 가능

```python
print("hello world")
```



```bash
git commit -m "first line"
```



5. 링크

- `[표시하려는 텍스트](url 주소)` 입력
  - ex. [네이버](https://www.naver.com/)에 접속하기



6. 이미지

- `![표시하려는 텍스트](이미지 url 주소)` 입력

  - ex. ![Larry the cat](day01.assets/images-16457146766292.jpeg)

  - 복사 붙여넣기 할 때 ,`asset으로 복사`



7. 구분선

- `---`, `___`, `***` 입력



8. 표 만들기

- `Ctrl + t` 누르기

|      |      |      |
| ---- | ---- | ---- |
|      |      |      |
|      |      |      |



9. 인용

- 주석 혹은 인용문을 작성할 때 사용

- `>` 입력

- 중첩이 가능

- >
  >
  >>
  >>
  >>>
  >>>
  >>>

