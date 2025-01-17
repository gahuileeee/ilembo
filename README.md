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


### 제가 직접 구현한 기능에 대한 시현 영상 및 간단 설명
*담당한 기능에 대해 ERD , Back, Front 모두 하였습니다. 

<p align="center" style="font-size: 22px; font-weight: bolder;">
  채팅방 개설 기능
  <details align="center">
  <summary>  채팅방을 개설하고, 이메일을 통해 가입된 다른 이들을 초대할 수 있습니다 [클릭] </summary>
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
  <summary> 메인화면에서도 알람이 실시간으로 뜨며(종모양에 숫자가 변함), 실시간 파일도 보낼 수 있습니다  [클릭] </summary>
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
  <summary> 프라이빗한, 1대1 대화방 기능도 있습니다  [클릭]]</summary>
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
  <summary>사용자 질문하기 (qna) 기능과 자주 묻는 질문(faq) 구현 하였습니다  [클릭]</summary>
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
  <summary> 관리자만이 할 수 있으며, 사용자 qna 및 faq를 관리할 수 있습니다  [클릭]</summary>
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
  <summary> 악성 게시글 신고하기 기능입니다  [클릭]</summary>
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
  <summary> 악성 유저도 신고가 가능하며, 관리자가 이를 관리(게시글 숨기기, 유저 정지하기)할 수 있습니다  [클릭]</summary>
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
✏️ React의 여러 hook (useState, useEffect, useRef 등) 들을 직접 사용해보며 사용 목적과 사용 방법을 알게 되었습니다. </br>
    <details >
  <summary> 학습한 react hook 내용 (사용 목적, 사용 방법)  [클릭]</summary>
 <div>
  :one: useState : 컴포넌트의 상태값을 선언하고 관리하는 hook입니다. const [count, setCount] = useState(0); 식으로 초기 값을 0으로 선언할 수도 있고, const [list, setList] = useState([])로 빈 배열 형태로 선언할 수도 있습니다. 혹은 const [user, setUser ] = useState({uid:'', name:"", age:0}) 이렇게 원하는 빈 객체 값으로 선언할 수도 있습니다.
  <br>
  <br>
  
  :two: useEffect : 의존성 배열을 이용해, 상태값이 업데이트 될 때마다 실행할 수 있습니다. 
<br>
   useEffect(() => {
    console.log("state name update...");
  }, [name]);
  <br>
  이렇게 하면 name의 값이 변경될 때마다 console.log 가 실행됩니다. <br>
  <br>
  
  :three: useRef : 컴포넌트에 참조값을 설정하고, 참조하기  위한 hook 입니다. <br>
  const refUid =useRef(); 로 ref 를 생성하고 <input type="text" name="uid" ref={refUid}/> 이렇게 하면 입력한 값을 참조할 수 있습니다.  <br>
  <br>
  
  :four: useSearchParams :스프링의 @requestParam 어노테이션처럼 url의 쿼리 매개변수에 접근할 때 사용합니다. <br>
  예를 들어   let [searchParams, setSearchParams] = useSearchParams();
  let name = searchParams.get('name'); 이렇게 하여 url 쿼리 매개변수에서 name 의 값을 얻을 수 있습니다. <br>
  <br>
  
  :five: useLocation :현재 url에 대한 정보에 접근하기 위한 hook입니다. 
  <br>
<br>
  :six: useNavigate : 자바스크립트의 window.location.href  와 비슷한 역할을 합니다. 이 프로젝트에서는 사용자가 로그인을 하지 않았는데 채팅으로 접속을 시도 할 경우 alert("로그인 후 사용해주세요.") 이후 useNavigate를 이용해 login 화면으로 이동시킬 때 사용하였습니다. <br>
  <hr>
  </div>
</details>
</br>


✏️ DropZone에 대해 알게 되었습니다. 그리고 기존의 dropZone 라이브러리를 사용해보며 라이브러리 사용 능력이 향상되었습니다. </br>
  <details>
  <summary> 학습한 DropZone 라이브러리 응용 사용법 [클릭]</summary>
 <div>
 :one: npm install react-dropzone 로 우선 설치를 합니다.
  <br>
 :two: 라이브러리에 있는 예시 코드를 분석하여 프로젝트에 우선 적용을 하였습니다. (라이브러리엔 이미지를 드래그하면, 썸네일을 노출시키는 것만 구현되어 있었음)
  <br>
  :three: 이후, 파일을 담을 빈 객체를 생성하였습니다. 그리고 파일이 업로드 되면 빈 객체에 저장하고, 썸네일을 띄워 전송 버튼을 누르면 back으로 파일 객체가 전송되도록 하였습니다.
  <br>
  :four: 삭제 기능을 구현하기 위해 x 버튼을 누르면, 파일 객체를 비우고, 썸네일 div에도 값을 null로 수정해, 기존 라이브러리를 이용해 삭제 기능을 완성하였습니다.
  <hr>
  </div>
  </details>

