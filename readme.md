# 2020 여름방학 반려동물보조프로그램 
  ### 기능 설명
<img src="https://user-images.githubusercontent.com/66550739/110618526-2ba4b400-81da-11eb-88ae-c3f70baa21c1.png" width="510" height="400"></img>
+ 사용기술
  * pyqt5 사용하여 제작
  * Designer 프로그램 사용하여 레이아웃 제작
  * 메인 페이지 유튜브 위젯 상의 썸네일사진, 병원 찾기 페이지의 병원정보들은 Selenium으로 파싱
 
1. 메뉴
  * 메뉴바 내용
  
 <img src="https://user-images.githubusercontent.com/66550739/110642171-1b023700-81f6-11eb-9b48-27a1c68a15dd.png" width="300" height="300"></img>(적색 하이라이트 부분이 사용자 편집 부분)

  > 1. 프로필, 로그인/로그아웃 버튼
  >> 프로필 사진 클릭으로 사진변경 기능
  >> 로그인/로그아웃/회원가입 기능
  > 2. 홈
  >> 홈버튼이 기본값, 이외 메뉴 진입 시 해당 메뉴버튼 색상 변경
  > 3. 친구찾기
  > * 가입시 등록한 거주지 기준으로 같은 지역 거주하는 회원명단 출력
  > 
  > <img src="https://user-images.githubusercontent.com/66550739/110642712-9ebc2380-81f6-11eb-806b-0a1ae9521cee.png" width="400" height="300"></img>
  >> 화면 상단에 내 거주지 출력
  >> 목록에 거주지 일치하는 다른 회원들 프로필, ID, 이메일, 거주지 표시
  >> 아래 숫자버튼으로 페이지 조작
  >> 페이지 넘길 때 마다 다음 4명 db에서 가져오기
  > 4. 병원 찾기
  > * 가입시 등록한 거주지 기준으로 해당 지역에 있는 병원 명단 출력
  > 
  ><img src="https://user-images.githubusercontent.com/66550739/110646832-a2ea4000-81fa-11eb-867d-17349c266fde.png" width="400" height="300"></img>

  >> 화면 상단에 내 거주지 출력
  >> 해당 거주지 인근 병원정보 출력
  >> 이름, 주소, 전화번호, 네이버 지도에서 파싱
  >> 페이지 넘길 때 마다 다음 4곳 파싱
  > 5. 사료 구입
  > * 사료 정보에서 등록한 사료명을 키워드로 네이버 쇼핑을 파싱, 출력
  >
  > <img src="https://user-images.githubusercontent.com/66550739/110644043-09219380-81f8-11eb-9c27-75a9f6a333d8.png" width="400" height="300"></img>
  >> 메뉴창에서 사료 구입버튼 클릭시 인터넷 브라우저 창 띄워줌
  >> 사료정보에서 받아온 사료명 키워드로 네이버 쇼핑 검색창 시현
2. 달력
  * 금일 날짜를 기준으로 달력표시
  * 예정된 이벤트가 있는 일자에 별표 표시
3. 위젯



<img src="https://user-images.githubusercontent.com/66550739/110636891-25213700-81f0-11eb-97bc-9134aec14685.png" width="280" height="220"></img>
<img src="https://user-images.githubusercontent.com/66550739/110637706-0cfde780-81f1-11eb-8056-406932a84f66.png" width="200" height="180"></img>
<img src="https://user-images.githubusercontent.com/66550739/110640355-163c8380-81f4-11eb-961e-bfc113a8d3bf.png" width="100" height="130"></img> (적색 하이라이트 부분이 사용자 편집 부분)


   3-1. 일정 알림 위젯
  * 등록된 일정을 기준으로 해당날짜/내용표시
  * 하단 일정추가/편집 버튼을 통해 수정
    > + 삭제시 현재 일정에서 휴지통 모양 클릭
    > + 수정시 현재 일정에서 해당 내용 클릭하면 아래 추가/변경 창에 내용 표시, 이를 수정 후 확인 클릭
    > + 추가시 아래 추가/변경 창에서 작성 후 확인 클릭
  
   3-2. 사료 소모량 표시 위젯
  * 입력된 값을 토대로 계산해 내용 표시
  * 하단 정보수정 버튼을 통해 수정
  
   3-3. 유튜브 추천영상 위젯
  * 회원가입시 입력한 정보를 토대로 유튜브에서 추천영상 썸네일 3개를 파싱 후 보여줌
  * 추가로 더 보고 싶을땐 우측의 ... 버튼 클릭 시 해당 정보로 검색된 유튜브 웹페이지로 이동
 4. 조건부 팝업
  * 사료 잔여량이 10% 미만이면, 프로그램 최초 실행 시 팝업창 생성
