# Individual Project - 서울특별시 따릉이 증설

## 주제

서울특별시의 자전거도로 현황과 따릉이 분포를 바탕으로 따릉이 증설이 더 필요한 지역을 뽑아내기

## URL

1. 서울특별시 자전거도로 현황 : 'https://data.seoul.go.kr/dataList/276/S/2/datasetView.do'
2. 따릉이 정류장 홈페이지 : 'https://www.bikeseoul.com/app/station/moveStationRealtimeStatus.do'

## 개요

0. 순서: 데이터 수집 -> 저장 -> 전처리 -> 시각화 -> 딥다이브
1. 데이터 수집

- 서울특별시 홈페이지: BeautifulSoup 활용, 비동기 크롤링
- 따릉이 정류장 홈페이지: BeautifulSoup 활용, 비동기 크롤링

3. 전처리

- Rev-Geocoding 활용: 크롤링한 정보: 정류장 별 위도/경도
  - Naver Cloud Platform API 활용하여 주소로 변환, 지역구 정보로 전처리
- 텍스트 파싱 및 리스트/딕셔너리 인덱싱 활용

4. 시각화

- matplotlib pyplot
- twinx 사용하여 지역구별 '자전거도로 현황' 및 '따릉이 정류장 현황'을 동시에 파악 가능케 함
- 결과 차트는 딕셔너리 재정렬하여 barh로 표현, 우선순위를 더욱 명시적으로 볼 수 있도록 시각화

5. 프로젝트 결론 및 딥다이브

- 시사점 도출
- 미흡한 점과 보완 및 발전 가능한 방향