</br>
✏️ Socket 통신을 이해하게 되었습니다. 또한 파일 전송과 일반 문자 전송을 어떻게 구분할 지 생각하면서 사고력이 증가되었습니다. </br>
 그리고 실시간 알람을 모든 페이지에서 확인 할 수 있도록, socket을 생성하고, 이를 모든 페이지에 주입시켜 하나의 socket으로 여러 곳에서 사용가능 하도록 구현하는 법을 알 수 있었습니다. </br>
 <br>
     <details >
  <summary> 학습한 socket 통신 내용 및 구현 과정 [클릭]</summary>
 <div>
  </br>
webSocket이란 서버와 클라이언트 간의 메시지 교환을 위한 통신규약을 말합니다. 양방향 통신이 가능하며, http와 다르게 지속적 연결을 수립하여 실시간 데이터 처리를 요하는 작업에 유용하게 쓰입니다. 
  <p font-weight="bold"> 구현한 과정 </p>
  :one: implementation 'org.springframework.boot:spring-boot-starter-websocket' 로 스프링에 의존성을 주입합니다. <br>
  :two:  TextWebSocketHandler를 상속하는 SocketHandler class를 작성하여, 소켓 연결, 소켓 종료, 메시지 발송 메소드를 작성합니다.
  :three: WebSocketConfigurer를 구현한 WebSocketConfig class를 작성합니다. 요청과 생성한 handler를 연결시켜 줍니다. <br>
  :three: 프론트(react)에서 ws = new WebSocket("ws://요청 주소")로 소켓을 생성합니다. <br> 
    <p font-weight="bold"> 소켓을 모든 페이지에 사용할 수 있도록 한 방법 </p>
  우선 모든 페이지를 components화 시켜, Header도 컴포넌트화 시켰습니다.<br>
  그런 다음 WebSocket을 생성하는 method를 만들고, 이를 header에서 사용해 websocket을 모든 페이지에서 사용 가능하도록 하였습니다. 
    <details >
  <summary>createWebSocket method 코드가 궁금하시다면 클릭해주세요! [클릭]</summary>
 <div>
  const createWebSocket = () => { <br>
  const ws =  new WebSocket(`wss://api.illrreumbow.store/community/chattings`); <br>
  ws.onopen = () => { <br>
    console.log('WebSocket connection succeed');<br>
  }; <br>
  return ws; <br>
}; <br>

export default createWebSocket;
  </div>
</details>

<hr>
  </div>
</details>

 </br>
✏️ 처음으로 back과 front를 다르게 관리하여 Restful API 통신에 대해 더 잘 이해하게 되었습니다. </br>
  또한, front에서 back으로 요청을 보낼 때, 현재 주소가 localhost...라면 back도 localhost..로 보내고, 아니라면 서버 back 주소로 보내는 method를 구현하여 back 과 front 서버가 다를 때의 요청 주소 관리 요령을 체득했습니다.<br>
  <br>
     <details >
  <summary>체득한 back과 front 서버가 다를 때의 front에서 back으로 요청 주소 관리 요령 [클릭]</summary>
 <div>
 프로젝트 초기에는 axios.get("http://localhost:8080..."식으로 하드 코딩 했습니다. <br>
그런데 그렇게 하니 배포를 할 때, 요청 주소가 localhost:8080으로 보내져 문제가 생겼고, 이를 해결하기 위해 완성된 api의 경우에만 http://배포된서버주소/ 로 요청을 보내도록 하였습니다. <br>
하지만, 이 방법은 요청 주소를 바꾸는걸 잊거나 틀리게 타이핑하는 등의 상황으로 계속 문제가 생겼습니다. <br>
  따라서 근본적으로 해결해야 함의 필요성을 깨닫고 다음과 같이 해결하였습니다. <br>
  :one: .env 파일에 LOCAL과 개발 주소를 작성했습니다. (ex REACT_APP_BACKEND_URL_LOCAL=http://localhost:8080/community ,
REACT_APP_BACKEND_URL_PROD=https://api.illrreumbow.store/community)<br>
:two:  window.location.hostname를 이용해 현재 환경이 local인지 배포 서버 환경인지를 구분하고, 이에 따라 요청 주소를 다르게 할당하는 method를 생성했습니다.
   <details >
  <summary>코드가 궁금하다면 클릭 해 주세요 [클릭]</summary>
 <div>
  import React from 'react' <br>

const isLocalhost = window.location.hostname === "localhost"; <br>
const url = { <br>
    backendUrl: isLocalhost <br>
        ? process.env.REACT_APP_BACKEND_URL_LOCAL <br>
        : process.env.REACT_APP_BACKEND_URL_PROD  <br>
}; <br>


export default url; <br>
  </div>
</details>
:three: 이를 axios.get(`${url.backendUrl}/...`) 처럼 이용하여 간단하게 문제를 해결하였습니다.
  </div>
</details>
  

  
