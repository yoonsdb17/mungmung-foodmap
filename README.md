# 멍멍 푸드맵

내 위치나 검색한 동네 근처 맛집을 보여 주는 지도예요. 메뉴를 못 고르겠으면 말티즈 강아지가 골라 줘요.

## 기능

- **전국 어디서나**: 처음엔 내 위치 근처를, 위쪽 검색창으로는 다른 동네·역 근처를 찾아요. 위치를 못 받으면 서울역 근처를 보여 줘요.
- **음식 종류 필터**: 한식, 국밥·탕, 고기·구이, 해산물·회, 분식, 중식, 카페·디저트
- **반경·정렬·평점·영업 중** 필터
- **🦴 강아지가 골라줘**: 메뉴, 거리, 평점, 영업 중 기준을 고르면 강아지가 킁킁거리며 한 곳을 골라요.
- 식당을 고르면 강아지가 걸어가서 아이콘을 냠냠 먹고 하트를 날려요.

## 실행 방법

1. Google Cloud Console에서 **Maps JavaScript API**와 **Places API (New)**를 사용 설정해요.
2. `config.example.js`를 `config.js`로 복사하고 API 키를 넣어요. 비워 두면 화면에서 키를 입력할 수 있어요.
3. `index.html`을 열어요. 위치 기능은 **https 주소나 localhost**에서만 확실히 돼요.
   ```bash
   python -m http.server 8000
   ```
   그다음 브라우저에서 `http://localhost:8000`을 열어요.

## API 키 보안

브라우저용 키는 방문자가 볼 수 있어서, 숨기기보다 **제한을 거는 게** 중요해요.

- 애플리케이션 제한: HTTP 리퍼러(내 사이트 주소, `http://localhost:*/*`)
- API 제한: Maps JavaScript API, Places API (New)만 허용
- API별 일일 할당량 상한 설정

## 파일

| 파일 | 설명 |
|---|---|
| `index.html` | 지도 페이지 전체 (HTML·CSS·JS 한 파일) |
| `fonts/Griun_Myoeunddobak-Rg.ttf` | 그리운 묘은또박체 (제목·버튼용) |
| `config.example.js` | API 키 설정 양식 |
| `config.js` | 실제 키가 들어가는 파일 (Git에 올리지 않음) |
