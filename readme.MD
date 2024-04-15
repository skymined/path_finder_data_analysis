#


## DDA
<details open>
<summary> data_attraction : 관광명소 검색량 </summary>

- 13,600 non-null
- 년도에 따라 관광명소 중에 중복되는 것이 있는지 확인
- rank가 무슨 의미인지 확인

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|rank|랭크?||int64||
|3|attracton_name|관광명소 이름||object||
|4|address|주소||object||
|5|classiication|분류|시장, 자연경관, 콘도미니엄, 종교성지, 기타관광, 호텔, 테마공원|object|각 분류별로 관광명소 검색량을 알아낼 수 있어 유의미할 것으로 보임|
|6|attraction_search|검색량||int64|관광명소 검색량으로 가장 중요한 데이터|
|7|region|지역|'강원', '경기', '경남', '경북', '광주', '대구', '대전', '부산', '서울', '세종', '울산','인천', '전남', '전북', '제주', '충남', '충북'|object||
|8|std_year|년도|2020~2023|int64|해당 년도에 얼마나 검색되었는지 알 수 있음|

</details>

<details open>
<summary> data_concept_search : 월별 관광 테마 검색량 </summary>

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|destinatinon_type|목적지 타입|전체, 숙박, 음식, 기타관광, 쇼핑, 레저스포츠|object|분류에 사용 가능|
|3|destination_search|검색량||int64|년/월 별로 다르기 때문에 상황에 따라 합할 필요성 있음|
|4|region|지역||object||
|5|std_year|년도||int64||
|6|std_month|월||int64|월별로 나눌 수 있음|
|7|std_year_month|년월|xxxxxx 형식|int64||

</details>

<details open>
<summary> data_consume : 분야별 소비량 </summary>

- 1177개

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|std_year|년도||int64||
|3|region|지역||object||
|4|consumption_amount|소비량||float64||
|5|industry_major_cate|대분류|'쇼핑업', '숙박업', '식음료업', '여가서비스업', '여행업', '운송업'|object||
|6|industry_middle_cate|중분류|'관광기념품', '레저용품쇼핑', '대형쇼핑몰', '면세점', '호텔', '콘도', '캠핑장/펜션', '기타숙박', '식음료', '관광유원시설', '골프장', '기타레저', '문화서비스', '스키장', '여행업', '수상운송', '렌터카', '육상운송', '항공운송', '카지노'|object||

</details>

<details open>
<summary> data_consume_transition : 소비 유형들의 월별 소비량 </summary>

-5693개

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|industry_major_cate|대분류|'전체', '운송업', '여행업', '숙박업', '식음료업', '여가서비스업', '쇼핑업'|object||
|3|std_year_month|년월|xxxxxx 형식|int64||
|4|std_year|년도||int64||
|5|std_month|월||int64|월별로 나눌 수 있음|
|6|consumption_amount|소비량||int64||
|7|region|지역||object||

</details>

<details open>

<summary> data_trend_search : 월별 여행 트렌드 검색량 </summary>

- 4080개

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|region|지역||object||
|3|std_year_month|년월|xxxxxx 형식|int64||
|4|std_year|년도||int64||
|5|std_month|월||int64|월별로 나눌 수 있음|
|6|tour_trend|투어유형|'레포츠', '휴식/힐링', '기타', '미식', '체험'|object||
|7|num_mention|검색량||int64||

</details>

<details open>

<summary> data_tour_NLP_train : 네이버 블로그 제목 </summary>

- 10000개
- [라벨링 참고](https://docs.google.com/spreadsheets/d/1WCxhauSWOAOyteTYYRZVgUhpZjO9dhXZ/edit#gid=2013088085)

|no|Variable|Definition|Key|Dtype|분석가 의견|
|--|--|--|--|--|--|
|1|_id|아이디||object||
|2|concept|컨셉|1:문화,2:레저, 3:역사, 4:음식, 5:자연, 6:힐링|int64|직접 라벨링한 것이므로 해당 부분에 대한 수정 필요할 수도 있음|
|3|season|계절|1:봄, 2:여름, 3:가을, 4:겨울|int64|직접 라벨링한 것이므로 해당 부분에 대한 수정 필요할 수도 있음|
|4|review_text|블로그 제목||object|raw_data이므로 보존|
|5|지역|지역|'울산', '전북', '대전', '경기', '전남', '제주', '대구', '강원', '광주', '경남', '서울', '부산', '경북', '인천', '충남', '충북', '세종'|object||
|6|review_text_clean|동사, 명사만 찾아낸 것||object||

</details>