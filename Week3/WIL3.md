기초 웹 스터디 3주차 - 2023년 3월 28일 화요일

오늘은 저번 시간에 배운 것을 간단히 복습하고 '깃허브와 협업'이라는 주제로 수업을 진행하셨다.

우선 복습 시간에 복습한 내용들을 적자면, 
git(소프트웨어)은 분기 나누기 및 합치기가 가느앟고 변화 추적(버전 관리)할 수 있는 시스템이다.

그리고 파일의 4가지 상태에는 untracked(추적X), unmodified(추적O, 변경X), modified, staged가 있다.

여기서 실제로 commit하면 unmodified 상태로 온다는 것을 복습했고, unmodified 상태에서 변경하고 싶으면 modified 상태로 가면 된다는 것을 확인했다.

이 다음에 적을 것은 사진과 함께해 조금은 간단하게 적으면 될 것 같다.

[스터디에서 설명을 들으며 그린 그림 - 복습](https://user-images.githubusercontent.com/127318008/228611067-842d2ea3-9a4f-45b2-9823-d68deb887de4.png)

위의 그림에 나와있듯이 내 컴퓨터에 working directory, staging area(변경 사항을 저장하는 공간) 및 local repository(.git repository)가 있다.

working directory에서 staging area로 add하면 staging area에 변경 사항들이 쌓인다. 여기서 add는 다음 commit에 추가할 변경 사항을 (staging area에) 넘긴다.

이제 staging area로 넘어온 변경 사항들을 local repository로 넘기는 것을 commit이라고 한다. commit은 staging area에 있는 너저분한(?) 변경 사항들을 깔끔하게 local repository에 넘겨주는 역할을 한다. 

이제 local repository에 있는 것을 공유하려면 공유할 서버 즉, remote repository가 필요하다.

이 remote repository의 대표적인 예가 우리(기초 웹 스터디 수강하시는 분들을 일컫는 말이겠지...?)가 조금이라도 잘 사용하기 위해 배우고 있는 github가 있다!

이 말의 의미는 remote repository에는 github만 있는 것이 아니라는 것이다.

다시 본론으로 돌아와서, local repository에 있는 변경 사항을 remote repository에 넘겨주는 것을 push라고 한다. 

여기서 remote repository에서 local repository의 변경 사항을 확인할 수 있는 방법이 두 가지가 있는데 변경 사항만 확인할 수 있는 fetch와 변경 사항 확인뿐만 아니라 최신 데이터를 복사하여 local Git에 가져올 수 있는(내가 설명하시는 모든 것을 받아적지는 못해 약간의 검색을 해보았다.) pull이 있다.

마지막으로 remote repository에서 working directory로 가 복제하는 clone도 있다.

여기까지가 저번 시간에 배운 것을 복습한 것이다.

이제 진짜 이번 시간에 배운 내용을 적어보자면, 

git branch라는 말을 저번 시간에 들어봤지만 오늘은 git branch이 실체에 대해 알아보자면 git branch의 실체는 가장 마지막 커밋을 가리키고 있는 포인터(무언가를 가리키는 것)이다. 

[스터디에서 설명을 들으며 그린 그림 - git branch](https://user-images.githubusercontent.com/127318008/228615528-a3bd61aa-b30e-4cdc-9ae0-6c84632dee9a.jpg)

위에 첨부한 그림과 함께 설명하자면 원래 가리키고 있던 포인터는 master이고 새로운 포인터는 testing이다.
HEAD는 내가 바라보고 있는 곳인 것이다.

그리고 branch와 관련된 명령어를 정리하면

1> git branch testing : testing이라는 브랜치를 만들라고 하는 의미의 명령어

2> git checkout testing : (기존 브랜치에서) testing 브랜치로 옮기라고 하는 의미의 명령어

3> git branch : 내가 가지고 있는 브랜치를 보여달라고 하는 의미의 명령어(이 명령어를 통해 내가 가지고 있는 브랜치를 확인할 수 있는 것이다!)

이렇게 된다고 알려주셨다.

그 다음에는 git merge(병합)에 대해 알려주셨다.

우선 첫 번째로 fast-forward가 있다. 
이것도 그림과 함께 보자면, 

[스터디에서 설명을 들으며 그린 그림 - git merge1](https://user-images.githubusercontent.com/127318008/228618753-e3d72607-3fdf-43d7-be13-6651aa507cca.jpg)

master와 test가 병합되어 c2를 가리키고 있던 master가 이제 c3를 가리키고 있는 test를 가리키고 있다. 

이것이 fast- forward라고 하셨고 또 다른 병합 방식을 보면,

[스터디에서 설명을 들으며 그린 그림 - git merge2](https://user-images.githubusercontent.com/127318008/228619860-0990ea64-0b37-4f51-b9cf-f9191f515148.jpg)

c2를 기준으로 해서 c3와 c4로 나뉘어져 있고 master라는 포인터는 c4를, test라는 포인터는 c5(c3에게 화살표를 하고 있는 것)를 가리키고 있다. 

여기서 master와 test가 병합하면 위에 그림에서 나왔듯이 c4와 c5를 가리키는 c6이라는 것이 새로 생겨서 이것을 master가 가리키게 된다. 