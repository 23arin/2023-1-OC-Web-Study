# 2023-1-OC-Web-Study
2023년 1학기에 진행된 OC 기초 웹 스터디 커리큘럼 과제 제출입니다.

기초 웹 스터디 2주차 - 2023년 3월 21일 화요일

오늘은 git에 대해 알아가는 시간이었는데, 지난 주에 배운 것과 이번 주에 배운 것을 햡쳐서 내가 알아간 만큼 최대한 작성할 것이다.

1주차 시간에 배운 것을 먼저 작성해보면,

인터넷 사이트 주소는 resource가 저장된 주소를 의미하고, 이해하기 쉽게 예를 들면 허니콤보를 얻을 수 있는 주소인 교촌치킨 신촌점이라고 하셨다. 

그리고 Resource를 식별하는 통일된 방식 즉, 허니콤보를 얻을 수 있는 위치를 알아내기 위한 방식인 URI(Uniform Resource Identifier)에는 URN과 URL이 있다고 하셨다. 

먼저 우리가 많이 들어본 URL은 'Unifrom Resource Location'의 약자로 아까 예를 들었던 것으로 이어서 적어보면 URL은 교촌치킨 신촌점이 되는 것이다. URL를 보면 http:(프로토콜) + DNS 주소가 있는데 그중에서 프로토콜은 나중에 알려주신다고 하셨다.

위에서 나왔던 DNS는 Domain Name(사이트가 가지게 된 이름) System의 약자로, 그것을 가지고 있는 서버, IP 주소가 바뀌더라도 연결해주는 역할을 한다고 배웠다. 
DNS가 생겨난 이유(필요한 이유)는 'IP 주소의 문제점을 해결하기 위해'라고 말씀하시면서 IP 주소는 숫자 주소라 사람이 외우기 힘들고, IP 주소가 바뀌면 다시 그곳으로 찾아가는 것이 힘들다는 문제점이 있다고 하셨다. 

다음, URN은 Uniform Resource Name의 약자로 우리가 알기 쉽게 예를 들면 도서 출판 번호와 같은 것이라고 하셨다. 

그리고 서버의 예로는 학생들에게 자료를 주기 위한 홍익대학교가 가진 컴퓨터이고, 리소스의 예로는 그 자료라고 하셨다. 

그리고 Resource에는 HTML(자료-뼈대), CSS(UI-실과 옷), JS(Javascript,제어)가 있고 브라우저는 인터넷이 아닌 프로그램으로 예를 들어 Chrome, Internet Explorer가 있다고 배웠다. 
브라우저가 HTML 받고 CSS 옷 입혀주고 JS 제어해서 멀쩡한 홈페이지가 되는 것이라고 하셨다. 

이제 2주차 시간에 배운 것을 작성해보면, 

우선 git이란 파일의 변경 상황을 '추적'하고, 협업을 '조율'하는 것이다.
사실 git의 정의는 인터넷에 찾아보면 더 길게 나와 있지만 멘토님께서 크게 보여주시고 여러 번 말씀하신 부분이 이 부분이라 git의 정의를 이렇게 알면 될 것이라고 생각한다. 

그 다음은 git의 장점이다.

git은 분기 나누기 및 합치기가 된다는 장점이 있다.

좀 더 쉽게 말하자면 한 코드의 다른 버전을 나뭇가지처럼 만들어낼 수 있다는 것이다. 

그리고 버전 관리를 할 수 있다는 것인데 이 부분에 대해 설명하실 때 git은 변화를 추적할 수 있고 특정 시점으로 되돌리기가 가능하다는 말씀을 하셨다.

세 번째는 git의 기본 동작 방식이다.

파일의 4가지 상태가 있는데

1번 추적 X

2번 변화 X

3번 변화 O

4번 Staged

이렇게 설명해주셨다.

스터디에서 설명을 들으며 그린 그림..? 표 같은 것이 있는데 이것에 대해 간단히 찾아본 결과, 

1번에서 4번으로 향하는 것은 파일을 추가하는 것이고

2번에서 3번으로 향하는 것은 파일을 편집하는 것이며

3번에서 4번으로 향하는 것은 파일을 stage하는 것이고

4번에서 2번으로 향하는 것은 commit하는 것이다.

마지막으로 2번에서 1번으로 향하는 것은 파일을 지우는 것이다. 

마지막으로 적어볼 것은 working directory & staging area & local reposity & remote reposity에 관해 배운 것이다.

working directory에서 code를 작업하면 add를 통해 stage fixes되어 staging area에 쌓이고 이것을 Commit하면 local reposity에 가는 것이라고 배웠다. 

그리고 staging area는 가상의 무대(공간)이고, commit해서 local reposity로 가면 이름을 만들 수 있다고 하셨다. 
또한, local reposity는 내 컴퓨터에 있는 방구석 저장소이며, git이 관리한다고 배웠다.
결국 working directory와 staging area 및 local reposity는 내 컴퓨터에 있는 것이다.

이것을 내 컴퓨터에서만 보여주는 것이 아니라 다른 컴퓨터에도 보여지게 하기 위해서는(사실 정확하게 맞는지 잘 모르겠다!) local reposity를 push하여 remote reposity에 가게끔 하면 여기서 pull하여 다른 developer가 볼 수 있게(feedback할 수 있게..?) 된다고 배웠다.
중간중간에 볼 수 있는 fetch라는 것도 있지만 이것보다는 pull을 더 많이 사용한다고 하셨다.
마지막으로 local reposity는 git이 관리한다고 하였는데, remote reposity는 github에서 관리한다는 것을 배웠다.

----------------------------------------------------

기초 웹 스터디 3주차 - 2023년 3월 28일 화요일

이번 주 WIL인 WIL3에 담을 내용은 과제를 하며 수행한 내용이나 배운 점 및 느낀 점에 관련한 것들이다.

그래서 오늘의 WIL 작성 방식(틀)은 각 수행 단계를 적고 그 수행 단계마다 내가 무엇을 배웠고 무엇을 느꼈는지 적어볼 것이다.

과제 수행 1단계 : 
멘토님께서 제시해주신 repository를 fork하여 나의 repository에 저장하기
(저장할 때 repository의 이름을 webstudy-homework-본인핸들명으로 하기)

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
우선 fork가 무엇인지 알게 되었다. 
내가 찾아본 결과, fork 해당 원격 저장소(remote repository)  즉, 지금 나에게는 멘토님께서 제시해주신 repository를 나의 원격 저장소로 복사하는 것이었다. 

그리고 핸들명은 내가 사용하고 있는 이름이라는 것도 알게 되었다... 
이렇게 보니 모르는 용어가 너무 많나 싶기도 한데 차차 알아가는 과정이니 모르는 것들은 바로 검색해서 배워나가면 된다고 생각했다. 

과제 수행 2단계 : 
fork한 repository를 git clone 명령어를 이용해 본인 컴퓨터에 받는다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
어제 스터디 실습 시간에 clone을 해보긴 했지만 기억이 잘 나지 않았는데 이번 과제를 통해 다시 한 번 clone하는 방법
(clone한 remote repository를 받을 폴더에서 git bash를 열어  'git clone remote repository 주소'라고 입력하면 된다.)
에 대해 알아보는 시간을 가질 수 있어 좋았다.

과제 수행 3단계 : 
local에 본인의 깃허브 핸들로 된 브랜치를 만든다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : branch를 만들어본 적은 있지만 local에 만들어야 된다고 했을 때 어디서 해야 되는지 몰라서 조금 당황하였는데 생각보다 쉬운 곳에서 쉽게 만들 수 있어서 안심했었다.

과제 수행 4단계 : 
만든 브랜치에서 본인의 핸들명으로 된 폴더를 하나 만든다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
이것은 할 수 있는 것이어서 기분 좋게 했다. ^_^ 

과제 수행 5단계 : 
폴더 안에 README.md를 만들어 자기 소개를 적는다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
이것도 쉽게 했다! 
아는 것이 나오니 기분이 좋았다. 
약간의 걱정이 있었다면 무슨 말을 적어야 할지 조금 고민했던 것 같다.

추가> 
파일 추가 시 여기서 커밋 메시지를 컨벤션에 맞게 수정한다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
이것을 하기 위해 google에 'github commit message convention'이라고 검색하여 찾아봤는데 내가 원하는 정보가 바로 나오진 않았다. 
물론 주로 나왔던 7가지의 commit massage type은 배우게 되었지만 파일 생성이나 문서 생성을 나타내는 type은 없어 문서 수정을 의미하는 Docs로 적어서 제출했다...
나름 찾아보고 여러 군데 들어가서 내가 원하는 것이 있나 들여다봤지만 딱 정확한 정보를 아는 것이 아닌 이건가..? 싶은 것들이 몇 개 있어서 확실히 알아간다는 느낌이 들지 않는다. 

그래도 나름 찾아보며 알게 된 7가지의 commit message들을 적어보자면, 

1> feat : 새로운 기능 추가

2> fix : 버그 수정

3> docs : 문서 수정

4> style : 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우

5> chore : 빌드 업무 수정, 패키지 매니저 수정

6> test : 테스트 코드 추가 및 리팩토링(결과의 변경 없이 코드의 구조를 재조정한다는 의미)

7> refactor : 코드의 리팩토링

설명해주는 분들마다 내용이 약간씩 다르긴 하지만 그래도 이렇게 알게 되었다.

과제 수행 6단계 :
 본인의 깃허브에 저장된 remote repository 'webstudy-homework-본인핸들명'에서 새로운 브랜치의 내용을 push한다. 
단, remote repository에도 본인 핸들명으로 된 브랜치에 push해야 한다.

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
'단,' 이란 글자가 먼저 보여 조금 긴장하면서 봤는데 생각보다 수월하게 넘어가서 다행이라 여겼다... 
그리고 push는 해본 것이라 특별히 기록할 만큼 배운 점은 없는 것 같다.

과제 수행 7단계 : 
push가 되었다면 이제 이 원본 repository에 Pull Request를 보낸다. 

-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
Pull Request는 처음 해보는 것이라 무슨 의미인지 찾아봤는데, 
Pull Request는 기존 Github 저장소에 보관된 코드 베이스에서 나의 적업으로 생긴 변경사항들(수정, 추가, 삭제)을 코드베이스에 포함시켜달라고(merge 시켜달라고) 보내는 요청이었다. 
찾아보고 해보며 이렇게 또 하나 배워간다는 생각이 들었다. 

과제 수행 마무리 :
멘토님께서 승인해주시기
-> 이 단계를 수행하면서 배운 점 및 느낀 점 : 
과제를 하루 만에 다 한 것이 아니고 며칠 동안 조금씩 한 것이라 과제 제출을 3월 30일 목요일에 했다. 
그래서 승인은 3월 31일 금요일에 받은 것이다. 
승인되었다는 메일을 받고 github에 들어가서 볼 때 과제하면서 그동안은 과제를 나보다 먼저 제출하신 분들의 과제만 보였는데 이제 내가 제출한 과제도 보이니 나름 뿌듯했다.

최종적으로 느낀 점을 마무리하자면 이번 주 과제는 저번 주 과제를 수행할 때보다 내가 과제를 해나간다는 것이 눈에 더 잘 보이는 느낌이라 좋았다.

--------------------------------------------------------------------

기초 웹 스터디 4주차 - 2023년 4월 4일 화요일

이번 주 WIL인 WIL4에 담을 내용은 수업 시간에 배운 tag들과 과제를 수행하면서 배우게 된 tag들이다.

## 수업 시간에 배운 tag들

본격적으로 적기 전에 중요한 것을 적자면, 

**tag는 tag로 열면 tag로 반드시 닫아야 한다!**

_(예외도 있는데 그건 밑에 적을 것이다!)_

_(참고로 닫을 때는 알파벳 앞에 ' / ' 하나 붙여야 한다.)_

_('<>' 안에 글자들이 다 작은 따옴표 안에 있는데 실제로 쓸 때는 작은 따옴표 없이 쓴다!!)_
1. <'head'> : 이 tag 안에는 대부분 우리 눈에 보이지 않고 컴퓨터나 프로그램에게 주어지는 힌트들(속성 등)을 적힌다. 그래서 자세하고 많을수록 검색 엔진이 좋아한다. (대부분 보이지 않지만 우리 눈에 보이는 것들 중 대표적인 것은 4번에 있는 title이다.)
2. <'p'> : 이 tag 안에 있는 글은 한 문단이다. 
3. <'body'> : 이 tag 안에 있는 내용은 html 문서 안에 우리가 볼 수 있는 부분이다.
4. <'title'> : 이 tag 안에 있는 내용은 1번에서도 나왔지만 <'head'>에서 우리가 볼 수 있는 부분에 속하고, 우리 눈에 보인다는 의미는 문서 안에서 보인다는 것이 아니라 브라우저 탭에서 보인다는 의미이다. 
5. <'br'> : 이것이 바로 예외이다! 이 tag는 열고 닫을 필요가 없다. 한 문장을 쓰고 다음 문장을 쓸 때 줄을 바꾸고 싶다면 한 문장과 다음 문장 사이에 이 tag를 쓰면 된다.
6. <'h1'>, <'h2'> .... : 이 tag 안에 있는 내용은 강조가 된다. 이 tag에 써있는 h는 highlight(강조)를 의미한다. (글씨가 커지며 강조가 된다!)
7. <'strong'> : 이 tag 안에 있는 글씨들은 굵직한 글씨체로 바뀐다. 
8. <'mark'> : 이 tag 안에 있는 글씨들은 노란색 형광펜 줄이 그어진다.
9. <'meta'> : 이 tag 안에 있는 내용은 정보들의 정보이다. 즉, 해당 문서들의 정보인 메타데이터(metadata)를 정의한다. 

## 과제하면서 배운 tag들

주의해야 할 것들은 수업 시간에 배운 tag들에 다 적어놓은 것 같으니 여기에는 적지 않겠다!

1. <'html'> : 이 tag 안에 있는 글은 HTML이 작용한다.
2. <'!DOCTYPE'> : 이 tag가 적힌 문서의 종류를 정의한다.
3. <'ul'> : 이 tag 안에 있는 내용들을 순서 없는 HTML 목록(list)으로 만들어준다. (순서가 있는 것은 ol이다!)
4. <'li'> : 이 tag 안에 있는 내용은 목록의 각 항(아이템)을 의미한다. (li 안에 li를 적으면 이 목록에 대한 하위 목록이 생긴다!)
5. <'table'> : 이 tag는 테이블을 만든다. (여기서 말하는 테이블은 데이터를 포함하는 셀(cell)들의 행과 열로 구성된 2차원 테이블을 의미한다.)
6. <'tr'> : 이 tag 안에 있는 내용은 테이블에서 셀로 이루어진 하나의 행(row)이다.
7. <'td'> : 이 tag 안에 있는 내용은 테이블에서 하나의 셀(cell)을 의미한다.(여기서 말하는 셀(cell)은 우리가 흔히 알고 있는 사각형 칸을 의미한다.)
8. <'th'> : 이 tag 안에 있는 내용은 테이블에서 행, 열의 머리말을 의미한다.(다른 말로 헤더 셀(header cell)이다. 그리고 헤더 셀은 기본적으로 가운데로 정렬되고 굵은 글씨로 나타난다!)
9. <'input'> : 이 tag는 사용자로부터 입력을 받을 수 있는 입력 필드(input field)를 정의한다. type에 따라 다른 입력값을 취하며 다양한 속성이 있다는 특징이 있다. (다양한 속성 때문에 input이 강력하다!)

-------------------------------------------------------------------

기초 웹 스터디 5주차 - 2023년 4월 11일 화요일

이번 주 WIL인 WIL5에 담을 내용은 잘 정리되어 있는 래퍼런스 사이트에서 정해준 내용을 공부한 후 내가 새로 알게 된 내용 및 기억하고 싶은 내용을 정리한 것이다.

## HTML5

1. HTML5에 새로 추가된 것들
   
   1> HTML5에 새로 추가된 기능들
   
     _(이 부분은 기억하고 싶어서 적기보다는 새로 알게 되어서 적는 것이다.)_
   
    (1) 멀티미디어(Multimedia) : 플러그인의 도움없이 비디오 및 오디오 기능을 자체적으로 지원한다. 
    -> 플래시도 그러하다.

    => 용어 정리
      
       1] 플러그인 : 웹 브라우저의 표준 기능을 확장해 주는 프로그램
       예} Java Applet, Flash Player
   
    (2) 그래픽(Graphics & Effects) : SVG, 캔버스를 사용한 2차원 그래픽과 CSS3, WebGL을 사용한 3차원 그래픽을 지원한다.

    => 용어 정리

       1] SVG : SVG는 Scalable Vector Graphics의 약자로 2차원 벡터 그래픽을 표현하기 위한 XML(W3C에서 개발된 다른 특수한 목적을 갖는 마크업 언어를 만드는데 사용하도록 권장하는 다목적 마크업 언어) 기반의 파일 형식이다. 

       2] 캔버스 : 2차원 모양과 비트맵 그림의 스크립트 작성이 가능한 동적 렌더링을 허용한다.

       3] CSS3 : 차세대 웹 개발을 위한 새로운 표준이며 CSS의 최신 버전(-> 기존 CSS2.1에서 부족한 부분을 보완하고 개선한 버전)이다.

       4] WebGL : 웹 기반의 그래픽 라이브러리 
       -> 자바스크립트 프로그래밍 언어를 통해서 사용할 수 있으며 호환성이 있는 웹 브라우저에서 상호활동적인(interactive) 3D 그래픽을 사용할 수 있도록 제공된다.

    (3) 통신(Connectivity) : 지금까지의 HTML은 단방향 통신만이 가능하였으나 HTML5는 서버와의 소켓통신을 지원하므로 서버와의 양방향 통신이 가능하다.
   
    => 용어 정리
      
       1] 소켓통신 : 소켓통신에 대한 정의를 알아보기 전에 
       소켓(Socket)이란, TCP/IP 기반 네트워크 통신에서 데이터 송수신의 마지막 접점이다. 
       그리고 추가적으로 용어 정리를 해보자면,
       TCP(전송 제어 프로토콜)는 두 개의 호스트를 연결하고 데이터 스트림을 교환하게 해주는 중요한 네트워크 프로토콜이다.

       마지막으로 IP란, Internet Protocol의 약자로 인터넷이 통하는 네트워크에서 어떤 정보를 수신하고 송신하는 통신에 대한 규약을 의미한다. 

    (4) 디바이스 접근(Device acess) : 카메라, 동작센서 등의 하드웨어 기능을 직접적으로 제어할 수 있다.

    (5) 오프라인 및 저장소(Offline & Storage) : 오프라인 상태에서도 애플리케이션을 동작시킬 수 있다. 
    -> HTML5가 플랫폼으로서 사용될 수 있음을 의미한다.
   
    => 용어 정리
   
       1] 플랫폼 : 플랫폼은 승강장 플랫폼과 디지털 플랫폼으로 나눌 수 있는데 여기서 말하는 것은 디지털 플랫폼이다.
      그러하여 디지털 플랫폼이란 온라인에서 생산, 소비, 유통이 이루어지는 장소를 의미한다. 

    (6) 시맨틱 태그(Semantics) : HTML 요소의 의미를 명확히 설명하는 시맨틱 태그를 도입하여 브라우저, 검색 엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명할 수 있다. 

    => 용어 정리
       1] 시맨틱(semantic : 의미의, 의미론적인) 태그 : 의미를 부여한 태그

       2] 시맨틱 웹 : 의미론적인 웹
      -> 현재의 인터넷과 같은 분산환경에서 리소스에 대한 정보와 지원 사이의 관계-의미 정보를 기계가 처리할 수 있는 온톨로지(신뢰 기반의 데이터 교환을 위한 차세대 멀티체인 퍼블릭 플랫폼) 형태로 표현하고, 이를 자동화된 기계가 처리하도록 하는 프레임워크(어떠한 목적을 달성하기 위해 복잡하게 얽혀있는 문제를 해결하기 위한 구조)이자 기술
   
    (7) CSS3 : HTML5는 CSS3를 완벽하게 지원한다.
   
   2> HTML에 새로 추가된 시맨틱 태그들

    (1) header : 헤더

    (2) nav : 내비게이션

    (3) aside : 사이드를 위치하는 공간

    (4) section : 본문의 여러 내용(article)을 포함하는 공간

    (5) article : 본문의 주내용이 들어가는 공간

    (6) footer : 사이트의 작성자나 그에 따른 저작권 정보, 연락처 등을 명시한다.

