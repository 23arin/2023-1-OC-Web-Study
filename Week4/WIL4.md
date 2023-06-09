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
7. <'td'> : 이 tag 안에 있는 내용은 테이블에서 하나의 셀(cell)을 의미한다.
(여기서 말하는 셀(cell)은 우리가 흔히 알고 있는 사각형 칸을 의미한다.)
8. <'th'> : 이 tag 안에 있는 내용은 테이블에서 행, 열의 머리말을 의미한다.(다른 말로 헤더 셀(header cell)이다. 그리고 헤더 셀은 기본적으로 가운데로 정렬되고 굵은 글씨로 나타난다!)
9.  <'input'> : 이 tag는 사용자로부터 입력을 받을 수 있는 입력 필드(input field)를 정의한다. type에 따라 다른 입력값을 취하며 다양한 속성이 있다는 특징이 있다. (다양한 속성 때문에 input이 강력하다!)