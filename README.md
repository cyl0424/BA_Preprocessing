# BA_Preprocessing
따릉이 대여소 정보 전처리 진행

## File Information
- **seoul_bicycle_master.json**<br/>
  : 서울시 따릉이대여소 마스터 정보 데이터 (http://data.seoul.go.kr/dataList/OA-21235/S/1/datasetView.do)
- **master_preprocessing.ipynb**<br/>
  : 마스터 정보 데이터 중 좌표가 0.0으로 들어가있는 데이터를 google api를 이용해 정상적인 좌표로 바꿈
- **seoul_bicycle_maser_preprocessed.csv**<br/>
  : master_preprocessing.ipynb로 전처리 진행한 데이터를 저장한 파일
- **master_info_with_nearby.ipynb**<br/>
  : seoul_bicycle_maser_preprocessed.csv를 이용해 각 대여소에서 가장 가까운 대여소와, 그 거리 데이터 컬럼을 추가함
- **master_info_with_nearby.csv**<br/>
  : master_info_with_nearby.ipynb를 이용해 인근대여소 정보까지 추가한 데이터

##  master_info_with_nearby.csv
- **stn_id** : 대여소 id를 나타내며 object 타입임
- **stn_addr** : 대여소의 주소 전체를 나타내며 object 타입임
- **stn_lat** : 대여소의 latitude를 나타내며 float64 타입임
- **stn_lng** : 대여소의 longitude를 나타내며 float64 타입임
- **nearby_id** : 가장 가까운 대여소의 id를 나타내며 object 타입임
- **nearby_km** : 가장 가까운 대여소와의 거리를 km 단위로 나타내며 float64 타입임
  
ex)<br/>
<img width="743" alt="스크린샷 2023-11-09 오후 5 05 15" src="https://github.com/cyl0424/BA_Preprocessing/assets/63573867/2ba906a4-7bd2-4df2-b45d-b31bad1b9f89">