2. 요소
   
   1> 빈 요소(Empty element or Self-closing element) : content를 가질 수 없는(content가 필요 없는) 요소
   -> attribute(속성)만을 가질 수 있다.

   예} br, input, hr(콘텐츠 내용에서 주제가 바뀔 때 사용할 수 있는 수평 가로선을 만들어주는 tag이다.), img(HTML 문서에서 이미지(image)를 정의할 때 사용하는 tag로, HTML 문서에 이미지가 직접 삽입되는 것이 아니라, HTML 문서에 이미지가 링크되는 형태이다.)

3. 속성(attribute)
   
   1> HTML Global Attribute
    : 모든 HTML 요소가 공통으로 사용할 수 있는 속성(attribute) 
    -> 예외가 존재하지만 대체로 모든 요소에서 사용 가능

    -> 자주 사용되는 Global Attribute :

    (1) id : 유일한 식별자(id)를 요소에 지정한다. 
    -> 중복 지정이 불가하다.

    (2) class : 스타일시트에 정의된 class를 요소에 지정한다.
    -> 중복 지정이 가능하다.

    (3) hidden : CSS의 hidden과는 다르게 의미상으로도 브라우저에 노출되지 않게 된다.

    (4) lang : 지정된 요소를 지정한다. 
    -> 검색엔진의 크롤링 시 웹페이지의 언어를 인식할 수 있게 한다.

    (5) style : 요소에 인라인 스타일을 지정한다.

    (6) tabindex : 사용자가 키보드로 페이지를 내비게이션 시 이동 순서를 지정한다. 

    (7) title : 요소에 관한 제목을 지정한다.

   2> 속성(attribute)의 예시

    (1) src : img 태그의 속성으로, 이미지 소스의 URL을 명시한다.

    (2) width : img 태그의 속성으로, 이미지의 너비를 픽셀(pixel) 단위로 명시한다.

    (3) height : img 태그의 속성으로, 이미지의 높이를 픽셀(pixel) 단위로 명시한다.

   3> 주석 적는 방법 : <'!-- text --'> -> text에는 주석에 적고자 하는 내용을 적으면 된다. 
   그리고 실제로 쓸 때는 작은따옴표를 제외하고 적으면 된다.
   (여기서 제외하면 저 부분이 주석이 되어 사라지기 때문에 작은따옴표를 붙인 것이다.)

4. 시맨틱 웹(Semantic Web)
   1> 검색엔진이 웹사이트 정보를 수집하는 방법
    (1) 크롤링(Crawling)

    정의 : 개인 혹은 단체에서 필요한 데이터가 있는 웹(Web)페이지의 구조를 분석하고 파악하여 모두 그대로 가져오는 것

    여기서 하는 크롤링 : 로봇(Robot)이라는 프로그램을 이용해 매일 전 세계의 웹사이트 정보를 수집하는 것 

    -> 검색엔진의 크롤러가 이를 수행한다.

    (2) 인덱싱(Indexing)

    여기서 하는 인덱싱 : 검색 사이트 이용자가 검색할 만한 키워드를 미리 예상하여 검색 키워드에 대응하는 인덱스(색인)을 만들어 두는 것이다.

    -> 검색엔진의 인덱서가 이를 수행한다. 

    => 인덱서를 생성할 때 사용되는 정보 : 검색 로봇이 수집한 정보 -> 웹사이트의 HTML 코드 <= 검색 엔진은 HTML 코드만으로 의미를 인지해야 한다.(시맨틱 요소 해석)
    
    _HTML으로 작성된 문서 = 메타데이터(컴퓨터가 해석) + 자연어(사람이 사용)_

   2> 시맨틱(Semantic) ~
    
    (1) 시맨틱 요소

    -> 시맨틱 요소로 구성되어 있는 웹페이지 : 검색엔진에 보다 의미론적으로 문서 정보 전달 가능함.

    <= 검색엔진 또한 시맨틱 요소를 이용하여 보다 효과적인 크롤링과 인덱싱 가능

    (2) 시맨틱 태그 

    -> 역할 : 브라우저, 검색엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명한다.

    (3) 시맨틱 웹

    정의 : 웹에 존재하는 수많은 웹페이지들에 메타데이터(Metadata)를 부여하여, 기존의 잡다한 데이터 집합이었던 웹페이지를 '의미'와 '관련성'을 가지는 거대한 데이터베이스로 구축하고자 하는 발상

5. HTML 요소
   1> non-semantic 요소  
   
    -> content에 대하여 어떤 설명도 하지 않는다. 
    
    예} div, span

   2> semantic 요소 

    -> content의 의미를 명확히 설명한다.

    예} form, table, img 

6. 웹페이지를 구성하는 기본 tag
   
   1> 문서 형식 정의 tag
   
    -> 문서 형식 정의는 DTD로, DTD는 Document Type Definition의 약자이다.

    (1) 역할 : 웹 페이지의 형식을 브라우저에게 전달한다. 

    (2) 위치 : 문서의 최상위

    (3) 특징 : 대소문자 구별 X

   2> html tag

    (1) 특징 
    
      1] 웹페이지 단 하나만 존재한다.

      2] 모든 HTML 요소의 부모 요소이다.

      -> 모든 요소 = HTML 요소의 자식 요소 
      
      => HTML 요소 내부에 기술해야 한다.
      
      => 예외} <'!DOCTYPE'> (실제 사용 시에는 작은 따옴표 제거)

   3> head tag
    
    (1) head 요소 : 메타데이터를 포함하기 위한 요소
      
      1] 웹페이지에 단 하나만 존재한다.

      2] 메타데이터 -> HTML 문서의 title, style, link, script에 대한 데이터로 화면에 표시되지 않는다.

      3] 메타데이터 이외의 화면에 표시되는 일체의 요소를 포함시킬 수 없다.

    (2) title tag 
    
    -> title 요소 : 문서의 제목을 정의한다.
    
    => 정의된 제목은 브라우저의 탭에 표시된다.

    (3) style tag
    
    -> HTML 문서를 위한 style 정보를 정의한다. 

    (4) link tag

    -> link 요소 : 외부 리소스와의 연계 정보를 정의한다. 

    => 주로 HTML과 외부 CSS 파일 연계에 사용된다.

    (5) script tag

    -> script 요소 : client-side JavaScript를 정의한다.

    => scr attribute를 사용하면? 외부 JavaScript 파일 로드 가능

    (6) meta tag

    -> meta 요소 : description, keywords, author, 기타 메타데이터 정의에 사용된다.

    => 메타데이터 : 브라우저, 검색엔진(keywords) 등에 사용된다.

    예} charset 속성(attribute) : 브라우저가 사용할 문자셋을 정의한다.

    (7) body tag
    
    -> HTML 문서의 내용을 나타내며 웹페이지에 단 하나만 존재한다.

    => 메타데이터를 제외한 웹페이지를 구성하는 대부분의 요소가 body 요소 내에 기술된다. 

7. 텍스트 관련 tag
   
   1> 제목(Heading) tag
    
    (1) 역할 : 제목을 나타낸다.

    (2) tag의 종류 : h1 ~ h6

    -> h1이 가장 중요한 제목을 의미하며 글자의 크기도 가장 크다.

    => 시맨틱 웹의 의미를 살려서 제목 이외에는 사용하지 않는 것이 좋다. 
    (검색엔진 : 제목 태그를 중요한 의미로 받아들일 가능성이 큼)

   2> 글자 형태(Text Formatting) tag

    (1) b
    
    -> bold체를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, bold tag 안에 들어있는 글씨들을 굵게 해준다.

    -> 의미론적(semantic) 중요성의 의미는 없다.

    (2) strong

    -> bold체를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, strong tag 안에 들어있는 글씨들을 굵게 해준다.

    -> 의미론적(semantic) 중요성의 의미를 갖는다.

    => 웹표준을 준수하고자 한다면 strong을 사용하는 것이 바람직하다. 

    (3) i

    -> Italic체를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, i tag 안에 들어있는 글씨들을 기울어지게 해준다. 

    -> 의미론적(semantic) 중요성의 의미는 없다.

    (4) em

    -> emphasized(강조, 중요한) text를 지정한다.

    -> Italic체로 표현된다.

    ==> 내가 이해하기 쉽게 다시 적자면, em tag 안에 들어있는 글씨들을 기울어지게 해준다.

    -> 의미론적(semantic) 중요성의 의미를 갖는다.

    (5) small

    -> samll text를 지정한다. 

    ==> 내가 이해하기 쉽게 다시 적자면, small tag 안에 들어있는 글씨들을 작게 해준다.

    (6) mark

    -> highlighted text를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, mark tag 안에 들어있는 글씨들에 노란색 형광펜이 칠해진다.

    (7) del

    -> deleted(removed) text를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, del tag 안에 들어있는 글씨들 가운데에 선이 그어지도록 해준다.

    (8) ins

    -> inserted(added) text를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, ins tag 안에 들어있는 글씨들에 밑줄이 그어지도록 해준다.

    (9) sub / sup

    -> sub tag : subscripted(아래에 쓰인) text를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, sub tag 안에 들어있는 글씨들을 약간 아래로 내려가게 해준다.

    -> sup tag : superscripted(위에 쓰인) text를 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, sup tag 안에 들어있는 글씨들을 약간 위로 내려가게 해준다.

   3> 본문 tag

    (1) p
    
    -> 단락(paragraphs)을 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, p tag 안에 들어있는 글은 한 문단을 의미한다. 

    (2) br

    -> 개행(line break)을 지정한다. => 강제로 실행되는 것이다.

    ==> 내가 이해하기 쉽게 다시 적자면, br tag를 쓰면 마치 우리가 한글 문서(혹은 word 문서)를 쓸 때 키보드에 enter를 누른 것처럼 글이 한 줄 넘어간다. 

    -> 특징 : 빈 요소(empty element)로 종료 tag가 없다.

    => HTML 문서에 공백을 삽입하는 방법
       
       1] 1개의 공백 : 1개 이상의 연속된 공백(space) 및 1개 이상의 연속된 줄바꿈(enter)

       2] 2개 이상의 공백 : '&nbsp;'를 쓰면 된다.

       예} 안녕&nbsp; &nbsp; 안녕 => 안녕  안녕

    (3) pre

    -> 형식화된(preformatted) text를 지정한다.

    -> pre tag 내의 content는 작성된 그대로 브라우저에 표시된다.

    ==> 내가 이해하기 쉽게 다시 적자면, pre tag 안에 들어있는 글은 작성한 그대로 우리에게 보여진다.

    (4) hr

    -> 수평줄을 삽입한다.

    ==> 내가 이해하기 쉽게 다시 적자면, hr tag를 쓰면 마치 하나의 주제에 대한 글이 끝난 것처럼 회색 가로줄이 그어진다.

    -> 특징 : 빈 요소(empty element)로 종료 tag가 없다.

    (5) q

    -> 짧은 인용문(quotation)을 지정한다.

    ==> 내가 이해하기 쉽게 다시 적자면, q tag 안에 들어있는 글이 인용된 것처럼 큰따옴표가 삽입된다.

    -> 특징 : 브라우저 - 인용부호(큰따옴표/quotation mark)로 q 요소를 감싼다.

    (6) blockquote

    -> 긴 인용문 블록을 지정한다.

    -> 특징
       
       1] 브라우저 - blockquote 요소를 들여쓰기한다.
       
       2] CSS를 이용하여 다양한 style을 적용할 수 있다.
    
    ==> 내가 이해하기 쉽게 다시 적자면, blockquote tag 안에 들어있는 글은 그전 글에서 줄바꿈 한 번, 공백 4번 정도 되게 한다.

--------------------------------------------------------------------

## CSS

0. 본격적으로 적기에 앞서...
    
   1> HTML5
     
    (1) HTML : 정보와 구조화

    (2) CSS : styling의 정의

1. CSS 기본 문법
   
   1> 선택자(selector)
   
    (1) CSS : HTML 요소의 style을 정의하는데 사용된다.
   
    -> 이를 위해 선행되어야 하는 것 : style을 적용하고자 하는 HTML 요소를 선택할 수 있어야 한다.

    (2) 선택자(selector) : 스타일을 적용하고자 하는 HTML 요소를 선택하기 위해 CSS에서 제공하는 수단

    (3) 스타일시트(Style Sheet) : Rule Set의 집합

      1] Rule Set(=Rule)...?

       -> 역할 : 선택자에 의해 선택된 특정 HTML 요소를 어떻게 렌더링(Rendering)할 것인지 브라우저에 지시한다.

       예} h1 {color: red;font-size: 12px;}

       여기서 
       
       {1} h1 : 선택자(Selector)
       
       {2} 중괄호({}) 안에 있는 글 : 선언 블록(Declaration block) 
       
       {3} color: red;' 및 'font-size: 12px; : 선언(Declaration)

       {4} color 및 font-size : 속성(Property)

       {5} red 및 12px : 값(Property value)

   2> 속성(Property)
   
    -> 다양한 style을 정의하려면?
   
       1] 선택자로 HTML 요소를 선택하고 중괄호({}) 내에 속성과 값을 지정한다.

       2] 여러 개의 속성을 연속으로 사용하려면..? -> 세미콜론(;)으로 구분하여 쓰면 된다. (참고 : CSS 1-3의 예시 in this document)

       => 속성은 표준 스펙으로 지정된 것을 사용해야하며 사용자가 임의로 정할 수 없다.

   3> 값(속성값, Value)
   
    -> 속성의 값은 해당 속성에 사용할 수 있는 값을 "키워드"나 "크기 단위" 또는 "색상 표현 단위" 등의 특정 단위로 지정하여야 한다.

    4> HTML과 CSS의 연동
   
    (0) 연동하는 방법에 들어가기 앞서...

       1] HTML은 CSS를 포함할 수 있다. (적고 싶어서 적어 보았다.)

    (1) Link style

    -> HTML에서 외부에 있는 CSS 파일을 로드하는 방식
    (가장 일반적으로 사용되는 방식)

    ==> 내가 이해하기 쉽게 다시 적자면, 링크를 통해 HTML과 CSS를 연동하는 방식이다.

    예} <' link rel="stylesheet" href="css/style/css" '>
    (실제 사용 시에는 가장 바깥쪽에 있는 작은 따옴표 제거)

    (2) Embedding style 

    -> HTML 내부에 CSS를 포함시키는 방식

    => 이 style보다 Link style을 사용하는 것이 좋다.
    (HTML과 CSS의 역할이 서로 다르므로 다른 파일로 구분되어 작성하고 관리되는 것이 바람직하다.)

    예} <'style'> ; h1 { color: red; } ; p { background: aqua; } <'/style'>

    (3) Inline style

    -> HTML 요소의 style 속성에 CSS를 기술하는 방식

    -> 사용하는 경우 : JavaScript가 동적으로 생성할 때

    => 이 style 또한 이 style보다 Link style을 사용하는 것이 좋다.

    예} <' h1 style="color:red" '>Hello World<' /h '>
    (실제 사용 시 작은따옴표 및 공백 제거)
   5> Reset CSS 사용하기

    -> 용도 : 기본적인 HTML 요소의 CSS를 초기화한다.

    -> 역할 : 브라우저 별로 제각각인 디폴트 스타일을 하나의 스타일로 통일시켜 준다.

    예} Eric Meyer's reset, normalize.css (-> 자주 사용되는 Reset CSS이다.)
