## Overview

 <br/>

# **엘리트 옥션**
<br/>
⭐️ 자신의 중고 물품을 경매형식으로 판매하는 사이트

 <br/>  <br/>

📆 프로젝트 기간: 2023. 12. 26 ~ 2024. 01. 03 

🔗 [배포 링크](https://elite-auction-snowy.vercel.app/)

<br/>

## 팀 소개
이동탁 : https://tak-web-front.tistory.com/ <br/>
김은비 : https://velog.io/@eunbi/posts <br/>
이다원 : https://velog.io/@dawnrose <br/>
권경열 : https://velog.io/@yeol10 <br/>

 <br/>

## 프로젝트 소개 <br/>
```
저희 프로젝트는 사용자들에게 손쉽게 원하는 물품을 경매할 수 있도록 하는 사이트입니다. 판매자는 원하는 물품을 등록하면서 상세한 정보, 경매 기간, 품질, 배송 방법, 입찰 하한가 등을 설정할 수 있습니다. 구매자는 경매 게시글에 편리하게 입찰가를 제시하며 이는 하한가보다 높아야 합니다. 경매 기간이 시작되기 전과 종료된 후에는 입찰이 불가능하며, 경매가 진행되는 동안 남은 시간이 실시간으로 표시됩니다.
회원 가입 및 로그인 후에는 사용자들이 상품을 등록하고 찜하기를 할 수 있으며, 궁금한 점을 질문하고 답변할 수 있는 기능을 제공합니다. 프로필 페이지에서는 등록한 게시물을 관리하고 수정할 수 있으며, 찜한 목록도 관리할 수 있습니다.
프로필 수정 탭에서는 회원 정보를 자유롭게 변경할 수 있고 홈화면을 제외한 모든 기능은 정상적인 회원 정보가 등록된 로그인 상태에서만 이용 가능합니다.
```
<br />

---
## Stack <br/>

### Enviroment   <br/>

<img src="https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=Git&logoColor=white"/></a>
<img src="https://img.shields.io/badge/GITHUB-181717?style=for-the-badge&logo=GitHub&logoColor=white"/></a>
<img src="https://img.shields.io/badge/VISUAL STUDIO CODE-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white"/></a>

 <br/>

### Config  <br/>

<img src="https://img.shields.io/badge/NPM-CB3837?style=for-the-badge&logo=NPM&logoColor=white"/></a>
<img src="https://img.shields.io/badge/YARN BERRY-2C8EBB?style=for-the-badge&logo=Yarn&logoColor=white"/></a>

 <br/>

### Development
<img src="https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"/></a>
<img src="https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"/></a>
<img src="https://img.shields.io/badge/TYPESCRIPT-3178C6?style=for-the-badge&logo=typescript&logoColor=black"/></a> 

<br />

#### 전역 상태관리

- 서버 상태 관리
<img src="https://img.shields.io/badge/React Query-61DAFB?style=for-the-badge&logo=reactquery&logoColor=white"/></a>

- 클라이언트 상태 관리
<img src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white"/></a>


 <br/>

### Database

<img src="https://img.shields.io/badge/SUPABASE-3FCF8E?style=for-the-badge&logo=supabase&logoColor=black"/></a>  

 <br/>

### Communication

<img src="https://img.shields.io/badge/SLACK-4A154B?style=for-the-badge&logo=Slack&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white"/></a>
<img src="https://img.shields.io/badge/FIGMA-F24E1E?style=for-the-badge&logo=Figma&logoColor=white"/></a>

 <br/>
 
---
## 화면 구성 및 주요 기능

 <br/>
 
 
- 메인 페이지
    - 카테고리별 필터링 및 정렬 기능
    - 좋아요 기능 
    - useInfinityQuery를 통한 무한 스크롤 구현
  
 <br/>
 
- 로그인 / 회원가입 페이지
    - supabase Auth를 통한 로그인과 회원가입 구현
    - supabase 소셜 로그인 기능을 사용한 소셜로그인 구현과 쿼리를 통한 회원정보 저장
    - react-hook-form을 사용한 로그인 및 회원가입 유효성 검사
 <br/>

- 상세 페이지
    - 경매 시간과 입찰값을 supabase Realtime을 이용하여 구현
    - 현재 최고 입찰가와 현재까지 입찰한 유저 정보 및 유저의 입찰값을 한번에 볼 수 있도록 구현
    - QnA를 통해 해당 게시물의 질문과 답변을 할 수 있도록 구현
 <br/>
 
- 게시물 작성 페이지
    - 경매품 이름, 소개, 최소입찰가격, 경매시작시간, 경매종료시간, 카테고리, 이미지를 입력받아 supabase에 insert
    - 유효성 검사를 통해 ""값, 글자수제한, 날짜제한, 이미지수 제한등을 유효성 검사
 <br/>
 
- 게시물 수정 페이지
    - 먼저 유저가 등록한 데이터 값을 화면에 뿌려주고 변경사항이 있으면 수정
    - auction_status를 받아와 경매가 진행중이면 최소입찰가겻, 경매 시작시간 변경 불가
 <br/>
 
- 프로필 페이지
    - 페이지네이션을 통한 유저가 작성한 게시물 목록과 찜한 목록 구현
    - 게시물 수정 및 삭제 기능과 찜한 목록에서 제거 기능 구현
    - supabase를 통한 회원정보(프로필 이미지, 닉네임, 주소) 업데이트 기능
    - 유저가 작성한 개시물 수정, 삭제 가능
 <br/>

 
- 검색창
    - supabase의 ilike와 or 쿼리를 사용한 검색 키워드 및 카테고리 별 검색 기능 구현

 <br/>
 
---
## 아키텍처


### 와이어프레임 <br/>

[프로젝트 와이어프레임](https://www.figma.com/file/8EulxNUZx6EYdiQcVrxRtQ/Untitled?type=design&node-id=0-1&mode=design&t=M3zOyCeokyddmHGc-0)

<br/>

### ERD <br/>

[프로젝트 ERD
](https://teamsparta.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F83c75a39-3aba-4ba4-a792-7aefe4b07895%2F7375634c-2a28-470b-853a-075187172f76%2FScreen_Shot_2023-12-27_at_10.54.06_AM.png?table=block&id=10c593ca-8a16-4f0b-9b6f-ad24222b5612&spaceId=83c75a39-3aba-4ba4-a792-7aefe4b07895&width=1310&userId=&cache=v2)

 <br/>

