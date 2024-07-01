# ilembo (일름보)


### 프로젝트 개요
 1) 프로젝트 주제 : 사내 커뮤니티, 일름보 
 2) 프로젝트 기간 : 2024-05-20 ~ 2024-06-30
 3) 배경 및 목적 : 사내 커뮤니티를 개설해 보았습니다. 일정을 관리하고, project를 생성하고, 실시간 채팅을 통해 업무 효율화를 목적으로 합니다.
 4) 주요기능 : 채팅, project 관리, 스케줄 관리, 게시판 기능
 5) 담당한 기능: 채팅, faq, (유저, 관리자) ,qna(유저, 관리자), 관리자 페이지 (게시판 관리, 유저 관리)
 6) 팀 구성 : 이가희 외 3인
7) [프론트 깃헙 (react) 이동](https://github.com/gahuileeee/ilemboFront), [백엔드 깃헙 (Spring boot) 이동](https://github.com/gahuileeee/ilemboBack)


### 사용한 기술
Spring Boot, Java, REACT, HTML5/CSS3/JavaScript, MyBaits, JPA, AWS 

### ERD
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/a78d87e1-4f03-4327-a17a-156332b4921e" width="600px">


### 직접 구현한 기능 시현 영상 및 간단 설명

<p align="center" style="font-size: 22px; font-weight: bolder;">
  채팅방 개설 기능
  <details align="center">
  <summary>  채팅방을 개설하고, 이메일을 통해 가입된 다른 이들을 초대할 수 있습니다. </summary>
 <div>
  </br>
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

   <details align="center">
  <summary> 메인화면에서도 알람이 실시간으로 뜨며(종모양에 숫자가 변함), 실시간 파일도 보낼 수 있습니다. </summary>
 <div>
  </br>
  실시간 알람을 위해 모든 페이지에 socket을 참조하도록 하였습니다. </br>
  </br>
  :one: 파일 전송을 위해, 먼저 react dropzone을 활용해 썸네일을 구현했습니다. </br>
  :two: 채팅 전송시에 파일도 함께 보내면, back에서 파일을 저장하고, 저장한 fileName을 보내도록 구현하였습니다. 
  </div>
</details>
</p>

<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/056ac682-5334-4ef0-8d4e-6e5edf9a04a5" width="600" height="400">
</p>


<p align="center" style="font-size: 22px; font-weight: bolder;">
DM (1대1 대화방)

 <details align="center">
  <summary> 프라이빗한, 1대1 대화방 기능도 있습니다.</summary>
 <div>
  </br>
  사람 초대 기능 구현과 같이, 이메일을 통해 1대1 대화 기능을 구현하였습니다. </br>
  처음엔 단순 이름으로 대화방을 개설했더니, 동명이인의 경우 문제가 있다는걸 자각했습니다. </br>
  따라서, 아이디로 대화방을 개설하는 것으로 문제를 해결했습니다. </br>
  </div>
</details>

</p>

<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/69475b7e-8488-4547-9903-4c8375c5fed9" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
질문 + faq 
<details align="center">
  <summary>사용자 질문하기 (qna) 기능과 자주 묻는 질문(faq) 구현 하였습니다. </summary>
 <div>
  </br>
  사용자가 질문하면 '답변전'상태로 db에 저장됩니다. </br>
  자주 묻는 질문의 경우 아코디언 형식으로 구현하여 사용자가 더욱 보기 좋게 하였습니다. 
  </div>
</details>

</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/bf8cd3d8-daf2-4f03-b016-33f9d49db4d0" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
관리자: 질문 답변 및 faq 수정
  <details align="center">
  <summary> 관리자만이 할 수 있으며, 사용자 qna 및 faq를 관리할 수 있습니다. </summary>
 <div>
  </br>
  메인 화면에서 관리자 등급만이 관리자(톱니바퀴) 아이콘이 노출되도록 하였습니다. </br>
  관리자가 답변을 할 경우 바로 '답변 완료'로 db 상태값을 변경하였습니다. </br>
  faq의 경우 + 버튼을 눌러 추가할 수 있으며 기존 faq를 삭제할 수도 있습니다. </br>
  </div>
</details>
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/a71b7ef0-3066-44c3-bb9e-7955950b7c35" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
게시판 신고
    <details align="center">
  <summary> 악성 게시글 신고하기 기능입니다. </summary>
 <div>
  </br>
  악성 게시글을 본 경우 신고를 할 수 있습니다. </br>
  이때, report table에 신고 당한 게시물, 신고 사유, 신고한 유저 정보가 insert 되며 </br>
  해당 게시글(article table)에 report 값이 ++ 됩니다.
  </div>
</details>
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/86d05a70-7e64-412f-8ed3-97047c1e5c19" width="600" height="400">
</p>

<p align="center" style="font-size: 22px; font-weight: bolder;">
악성 유저 신고, 관리자 (게시판, 유저) 관리
    <details align="center">
  <summary> 악성 유저도 신고가 가능하며, 관리자가 이를 관리(게시글 숨기기, 유저 정지하기)할 수 있습니다. </summary>
 <div>
  </br>
  해당 유저/게시글을 누르면 신고 사유를 볼 수 있고 이에 따라 관리자가 제재를 결정할 수 있습니다. </br>
  제재를 당하면 유저의 경우 15일 정지, 게시글의 경우 숨김 처리됩니다. </br>
  orderBy를 이용해, 신고가 높은 순, 낮은 순으로 정렬기능도 구현하였습니다.
  </div>
</details>
</p>
<p align="center"> 
<img src="https://github.com/gahuileeee/ilembo/assets/141610403/246210b2-1a01-4d20-acb0-197d6cf02e57" width="600" height="400">
</p>


### 프로젝트를 통해 학습하게 된 내용
✏️ React의 여러 hook (useState, useEffect, useRef 등) 들을 직접 사용해보며 어떨 때 사용하고, 어떻게 쓰는지를 알게 되었습니다. </br>
✏️ DropZone에 대해 알게 되었습니다. 그리고 기존의 dropZone API를 사용해보며 api 사용 능력이 향상되었습니다. </br>
✏️ Socket 통신을 이해하게 되었습니다. 또한 파일 전송과 일반 문자 전송을 어떻게 구분할 지 생각하면서 사고력이 증가되었습니다. </br>
 <span> </span>그리고 실시간 알람을 모든 페이지에서 확인 할 수 있도록, socket을 생성하고, 이를 모든 페이지에 주입시켜 하나의 socket으로 여러 곳에서 쓸 수 있도록 해 보았습니다. </br>
✏️ 처음으로 back과 front를 다르게 관리하여 Restful API 통신에 대해 더 잘 이해하게 되었습니다. </br>
  또한, front에서 back으로 요청을 보낼 때, 현재 주소가 localhost...라면 back도 localhost..로 보내고, 아니라면 서버 back 주소로 보내는 method를 구현하여 </br>
  back 과 front 서버가 다를 때의 요청 주소 관리 요령을 체득했습니다.

  