2. 선택자(selector)
   
   0> 본격적으로 들어가기 앞서...

    -> 목적 : style을 적용하고자 하는 HTML 요소를 선택자로 특정하고 선택된 요소에 style을 정의하는 것이다.

    => 여러 개의 선택자를 연속하여 지정할 수 있으며 쉼표(,)로 구분한다.
   
   1> 전체 선택자(Universal Selector)

    (1) Pattern : *

    (2) Description : HTML 문서 내의 모든 요소를 선택한다. 
    
    -> head 요소도 포함된다.

   2> tag 선택자(Type Selector)

    (1) Pattern : tag명

    (2) Description : 지정된 tag명을 가지는 요소를 선택한다.

   3> ID 선택자(ID Selector)

    (1) Pattern : #id 속성 값

    (2) Description : id 속성 값을 지정하여 일치하는 요소를 선택한다.

    -> id 속성 값은 중복될 수 없는 유일한 값이다.

   4> 클래스 선택자(Class Selector)

    (1) Pattern : .class 속성 값

    (2) Description : class 속성 값을 지정하여 일치하는 요소를 선택한다.

    -> class 속성 값은 중복될 수 있다. 
    
    => class 속성 값은 공북으로 구분하여 여러 개 지정할 수 있다. (재사용의 측면에서 유용)

   5> 속성 선택자(Attribute Selector)

    (1) Pattern - Description 1

    -> Pattern : 선택자[속성]

    -> Description : 지정된 속성을 갖는 모든 요소를 선택한다.

    (2) Pattern - Description 2

    -> Pattern : 선택자[속성="값"]

    -> Description : 지정된 속성을 가지며 지정된 값과 속성의 값이 일치하는 모든 요소를 선택한다.

    (3) Pattern - Description 3

    -> Pattern : 선택자[속성~="값"]

    -> Description : 지정된 속성의 값이 지정된 값을(공백으로 분리된) 단어로 포함하는 요소를 선택한다.

    (4) Pattern - Description 4

    -> Pattern : 선택자[속성|="값"]

    -> Description :  지정된 속성의 값과 일치하거나 지정 속성 값 뒤 연이은 하이픈("값-")으로 시작하는 요소를 선택한다.

    (5) Pattern - Description 5

    -> Pattern : 선택자[속성^="값"]

    -> Description : 지정된 속성 값으로 시작하는 요소를 선택한다.

    (6) Pattern - Description 6

    -> Pattern : 선택자[속성$="값"]

    -> Description : 지정된 속성 값으로 끝나는 요소를 선택한다.

    (7) Pattern - Description 7

    -> Pattern : 선택자[속성*="값"]

    -> Description : 지정된 속성 값을 포함하는 요소를 선택한다.

   6> 복합 선택자(Combinator)

    (1) 후손 선택자(Descendant Combinator)

       1] 부모 요소 : 자신의 1 level 상위에 속하는 요소

       2] 자손 요소(자식 요소) : 자신의 1 level 하위에 속하는 요소

       3] 후손 요소(하위 요소) : 자신보다 n level 하위에 속하는 요소

    -> 선택자 A의 모든 후손(하위) 요소 중 선택자 B와 일치하는 요소를 선택한다.

    (2) 자식 선택자(Child Combinator)

    -> 자손 선택자는 선택자 A의 모든 자식 요소 중 선택자 B와 일치하는 요소를 선택한다. 

    (3) 형제(동위) 선택자(Sibling Combinator)
    
    -> 형제 관계(동위 관계)에서 뒤에 위치하는 요소를 선택할 때 사용한다.

      1] 인접 형제 선택자(Adjacent Sibling Combinator)
      
      -> 선택자 A의 형제 요소 중 선택자 B 바로 뒤에 위치하는 선택자 B 요소를 선택한다. 

      -> A와 B 사이에 다른 요소가 존재하면 선택되지 않는다.

      2] 일반 형제 선택자(General Sibling Combinator)

      -> 선택자 A의 형제 요소 중 선택자 B 요소를 모두 선택한다.

   7> 가상 클래스 선택자(Pseudo-Class Selector)
    
    (0) 들어가기 앞서...
       
       1] 가상 클래스 : 요소의 특정 상태에 따라 스타일을 정의할 때 사용한다.

       특정 상태의 예} 마우스가 올라와 있을 때, 링크를 방문했을 때와 아직 방문하지 않았을 때

       -> 마침표(.) 대신 콜론(:)을 사용한다.

    (1) 링크 선택자 및 동적 선택자(Link pseudo-classes & User action pseudo-classes)

       1] Pseudo-class - Description 1
       
       -> Pseudo-class : :link

       -> Description : 선택자가 방문하지 않은 링크일 때

       2] Pseudo-class - Description 2

       -> Pseudo-class : :visited

       -> Description : 선택자가 방문한 링크일 때

       3] Pseudo-class - Description 3

       -> Pseudo-class : :hover

       -> Description : 선택자가 마우스가 올라와 있을 때

       4] Pseudo-class - Description 4

       -> Pseudo-class : :active

       -> Description :  선택자가 클릭된 상태일 때

       5] Pseudo-class - Description 5

       -> Pseudo-class : :focus

       -> Description : 선택자에 포커스가 들어와 있을 때

    (2) UI 요소 상태 선택자(UI element states pseudo-classes)

       1] Pseudo-class - Description 1

       -> Pseudo-class : :checked

       -> Description : 선택자가 체크 상태일 때

       2] Pseudo-class - Description 2

       -> Pseudo-class : :enabled

       -> Description : 선택자가 사용 가능한 상태일 때

       3] Pseudo-class - Description 3

       -> Pseudo-class : :disabled

       -> Description : 선택자가 사용 불가능한 상태일 때

    (3) 구조 가상 클래스 선택자(Structural pseudo-classes)

       1] Pseudo-class - Description 1

       -> Pseudo-class : :first-child

       -> Description : 선택자가 해당하는 모든 요소 중 첫번째 자식인 요소를 선택한다.

       2] Pseudo-class - Description 2
       
       -> Pseudo-class : :last-child

       -> Description : 선택자에 해당하는 모든 요소 중 마지막 자식인 요소를 선택한다.

       3] Pseudo-class - Description 3

       -> Pseudo-class : :nth-child(n)

       -> Description : 선택자에 해당하는 모든 요소 중 앞에서 n번째 자식인 요소를 선택한다.

       4] Pseudo-class - Description 4

       -> Pseudo-class : :nth-last-child(n)

       -> Description : 선택자에 해당하는 모든 요소 중 뒤에서 n번째 자식인 요소를 선택한다.

       => 3], 4]번만 해당 - n : 0부터 시작하는 정수 & 0과 음수는 생략되기 때문에 2n+1과 2n-1, 3n-2와 3n+1은 결과적으로 같은 수열을 생성한다.

       5] Pseudo-class - Description 5

       -> Pseudo-class : :first-of-type

       -> Description : 선택자가 해당하는 요소의 부모 요소의 자식 요소 중 첫번째 등장하는 요소를 선택한다.

       6] Pseudo-class - Description 6

       -> Pseudo-class : :last-of-type

       -> Description : 선택자에 해당하는 요소의 부모 요소의 자식 요소 중 마지막에 등장하는 요소를 선택한다.

       7] Pseudo-class - Description 7

       -> Pseudo-class : :nth-of-type(n)

       -> Description  선택자에 해당하는 요소의 부모 요소의 자식 요소 중 앞에서 n번째에 등장하는 요소를 선택한다.

       8] Pseudo-class - Description 8

       -> Pseudo-class : :nth-last-of-type(n)

       -> Description : 선택자에 해당하는 요소의 부모 요소의 자식 요소 중 뒤에서 n번째에 등장하는 요소를 선택한다.

    (4) 부정 선택자(Negation pseudo-class)

       1] Pseudo-class - Description 1

       -> Pseudo-class : :not(선택자)

       -> Description : 선태자에 해당하지 않는 모든 요소를 선택한다.

    (5) 정합성 체크 선택자(Validity pseudo-class)

       1] Pseudo-class - Description 1

       -> Pseudo-class : :valid(선택자)

       -> Description : 정합성 검증이 성공한 input요소 또는 form 요소를 선택한다.

       2] Pseudo-class - Description 2

       -> Pseudo-class : :invalid(선택자)

       -> Description : 정합성 검증이 실패한 input 요소 또는 form 요소를 선택한다. 

   8> 가상 요소 선택자(Pseudo-Element Selector)

    (1) 가상 요소...?
    
       1] 사용 목적 : 요소의 특정 부분에 스타일을 적용하기 위하여

       특정 부분의 예} 요소 콘텐츠의 첫글자 또는 첫줄

       2] 사용 방법 : 두 개의 콜론(:) & CSS 표준에 의해 미리 정의된 이름 쓰기(임의의 이름 사용할 수 X)

    (2) Pseudo-element - Description

       1] Pseudo-element - Description 1

       -> Pseudo-element : ::first-letter

       -> Description : 콘텐츠이 첫글자를 선택한다.

       2] Pseudo-element - Description 2

       -> Pseudo-element : ::first-line

       -> Description : 콘텐츠의 첫줄을 선택한다. 
       => 블록 요소에만 적용할 수 있다.

       3] Pseudo-element - Description 3

       -> Pseudo-element : ::after

       -> Description : 콘텐츠의 뒤에 위치하는 공간을 선택한다.
       => 일반적으로 content 속성과 함께 사용된다.

       4] Pseudo-element - Description 4

       -> Pseudo-element : ::before

       -> Description : 콘텐츠의 앞에 위치하는 공간을 선택한다.
       => 일반적으로 content 속성과 함께 사용된다.

       5] Pseudo-element - Description 5

       -> Pseudo-element : ::selection

       -> Description : 드래그한 콘텐츠를 선택한다.
       => iOS Safari 등 일부 브라우저에서 동작 않는다.
3. CSS 속성 값의 단위
   
   -> CSS 속성 : 키워드, 크기 단위, 색상 표현 단위 등의 특정 단위를 갖는 값을 지정한다.
   
   1> 키워드
    
    -> 각 속성에 따라 사용할 수 있는 키워드가 존재한다.

    예} display 속성의 값으로 사용할 수 있는 키워드 : block, inline, inline-block, none

   2> 크기 단위

    (1) px (절대값)

    -> 요소의 크기나 이미지의 크기 지정에 주로 사용된다.

       1] 의미 : px는 픽셀(화소) 단위로, 1 px은 화소 1개 크기를 의미한다.

       2] 픽셀은 디바이스 해상도(resolution)에 따라 상대적인 크기를 갖는다.
       -> 따라서 대부분의 브라우저는 1 px을 1/96 인치의 절대단위로 인식한다.

    (2) % (상대값)

    -> 의미 : 백분율 단위의 상대 단위

    -> 요소에 지정된 사이즈(상속된 사이즈나 디폴트 사이즈)에 상대적인 사이즈를 설정한다.

    (3) em (상대값)

    -> 요소에 지정된 사이즈(상속된 사이즈나 디폴트 사이즈)에 상대적인 사이즈를 설정한다. 

       1] 의미 : 배수 단위 -> 상대 단위

       2] 주의 사항 : 중첩된 자식 요소에 em을 지정
       ->  모든 자식 요소의 사이즈에 영향을 미치기 때문이다. 

       예} 1em : 요소에 지정된 사이즈와 같다. / 2em : 요소에 지정된 사이즈의 2배

    (4) rem

    -> rem의 기준 : 최상위 요소(HTML)의 사이즈 
    <- em의 기준 : 상속의 영향으로 바뀐다.

    (5) Viewport 단위 (vh, vw, vmin, vmax)

    -> 의미 : viewport를 기준으로 한 상대적 사이즈 -> 상대적인 단위

    -> 단위 - Decription

       1] 단위 - Description 1

       -> 단위 : vw

       -> Description : viewport 너비의 1/100

       2] 단위 - Description 2

       -> 단위 : vh

       -> Description : viewport 높이의 1/100

       3] 단위 - Description 3

       -> 단위 : vmin

       -> Description : viewport 너비 또는 높이 중 작은 쪽의 1/100

       4] 단위 - Description 4

       -> 단위 : vmax

       -> Description : viewport 너비 또는 높이 중 큰 쪽의 1/100

    -> 주의 사항 : IE 8 이하 : 지원 X & IE 9~11, Edge : 지원이 완전하지 X

   3> 색상 표현 단위

    (1) 장점과 단점

       1] 장점 : 사용이 간편하다.

       2] 단점 : 표현할 수 있는 색상의 수가 제한된다.

    (2) 단위 - 사용 예

       1] 단위 - 사용 예 1

       -> 단위 : HEX 코드 단위(Hexadecimal Colors)

       -> 사용 예 : #000000

       2] 단위 - 사용 예 2

       -> 단위 : RGB(Red, Green, Blue)

       -> 사용 예 : rgb(255, 255, 0)

       3] 단위 - 사용 예 3

       -> 단위 : RGBA(Red, Green, Blue, Alpha(=투명도))

       -> 사용 예 : rgba(255, 255, 0, 1)

       4] 단위 - 사용 예 4

       -> 단위 : HSL(Hug(=색상), Saturation(=채도), Lightness(=명도))

       -> 사용 예 : hsl(0, 100%, 25%)

       5] 단위 - 사용 예 5

       -> 단위 : HSLA(Hug, Saturation, Lightness, Alpha)

       -> 사용 예 : hsla(60, 100%, 50%, 1)

4. 박스 모델
   
   0> Box 형태...?

    (1) 정의 : 사각형

    (2) 구성 : 콘텐트(Content), 패딩(Padding), 테두리(Border), 마진(Margin)

    (3) 브라우저 : 박스 모델의 크기(dimension)와 속성(색, 배경, 모양 등), 위치를 근거로 하여 렌더링을 실행

    (4) 웹디자인 : 콘텐츠를 담을 박스 모델을 정의하고 CSS 속성을 통해 스타일(배경, 폰트와 텍스트 등)과 위치 및 정렬을 지정하는 것

    (5) 명칭 - 설명
    
       1] 명칭 - 설명 1

       -> 명칭 : Content

       -> 설명 : 요소의 텍스트나 이미지 등의 실제 내용이 위치하는 영역
       <- width,height 속성을 갖는다.

       2] 명칭 - 설명 2

       -> 명칭 : Padding

       -> 설명 : 테두리(Border) 안쪽에 위치하는 요소의 내부 여백 영역

       <- 요소에 적용된 배경의 컬러, 이미지는 패딩 영역까지 적용된다.

       -> 추가 설명 - padding 속성 값 : 패딩 영역의 두께 & 기본색 : 투명(transparent)

       3] 명칭 - 설명 3

       -> 명칭 : Border

       -> 설명 : 테두리 영역

       -> 추가 설명 - border 속성 값 : 테두리의 두께

       4] 명칭 - 설명 4

       -> 명칭 : Margin

       -> 설명 : 테두리(Border) 바깥에 위치하는 요소의 외부 여백 영역

       -> 추가 설명 - margin 속성 값 : 마진 영역의 두께 & 기본적으로 투명하며 배경색을 지정할 수 X
      
   1> width / height 속성

       1] 사용 목적 : 요소의 너비와 높이를 지정하기 위하여

       2] 사용 대상 : 지정되는 요소의 너비와 높이 - 콘텐츠 영역을 대상으로 한다.
       -> box-sizing 속성에 기본값인 content-box가 적용되었기 때문이다.

       box-sizing 속성에 border-box를 적용하면?
       => 콘텐츠 영역, padding, border가 포함된 영역을 width / height 속성의 대상으로 지정할 수 있다. 

       3] 주의 사항 : width와 height로 지정한 콘텐츠 영역보다 실제 콘텐츠가 크면 콘텐츠 영역을 넘치게 된다.
       => 넘친 콘텐츠를 감추는 방법 : 'overflow: hidden;'을 지정

       4] 박스 전체 크기 계산

       -> 전체 너비 = width + left padding + right padding + left border + right border + left margin + right margin

       -> 전체 높이 = height +  top padding + bottom padding + top border + bottom border + top margin + bottom margin

       5] width와 height 속성의 초기값 : auto 
       -> 브라우저가 상황에 따라 적당한 width와 height 값을 계산할 것을 의미한다.

       6] width와 height의 단위 : 크기 단위 예} px, %

   2> margin / padding 속성

       1] 사용 목적 : content의 4개 방향(top, right, bottom, left)에 대하여 지정하기 위하여

       2] n개의 값을 지정할 때

       -> 4개의 값을 지정할 때
       
       margin: 25px 50px 75px 100px;

       margin-top: 25px;

       margin-right: 50px;

       margin-bottom: 75px;

       margin-left: 100px;

       -> 3개의 값을 지정할 때

       margin: 25px 50px 75px;

       margin-top: 25px;

       margin-right: 50px; margin-left: 50px;

       margin-bottom: 75px;

       -> 2개의 값을 지정할 때

       margin: 25px 50px;

       margin-top: 25px; margin-bottom: 25px;

       margin-right: 50px; margin-left: 50px;

       -> 1개의 값을 지정할 때

       margin: 25px;

       margin-top: 25px; margin-right: 25px; margin-bottom: 25px; margin-left: 25px;

       3] margin 속성에 auto 키워드 설정 -> 해당 요소를 브라우저 중앙에 위치시킬 수 있다.

       4] max-width 속성 사용 : 브라우저 너비가 요소의 너비보다 좁아질 때 자동으로 요소의 너비가 줄어든다. 

   3> border 속성

    (1) border-style

    -> 테두리 선의 스타일을 지정한다.

    => 속성 값의 개수에 따라 4개 방향(top, right, left, bottom)에 대하여 지정이 가능하다.

    (2) border-width

    -> 테두리의 두께를 지정한다.

    => 속성 값의 개수에 따라 4개 방향(top, right, left, bottom)에 대하여 지정이 가능하다.

    => border-width 속성은 border-style과 함께 사용하지 않으면 적용되지 않는다.

    (3) border-color

    -> 테두리의 색상을 지정한다.

    => 속성 값의 개수에 따라 4개 방향(top, right, left, bottom)에 대하여 지정이 가능하다.

    => border-color 속성은 border-style과 함께 사용하지 않으면 적용되지 않는다. 

    (4) border-radius

    -> 테두리 모서리를 둥글게 표현하도록 지정한다.

    -> 속성 값의 단위 : 길이를 나타내는 단위 (예} px, em 등) & %

    => 각각의 모서리에 border-radius 속성을 개별적으로 지정할 수 있고 4개의 모서리를 short-hand로 한 번에 지정할 수도 있다. 

    -> 원 혹은 타원의 모양으로 정의 가능 : 하나 혹은 두 개의 반지름을 설정하여 각각의 모서리 굴곡을 설정할 수 있다.
       
       1] 두 개의 반지름을 지정하여 타원형 둥근 모서리 설정

       -> .border-rounded {border-top-left-radius: 50px 23px;}

       2] 각각의 모서리에 타원형 둥근 모서리 축약 설정

       -> .border-rounded {border-radius: 50px 50px 0 0 / 25px 25px 0 0;}

    (5) border

    -> 정의 : border-width, border-style, border-color를 한 번에 설정하기 위한 shorthand 속성

   4> box-sizing 속성

    (1) 기능 : width, height 속성의 대상 영역을 변경할 수 있다.

    (2) 키워드 - 설명

       1] 키워드 - 설명 1

       -> 키워드 : content-box

       -> 설명 : width, height 속성 값은 content 영역을 의미한다. (기본값)

       2] 키워드 - 설명 2

       -> 키워드 : border-box

       -> 설명 : width, height 속성 값은 content 영역, padding, border가 포함된 값을 의미한다.

    (3) 상속 : box-sizing 속성은 상속되지 않는다.

    -> box-sizing 속성을 사용하도록 초기화하려면 아래와 같이 정의한다.

    html {box-sizing: border-box;}

    *, *:before, *:after {box-sizing: inherit;}

