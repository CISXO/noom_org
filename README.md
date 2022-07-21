
# gitflow를 활용하여 webRTC git 협업

1.정의

a) GitFlow란 무엇인가?

	- GitFlow란
	개발자 여러명이서 작업하거나 프로젝트가 커져도 branch, merge를 깔끔하게 하기 위한
	 전략중 하나이다.
	(GitFlow / Github Flow / Trunk-based / Gitlab Flow 등이 있다. )

	
	- 

b)  GitFlow를 하기 위한 branch 종류

	- 1.master(main): 기준이 되는 브렌치
    2.develop: 개발 브랜치로 개발자들이 이 브랜치를 기준으로 각자 작업한 기능을 merge 한다.
    3.feature: 단위 기능을 개발하는 브랜치로 기능 개발이 완료되면 develop 브랜치에 merge 한다.
    4.release: 배포를 위해 master(main) 브랜치로 보내기 전에 먼저 검사를 하기 위한 브랜치이다.
    5.hotfix: master 브랜치로 배포를 했는데 버그가 생겼을 때 긴급하게 수정하는 브랜치이다.

c)  GitFlow 활용 방법
	

	-main에 있는 version0.9 버전에 신기능을 만들 때 main에서
	직접 짜게 되면 위험할 수 있으므로 main에 develop branch를
	만들어 복제하여 안전하게 개발할 수 있다.
	develop에 직접 push하지 않고 feature 브랜치를 만들어
	신기능을 개발하고 잘 실행 된다면 develop에 merge하는
	식으로 진행된다. develop이 완성되엇다 싶을 때 release
	라는 임시 브렌치를 만든다. version1.0을 만들기 전에
	여러가지 테스트를 하거나 고치고 완성이 되었을 때 main에
	merge하는 방식이다. release 단계를 develop에도 
	브렌치를 해주어 다음 version에서도 이용할 수 있게 해준다.
	급하게 버그가 생겼을 때 hotfix 브랜치를 만들어 main에 합친다.

<p align="center">
<img src= "https://user-images.githubusercontent.com/99077276/180276390-e205d415-8064-4e49-ab72-65bd389f3ac5.png">
</p>

d) gitflow 장점과 단점

	-장점: 안정적으로 개발과 출시를 할 수 있다.

	--단점: 너무 많은 수의 브렌치를 요구한다. 브랜치를 복잡하게 구성한다고 해서
	 버전 관리를 더 안정적으로 할 수 있는 것은 아니다. 적합한 환경이 있으므로
	  유연하게 branch 전략을 이용해야 한다.



d) Git을 이용한 협업 진행 과정

	-최대한 gitflow 방식을 이용하여 진행하려 하였으나 급하게 진행하다 보니 branch
	를 master, develop, feature 3가지를 사용했다.
	
	-webRTC 프로그램을 fork 하여 기능및 추가를 하는 방식으로 진행하였고 오픈 소스는
	 https://github.com/nomadcoders/noom 이다. organization은 나의
	  계정으로 생성하였고 organization에 noom을 레포에 추가하였다.
	개발을 진행하는데 있어서 팀원의 pull request를 merge하는데 있어
	conflict가 생긴 문제를 해결하지 못해 나의 레포에서 버전을 merge하고 
	pull request를 진행했다.

	나와 팀원은 처음으로 팀프로젝트를 진행하다 보니 난감했고 웹개발 경험이 거의 없다보니 
	자료를 찾고 공부하는 것에 시간을 많이 들였다. 너무 짧은 시간동안 진행하다 보니 백앤드
	 쪽은 거의 건들지 못했고 html과 비슷한 pug와 css를 이용해 프론트를 진행한것이 많았다.

* 팀 프로젝트 레포: < https://github.com/20220719-JoJeongHyeon/noom >
* 나의 줌 레포: < https://github.com/CISXO/noom_org >
* 팀원 레포: < https://github.com/h2k9971/noom_org >

<p align="center">
<img src= "https://user-images.githubusercontent.com/99077276/180314722-420c59a3-c36d-4999-aadc-6086c5d7bf5f.png">
</p>



e) 최종 개발 상태

## 오픈소스로 받아온 상태

<p align="center">
<img src= "https://user-images.githubusercontent.com/99077276/180315725-5020bd43-15a1-4681-890b-a8e7f94fd203.png">
</p>

## 개발 상태

<p align="center">
<img src= "https://user-images.githubusercontent.com/99077276/180315332-67256dae-4356-4180-a75c-cb4aa454bee1.png">
</p>

