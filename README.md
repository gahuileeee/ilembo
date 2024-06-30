# ilembo (일름보)


### 프로젝트 개요
 1) 프로젝트 주제 : 사내 커뮤니티, 일름보 
 2) 프로젝트 기간 : 2024-05-20 ~ 2024-06-30
 3) 배경 및 목적 : 사내 커뮤니티를 개설해 보았습니다. 일정을 관리하고, project를 생성하고, 실시간 채팅을 통해 업무 효율화를 목적으로 합니다.
 4) 주요기능 : 채팅, project 관리, 스케줄 관리, 게시판 기능
 5) 담당한 기능: 채팅, faq, (유저, 관리자) ,qna(유저, 관리자), 관리자 페이지 (게시판 관리, 유저 관리)
 6) 팀 구성 : 이가희 외 3인


### 사용한 기술
Spring Boot, Java, REACT, HTML5/CSS3/JavaScript, MyBaits, JPA, AWS, 

### 직접 구현한 기능 시현 영상 및 간단 설명

<p align="center" style="font-size: 22px; font-weight: bolder;">
  채팅방 개설 기능
  <details align="center">
  <summary>  채팅방을 개설하고, 이메일을 통해 가입된 다른 이들을 초대할 수 있습니다. </summary>
 <div>
다른 이들 초대 시, 입력값이 달라질 때마다 비동기 처리로 서버와 연동하여, </br> 그 글자에 해당하는 유저 이메일 목록들을 모두 불러오도록 하였습니다. </br>
  </br>
또한 채팅 기능을 구현하기 위해 chatRoom, chatUser, chat table을 만들어 관리하였습니다.</br>
:one: 채팅방을 만들면, 개설된 채팅방이 chatRoom에 저장됩니다.</br>
:two: chatUser에 채팅방에 포함된 유저 정보와 chatRoom 정보가 저장됩니다. </br>
:three: chat table에는 해당 채팅방에서 나눈 대화들이 저장됩니다. 
  </div>
</details>
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/54ce9a00-3694-4918-9fc4-275d0f467016"  width="600" height="400">
</p>


<p align="center" style="font-size: 22px; font-weight: bolder;">
실시간 알람 및 파일 보내기
</p>

<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/056ac682-5334-4ef0-8d4e-6e5edf9a04a5" width="600" height="400">
</p>


<p align="center" style="font-size: 22px; font-weight: bolder;">
DM (1대1 대화방)
</p>

<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/69475b7e-8488-4547-9903-4c8375c5fed9" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
질문 + faq 
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/bf8cd3d8-daf2-4f03-b016-33f9d49db4d0" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
관리자: 질문 답변 및 faq 수정
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/a71b7ef0-3066-44c3-bb9e-7955950b7c35" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
게시판 신고
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/86d05a70-7e64-412f-8ed3-97047c1e5c19" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
악성 유저 신고, 관리자 (게시판, 유저) 관리
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/246210b2-1a01-4d20-acb0-197d6cf02e57" width="600" height="400">
</p>