5. 폰트와 텍스트
   
   1> font-size 속성

    -> 텍스트의 크기를 정의한다.

   2> font-family 속성

       1] 폰트를 지정한다.
       
       -> 주의 사항 : 컴퓨터에 해당 폰트가 설치되어 있지 않으면 적용되지 않는다. 

       2] 폰트 - 여러 개를 동시에 지정 가능

       -> 첫 번째 지정한 폰트가 클라이언트 컴퓨터에 설치되어 있지 않은 경우, 다음에 지정된 폰트를 적용한다.

       -> 마지막에 지정하는 폰트 : 대부분의 OS에 기본적으로 설치되어 있는 generic-family 폰트(Serif, Sans-serif, Nono space)를 지정하는 것이 일반적이다. 

       3] 폰트명 : 따옴표로 감싸주며 폰트명이 한 단어인 경우 
       -> 따옴표로 감싸주지 않아도 된다.

   3> font-style / font-weight 속성

    -> font-style 속성 : Italic체 지정

    -> font-weight 속성 : 폰트 굵기 지정

   4> font Shorthand

    -> Shorthand Syntax

   5> line-height 속성

    -> 텍스트의 높이를 지정한다.

    -> 텍스트 수직 정렬에도 응용되어 사용된다.

    예} 수직 중앙 정렬 : a 요소의 line-height 값과 a 요소를 감싸는 div 요소의 height 값을 일치시킨다.

   6> letter-spacing 속성

    -> 글자 상의 간격을 지정한다.

   7> text-align 속성

    -> 텍스트의 수평 정렬을 정의한다.

    예} 중앙 정렬 - inline 요소 : width 속성 X -> 중앙 개념 존재 X
    
    => 예를 들어 a 요소가 inline 요소라면, a 요소에 display: block;을 지정한다면 중앙 정렬이 가능할 것이다.

   8> text-decoration 속성

    -> 링크 underline을 제거 & 텍스트에 underline, overline, line-through 추가 가능

   9> white-space 속성

       1] white space : 공백(space), 들여쓰기(tab), 줄바꿈(line break)

       2] HTML

       -> 공백(space) & 들여쓰기(tab) : 기본적으로 연속된 것들은 1번만 실행

       -> 줄바꿈(line break) : 무시

       3] 텍스트 : 부모의 가로 영역을 벗어나지 않고 자동 줄바꿈(wrap)

       4] 속성값 - line break - space/tab - wrapping(자동 줄바꿈)

       -> 속성값 - line break - space/tab - wraaping(자동 줄바꿈) 1

         속성값 : normal

         line break : 무시

         space/tab : 1번만 반영

         wrapping(자동 줄바꿈) : O

       -> 속성값 - line break - space/tab - wrapping(자동 줄바꿈) 2

        속성값 : nowrap

        line break : 무시

        space/tab : 1번만 반영

        wrapping(자동 줄바꿈) : X

       -> 속성값 - line break - space/tab - wrapping(자동 줄바꿈) 3

        속성값 : pre

        line break : 반영

        space/tab : 그대로 반영 

        wrapping(자동 줄바꿈) : X

       -> 속성값 - line break - space/tab - wrapping(자동 줄바꿈) 4

        속성값 : pre-wrap

        line break : 반영

        space/tab : 그대로 반영

        wrapping(자동 줄바꿈) : X

       -> 속성값 - line break - space/tab - wrapping(자동 줄바꿈) 5

        속성값 : pre-line 

        line break : 반영

        space/tab : 1번만 반영

        wrapping(자동 줄바꿈) : O

   10> text-overflow 속성

       1] 정의 : 부모 영역을 벗어난 wrapping(자동 줄바꿈)이 되지 않은 텍스트의 처리 방법

       2] 조건

       -> width 속성이 지정되어 있어야 한다.
       => 이를 위해 필요할 경우 block 레벨 요소로 변경하여야 한다.

       -> 자동 줄바꿈 방지 : white-space 속성을 nowrap으로 설정한다.

       -> overflow 속성에 반드시 "visible" 이외의 값이 지정되어 있어야 한다.

       3] 속성값 - Description

       -> 속성값 - Description 1

        속성값 : clip

        Description : 영역을 벗어난 텍스트를 표시하지 않는다. (기본값)

       -> 속성값 - Description 2

        속성값 : ellipsis

        Description : 영역을 벗어난 텍스트를 잘라내어 보이지 않게 하고 밑줄임표(...)를 표시한다.

       -> 속성값 - Description 3

        속성값 : <!-

        Description : <string>

        속성 값으로 지정한 임의의 문자열을 출력한다. Firefox(9.0~)만 지원하는 기능이다. ->

   11> word-wrap 속성

    -> 정의 : 한 단어의 길이가 길어서 부모 영역을 벗어난 테스트의 처리 방법

    -> link 등을 표기할 때, 그 길이가 매우 길어지는데 이 속성을 사용하지 않으면 부모 영역을 넘어가게 된다.

   12> word-break 속성

       1] 정의 : 한 단어의 길이가 길어서 부모 영역을 벗어난 텍스트의 처리 방법

       2] 개행

       -> word-wrap 속성 : 단여를 어느 정도는 고려하여 개행
       => '.'과 '-' 등을 고려한다.

       -> word-break: break-all; : 단어를 고려하지 않고 부모 영역에 맞추어 강제 개행

6. 요소의 위치 정의
   
   1> position 속성

    (0) position 속성...?

       1] 정의 : 요소의 위치

       2] top, bottom, left, right 속성과 함께 사용하여 위치를 지정한다.

    (1) static(기본위치)

       1] static...?

       -> position 속성의 기본값
       => position 속성을 지정하지 않았을 때와 같다. 

       2] 배치

       -> 기본 : 위에서 아래로, 왼쪽에서 오른쪽으로 순서에 따라 배치

       -> 부모 요소 내에 자식 요소로서 존재할 때 : 부모 요소의 위치를 기준으로 배치

    => 이미 설정된 position을 무력화하기 위해 사용

    -> 주의 사항 : 좌표 속성(top, bottom, left, right)를 같이 사용할 수 없으며 사용할 경우, 무시된다.

    (2) relative(상대위치)

    -> 기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 속성(top, bottom, left, right)를 사용하여 위치를 이동시킨다.

    -> statix을 선언한 요소와 차이점 : 좌표 속성의 동작 여부

    (3) absolute(절대위치)

       1] 부모 요소 또는 가장 가까이 있는 조상 요소(static 제외)를 기준으로 좌표 속성(top, bottom, left, right)만큼 이동한다.

       -> relative, absolute, fixed 속성이 선언되어 있는 부모 또는 조상 요소를 기준으로 위치가 결정된다.

       2] 부모 또는 조상 요소가 static인 경우, document body를 기준으로 하여 좌표 속성대로 위치하게 된다.

       -> 부모 요소를 배치의 기준으로 삼기 위해서는 부모 요소에 relative를 정의하여야 한다.

       3] 부유 (객체) : 다른 요소가 먼저 위치를 점유하고 있어도 뒤로 밀리지 않고 덮어쓰게 된다.

       4] block 레벨 요소의 width : absolute 선언 시, inline 요소와 같이 content에 맞게 변화되므로 적절한 width를 지정하여야 한다.

       5] relative 속성과 absolute 속성의 차이점

       -> relative 속성 : 기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 속성(top, bottom, left, right)을 사용하여 위치를 이동시킨다.
       => 무조건 부모를 기준으로 위치하게 된다.

       -> absolute 속성 : 부모를 위치하게 되는 경우 
       => 부모에 static 이외의 position 속성이 지정되어 있을 때

       => 그렇다면 부모, 조상이 모두 static 속싱인 경우는?
       document body를 기준으로 위치하게 된다.

       6] 부모 요소의 영역을 벗어나 자유롭게 어디든지 위치할 수 있다.

    (4) fixed(고정위치)

    -> 부모 요소와 관계없이 브라우저의 viewport를 기준으로 좌표 속성(top, bottom, left, right)을 사용하여 위치를 이동시킨다.

    -> 스크롤이 되더라도 화면에서 사라지지 않고 항상 같은 곳에 위치한다.

    => fixed 속성 선언 시, block 요소의 width 
    -> inline 요소와 같이 content에 맞게 변화
    -> 적절한 width를 지정하여야 한다. 

   2> z-index 속성

    -> z-index 속성에 큰 숫자값을 지정할수록 화면 전면에 출력된다.

    -> position 속성이 static 이외인 요소에만 적용된다.

   3> overflow 속성

    (1) 정의 : 자식 요소가 부모 요소의 영역을 벗어났을 때 처리 방법

    (2) 속성값 - Description

       1] 속성값 - Description 1

       -> 속성값 : visible

       -> Description : 영역을 벗어난 부분을 표시한다. (기본값)

       2] 속성값 - Description 2

       -> 속성값 : hidden

       -> Description : 영역을 벗어난 부분을 잘라내어 보이지 않게 한다.

       3] 속성값 - Description 3

       -> 속성값 : scroll

       -> Description : 영역을 벗어난 부분이 없어도 스크롤 표시를 한다.
       (현재 대부분 브라우저는 auto와 동일하게 작동한다.)

       4] 속성값 - Description 4

       -> 속성값 : auto

       -> Description : 영역을 벗어난 부분이 있을 때만 스크롤 표시한다.

    (3) 특정 방향으로만 스크롤을 표시하고자 할 때 : overflow-x 또는 overflow-y 속성 사용
 
7. 요소 정렬
   
   0> float 속성

    (1) 정의 : 주로 레이아웃을 구성할 때 블록 레벨 요소를 가로 정렬하기 위해 사용되는 중요한 기법

    (2) flexbox 레이아웃 : 더욱 간단하게 정렬을 구현할 수 있다.
    -> flexbox 레이아웃을 지원하지 않는 IE를 고려해야 한다면 float 속성을 사용해야 한다.

    (3) 이미지와 텍스트가 있을 때, 이미지 주위를 텍스트로 감싸기 위해 만들어진 것이다. 

    (4) 아래에 적을 요소를 다음 요소 위에 떠 있게(부유하게) 한다.
    
    -> '떠 있다(float)'의 의미 : 요소가 기본 레이아웃 흐름에서 벗어나 요소의 모서리가 페이지의 왼쪽이나 오른쪽에 이동하는 것

    (5) 속성값 - Description

       1] 속성값 - Dscription 1

       -> 속성값 : none

       -> Description : 요소를 떠 있게 하지 않는다. (기본값)

       2] 속성값 - Description 2

       -> 속성값 : right

       -> Description : 요소를 오른쪽으로 이동시킨다.

       3] 속성값 - Description 3

       -> 속성값 : left

       -> Description : 요소를 왼쪽으로 이동시킨다.

    (6) 주의 사항 : 요소의 위치를 고정시키는 position 속성의 absolute를 사용하면 안된다.

   1> 정렬

    -> float 속성을 사용하지 않은 블록 요소들 : 수직으로 정렬

    -> float:left; 속성 : 왼쪽부터 가로 정렬

    -> float:right; 속성 : 오른쪽부터 가로 정렬
    => 출력 순서가 역순이 된다.

    -> 중앙 가로 정렬 : margin 속성을 사용해야 한다.

   2> width

    (1) 속성의 기본값 : 100%

    -> width 속성값을 지정하지 않은 block 요소 : 부모 요소의 가로폭을 가득 채운다.

    (2) width 속성을 선언하지 않은 block 레벨 요소에 float 속성이 선언 
    
    -> width가 inline 요소와 같이 content에 맞게 최소화

    -> 다음 요소 위에 떠 있게(부유하게) 됨.

   3> float 속성 관련 문제 해결 방법

    (1) float 속성이 선언된 요소와 float 속성이 선언되지 않은 요소 간 margin이 사라지는 문제

       1] float 속성이 선언된 요소가 다음 요 소 위에 떠 있는(부유하고 있는) 상태
       -> 두 요소 간의 margin이 제대로 표현되지 않는다.

       2] 두번째 요소에 float 속성을 선언하지 않았기 때문에 발생하는 박스 모델 상의 문제이다.

       3] 가장 쉬운 해결법 : float 속성을 선하지 않은 요소에 'overflow: hidden' 속성을 선언하는 것이다.

       4] overflow: hidden 속성의 역할
       : 자식 요소가 부모 요소의 영역보다 클 경우 넘치는 부분을 안보이게 해준다.

       5] 두번째 요소에도 float 속성을 선언하면 overflow: hidden 속성은 선언하지 않아도 되지만 너비가 최소화된다. 

    (2) float 속성이 선언된 자식 요소를 포함하는 부모 요소의 높이가 정상적으로 반영되지 않는 문제

       1] float 속성이 선언된 두 개의 자식 요소를 포함하는 부모 요소의 높이가 정상적인 값을 가지지 못하는 문제 발생

       2] float 요소의 높이를 알 수 없기 때문이다.
       -> float 요소는 일반적인 흐름 상에 존재하지 않기 때문이다.

       3] 위의 문제는 부모 요소 이후에 위치하는 요소의 정렬에 문제를 발생시킨다.

       4] 가장 쉬운 해결법 : float 속성이 선언된 자식 요소의 부모 요소(.container)에 overflow:hidden 속성을 선언하는 것이다.

       5] 다른 해결법
       -> 부모 요소의 너비 : float된 두 개의 자식 요소의 콘텐츠를 표현할 수 있는 만큼만으로 작게 줄어들게 된다.

       => 권장할 수 있는 방법 X

       6] 다른 해결법 : container 영역이 끝나기 직전 빈 요소를 만들고 clear:both를 설정하는 방법도 가능하다.

       => 의미 없는 빈 요소를 사용하여야 하기 때문에 이 방법 역시 권장하는 방법은 아니다. 

       7] overflow: hidden;과 함께 많이 사용되는 방법 : ::after 가상 요소 선택자를 이용하는 것

       -> 가상 요소 선택자 : CSS2 문법(:after)과CSS3 문법(::after)이 있는데 IE8까지 지원하는 CSS2 문법을 사용하는 편이 좋다.

       -> 부모 요소에 사전에 작성한 clearfix 클래스만 추가하거나, 해당 요소를 선택하여 클리어 문법을 선언하면 되기 때문에 가장 깔끔하고 간편하다.

       8] 또 다른 방법 : float 속성 대신 display: inline-black;을 선언하는 것이다.

       => 주의해야 할 점 : inline-block 속성 요소를 연속 사용하는 경우, 두 요소 사이에 정의하지 않은 공백(4px)가 자동 지정되는 것이다.

       9] 두 요소 사이에 정의하지 않은 공백(4px)이 자동 지정되어 부모 요소의 width를 초과하여 가로 정렬이 되지 않은 현상을 회피하는 방법

       => 부모 요소에 font-size: 0;을 선언하여 두 요소 사이에 정의하지 않은 공백을 제거한다.

   
   P.S 정리 내용이 이렇게 길어진 까닭은 내가 본 내용이 거의 다 새로 본 내용들이라 조금이라도 잘 이해해 보기 위해서 최대한 정리하려다 보니 이렇게 되었다... 나중에 더 공부하다 보면 같은 내용을 봐도 조금 더 깔끔하게 정리되지 않을까 하는 생각이 들었다.

-------------------------------------------------------------------

기초 웹 스터디 6주차 - 2023년 5월 2일 화요일

이번 주 WIL인 WIL6에 담을 내용은 수업 시간에 배운 내용들이다.

늘 수업의 본론 내용으로 들어가기 전에 지난 수업 시간에 배웠던 것을 리뷰해주시는데 그 내용을 적어보자면,

CSS는 Cascading Style Sheet의 약자라고 하셨다.

여기서  Cascading은 마치 계곡물이 떨어지는 것처럼 생각하면 된다고 하셨다.

CSS의 특징에는 상속과 우선순위가 있는데 여기서 상속은 나중에 배울 트리를 통해 알 수 있다고 하셨다.

그리고 우선순위에는 크게 세 가지가 있다고 하셨는데 적어보면,

1} 사용자 스타일 (컴퓨터 사용자)

2} 제작자 스타일 (개발자)

3} 브라우저 스타일

이렇게 있다.

여기서 숫자가 적을수록 우선순위가 높은 것이다.

그리고 3번인 브라우저 스타일은 개발자가 지정하지 않은 곳을 위해 있는 것인데 요즘은 잘 쓰이지 않는다고 말씀하셨다.

그리고 만약 다 제작자 스타일이라 우선순위가 같다면 어떻게 되는지 알려주셨는데 적어보면,

1] !important 스타일

2] 인라인 스타일

3] id 스타일

4] 클래스 스타일

5] 타입 스타일

이렇게 있는데 이건 selector가 정한다고 하셨다.

여기서 selector는 id 선택자, 클래스 선택자, 타입 선택자, 전체 선택자가 있다.

그리고 내부에서 정하는 것이 아니라 외부 링크를 통해 정하는 방법이 있다.

<'link rel = "stlyesheet" href 
<ins>링크<ins>
'>

이렇게 쓰면 된다.

이제 오늘 배웠던 Box model과 FLEX Box Layout에 대해 적을 것인데 그중에서 Box model에 대해 먼저 적을 것이다.

[스터디 들으면서 그린 그림 - Box model](https://user-images.githubusercontent.com/127318008/235733567-b65aa9e0-7f1d-414a-8753-43896fa97b43.jpg)

이 그림에 대한 설명을 더 적어보자면,

1] border : 박스의 테두리

2] padding : 테두리와 content의 간격

3] margin : 테두리와 다른 요소와의 간격

4] 화살표의 의미
예)
1} margin : 10px(top) 30px(right) 0px(bottom) 20px(left)
2} margin : 10px 30px -> 위/아래 : 10px & 좌/우 : 30px

그리고 추가적으로 설명하신 것이 있는데 그것도 적어보자면,

1] 블록 레벨 요소

1} 한 줄을 차지하는 박스

2} 부모 요소 공간 전체 차지 O

2] 인라인 레벨 요소

1} 자신만을 감싸는 박스

2} 부모 요소 공간 전체 차지 X

이렇게 설명해주셨다.
이제 다음 것인 FLEX Box Layout에 대해 적어볼 차례이다.

여기서 FLEX는 Flexible을 의미한다고 하셨다.

그리고 아이템이 배열된 방향인 주축을 정할 수 있다고 하셨다.

예)
.flex-box{

display : flex ;

flex-direction : row ;

}

그다음 설명해주신 것은 그림과 함께 볼 것이다. (그림으로 충분한 설명이 될 정도로 간단한 내용이다...)

[스터디 들으면서 그린 그림 - FLEX Box Layout](https://user-images.githubusercontent.com/127318008/236006924-b3a289eb-95a7-410d-ace0-caeb2c138ca8.jpg)

여기서 추가적으로 설명해주신 것은,

1] justify content : mainaxis

2] align-item : cross-axis

이렇게 있다.

그리고 외우는 방법을 알려주셨는데 기억이 나진 않지만 말하실 때 조금 머뭇거리며 하셨다.

마지막으로 css grid layout, can i use라는 것이 있다는 것을 설명해주셨다.

## Flexbox Froggy 답안

stage 1 : justify-content: flex-end;

stage 2 : justify-content: center;

