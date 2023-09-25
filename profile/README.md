<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=header&text=Commit_Message_Style_Guide&fontSize=56" /></div>

> GDSC_DGU 1기의 원활한 협업을 위해 권장하는 **git 커밋컨벤션 설정**입니다! [**Udacity Git Commit Message Style Guide**](https://udacity.github.io/git-styleguide)를 주로 참고하여 설정했습니다.

# commit 메세지 구조 
- 기본 적인 커밋 메시지 구조는 `제목`,`본문`,`꼬릿말` 세가지 파트로 나누고, 각 파트는 **빈줄**을 두어 구분합니다. 레이아웃은 다음과 같습니다.

```
type : subject

body 

footer
```

# 1. 제목
제목은 `type: subject` 형식으로 작성합니다. `:` 뒤에 `space`가 있음을 유의합니다.
##  Commit Type
`type`은 다음 중 하나를 선택합니다. 타입은 **영어**로 쓰며 첫글자는 **대문자**로 작성합니다.

|타입 이름|설명|
|:---:|:---:|
|**Feat**|새로운 기능을 추가할 경우|
|**Fix**|버그를 고친 경우|
|**Design**|CSS 등 사용자 UI 디자인 변경|
|**!BREAKING CHANGE**|커다란 API 변경의 경우 (ex API의 arguments, return 값의 변경, DB 테이블 변경, 급하게 치명적인 버그를 고쳐야 하는 경우)|
|**!HOTFIX**|급하게 치명적인 버그를 고쳐야하는 경우|
|**Style**|코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우|
|**Refactor**|프로덕션 코드 리팩토링, 새로운 기능이나 버그 수정없이 현재 구현을 개선한 경우|
|**Comment**|필요한 주석 추가 및 변경|
|**Docs**|문서를 수정한 경우|
|**Test**|테스트 추가, 테스트 리팩토링(프로덕션 코드 변경 X)|
|**Chore**|빌드 태스트 업데이트, 패키지 매니저를 설정하는 경우(프로덕션 코드 변경 X)|
|**Rename**|파일 혹은 폴더명을 수정하거나 옮기는 작업만인 경우|
|**Remove**|파일을 삭제하는 작업만 수행한 경우|

### `type`은 다음과 같은 같은 종류로 구분됩니다.

>1. **기능:** `Feat`, `Fix`, `Design`, `!BREAKING CHANGE`
>
>	  추가적인 문맥 정보를 제공하기 위한 목적으로 괄호 안에 적을 수도 있습니다.
>	  ex) "Feat(navigation): " "Fix(database): "
  
>2. **개선:** `Style`, `Refactor`, `Comment`
>   
>    Style의 경우 오타 수정, 탭 사이즈 변경, 변수명 변경 등에 해당하고, Refactor의 경우 코드를 리팩토링 하는 경우에 적용할 수 있습니다.

>3. **그 외:** `Docs`, `Test`, `Chore`, `Rename`, `Remove`
>    
>    Docs의 경우 README.md 수정 등에 해당하고, Test는 test 폴더 내부의 변경이 일어난 경우에만 해당합니다. Chore의 경우 package.json의 변경이나 dotenv의 요소 변경 등, 모듈의 변경에 해당됩니다.

## Subject
`subject`는 코드 변경 사항에 대한 짧은 요약을 나타냅니다. 제목은 다음의 규칙을 지킵니다.

>1. 제목의 처음은 동사 원형으로 시작합니다.  
>2. 총 글자 수는 50자 이내로 작성합니다.  
>3. 마지막에 특수문자는 삽입하지 않습니다. 예) 마침표(.), 느낌표(!), 물음표(?)  
>4. 제목은 **개조식 구문**으로 작성합니다.

```
* Fixed --> Fix
* Added --> Add
* Modified --> Modify
```

만약 영어로 작성한다면 다음과 같은 규칙을 따릅니다.

>1. 첫 글자는 **대문자**로 작성합니다.  
>2. "Fix", "Add", "Change"의 명령어로 시작합니다.

한글로 제목을 작성하는 경우 다음의 규칙을 따릅니다.

>1. "고침", "추가", "변경"의 명령어로 시작합니다.

```
예시)  
Feat: "추가 get data api 함수"
```

# 2. 본문
본문은 다음의 규칙을 지킵니다.

>- 본문은 한 줄 당 72자 내로 작성합니다.
>- 본문 내용은 양에 구애받지 않고 최대한 상세히 작성합니다.
>- 본문 내용은 어떻게 변경했는지 보다 무엇을 변경했는지 또는 왜 변경했는지를 설명합니다.

# 3. 꼬릿말
꼬리말은 다음의 규칙을 지킵니다.

> 1. 꼬리말은 optional이고 이슈 트래커 ID를 작성합니다.  
> 2. 꼬리말은 "유형: #이슈번호" 형식으로 사용합니다.  
> 3. 여러 개의 이슈 번호를 적을 때는 쉼표로 구분합니다.  
> 4. 이슈 트래커 유형은 다음 중 하나를 사용합니다.  
>     - Fixes: 이슈 수정중 (아직 해결되지 않은 경우)  
>     - Resolves: 이슈를 해결했을 때 사용  
>     - Ref: 참고할 이슈가 있을 때 사용  
>     - Related to: 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)  
> **ex) Fixes: #45 Related to: #34, #23**

# 예시
- 한글 예시

```null
Feat: 회원 가입 기능 구현

SMS, 이메일 중복확인 API 개발

Resolves: #123
Ref: #456
Related to: #48, #45
```

- 영어 예시

```
feat: Summarize changes in around 50 characters or less 

More detailed explanatory text, if necessary. Wrap it to about 72 
characters or so. In some contexts, the first line is treated as the 
subject of the commit and the rest of the text as the body. The 
blank line separating the summary from the body is critical (unless 
you omit the body entirely); various tools like `log`, `shortlog` 
and `rebase` can get confused if you run the two together. 

Explain the problem that this commit is solving. Focus on why you 
are making this change as opposed to how (the code explains that). 
Are there side effects or other unintuitive consequences of this 
change? Here's the place to explain them. 

Further paragraphs come after blank lines. 

	- Bullet points are okay, too 
	
	- Typically a hyphen or asterisk is used for the bullet, 
      preceded by a single space, with blank lines in between, but conventions 
      vary here 
      
If you use an issue tracker, put references to them at the bottom, like this:

Resolves: #123 
See also: #456, #789
```
