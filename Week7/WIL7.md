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

사실 이번 주 과제는 수업 내용도 거의 못 듣고 하는 것(1시간 동안 기침함...)이라 많이 어려웠다.

이제 감기도 거의 다 나았으니(기침도 많이 없어졌다!) 제대로 수업 듣고 잘해보았으면 좋겠다...

이번 주 WIL은 여기서 마치겠다.