stage 3 : justify-content: space-around;

stage 4 : justify-content: space-between;

stage 5 : align-items: flex-end;

stage 6 : justify-content: center; align-items: center;

stage 7 : justify-content: space-around; align-items: flex-end;

stage 8 : flex-direction: row-reverse;

stage 9 : flex-direction: column;

stage 10 : justify-content: flex-end; flex-direction: row-reverse;

stage 11 : flex-direction: column; justify-content: flex-end;

stage 12 : flex-direction: column-reverse; justify-content: space-between;

stage 13 : flex-direction: row-reverse; justify-content: center; align-items: flex-end;

stage 18 : flex-wrap: wrap;

stage 19 : flex-direction: column; flex-wrap: wrap;

stage 20 : flex-flow: column wrap;

-------------------------------------------------------------------

기초 웹 스터디 7주차 - 2023년 5월 9일 화요일

이번 주 WIL인 WIL7에 담을 내용은 내가 실습해보면서 알게 된 내용들과 느낀 점이다.
(사실 수업 시간에 실습하면서 배운 점을 위주로 적고 싶지만 내가 컨디션이 너무 좋지 않아 수업 시간에 어떤 것도 할 수 없었기에 그건 적을 수 없다...)

이번 스터디 시간에는 클론 코딩을 실습하는 시간을 가졌는데 수월한 실습을 위해 자료를 만들어주셨다.
정리 내용은 그 자료를 바탕으로 이루어질 것이다.

자료 순서대로 실습 과정을 따라가보자면,
우선 구현할 화면을 분석하였다.

## 1. 화면 분석

이번 실습 때 구현할 화면은 Youtube 화면이었는데 내가 보기에는 크게는 세 사각형

1> view : 전체 화면

2> header : 우리가 흔히 Youtube 화면 내려도 계속 위로 고정되어 있는 것

3> container : view에서 header 빼고 나머지

이렇게 구분할 수 있다.

여기서 container를 조금 더 나누면

1> main container : video container, video-info container, comment-container를 포함하고 있는 container

1] video container : 영상 재생 부분

2] video-info container : 영상 제목, 채널 이름, 좋아요, 공유 등이 나오는 부분

3] comment-container : 댓글 나오는 부분

2> aside-container : main container 오른쪽에 추천 영상들 나오는 부분

이렇게 나눌 수 있다.
이로써 화면 분석은 완료하였다.

## 2. CSS 초기화 & html 파일 생성

CSS 초기화는 필수는 아니지만 브라우저(예 : Chrome)마다의 기본 디폴트 스타일 값이 아니라 동일한 CSS 스타일 값을 보여주기 위해 초기화 해주는 것이라고 하셨다.

그리고 구현할 문서인 index.html을 만들었다.

## 3. Header 생성

우선 길게 적을 것이 있어 복사 및 붙여넣기 할 수 있게 해주셨다.

그리고 유튜브 헤더처럼 위에 늘 붙어있게 해주기 위해 top: 0; 속성과 position: sticky; 속성을 가지게 해주었다.

그리고 아이템들이 가로 줄로 길게 배치되어 있고 동일한 간격을 가지고 있게 하기 위해서 justify-content: space-between (동일한 간격을 가지고 있게 하는 속성), flex-direction: row(가로 줄로 길게 배치되게 하는 속성)을 이용하였다.

그리고 보통 우리가 클릭할 수 있는 요소들은 마우스로 갖다대면 약간의 회색으로 변하면서 마우스가 손모양으로 바뀌도록 한다.
이것을 구현하기 위해 grey-background(너무 붙지 않게 띄어주기), grey-background:hover(회색으로 변하게, 마우스로 갖다대면 변하게 하기)

그리고 flex-row-center 속성을 이용하여 한 박스 안에 있는 요소들이 가운데 있도록 해주며 pointer:hover로 마우스를 갖다대면 손모양으로 바뀌게 해준다.

여기서 느낀 점을 조금만 써보자면 아직 많이 바뀐 것은 없지만 그래도 한 번쯤은 '이건 과연 어떻게 할까?' 라고 생각했던 것들이 실제로 되니 신기했다.

다시 본론으로 돌아가자면,

이제 Header 말고 Search Bar를 CSS를 통해 꾸며보기 위해 Search Bar의 길이를 늘리고 테두리를 굵고 둥글게 해야겠다는 생각을 먼저 떠올리는 것이 1순위이다.

이것을 먼저 생각한 다음에 문서를 밑으로 내려 복사 및 붙여넣기가 아닌 내가 입력해본다. (width: 450px; border: 3px solid grey; ...)

이렇게 하면 Search Bar가 완성된다.

## 4. container 생성

그다음은 container를 꾸며볼 차례이다.

가장 먼저 큰 틀을 생각해보면 container는 main container와 aside container가 좌우로 놓여져 있다.

이 부분은 flex-direction: row;를 통해 좌우로 놓으면 된다.

main container와 aside container를 더 자세히 알아볼 것인데 그중 main container를 먼저 자세히 알아볼 것이다.
main container가 container 전체와 너무 딱 붙어 있지 않게 하기 위해 적당히 거리를 만들어주고 main container 안에 있는 video-container, video-info-container, comment-container를 만들면 된다.

여기서 comment-container는 만들지 않아도 된다고 하셨으니 video-container와 video-info-container를 만들면 된다.

그 다음 다른 꾸미기 요소들은 복사 및 붙여넣기할 수 있게 해주셨으니 겹치기 않게 내용 보고 복사 및 붙여넣기하면 된다. 

이 다음에는 comment-container를 볼 차례이다.

사실 이 활동은 복사 및 붙여넣기가 많은데 여기서 주의할 점은 복사 및 붙여넣기로 제자리를 찾지 못한 줄들을 다시 잘 보고 줄 맞추기를 잘해야 한다는 것이고 미처 잘린 부분이 있는 곳은 다른 곳과 잘 비교하여 채워야 한다는 것이다.

이것들을 지키지 못한다면 error가 나거나 우선순위가 바뀔 수 있으니 꼭 잘 지키도록 하자.
(사실 이것들은 나에게 하는 말이다.)

이렇게 내용을 보며 꾸며나가다 보면 진짜 과제를 해야 하는 부분이 온다.

## 5. 오른쪽 사이드 부분

진짜 과제를 해야 하는 부분은 바로 오른쪽 사이드 부분이다. 

aside-container와 aside-video, aside-info 및 aside-video-info를 style.css에 만들어 위치 배열 및 크기 조정을 하면 된다.

그리고 video는 main container에 쓰였던 사진을 크기 조절하여 쓰면 된다.

마지막으로 info 부분에 해당하는 글은 역시 main container 안에 있는 video-info-container에 있는 내용을 참고하여 써보았다.

사실 이번 주 과제는 완벽하게 수행했다고 할 수 없을 것 같다.

하지만 그래도 오른쪽 사이드에 그림(사진?)과 글이 나오게 위치 조정에 성공하였으니(flex-start와 flex-end를 이용하여 성공하였다!) 이번 주 과제는 여기서 마치도록 하겠다.

사실 이번 주 과제는 수업 내용도 거의 못 듣고 하는 것(1시간 동안 기침함...)이라 많이 어려웠다.

이제 감기도 거의 다 나았으니(기침도 많이 없어졌다!) 제대로 수업 듣고 잘해보았으면 좋겠다...

이번 주 WIL은 여기서 마치겠다.

-------------------------------------------------------------------

기초 웹 스터디 8주차 - 2023년 5월 16일 화요일

이번 주 WIL인 WIL8에 담을 내용은 잘 정리되어 있는 래퍼런스 사이트에서 정해준 내용을 공부한 후 내가 새로 알게 된 내용 및 기억하고 싶은 내용을 정리한 것이다.  

## JavaScript

1. 기본 개념과 동작 원리 이해의 중요성
   
   1> 프로그래밍이란?

   (1) 프로그래밍 : 컴퓨터에게 실행을 요구하는 일종의 커뮤니케이션

   즉, 요구사항의 집합을 분석하여 적절한 자료구조와 함수의 집합으로 변환한 후, 그 흐름을 제어하는 것

   (2) 프로그래밍은 문제 해결 능력을 요구하며 정확하게 상세하게 요구사항을 설명하는 작업이다. 

   2> 프로그래밍 언어

   (1) 프로그래밍 언어는 Syntax(구문, 문법)와 Semantics(의미)의 조합으로 표현된다.

   => 용어 정리

      1] 기계어(Machine code) : 컴퓨터가 이해할 수 있는 언어

      2] 컴파일러(compiler) 혹은 인터프리터(interpreter) : 프로그래밍 언어를 컴퓨터가 이해할 수 있는 기계어로 변환하여 주는 일종의 번역기 

      3] 언어(language) : 자신의 생각을 상대에게 전달하는 방법으로 언어 공동체 내에서 이해될 수 있는 말의 집합

      (언어에는 자연어(인간이 이해할 수 있는 언어)와 인공어로 구분할 수 있다.)

   3> Syntax & Semantics (문법 & 의미)

   (1) Syntax(문법) : 문제 해결 능력을 통해 만들어낸 해결 방안은 프로그래밍 언어의 문법을 통해 표현한다.
   (작성된 코드 : 해결 방안의 구체적 구현물)

   (2) Semantics(의미) : 프로그래밍 언어의 문법에 부합하는 것은 물론, 요구사항이 실현(문제가 해결)되어야 의미가 있다.

   4> 기본 개념과 동작 원리 이해의 중요성

   (1) 프로그래머가 해야 할 일 : 문제를 해결하기 위한 방안을 고안하고 이것을 문법에 맞게 코드로 구현하는 것
   -> 기본 개념과 동작 원리를 정확히 이해하는 것이 중요하다.

   (2) 기본 개념 
   
      1] 문맥에 맞는 정확한 용어를 사용할 수 있게 돕는다.

      2] 문맥에 맞는 정확한 용어의 사용 : 오해를 불러 일으키지 않는 명확한 의사 소통을 가능케 한다. -> 협업의 기본이며 필수 요소

   (3) 동작 원리 이해

      1] 코드의 동작을 예측할 수 있게 돕는다.

      2] 코드의 동작을 예측할 수 있는 능력 : 필수 불가결적 요소

   (4) 기본 개념과 동작 원리의 이해 : 어렵고 생소한 용어들로 이루어진 기술적 의사 소통을 가능케 하고, 자신의 머릿속에서 코드를 실행시켜 볼 수 있는 능력을 갖게 한다.

2. 자바스크립트의 기본 문법
   
   1> 변수
   
      1] 정의 : 메모리 주소(Memory address)에 접근하기 위해 사람이 이해할 수 있는 언어로 지정한 식별자(identifier)

      2] 사용 목적 : 값(vlaue)을 저장(할당)하고 그 저장된 값을 참조하기 위해
      (변수의 이름을 통해 값의 의미를 명확히 할 수 있어 코드의 가독성이 좋아진다.)

      3] 선언 : 'var' 키워드 사용

      4] 할당 : 할당 연산자 '=' 사용

      5] 예시
      
        1} var = x; 
           x = 6;

        2} var x = 6;
      
   2> 값

      1] 정의 : 프로그램에 의해 조작될 수 있는 대상

      2] 생성 방법 : 리터럴 표기법(literal notation) 등

      3] 데이터 타입

        1} 원시 타입(primitive data type)

          (1) number

          (2) string

          (3) boolean

          (4) null

          (5) undefined

          (6) symbol (New in ECMAScript6)

          => 다양한 연산자의 피연산자가 되어 하나의 값으로 평가될 수 있다.
          -> 리터럴은 연산에 의해 하나의 값이 될 수 있다.

        2} 객체 타입 (Object data type)

          (1) object

        3} 동적 타이핑 : 변수에 할당된 값의 타입에 의해 동적으로 변수의 타입이 결정되는 것

          => 자바스크립트가 다른 프로그래밍 언어와 구별되는 특징 중 하나이다.

        4} 용어 정리

          (1) 데이터 타입(Data Type) : 프로그래밍 언어에서 사용할 수 있는 값의 종류

          (2) 변수(Variable) : 값이 저장된 메모리 공간의 주소를 가리키는 식별자(identifier)

          (3) 리터럴(literal) : 소스코드 안에서 직접 만들어 낸 상수 값 자체를 말하며 값을 구성하는 최소 단위

   3> 연산자(Operator)

      1] 정의 : 하나 이상의 표현식을 대상으로 산술, 할당, 비교, 논리, 타입 연산 등을 수행해 하나의 값을 만든다.

      2] 피연산자(Operand) : 연산의 대상

      3] 자바스크립트는 암묵적 타입 강제 변환을 통해 연산을 수행한다.

   4> 키워드(keyword)

      1] 정의 : 수행할 동작을 규정한 것

      2] 예시

        1} var 키워드 : 새로운 변수를 생성할 것을 지시한다.

   5> 주석(Comment)

      1] 사용 목적 : 작성된 코드의 의미를 설명하기 위해
      (가독성이 좋아지게 하기 위해)

      2] 사용 방법

        1} 한 줄 주석 : '//' 다음에 작성한다.

        2} 여러 줄 주석 : '/*'과 '*/'의 사이에 작성한다.

      3] 주석은 해석기(parser)가 무시하며 실행되지 않는다.

      4] 주의사항 : 과도한 주석은 오히려 가독성을 해칠 수 있다.

   6> 문

      1] 프로그램(스크립트) : 컴퓨터(Client-side Javascript의 경우, 엄밀히 말하면 웹 브라우저)에 의해 단계별로 수행될 명령들의 집합

      2] 문(statement) : 각각의 명령
      -> 문이 실행되면 무슨 일인가가 일어나게 된다.

      3] 리터럴(literal), 연산자(Operator), 표현식(Expression), 키워드(Keyword) 등으로 구성되며 세미콜론(;)으로 끝나야 한다.

      4] 그룹화

        1} 문은 코드 블록(code block, {...})으로 그룹화할 수 있다.

        2} 목적 : 함께 실행되어져야 하는 문을 정의하기 위해

      5] 순서

        1} 일반적인 순서 : 위에서 아래로 순서대로 실행된다.

        2} 흐름 제어(Control Flow) : 조건문(if, switch)이나 반복문(while, for)의 사용으로 제어할 수 있다.

        3} 또는 함수 호출로 변경될 수 있다.

      6] 자바스크립트에서는 함수 단위의 유효범위(Function-level scope)만이 생성된다.

   7> 표현식

      1] 표현식(Expression)은 하나의 값으로 평가(Evaluation)된다.

      2] 표현식의 종류

         1} 값(리터럴)

         2} 변수

         3} 객체의 프로퍼티

         4} 배열의 요소

         5} 함수 호출

         6} 메소드 호출

         7} 피연산자와 연산자의 조합

      3] 표현식은 다른 표현식의 일부가 되어 조금 더 복잡한 표현식을 구성할 수도 있다. 
      -> 표현식은 결국 하나의 값이 되기 때문이다.

   8> 문과 표현식의 비교

      1] 문(Statement)

        1} 정의 : 마침표로 끝나는 하나의 완전한 문장

        2} 표현식을 통해 평가한 값을 통해 실제로 컴퓨터에게 명령을 하여 무언가를 하는 것이다.

      2] 표현식 : 문을 구성하는 요소

        1} 정의 : 문을 구성하는 요소

        2} 평가되어 값을 만들지만 그 이상의 행위를 할 수 없다.

        3} 표현식은 그 자체로 하나의 문이 될 수도 있다.

   9> 함수

      1] 정의 : 어떤 작업을 수행하기 위해 필요한 문(statement)들의 집합을 정의한 코드 블록

      2] 호출

        1} 함수는 이름과 매개변수를 갖고 필요할 때에 호출한다.

        2} 함수는 호출에 의해 실행된다.

        3} 한 번만 호출할 수 있는 것이 아니라 여러 번 호출할 수 있다.

      3] 코드의 재사용 : 동일한 작업을 반복적으로 수행해야 한다면 미리 정의된 함술르 재사용하는 것이 효율적이다.

   10> 객체

      1] 자바스크립트 : 객체(object) 기반의 스크립트 언어

      2] 객체

        1} 정의 : 데이터를 의미하는 프로퍼티(property)의 데이터를 참조하고 조작할 수 있는 동작(behavior)을 의미하는 메소드(method)로 구성된 집합

        2] 구조화 : 데이터와 동작을 하나의 단위로 구조화할 수 있어 유용하다.
        -> 객체는 데이터(프로퍼티)와 그 데이터에 관련되는 동작(메소드)을 모두 포함할 수 있기 때문이다.

        3} 자바스크립트를 이루고 있는 거의 모든 것
        => 원시 타입(Primitives)을 제외한 나머지 값들(함수, 배열, 정규표현식 등)

      3] 자바스크립트 객체

        1} 정의 : 키(이름)와 값으로 구성된 프로퍼티(property)의 집합

        2} 프로퍼티의 값 : 자바스크립트에서 사용할 수 있는 모든 값을 사용할 수 있다.

        3} 자바스크립트의 함수는 일급 객체이므로 값으로 취급할 수 있다.

        4} 객체지향의 상속을 구현하기 위해 "프로토타입"이라고 불리는 객체의 프로퍼티와 메소드를 상속받을 수 있다.

   11> 배열(array)

      1] 사용할 때 : 1개의 변수에 여러 개의 값을 순차적으로 저장할 때

      2] 자바스크립트의 배열 : 객체이며 유용한 내장 메소드를 포함하고 있다.

