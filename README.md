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