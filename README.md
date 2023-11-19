# BOGEOM
<img width="293" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/7ca41323-31e6-47dc-92d7-1f3403a22b89">

### Summary
"오프라인 상점에서 간편하게 상품 정보, 리뷰, 온라인 가격을 검색할 수 없을까?"라고 자주 생각했습니다. <br/>
쇼핑 중에 상품을 일일이 타자로 검색하기에는 많은 시간 비용이 들고, 신뢰성 있는 정보를 찾기 어려웠습니다. <br/>
<br/>
그래서 빠르고 현명한 소비를 하고 싶은 소비자의 욕구를 충족시키기 위해, <br/>
**가격표를 촬영하는 것만으로도 상품에 대한 정보 및 리뷰를 한 번에 확인할 수 있는 ‘보검’ 서비스**를 만들었습니다.

## 사용 기술
- Spring Boot
-  MySQL
-  JPA
-  JPQL
-  Thymeleaf
-  Lombok
-  Proxy
-  REST API

## Collaborator
- **최우진(팀장)** : iOS, AI, Chatbot
- **김명지** : Server, DB
- **최은성** : Server, DB


## 프로젝트 전체 구조
![image](https://github.com/Starlight258/Bogeom_Server/assets/78211281/fbb350ac-294e-4ab7-b038-cda62465660c)

- **모바일 애플리케이션**: 사용자가 실시간으로 가격표 객체 탐지가 되는 카메라를 통해 상품의 가격표를 촬영하면 인식된 가격표 이미지가 웹 서버로 전송된다. 
- **웹 서버**: 사용자로부터 전송받은 이미지를 다시 인공지능 서버로 전송한다. 
- **인공지능 서버**: 광학 문자 인식, Parsing, Search Server 과정을 거쳐 웹 서버에게 상품명 및 가격을 제공한다. 
- **웹 서버**: 상품명에 해당하는 데이터를 데이터베이스로부터 찾아 사용자 모바일에 전송한다. 
- **크롤링 서버**: 일정 주기마다 상품 가격을 수집하여 데이터베이스에 업데이트한다. 
- **Chat 서버**: 사용자가 상품 추천 메시지를 보내면 Prompt Engineering 및 ChatGPT를 활용하여 모바일에 응답 메시지를 보낸다.

</br>

## 메인 서버 및 데이터베이스
### MVC Architecture
<img width="620" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/8e5c7306-497f-4697-a3d1-924f6d384b59">


### Database Class Diagram
<img width="620" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/e6cd575e-1c08-4574-9435-6b9fc9538f37">

### Database ER Diagram
<img width="620" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/20ce0fa0-66a0-4372-a2cd-096130a3e8b1">

### Database Entity
<img width="571" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/e727c237-596f-4fb2-8f44-ec883235a061">

### Behavior Diagram
<img width="607" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/9ea92849-ab19-4eb1-a6b3-8e311557eb46">
<img width="607" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/8fbfecf6-a66c-4e3a-9212-10fcc6e0ebd3">
<img width="607" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/e3dcfd24-9781-4880-8d6e-d3abcfd67846">


## 객체 탐지 모델
### 학습시킨 YOLOv5s 모델
<img width="593" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/947cde2f-03e0-400e-ad3e-78ffca1117ea">

### 모바일(iOS)에 적용
<img width="593" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/b17f7027-f4e0-47f4-b4ac-d1d078d6a9a1">

## 모바일 구현
<img width="593" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/ab148b35-f819-49e6-b281-fdfeac808688">
<img width="593" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/4943144d-2fa6-4703-a8ac-bed544949138">

## AI, Search Server, Parser
<img width="604" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/a198b447-0709-4b50-b8c8-a215e4d4204a">

### Parsing Rule
<img width="596" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/9c572176-a99d-4ea4-9074-71d3ffd05e90">

## 모바일 UI 디자인
<img width="617" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/76cb80ec-a31c-4938-8215-39f8fbb33487">
<img width="617" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/1b7d0530-3e33-4fbe-bac6-18a7e56db03f">
<img width="593" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/69259834-1112-4b8d-abe9-77083cbfa5e1">

## 연구 성과
<img width="604" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/39f5cfe5-a365-4f91-bb86-c2462b0198af">
<img width="604" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/3576d69e-2207-41da-9411-7453cfc0b3f7">

### 수상 내역
<img width="580" alt="image" src="https://github.com/Starlight258/Bogeom/assets/78211281/644e8996-8b76-43eb-af8a-7f9dde877b2b">