3. 데이터 타입과 변수
   
   0] 시작하기에 앞서...

        1} 메모리에 값 저장하기

          (1) 메모리 공간을 확보해야 할 메모리의 크기(byte)를 알아야 한다.
          -> 값의 종류(= 데이터의 종류, 데이터 타입(Data Type))에 따라 확보해야 할 메모리의 크기가 다르기 때문이다.

        2} C-family 언어(C, Java / 정적 타입(Static/Strong Type)의 언어) : 변수 선언 시 변수에 저장할 값의 종류를 사전에 타입 지정(Type annotation)하여야 한다.

        3} 동적 타입(Dynamic/Weak Type) 언어(자바스크립트) : 변수의 타입 지정(Type annotation) 없이 값이 할당되는 과정에서 자동으로 변수의 타입이 결정(타입 추론, Type Inference)된다.
        -> 같은 변수에 여러 타입의 값을 자유롭게 할당할 수 있다. (변수 : 고정된 타입 X)

   1] 데이터 타입

        0} 들어가기에 앞서...

          (1) 코드에서 사용되는 모든 데이터는 메모리에 저장하고 참조할 수 있어야 한다.

        1} 원시 타입(Primitive Data Type)

          (1) 원시 타입의 값 : 변경 불가능한 값(immutable value) & 값에 의한 전달(pass-by-value)
   
          (2) number

           1| 자바스크립트는 독특하게 실수(일반적으로 소수를 가리킨다.) 타입만 존재한다.

           2| 추가적으로 3가지 특별한 값들도 표현할 수 있다.

             1/ Infinity : 양의 무한대

             2/ -Infinity : 음의 무한대

             3/ NaN : 산술 연산 불가(not-a-number)

          (3) string
          
           1| 사용

             1/ 텍스트 데이터를 나타낸다.

             2/ 표기법 : 작은 따옴표('')(가장 일반적인 표기법) 또는 큰 따옴표("") 안에 텍스트를 넣어 생성한다.

           2| 자바스크립트의 문자열 : 원시 타입 & 변경 불가능(immutable)

             1/ 예시
                var str = 'Hello';
                str = 'world'; 
                -> 변수 str은 문자열 'Hello'를 가리키고 있다가 문자열 'world'를 가리키도록 변경된 것이다.

             2/ 유사 배열 : 배열처럼 인덱스를 통해 접근할 수 있는 데이터

             3/ 변경 불가능(immutable)의 의미 : 이미 생성된 문자열의 일부 문자를 변경해도 반영되지 않는다.
             -> 새로운 문자열을 재할당하는 것은 가능하다.

          (4) boolean
           
           1| 불리언(boolean) 타입의 값 : 논리적 참, 거짓을 나타내는 true와 false뿐이다.

           2| 사용 : 조건문에서 자주 사용한다.
           -> 조건문은 참과 거짓으로 구분되는 조건에 의해 프로그램의 흐름을 제어한다.

           3| false로 간주되는 것 : 비어있는 문자열, null, undefined, 숫자 0

          (5) undefined

           1| undefined 타입의 값 : undefined
           -> 선언 이후 값을 할당하지 않은 변수는 undefined 값을 가진다.
           -> 이는 변수 선언에 의해 확보된 메모리 공간을 처음 할당이 이루어질 때까지 빈 상태(대부분 비어있지 않고 쓰레기 값(Garbage value)이 들어있다.)로 내버려두지 않고 자바스크립트 엔진이 undefined로 초기화하기 때문이다.
           -> 개발자가 변수의 값이 없다는 것을 명시하고 싶은 경우 : null을 할당한다.

          (6) null

           1| null 타입의 값 : null
           -> 자바스크립트는 대소문자를 구별(case-sensitive)하므로 null은 Null, NULL등과 다르다.

           2| 사용 : 의도적으로 변수에 값이 없다는 것을 명시할 때 사용한다.
           -> 이는 변수가 기억하는 메모리 어드레스의 참조 정보를 제거하는 것을 의미한다.
           -> 자바스크립트 엔진은 누구도 참조하지 않는 메모리 영역에 대해 가비지 콜렉션을 수행할 것이다.

           3| null 반환 : 함수가 호출되었으나 유효한 값을 반환할 수 없는 경우. 명시적으로 null을 반환하기도 한다.

           4| typeof 연산자 

             1/ 정의 : 타입을 나타내는 문자열을 반환하는 연산자

             2/ 연산 : null이 아닌 object가 나온다.
             -> 이는 자바스크립트의 설계상의 오류이다.
             -> null 타입을 확인하는 방법 : 일치 연산자(===) 사용

          (7) symbol

           1| 정의 : ES6에서 새롭게 추가된 7번째 타입으로 변경 불가능한 원시 타입의 값

           2| 사용 목적 : 주로 이름의 충돌 위험이 없는 유일한 객체의 프로퍼티 키(property key)를 만들기 위해

           3| 호출 : 심볼은 Symbol 함수를 호출해 생성한다.
           -> 이때 생성된 심볼 값은 다른 심볼 값들과 다른 유일한 심볼 값이다.

        2} 객체 타입(Object type, Reference type)

          (1) 객체

           1| 정의

             1/ 데이터와 그 데이터에 관련한 동작(절차, 방법, 기능)을 모두 포함할 수 있는 개념적 존재

             2/ 이름과 값을 가지는 데이터를 의미하는 프로퍼티(property)와 동작을 의미하는 메소드(method)를 포함할 수 있는 독립적 주체

            2| 자바스크립트

             1/ 원시 타입(Primitives)을 제외한 나머지 값들(배열, 함수, 정규표현식 등)은 모두 객체이다.

             2/ 객체는 pass-by-reference(참조에 이한 전달) 방식으로 전달된다.

   2] 변수

        0} 들어가기에 앞서...

          (1) 정의 : 프로그램에서 사용되는 데이터를 일정 기간 동안 기억하여 필요한 때에 다시 사용하기 위해 데이터에 고유의 이름인 식별자(identifier)를 명시한 것
   
          (2) 변수명 : 변수에 명시한 고유한 식별자
   
          (3) 변수값 : 변수로 참조할 수 있는 데이터
   
          (4) 식별자 : 어떤 대상을 유일하게 식별할 수 있는 이름
          -> 식별자에는 변수명, 함수명, 프로퍼티명, 클래스명 등이 있다.

          (5) 변수는 키워드(var, let, const)를 사용하여 선언하고 할당 연산자를 사용해 값을 할당하며 식별자인 변수명을 사용해 변수에 저장된 값을 참조한다.

        1} 변수의 선언

          (1) 변수명(식별자(identifier)) 명명 규칙
   
            1| 반드시 영문자(특수문자 제외), jnderscore( _ ), 또는 달러 기호($)로 시작하여야 한다.
            이어지는 문자에는 숫자(0-9)도 사용할 수 있다.

            2| 사용할 수 있는 문자 : "A"~"Z"(대문자)와 "a"~"z"(소문자)
            -> 자바스크립트는 대/소문자를 구별하기 때문이다.

          (2) 선언 : var 키워드 사용한다.

            1| var 키워드를 사용한다.

            2| 할당 연산자 : 등호(=, equal sign)

            3| 선언하지 않은 변수에 접근하면 ReferenceError가 발생한다.

        2} 변수의 중복 선언

          (1) var 키워드로 선언한 변수는 중복 선언이 가능하다.
   
          (2) 부작용 : 동일한 변수명이 선언되어 있는 것을 모르고 변수를 중복 선언했다면 의도치 않게 변수의 값을 변경한다.
          -> 사용하지 않는 것이 좋다.

        3} 동적 타이핑(Dynamic Typing)

          (1) 정의 : 같은 변수에 여러 타입의 값을 할당할 수 있다.
          
        4} 변수 호이스팅(Variable Hoisting)

          (1) 호이스팅

            0| 자바스크립트는 모든 선언문이 호이스팅(Hoisting)된다.

            1| 정의 : 모든 선언문(var 선언문이나 function 선언문 등)이 해당 Scope의 선두로 옮겨지는 것처럼 동작하는 특성
            -> 자바스크립트는 모든 선언문이 선언되기 이전에 참조 가능하다.

          (2) 변수 생성

            1| 선언 단계(Declaration phase) : 변수 객체(Variable Object)에 변수를 등록한다.
            -> 변수 객체 : 스코프가 참조하는 대상

            2| 초기화 단계(Initialization phrase) : 변수 객체(Variable Object)에 등록된 변수를 메모리에 할당한다.
            -> 변수는 undefined로 초기화된다.
            => 선언 단계와 초기화 단계는 한 번에 이루어진다.

            3| 할당 단계(Assignment phase) : undefined로 초기화된 변수에 실제값을 할당한다.

            4| 변수 호이스팅 : 변수 선언문 이전에 변수에 접근하여도 Variable Object에 변수가 존재하기 때문에 에러기 발생하지 않고 undefined를 반환하는 현상

          (3) 스코프

            1| 함수 레벨 스코프(Function-level scope) : 함수 내에 선언된 변수는 함수 내에서만 유효하며 함수 외부에서는 참조할 수 없다.
            -> 함수 내부에서 선언한 변수 : 지역 변수
            -> 함수 외부에서 선언한 변수 : 전역 변수

            2| 블록 레벨 스코프(Block-level scope) : 코드 블록 내에서 선언된 변수는 코드 블록 내에서만 유효하며 코드 블록 외부에서는 참조할 수 없다.

        5} var 키워드로 선언된 변수의 문제점

          (1) var 키워드로 선언된 변수의 특징

            1| 함수 레벨 스코프(Function-level scope)

                1/ 전역 변수의 남발

                2/ for loop 초기화식에서 사용한 변수를 for loop 외부 또는 전역에서 참조할 수 있다.

            2| var 키워드 생략 허용

                1/ 의도하지 않은 변수의 전역화

            3| 중복 선언 허용

                1/ 의도하지 않은 변수값 변경

            4| 변수 호이스팅

                1/ 변수를 선언하기 전에 참조가 가능하다.

          (2) 대부분의 문제는 전역 변수로 인해 발생한다.

            1| 유효 범위(scope)가 넓어서 어디에서 어떻게 사용될지 파악하기 힘들다.

            2| 복잡성이 증가한다.

          -> 변수의 유효 범위(scope)는 좁을수록 좋다.
          -> ES6는 이러한 var의 단점을 보완하기 위해 let과 const 키워드를 도입하였다.

4. 연산자

   1] 표현식과 연산자

     1} 표현식과 값
     
       (1) 표현식과 값은 동등한 관계이다.
       -> 동치(Equivalent)

       (2) 표현식은 값처럼 사용할 수 있다.
       -> 값이 위치할 수 있는 자리에는 표현식도 위치할 수 있다.
     
   2] 문과 표현식

     1} 자바스크립트의 모든 코든느 문 또는 표현식이다.

     2} 역할

       (1) 표현식의 역할 : 값을 생성하는 것

       (2) 문의 역할 : 표현식으로 생성한 값을 사용해 컴퓨터에게 명령을 내리는 것

     3} 문

       (1) 표현식인 문

         1| 예시 : 할당문(그 자체가 표현식인 문이다.)

       (2) 표현식이 아닌 문

         1| 예시 : 선언문(값으로 평가될 수 없다.)

   3] 연산자란?

     1} 정의 : 하나 이상의 표현식을 대상으로 산술, 할당, 비교, 논리, 타입 연산 등을 수행해 하나의 값을 만든다.

     2} 피연산자(Operand) : 연산의 대상

     3} 연산자와 표현식

       (1) 피연산자 : 표현식이다.
       -> 피연산자도 평가되어 하나의 값이 되기 때문이다.

       (2) 연산자 표현식 : 표현식이다.
       -> 연산자 표현식 : 피연산자를 연산자와 결합한 것

     4} 연산자와 피연산자

       (1) 연산자 : "값을 만든다"라는 동사의 역할
   
       (2) 피연산자 : "값"이라는 명사의 역할

   4] 산술 연산자

     0} 들어가기에 앞서...

       (1) 정의 : 피연산자를 대상으로 수학적 계산을 수행해 새로운 숫자 값을 만든다.
   
       (2) 산술 연산을 할 수 없는 경우 : NaN을 반환하다.

     1} 이항 산술 연산자

       (1) 연산 : 2개의 피연산자를 대상으로 연산하여 숫자 타입의 값을 만든다.

       (2) 피연산자의 값을 변경하는 부수 효과(Side effect)가 없다.
       -> 어떤 산술 연산을 해도 피연산자의 값이 바뀌는 경우는 없고 단지 새로운 값을 만들 뿐이다.

       (3) 종류

         1| + : 덧셈

         2| - : 뺄셈

         3| * : 곱셈

         4| / : 나눗셈

         5| % : 나머지

     2} 단항 산술 연산자

       (1) 연산 : 1개의 피연산자를 대상으로 연산한다.
   
       (2) 피연산자의 값을 변경하는 부수 효과가 있다.
       -> 증가/감소 연산을 하면 피연산자의 값이 바뀐다.

       (3) 종류

         1| ++ : 증가

         2| -- : 감소

         3| + : 어떠한 효과도 없다.(부수 효과 X)
         -> 음수를 양수로 반전하지도 않는다.

         4| - : 양수를 음수로 음수를 양수로 반전한 값을 반환한다. (부수 효과 X)

       (4) 전위 증가/감소 연산자(Prefix increment/decrement operator) & 후위 증가/감소 연산자(Postfix increment/decrement operator)

         1| 전위 증가/감소 연산자 : 피연산자의 값을 증가/감소시킨 후, 다른 연산을 수행한다.

         2| 후위 증가/감소 연산자 : 먼저 다른 연산을 수행한 후, 피연산자의 값을 증가/감소시킨다.

     3} 문자열 연결 연산자

       (1) + 연산자 : 피연산자 중 하나 이상이 문자열인 경우 문자열 연결 연산자로 동작한다.
       (그 외의 경우는 덧셈 연산자로 동작한다.)

       (2) + / - 단항 연산자도 암묵적 타입 변환 발생이 가능하다.

   5] 할당 연산자(Assignment Operator)

     1} 정의 : 우항에 있는 피연자의 평가 결과를 좌항에 있는 변수에 할당한다.

     2} 부수 효과 : 할당 연산자는 변수에 값을 할당하므로 부수 효과 O

     3} 종류

       (1) =
   
         1| 사례 : x = y

         2| 동일 표현 : x = y

       (2) +=

         1| 사례 : x += y

         2| 동일 표현 : x = x + y

       (3) -=

         1| 사례 : x -= y

         2| 동일 표현 : x = x - y

       (4) *=

         1| 사례 : x *= y

         2| 동일 표현 : x = x * y

       (5) /=

         1| 사례 : x /= y

         2| 동일 표현 : x = x / y

       (6) %=

         1| 사례 : x %= y

         2| 동일 표현 : x = x % y

     4} 표현식 : 할당 연산은 하나의 값으로 평가되는 표현식이다.
     -> 할당 표현식은 할당된 값으로 평가된다.

   6] 비교 연산자(Comparison Operator)

     0} 들어가기에 앞서...

       (1) 반환값 : 좌항과 우항의 피연산자를 비교하여 불리언 값을 반환한다.
   
       (2) 사용 : 제어문(if 문, for 문 등)의 조건식에서 주로 사용한다.

     1} 동등 / 일치 비교 연산자

       (1) 종류

         1| ==

             1/ 의미 : 동등 비교

             2/ 사례 : x == y

             3/ 설명 : x와 y의 값이 같음

             4/ 좌항과 우항의 피연산자를 비교할 때 암묵적 타입 변환을 통해 타입을 일치시킨 후 같은 값을 갖는지 비교한다.

         2| ===

             1/ 의미 : 일치 비교

             2/ 사례 : x === y

             3/ 설명 : x와 y의 값과 타입이 같음

             4/ 주의사항 : NaN, 숫자 0
             -> NaN의 정의 : 자신과 일치하지 않은 유일한 값
             -> NaN의 조사 방법 : 빌트인 함수 isNaN을 사용한다.

         3| !=

             1/ 의미 : 부등 비교

             2/ 사례 : x != y

             3/ 설명 : x와 y의 값이 다름

         4| !==

             1/ 의미 : 불일치 비교

             2/ 사례 : x !== y

             3/ 설명 : x와 y의 값과 타입이 다름

     2} 대소 관계 비교 연산자

       (1) 반환값 : 피연산자의 크기를 비교하여 불리언 값을 반환한다.
   
       (2) 종류

         1| >

             1/ 예제 : x > y

             2/ 설명 : x가 y보다 크다.

         2| <

             1/ 예제 : x < y

             2/ 설명 : x가 y보다 작다.

         3| >=

             1/ 예제 : x >= y

             2/ 설명 : x가 y보다 같거나 크다.

         4| <=

             1/ 예제 : x <= y

             2/ 설명 : x가 y보다 같거나 크다.

   7] 삼항 조건 연산자

     1} 반환값 : 조건식의 평가 결과에 따라 반환할 값을 결정한다.

     2} 자바스크립트의 삼항 연산자 : 삼항 조건 연산자가 유일하다.

     3} 부수 효과 : 부수 효과는 없다.

     4} 삼항 조건 연산자 표현식
     
     -> 조건식 ? 조건식이 true일 떄 반환할 값 : 조건식이 false일 때 반환할 값

       (1) 조건식 : 물음표(?) 앞의 첫번째 피연산자, 불리언 타입의 값으로 평가될 표현식

         1| 조건식의 평가 결과가 불리언 값이 아닐 경우 : 불리언 값으로 암묵적 타입 변환된다.

         2| 조건식이 참인 경우 : 콜론(:) 앞의 두번째 피연산자가 평가되어 반환된다.

         3| 조건식이 거짓인 경우 : 콜론(:) 뒤의 세번째 피연산자가 평가되어 반환된다.

     5} 삼항 조건 연산자 표현식 : 값으로 평가할 수 있는 표현식
     -> 삼항 조건 연산자식은 다른 표현식의 일부가 될 수 있어 매우 유용하다.

   8] 논리 연산자(Logical Operator)
   
     1} 연산 : 우항과 좌항의 피연산자(부정 논리 연산자의 경우, 우항의 피연산자)를 논리 연산한다.

     2} 종류

       (1) ||

         1| 의미 : 논리합(OR)

       (2) &&

         1| 의미 : 논리곱(AND)

       (3) !

         1| 의미 : 부정(NOT)

     3} 논리 부정(!) 연산자

       (1) 반환값 : 언제나 불리언 값을 반환한다.

       (2) 피연산자 : 반드시 불리언 값일 필요는 없다.
       -> 피연산자가 불리언 값이 아니면 불리언 타입으로 암묵적 타입 변환된다.

     4} 논리합(||) 연산자와 논리곱(&&) 연산자

       (1) 연산 결과 : 일반적으로 불리언 값을 반환하지만 반드시 반환해야 하는 것은 아니다.

       (2) 반환 : 언제나 피연산자 중 어느 한쪽 값을 반환한다.

   9] 쉼표(,) 연산자

     1} 반환 : 왼쪽 피연산자부터 차례대로 피연산자를 평가 
     
     -> 마지막 피연산자의 평가가 끝나면 마지막 피연산자의 평가 결과를 반환한다.

   10] 그룹((...)) 연산자

     1} 평가 : 그룹 내의 표현식을 최우선으로 평가한다.

     2} 역할 : 연산자의 우선 순위를 1순위로 높일 수 있다.

   11] typeof 연산자

     1} 반환 : 자신의 뒤에 위치한 피연산자의 데이터 타입을 문자열로 반환한다.

     => 여기서 말하는 문자열 : 7개의 데이터 타입과 일치하지 않다.
     
     2} typeof 연산자

       (1) 반환 : 7가지 문자열("string", "number", "boolean", "undefined", "symbol", "object", "function"(함수)) 중 하나를 반환한다.
       -> "null"을 반환하는 경우는 없다.

       (2) null
   
         1| 연산 : null이 아닌 "object"를 반환한다는 것이다.
         -> 자바스크립트의 첫 번째 버전에서 이렇게 설계된 것을 현재의 버전에 반영하지 못하고 있기 때문이다.

         2| 확인 : typeof 연산자를 사용하지 않고 일치 연산자(===)를 사용하도록 한다.

       (3) 주의사항 : 선언하지 않은 식별자를 typeof 연산자로 연산해보면 ReferenceError가 발생하지 않고 "undefined"를 반환한다.

