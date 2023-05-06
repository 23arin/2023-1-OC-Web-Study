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