5. 제어문
   
   0] 들어가기에 앞서...

     1} 사용 : 주어진 조건에 따라 코드 블록을 실행(조건문)하거나 반복 실행(반복문)할 때

     2} 코드 실행 : 일반적으로 코드는 위에서 아래 방향으로 순차적으로 실행된다.
     -> 제어문은 코드의 실행 순서를 인위적으로 제어할 수 있다.

   1] 블록문(Block statement/Compound statement)

     1} 정의 : 0개 이상의 문들을 중괄호로 묶은 것
     (코드 블록 또는 블록이라고 부르기도 한다.)

     2} 자바스크립트 : 블록문을 하나의 단위로 취급한다.

     3} 사용 : 단독으로 사용할 수 있으나 일반적으로 제어문이나 함수 선언문 등에서 사용한다.

     4} 세미콜론 : 블록문은 세미콜론(;)을 붙이지 않는다.

   2] 조건문

     0} 들어가기에 앞서...

       (1) 정의 : 주어진 조건식의 평가 결과에 따라 코드 블록(블록문)의 실행을 결정한다.
   
       (2) 조건문과 표현식 : 조건문은 불리언 값으로 평가될 수 있는 표현식이다.

     1} if..else 문

       (1) 정의 : 주어진 조건식(불리언 값으로 평가될 수 있는 표현식)의 평가 결과(논리적 참, 거짓)에 따라 실행할 코드 블록을 결정한다.

       (2) 평가 결과

         1| 불리언 값인 경우
         
             1/참(true)일 경우 : if 문 다음의 코드 블록이 실행된다.

             2/ 거짓(false)일 경우 : else 문 다음의 코드 블록이 실행된다.

         2| 불리언 값이 아닌 경우 : 불리언 값으로 강제 변환되어 논리적 참, 거짓을 구별한다.

       (3) else if 문과 else 문

         1| else if 문 : 조건식을 추가하고 싶을 때 사용한다.

         2| 옵션으로 사용할 수도 있고 사용하지 않을 수도 있다.

         3| if 문과 else 문 : 2번 이상 사용할 수 없다.
         
         4| else if 문 : 여러 번 사용할 수도 있다.

       (4) 코드 블록 : 코드 블록 내의 문이 하나뿐이라면 중괄홀를 생략할 수 있다.
   
       (5) 대부분의 if...else 문은 연산자에서 살펴본 삼항 조건 연산자로 바꿔쓸 수 있다.

     2} switch 문

       (1) 정의 : switch 문의 표현식을 평가하여 그 값과 일치하는 표현식을 갖는 case 문으로 실행 순서를 이동시킨다.
   
       (2) case 문
   
         1|상황(case)을 의미하는 표현식을 지정하고 콜론으로 마친다. 

         2| 그 뒤에 실행할 문들을 위치시킨다.

         3| 표현식과 일치하는 표현식을 갖는다.

         4| case문이 없을 경우 : 실행 순서는 default문으로 이동한다.
         -> default문 : 옵션으로 사용할 수도 있고 사용하지 않을 수도 있다.

       (3) 표현식 : 불리언 값보다는 문자열, 숫자 값인 경우가 많다.

       (4) 사용 : 논리적 참, 거짓보다는 다양한 상황(case)에 따라 실행할 코드 블록을 결정할 때 사용한다.
   
       (5) break 문
   
         1| 코드 블록에서 탈출하는 역할을 수행한다.

         2| break 문이 없을 때 : case 문의 표현식과 일치하지 않더라도 실행 순서는 다음 case 문으로 연이어 이동한다.

         3| break 생략 : default 문에는 break 문을 생략하는 것이 일반적이다.
         -> default 문은 switch 문의 가장 마지막에 위치하므로 default 문의 실행이 종료하면 switch 문을 빠져나가므로 별도로 break 문이 필요없다.

       (6) if...else 문과 switch 문

         1| switch 문 : 다양한 키워드를 사용해야 하고 문법도 복잡하다.
         -> if...else 문으로 해결할 수 있다면 if...else 문을 사용하는 편이 좋다.

         2| 가독성 : if...else 문의 가독성 < switch 문의 가독성
         -> switch 문을 사용하는 편이 좋다.

   3] 반복문(Loop statement)

     0} 들어가기에 앞서...

       (1) 실행
         
         1| 주어진 조건식(conditional expression)의 평가 결과가 참인 경우 코드 블럭을 실행한다.

         2| 그 후 조건식을 다시 검사하여 여전히 참인 경우 코드 블록을 다시 실행한다.

         3| 이는 조건식이 거짓일 때까지 반복된다.

     1} for 문

       (1) 실행 : 조건식이 거짓으로 판별될 때까지 코드 블록을 반복 실행한다.

       (2) 가장 일반적으로 사용되는 반복문이다.

       (3) 실행 순서

         1| for 문을 실행하면 가장 먼저 초기화식이 실행된다.
         -> 초기화식은 단 한 번만 실행된다.

         2| 초기화식의 실행이 종료되면 조건식으로 실행 순서가 이동한다.

         3| 조건식의 평가 결과가 true인 경우 : 실행 순서가 코드 블록으로 이동하여 실행된다.
         -> 주의 사항 : 증감문으로 실행 순서가 이동하는 것이 아니라 코드 블록으로 실행 순서가 이동한다.

         4| 코드 블록의 실행이 종료되면 증감식으로 실행 순서가 이동한다.

         5| 증감식 실행이 종료되면 다시 조건식으로 실행 순서가 이동한다.
         -> 주의 사항 : 초기화식으로 실행 순서가 이동하는 것이 아니라 조건식으로 실행 순서가 이동한다.

         6| 조건식의 평가 결과가 false인 경우 : for 문의 실행이 종료된다.

       (4) 선언

         1| 옵션 : 초기화식, 조건식, 증감식은 반드시 사용할 필요는 없다.

         2| 어떤 식도 선언하지 않은 경우 : 무한 루프가 된다.

       (5) 중첩 : 중첩 가능

     2} while 문

       (1) 실행

         1| 주어진 조건식의 평가 결과가 불리언 값인 경우 
         
             1/ 주어진 조건식의 평가 결과가 참인 경우 : 코드 블록을 계속해서 반복 실행한다.

             2/ 주어진 조건식의 평가 결과가 거짓인 경우 : 실행을 종료한다.

         2| 주어진 조건식의 평가 결과가 불리언 값이 아닌 경우 : 불리언 값으로 강제 변환되어 논리적 참, 거짓을 구별한다.

       (2) 무한루프

         1| 주어진 조건식의 평가 결과가 언제나 참이면 무한루프가 된다.

         2| 탈출 : 코드 블록 탈출 조건을 if 문에 부여하고 break 문으로 코드 블록을 탈출한다.

     3} do...while 문

       (1) 평가 : 코드 블록을 실행하고 조건식을 평가한다.
       -> 코드 블록은 무조건 한 번 이상 실행된다.

   4] break 문

     1} 탈출
     
       (1) 레이블 문, 반복문(for, for...in, for...of, while, do...while) 또는 switch 문의 코드 블록을 탈출한다.

       (2) 레이블 문, 반복문, switch 문의 코드 블록 이외에 break 문을 사용할 경우 : SyntaxError(문법 에러)가 발생한다.

     2} 레이블 문(Label statement)

       (1) 정의 : 식별자가 붙은 문

       (2) 사용 목적 : 프로그램의 실행 순서를 제어하기 위해

       (3) 예시 : switch 문의 case 문과 default 문
   
       (4) 탈출 : break 문에 레이블 식별자를 지정한다.
   
       (5) 권장

         1| 중첩된 for 문을 외부로 탈출할 때 : 레이블 문은 유용하다. 

         2| 그 외의 경우 : 레이블 문은 일반적으로 권장하지 않는다.
         -> 가독성이 나빠지고 오류를 발생시킬 가능성이 높아지기 때문이다.
   
     3} 중첩된 for 문 
     
       (1) 중첩된 for 문의 내부 for 문에서 break 문을 실행하면 내부 for 문으로 진입한다.
       -> 이때 내부 for 문이 아닌 외부 for 문을 탈출하려면 레이블 문을 사용한다.

     4} 사용 : 레이블 문 뿐만이 아니라 반복문, switch 문에서도 사용할 수 있다.

     -> 이 경우에는 break 문에 레이블 식별자를 지정하지 않는다.

     5} break 문은 반복문을 더 이상 진행하지 않아도 될 때 불필요한 반복을 회피할 수 있어 유용하다.

   5] continue 문

     1} 실행
     
       (1) 반복문(for, for...in, for...of, while, do...while)의 코드 블록 실행을 현 지점에서 중단하고 반복문의 증감식으로 이동한다.

       (2) if 문 내에서 실행해야 할 코드

         1| if 문 내에서 실행해야 할 코드가 한 줄인 경우 : continue 문을 사용했을 때보다 간편하며 가독성도 좋다.

         2| if 문 내에서 실행해야 할 코드가 길 경우 : 들여쓰기가 한 단계 더 깊어지므로 continue 문을 사용하는 것이 가독성이 더 좋다.

     2} 탈출 : break 문처럼 반복문을 탈출하지는 않는다.        

6. 타입 변환과 단축 평가

   1] 타입 변환이란?

     1} 명시적 타입 변환(Explicit coercion) 또는 타입 캐스팅(Type casting)
     
       (1) 정의 : 개발자에 의해 의도적으로 값의 타입을 변환하는 것

       (2) 타입을 변경하겠다는 개발자의 의지가 코드에 명백히 드러난다.

     2} 암묵적 타입 변환(Implicit coercion) 또는 타입 강제 변환(Type coercion)
     
       (1) 정의 : 개발자의 의도와는 상관없이 자바스크립트 엔진에 의해 암묵적으로 타입이 자동 변환되는 것

       (2) 변수 값을 재할당해서 변경하는 것이 아니라 자바스크립트 엔진이 표현식을 에러 없이 평가하기 위해 기존 값을 바탕으로 새로운 타입의 값을 만들어 단 한 번 사용하고 버린다.

       (3) 드러나지 않게 타입이 자동 변환되기 때문에 타입을 변경하겠다는 개발의 의지가 코드에 명백히 나타나지 않는다.
       
       (4) 타입 변환된 값으로 표현식의 평가 : 어떻게 평가될 것인지 예측 가능해야 한다.
       -> 만약 예측하지 못하거나 예측한 내용이 결과와 일치하지 않다면 버그를 생산할 가능성이 높아진다.

   2] 암묵적 타입 변환

     0} 들어가기에 앞서...

       (1) 자바스크립트 엔진은 표현식을 평가할 때 문맥, 즉 컨텍스트(Context)에 고려하여 암묵적 타입 변환을 실행한다.
       -> 표현식을 평가할 때 문맥(context)에 부합하지 않는 다양한 상황이 발생할 수 있다.
       -> 자바스크립트 : 가급적 에러를 발생시키지 않도록 암묵적 타입 변환을 통해 표현식을 평가한다.

     1} 문자열 타입으로 변환

       (1) + 연산자 
   
         1| 피연산자 중 하나 이상이 문자열일 때 문자열 연결 연산자로 동작한다.

         2| 문자열 연결 연산자
             1/ 역할 : 문자열 값을 만드는 것이다.

             2/ 피연산자 : 문맥(context)상 문자열 타입이여야 한다.

       (2) 자바스크립트 엔진

         1| 문자열 연결 연산자 표현식을 평가하기 위해 문자열 연결 연산자의 피연산자 중에서 문자열 타입이 아닌 피연산자를 문자열 타입으로 암묵적 타입 변환한다.

         2| 연산자식의 피연산자(피연산자도 표현식이다.)만이 암묵적 타입 변환의 대상이 되는 것은 아니다.

         3| 표현식을 평가할 때, 문맥(context)에 부합하도록 암묵적 타입 변환을 실행한다.

     2} 숫자 타입으로 변환

       (1) 산술 연산자
   
         1| 역할 : 숫자 값을 만드는 것이다.

         2| 피연산자 : 문맥(context)상 숫자 타입이여야 한다.
      
       (2) 자바스크립트 엔진

         1| 산술 연산자 표현식을 평가하기 위해 산술 연산자의 피연산자 중에서 수자 타입이 아닌 피연산자를 숫자 타입으로 암묵적 타입 변환한다.

         2| 피연산자를 숫자 타입으로 변환할 수 없는 경우 : 산술 연산을 수행할 수 없으므로 NaN을 반환한다.

         3| 비교 연산자

             1/ 역할 : 불리언 값을 만드는 것이다.

             2/ 피연산자의 크기를 비교하므로 피연산자는 컨텍스트 상 숫자 타입이여야 한다.

             3/ 자바스크립트 엔진이 숫자 타입 아닌 값을 숫자 타입으로 암묵적 타입 변환을 수행할 때
       (3) 비교 연산자

         1| 역할 : 불리언 값을 만드는 것이다.

         2| 피연산자의 크기를 비교하므로 피연산자는 컨텍스트 상 숫자 타입이여야 한다.

         3| 자바스크립트 엔진

             1/ 숫자 타입 아닌 값을 숫자 타입으로 암묵적 타입 변환을 수행할 때
             -> + 단항 연산자 : 피연산자가 숫자 타입의 값이 아니면 숫자 타입의 값으로 암묵적 타입 변환을 수행한다.

         4| 변환

             1/ 0으로 변환 : 빈 문자열(''), 빈 배열([]), null, false

             2/ 1로 변환 : true

             3/ 주의 사항 : 객체와 빈 배열이 아닌 배열, undefined는 변환되지 않아 NaN이 된다는 것이다.

     3} 불리언 타입으로 변환

       (1) 자바스크립트 엔진

         1| 제어문의 조건식을 평가 결과를 불리언 타입으로 암묵적 타입 변환한다.

         2| 불리언 타입이 아닌 값을 Truthy 값(참으로 인식할 값) 또는 Falsy 값(거짓으로 인식할 값)으로 구분한다.
         -> Truthy 값은 true로, Falsy 값은 false로 변환된다.

         3| 불리언 값으로 평가되어야 할 컨텍스트에서 false로 평가되는 Falsy 값의 종류

             1/ false

             2/ undefined

             3/ null

             4/ 0, -0

             5/ NaN

             6/ '' (빈 문자열)

         4| 불리언 값으로 평가되어야 할 컨텍스트에서 true로 평가되는 Truthy 값 : Falsy 값 이외의 값

   3] 명시적 타입 변환

     1} 문자열 타입으로 변환

       (1) 문자열 타입이 아닌 값을 문자열 타입으로 변환하는 방법

         1| String 생성자 함수를 new 연산자 없이 호출하는 방법

         2| Object.prototype.toString 메소드를 사용하는 방법

         3| 문자열 연결 연산자를 이용하는 방법

     2} 숫자 타입으로 변환

       (1) 숫자 타입이 아닌 값을 숫자 타입으로 변환하는 방법

         1| Number 생성자 함수를 new 연산자 없이 호출하는 방법

         2| parselnt, parseFloat 함수를 사용하는 방법 (문자열만 변환 가능)

         3| 단항 연결 연산자를 이용하는 방법

         4| 산술 연산자를 이용하는 방법

     3} 불리언 타입으로 변환

       (1) 불리언 타입이 아닌 값을 불리언 타입으로 변환하는 방법

         1| Boolean 생성자 함수를 new 연산자 없이 호출하는 방법

         2| ! 부정 논리 연산자를 두 번 사용하는 방법

   4] 단축 평가(Short-Circuit evaluation)

     1} 논리곱 연산자(&&)

       (1) 반환 : 두 개의 피연산자가 모두 true로 평가될 때 true를 반환한다.

       (2) 진행 : 오른쪽에서 왼쪽으로 평가가 진행된다.

     2} 논리합 연산자(||)

       (1) 반환 : 두 개의 피연산자 중 하나만 true로 평가되어도 true를 반환한다.

       (2) 진행 : 오른쪽에서 왼쪽으로 평가가 진행된다.

     3} 정의 : 논리 평가를 결정한 피연산자의 평가 결과를 그대로 반환하는 것

     4} 단축 평가 표현식

       (1) true || anything

         1| 평가 결과 : true

       (2) false || anything

         1| 평가 결과 : anything

       (3) true && anything 

         1| 평가 결과 : anything

       (4) false && anything
   
         1| 평가 결과 : false

     5} 단축 평가가 유용하게 사용되는 상황

       (1) 객체가 null인지 확인하고 프로퍼티를 참조할 때

         1| 객체가 null인 경우 : 객체의 프로퍼티를 참조하면 타입 에러(TypeError)가 발생한다.
         -> 단축 평가를 사용하면 에러를 발생시키지 않는다.

         2| 함수의 인수(argument)를 초기화할 때 : 함수를 호출할 때 인수를 전달하지 않으면 매개변수는 undefined를 갖는다.
         -> 단축 평가를 사용하여 매개변수의 기본값을 설정하면 undefined로 인해 발생할 수 있는 에러를 방지할 수 있다.

7. 프로토타입
   1] 프로토타입 객체

     1} 자바스크립트 : 프로토타입 기반 객체지향 프로그래밍 언어
     -> 클래스 없이(Class-less)도 (ECMAScript 6에서 클래스가 추가되었다) 객체를 생성할 수 있다.

     2} 자바스크립트의 객체 생성 방법

       (1) 자바스크립트의 모든 객체 : 자신의 부모 역할을 담당하는 객체와 연결되어 있다.
       -> 마치 객체 지향의 상속 개념과 같이 부모 객체의 프로퍼티 또는 메소드를 상속받아 사용할 수 있게 한다.

       (2) Prototype(프로토타입) 객체 또는 Prototype(프로토타입) : 부모 객체
       -> 사용 목적 : 생성자 함수에 의해 생성된 각각의 객체에 공유 프로퍼티를 제공하기 위해

     3} ECMAScript spec

       (1) 자바스크립트의 모든 객체 : [[Prototype]]이라는 인터널 슬롯(internal slot)를 가진다.

       (2) [[Prototype]]의 값 : null 또는 객체이며 상속을 구현하는데 사용된다.
     
         1| 객체 : Prototype(프로토타입) 객체이다.

         2| __proto__accessor property로 접근할 수 있다.

         3| __proto__ 프로퍼티에 접근한 경우 : 내부적으로 Object.getPrototypeOf가 호출되어 프로토타입 객체를 반환한다.

       (3) [[Prototype]] 객체의 데이터 프로퍼티 : get 액세스를 위해 상속되어 자식 객체의 프로퍼티처럼 사용할 수 있다.
       -> set 액세스는 허용되지 않는다.

       (4) student 객체 : __proto__ 프로퍼티로 자신의 부모 객체(프로토타입 객체)인 Object.prototype을 가리키고 있다.

     4} 객체를 생성할 때 프로토타입은 결정된다.

     5} 결정된 프로토타입 객체 : 다른 임의의 객체로 변경할 수 있다.

     => 부모 객체인 프로토타입을 동적으로 변경할 수 있다는 것을 의미한다.
     -> 이러한 특징을 활용하여 객체의 상속을 구현할 수 있다.

   2] [[Prototype]] vs prototype 프로퍼티

     1} 모든 객체 : 자신의 프로토타입 객체를 가리키는 [[Prototype]] 인터널 슬롯(internal slot)을 갖으며 상속을 위해 사용된다.

     -> 함수 객체 : 일반 객체와는 달리 prototype 프로퍼티도 소유하게 된다.

     -> 주의 사항 : prototype 프로퍼티는 프로토타입 객체를 가리키는 [[Prototype]] 인터널 슬롯은 다르다는 것이다.

     2} [[Prototype]]

       (1) 함수를 포함한 모든 객체가 가지고 있는 인터널 슬롯이다.

       (2) 객체의 입장에서 자신의 부모 역할을 하는 프로토타입 객체를 가리키며 함수 객체의 경우 Function.prototype를 가리킨다.
   
     3} prototype 프로퍼티

       (1) 함수 객체만 가지고 있는 프로퍼티이다.

       (2) 함수 객체가 생성자로 사용될 때 이 함수를 통해 생성될 객체의 부모 역할을 하는 개체(프로토타입 객체)를 가리킨다.

   3] constructor 프로퍼티

     1} 정의 : 객체의 입장에서 자신을 생성한 객체를 가리킨다.

     2} 프로토타입 객체는 constructor 프로퍼티를 갖는다.

   4] Prototype chain

     0} 들어가기에 앞서...

       (1) 정의 : 특정 객체의 프로퍼티나 메소드에 접근하려고 할 때 해당 객체에 접근하려는 프로퍼티 또는 메소드가 없다면 [[Prototype]]이 가리키는 링크를 따라 자신의 부모 역할을 하는 프로토타입 객체의 프로퍼티나 메소드를 차례대로 검색하는 것

     1} 객체 리터럴 방식으로 생성된 객체의 프로토타입 체인

       (1) 객체 생성 방법

         1| 객체 리터럴

         2| 생성자 함수

         3| Object() 생성자 함수

       (2) 객체 리터럴 방식으로 생성된 객체 : 내장 함수(Built-in)인 Object() 생성자 함수로 객체를 생성하는 것을 단순화시킨 것
       
       (3) 자바스크립트 엔진 : 객체 리터럴로 객체를 생성하는 코드를 만나면 내부적으로 Object() 생성자 함수(함수이므로 prototype 프로퍼티가 있다.)를 사용하여 객체를 생성한다.

       (4) 객체 리터럴을 사용하여 객체를 생성한 경우, 그 객체의 프로토타입 객체는 Object.prototype이다.

     2} 생성자 함수로 생성된 객체의 프로토타입 체인

       (1) 생성자 함수 정의
       -> 생성자 함수로 객체를 생성하기 위해서는 우선 생성자 함수를 정의하여야 한다.

         1| 함수를 정의하는 방식 .

             1/ 함수선언식(Function declaration) : 자바스크립트 엔진이 내부적으로 기명 함수표현식으로 변환한다.
             -> 함수 리터럴 방식을 사용한다.

             2/ 함수표현식(Function expression) : 함수 리터럴 방식을 사용한다.

             3/ Function() 생성자 함수

         2| 3가지 함수를 정의하는 방식
         
             1/ Function() 생성자 함수를 통해 함수 객체를 생성한다.

             2/ 어떠한 방식으로 함수 객체를 생성하여도 모든 함수 객체의 prototype 객체는 Function.prototype이다.
             -> 생성자 함수도 함수 객체이므로 생성자 함수의 prototype 객체는 Function.prototype이다.

         3| 함수 리터럴 방식 : Function() 생성자 함수로 함수를 생성하는 것을 단순화시킨 것

       (2) 객체를 생성하는 방식

         1| 객체 리터럴

             1/ 엔진의 객체 생성 : Object() 생성자 함수

             2/ 인스턴스의 prototype 객체 : Object.prototype

         2| Object() 생성자 함수

             1/ 엔진의 객체 생성 : Object() 생성자 함수

             2/ 인스턴스 prototype 객체 : Object.prototype

         3| 생성자 함수

             1/ 엔진의 객체 생성 : 생성자 함수

             2/ 인스턴스의 prototype 객체 : 생성자 함수 이름.prototype

         4| foo 객체의 프로토타입 객체 Person.prototype 객체와 Person() 생성자 함수의 프로토타입 객체인 Fuction.prototype의 프로토타입 객체는 Object.prototype 객체이다.

         5| 프로토타입 체인의 종점(End of prototype chain) : Object.prototype 객체
         -> 모든 객체의 부모 객체인 Object.prototype 객체에서 프로토타입 체인이 끝나기 때문이다.

   5] 프로토타입 객체의 확장

     1} 프로토타입 객체 : 일반 객체와 같이 프로퍼티를 추가/삭제할 수 있다.
     -> 이렇게 추가/삭제된 프로퍼티는 즉시 프로토타입 체인에 반영된다.

     2} Person.prototype 객체 : 일반 객체와 같이 프로퍼티를 추가/삭제가 가능하다.

   6] 원시 타입(Primitive data type)의 확장

     1} 원시 타입은 객체가 아니므로 프로퍼티나 메소드를 가질 수 없다.
     -> String 객체의 프로토타입 객체 String.prototype에 메소드를 추가하면 원시 타입, 객체 모두 메소드를 사용할 수 있다.
     
     2} 원시 타입으로 프로퍼티나 메소드를 호출할 때 원시 타입과 연관된 객체로 일시적으로 변환되어 프로토타입 객체를 공유하게 된다.

     3} 프로토타입 객체(String.prototype, Number.prototype, Array.prototype 등 : Built-in object(내장 객체)의 Global objects(Standard Built-in Objects)인 String, Number, Array 객체 등이 가지고 있는 표준 메소드에 정의되어 있다.) 또한 Object.prototype를 프로토타입 체인에 의해 자신의 프로토타입 객체로 연결한다.

     4} 자바스크립트 : 표준 내장 객체의 프로토 객체에 개발자가 정의한 메소드의 추가를 허용한다.

   7] 프로토타입 객체의 변경

     1} 객체를 생성할 때 프로토타입은 결정된다.

     2} 결정된 프로토타입 객체는 다른 임의의 객체로 변경할 수 있다.

     => 부모 객체인 프로토타입을 동적으로 변경할 수 있다는 것을 의미한다.
     -> 객체의 상속을 구현할 수 있다.

     3} 프로토타입 객체 변경 시 발생하는 일

       (1) 프로토타입 객체 변경 시점 이전에 생성된 객체 기존 프로토타입 객체를  [[Prototype]]에 바인딩한다.

       (2) 프로토타입 객체 변경 시점 이후에 생성된 객체 변경된 프로토타입 객체를  [[Prototype]]에 바인딩한다.

       (3) 단계

         1| constructor 프로퍼티는 Person() 생성자 함수를 가리킨다.

         2| 프로토타입 객체 변경 후, Person() 생성자 함수의 Prototype 프로퍼티가 가리키는 프로토타입 객체를 일반 객체로 변경하면서 Person.prototype.constructor 프로퍼티도 삭제되었다. 
         -> 따라서 프로토타입 체인에 의해 bar.constructor의 값은 프로토타입 체이닝에 의해 Object.prototype.constructor 즉 Object() 생성자 함수가 된다.

   8] 프로토타입 체인 동작 조건

     1} 객체의 프로퍼티를 참조하는 경우, 해당 객체에 프로퍼티가 없는 경우, 프로토타입 체인이 동작한다.

     2} 객체의 프로퍼티에 값을 할당하는 경우 : 프로토타입 체인이 동작하지 않는다.

     -> 객체에 해당 프로퍼티가 있는 경우, 값을 재할당하고 해당 프로퍼티가 없는 경우는 해당 객체에 프로퍼티를 동적으로 추가하기 때문이다.
8. 스코프

   1] 스코프란?

     1} 정의 : 참조 대상 식별자(identifier, 변수, 함수의 이름과 같이 어떤 대상을 다른 대상과 구분하여 식별할 수 있는 유일한 이름)를 찾아내기 위한 규칙

     2} 식별자는 자신이 어디에서 선언됐는지에 의해 자신이 유효한(다른 코드가 자신을 참조할 수 있는) 범위를 갖는다.

     3} 스코프가 없는 경우 : 같은 식별자 이름은 충돌을 일으키므로 프로그램 전체에서 하나밖에 사용할 수 없다.

   2] 스코프의 구분

     1} 스코프의 구분

       (1) 전역 스코프(Global scope) : 코드 어디에서든지 참조할 수 있다.

       (2) 지역 스코프(Local scope or Function-level scope) : 함수 코드 블록이 만든 스코프로 함수 자신과 하위 함수에서만 참조할 수 있다.

     2} 변수

       (1) 전역 변수(Global variable) : 전역에서 선언된 변수이며 어디에든 참조할 수 있다.

       (2) 지역 변수(Local variable) : 지역(함수) 내에서 선언된 변수이며 그 지역과 그 지역의 하부 지역에서만 참조할 수 있다.

   3] 자바스크립트 스코프의 특징

     1} 함수 레벨 스코프(function-level scope) : 함수 코드 블록 내에서 선언된 변수는 함수 코드 블록 내에서만 유효하고 함수 외부에서는 유효하지 않다(참조할 수 없다)는 것

     -> 단, ECMAScript 6에서 도입된 let keyword를 사용하면 블록 레벨 스코프를 사용할 수 있다.

   4] 전역 스코프(Global scope)

     1} 선언 : 전역에 변수를 선언하면 이 변수는 어디서든지 참조할 수 있는 전역 스코프를 갖는 전역 변수가 된다.

     2} var 키워드로 선언한 전역 변수 : 전역 객체(Global Object) window의 프로퍼티

     3} 자바스크립트 : 특별한 시작점(Entry point)이 없어서 위 코드와 같이 전역에 변수나 함수를 선언하기 쉽다.

     -> 전역 변수를 남발하게 하는 문제를 야기시킨다.

     4} 사용 : 전역 변수의 사용은 변수 이름이 중복될 수 있고, 의도치 않은 재할당에 의한 상태 변화로 코드를 예측하기 어렵게 만드므로 사용을 억제하여야 한다.

   5] 비 블록 레벨 스코프(Non block-level scope) 

     1} 자바스크립트 : 변수 x가 코드 블록 내에서 선언되지만 블록 레벨 스코프를 사용하지 않으므로 함수 밖에서 선언된 변수는 코드 블록 내에서 선언되었다할지라도 모두 전역 스코프를 갖게 된다. 

     -> 변수 x : 전역 변수

   6] 함수 레벨 스코프(Function-level scope) 

     1} 자바스크립트 : 함수 레베 ㄹ스코프를 사용한다.

     -> 함수 내에서 선언된 매개변수와 변수는 함수 외부에서는 유효하지 않다.

     2} 전역변수 x와 지역변수 x가 중복 선언된 경우

       (1) 전역 영역과 지역 영역

         1| 전역 영역 : 전역변수만이 참조 가능하다.

         2| 지역 영역 : 전역과 지역 변수 모두 참조 가능하다.

       => 지역변수를 우선하여 참조한다.

       -> 전역변수의 값도 변경할 수 있다.

       (2) 내부 함수 : 전역변수는 물론 상위 함수에서 선언한 변수에 접근/변경이 가능하다.

     3} 중첩 스코프 : 가장 인접한 지역을 우선하여 참조한다.

   7] 렉시컬 스코프

     1} 정의 : 함수를 어디서 호출하는지가 아니라 어디에 선언하였는지에 따라 결정된다.

     2} 자바스크립트 : 렉시컬 스코프를 따르므로 함수를 선언한 시점에 상위 스코프가 결정된다.

     -> 함수를 어디에서 호출하였는지는 스코프 결정에 아무런 의미를 주지 않는다.

   8] 암묵적 전역(implicit global)

     1} 정의 : 선언하지 않은 식별자에 값을 할당하면 전역 객체의 프로퍼티가 되어 마치 전역 변수처럼 동작한다.

     2} 식별자는 변수가 아니다.
     
     -> 변수 선언 없이 단지 전여 객체의 프로퍼티로 추가되었을 뿐이다.

     -> 변수 호이스팅 X

     -> 식별자 : 단지 프로퍼티
     => delete 연산자로 삭제할 수 있다.

     -> 전역 변수 : 프로퍼티이지만 delete 연산자로 삭제할 수 없다.

   9] 최소한의 전역변수 사용

     1} 전역변수 사용을 최화하는 방법 중 하나 : 애플리케이션에서 전역변수 사용을 위해 전역변수 객체 하나를 만들어 사용하는 것

   10] 즉시실행함수를 이용한 전역변수 사용 억제

     1} 전역변수 사용을 억제하기 위해 즉시 실행 함수(IIFE, Immediately-Invoked Function Expression)를 사용할 수 있다.

     -> 이 방법을 사용하면 전역 변수를 만들지 않으므로 라이브러리 등에 자주 사용된다.

     -> 즉시 실행 함수 : 즉시 실행되고 그 후 전역에서 바로 사라진다.

## ECMAScript6

1. let, const와 블록 레벨 스코프

   0] 시작하기에 앞서...

     1} var 키워드로 선언된 변수의 특징

       (1) 함수 레벨 스코프(Function-level scope)

         1| 함수의 코드 블록만을 스코프로 인정한다.
         => 전역 함수 외부에서 생성한 변수는 모두 전역 변수이다.
         -> 전역 변수를 남발할 가능성을 높인다.

       (2) var 키워드 생략 허용

         1| 암묵적 전역 변수를 양산할 가능성이 크다.

       (3) 변수 중복 선언 허용

         1| 의도하지 않은 변수값의 변경이 일어날 가능성이 크다.

       (4) 변수 호이스팅

         1| 변수를 선언하기 이전에 참조할 수 있다.

   1] let

     1} 블록 레벨 스코프

       (1) 자바스크립트 : ES6는 블록 레벨 스코프를 따르는 변수를 선언하기 위해 let 키워드를 제공한다.

     2} 변수 중복 선언 금지

       (1) var 키워드 : 동일한 이름을 갖는 변수를 중복해서 선언할 수 있다.

       (2) let 키워드 : 동일한 이름을 갖는 변수를 중복해서 선언할 수 없다.
       -> 변수를 중복 선언하면 문법 에러(SyntaxError)가 발생한다.

     3} 호이스팅

       (1) let 키워드로 선언된 변수
   
         1| 선언문 이전에 참조하면 참조 에러(ReferenceError)가 발생한다.
         -> 스코프의 시작에서 변수의 선언까지 일시적 사각지대(Temporal Dead Zone; TDZ)에 빠지기 때문이다.

         2| 선언 단계와 초기화 단계가 분리되어 진행된다.
         -> 스코프에 변수를 등록(선언 단계)하지만 초기화 단계는 변수 선언문에 도달했을 때 이루어진다.

         3| 초기화 이전에 변수에 접근하려고 하는 경우 : 참조 에러(ReferenceError)가 발생한다.
         -> 변수가 아직 초기화되지 않았기 때문이다.
         -> 변수를 위한 메모리 공간이 아직 확보되지 않았기 때문이다.

         4| 스코프 시작 지점부터 초기화 시작 지점까지는 변수를 참조할 수 없다.

         5| 일시적 사각지대(Temporal Dead Zone; TDZ) : 스코프의 시작 지점부터 초기화 시작 지점까지의 구간

     4} 클로저

       (1) 자바스크립트의 함수 레벨 스코프로 인하여 for 루프의 초기화 식에 사용된 변수가 전역 스코프를 갖게 되어 발생하는 문제를 회하기 위해 클로저를 활용한 방법이다.
       -> ES6의 let 키워드를 for 루프의 초기화 식에 사용하면 클로저를 사용하지 않아도 위 코드와 동일한 동작을 한다.

     5} 전역 객체와 let

       (1) 전역 객체(Global Object)
   
         1| 정의
         
             1/모든 객체의 유일한 최상위 객체

             2/ window 객체 in Browser-side

             3/ global 객체 in Server-side(Node.js)

         2| var 키워드로 선언된 변수 : 전역 객체의 프로퍼티가 된다.

         3| let 키워드로 선언된 변수 : 보이지 않는 개념적인 블록 내에 존재하게 된다.

   2] const

     0} 들어가기에 앞서...

       (1) 사용 목적

         1| 상수(변하지 않는 값)를 위해

         2| 반드시 상수만을 위해 사용하지는 않는다.

     1} 선언과 초기화

       (1) let과 const
   
         1| let : 재할당이 자유롭다.

         2| const : 재할당이 금지된다.

       
       (2) 주의 사항 : const는 반드시 선언과 동시에 할당이 이루어져야 한다.
       -> 그렇지 않으면 문법 에러(SyntaxError)가 발생한다.

       (3) 스코프 : 블록 레벨 스코프를 갖는다.

     2} 상수

       (1) 사용해야 하는 이유 : 가독성과 유지보수의 편의를 위해 적극적으로 사용해야 한다.

     3} const와 객체

       (1) const 변수의 타입이 객체인 경우 : 객체에 대한 참조를 변경하지 못한다.
       => 객체의 프로퍼티는 보호되지 않는다.
       -> 재할당은 불가능하지만 할당된 객체의 내용(프로퍼티의 추가, 삭제, 프로퍼티 값의 변경)은 변경할 수 있다.

       (2) let과 const

         1| 객체 타입 변수 선언 : const를 사용하는 것이 좋다.

         2| 재할당(객체 타입 변수의 주소값을 변경) : let을 사용하는 것이 좋다.

   3] var vs. let vs. const

     1} ES6를 사용한다며 var 키워드는 사용하지 않는다.

     2} 재할당이 필요한 경우에 한정해 let 키워드를 사용한다.
     
     -> 변수의 스코프는 최대한 좁게 만든다.

     3} 변경이 발생하지 않는(재할당이 필요 없는 상수) 원시 값과 객체에는 const 키워드를 사용한다.

     -> const 키워드는 재할당을 금지하므로 var, let보다 안전하다.