# 주제 선정

- 사전 조사를 통해 2026년 개장 예정인 렛츠런파크 영천에 대해 접함.
- 관광객 유치를 목표로, 소재지 위치 접근성이 좋지 않은 문제를 해결하기 위하여 시내 버스 노선 및 시외 셔틀 버스 노선 구축

# 활용 공공데이터

- ‘행정안전부_지역별(행정동) 성별 연령별 주민등록 인구수.csv’
- ‘대구교통공사_역별일별시간별승하차인원현황.csv’
- 'yc_busevent.csv'
- '20230501184751_중심 관광지.csv'

# 아이디어의 구체성

**시내버스 노선 추가**

이동수단별 영천터미널과 영천 경마공원 사이 이동시간을 네이버 길 찾기를 통해 검색했을 때, 자차로 13분 정도 소요되는 거리가 대중교통을 이용할 경우 출발시각에 따라 이동시간이 1시간에서 3시간까지 교통편이 좋지 않은 것을 확인할 수 있습니다. 그래서 저희는 관광객들이 이용하게 될 시내버스 노선을 추가하기로 계획했습니다. 노선을 구상하기에 앞서 영천시의 다른 관광지도 방문하도록 유도하기 위해 시내버스에 영천역과 렛츠런파크 영천 근처의 관광지를 추가하였습니다. 관광객들을 위한 버스 노선을 정하기 위해서 한국 관광 데이터랩에서 제공하는 영천시 중심 관광지 데이터를 사용했습니다. 이 데이터는 관광객이 많은 순으로 100개의 중심 관광지의 정보를 담고 있습니다. 100개의 데이터 중 관광으로 분류된 54개의 데이터를 추출하였고, 하위 데이터들은 방문객 순위가 너무 낮아, 그중 25개의 관광지를 사용하기로 했습니다. 25개의 중심 관광지를 회색 플래그로 지도 위에 표시했습니다.
<img width="576" alt="Untitled (2)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/20de2842-f08c-426a-88b9-7eebc836d38c">


저희가 구상한 버스 노선은 영천역과 렛츠런파크 주변으로 아래 지도에서 볼 수 있는 영역 들을 운행할 계획입니다. 회색이 중심 관광지이고 초록색으로 표시된 곳은 영천역, 금호역, 영천 버스터미널, 금호역 시외버스터미널입니다. 이는 관광객들을 위한 버스 노선으로 외지 에서 방문할 때 이용할 플랫폼이므로 운행 노선에 포함하였습니다. 현재 영천시 운행 버스들 의 기점을 확인해보았을 때, 영천터미널을 기점으로 하는 버스들이 많았으며 관광객들이 많 이 모인다고 판단하여 영천터미널을 기점으로 두었습니다. 빨간색 경로를 따라 롯데시네마 영천, 영천강변공원, 영천 전투메모리얼파크, 동의참누리원영천한의마을, 금호역, 금호시외버 스터미널 그리고 렛츠런파크를 종점으로 하여 전체적인 버스 노선 틀을 짜보았습니다.
<img width="591" alt="Untitled (3)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/8bb81e66-39d1-491f-b6dd-97475bce1081">


이어서 동의참누리원영천한의마을에서 렛츠런파크 방향으로 가는 길에 노선을 추가하기 위 해 영천 시내버스를 분석해보았습니다. 영천시 시내버스의 노선 데이터를 찾는 데 큰 어려움 이 있었습니다. 그래서 저희는 2022년 9월 중 주말의 영천시에서 하루 동안 운행한 버스 이벤 트 데이터를 이용하여 104개의 버스 노선을 지도에 시각화했습니다.
시각화 결과, 저희가 원하던 라인을 지나는 버스는 555-7, 111-1, 55, 555, 111, 5501로 총 6 가지가 있었습니다. 그 라인에 있는 모든 정류장을 6개의 버스 중 몇 개의 버스가 지나가는 지 분석했습니다. 6개의 버스가 모두 정차하는 정류장은 없었고, 영천공설시장, 금호시장앞, 금호터미널 건너 등 총 8개의 정류장에 5개의 버스가 정차하며, 4개의 버스, 3개의 버스가 정차하는 정류장들은 더욱 많은 것을 확인했습니다.

아래의 그림을 보면 주황색으로 표시된 위치가 6개의 버스 중 5개의 버스가 지나가는 정류 장이며, 보라색으로 표시된 위치는 4개의 버스가 지나가는 정류장입니다.
<img width="591" alt="Untitled (4)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/687134b7-b1df-4571-bebe-c40314ad38a0">


버스가 정차하는 정류장이 꽤 많아 보였지만, 양방향으로 표시된 정류장과 이미 지나쳐 온 경로의 버스를 제외하고 영천 버스터미널에서 렛츠런파크로 가는 방향의 버스만 살펴보아야 합니다.

<img width="592" alt="Untitled (5)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/8d3363a7-a32a-4070-aee0-b68ebcadc258">


저희는 최종적으로 아래와 같은 노선을 갖는 시내버스 추가를 기획하였습니다.

영천터미널-영천역-롯데시네마영천-영천강변공원-영천전투메모리얼파크-동의참누리원영천한 의마을-오수동.쌍계마을입구(금호방면)-오수동e마트-영천경찰서-원제리-윤성아파트앞-808종점 -금호초등학교-금호읍사무소-금호시장앞-금호터미널건너-금호역-렛츠런파크영천


**셔틀버스 노선 선정**

한국 관광 데이터랩 사이트에서 제공하는 영천시 방문자 거주지, 유출지 분포를 통해 경상북
도와 대구광역시에서 가장 많은 관광객이 방문하는 것을 알 수 있었습니다. 렛츠런파크 서
울, 부산 등의 셔틀버스 노선 현황을 통해 총 3개의 노선을 만들기로 했습니다. 먼저 대구광
역시에는 한 개의 노선, 경상북도에는 두 개의 노선을 계획했습니다.
대구광역시의 노선을 선정하기 위해 저희는 대구 지하철 승하차 데이터를 이용했습니다.
<img width="1074" alt="Untitled (6)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/482d5a27-6a2a-47ad-aae9-6daee97c6528">


승하차 인구수 분석 결과, 반월당, 동대구역, 중앙로역, 상인역, 서부 정류장 순으로 인구수가 많았으며, 이는 곧 유동인구가 많다는 의미입니다. 대구 셔틀버스 노선을 선정할 때 유동인 구가 많은 곳을 기준으로 선정하여, 반월당역과 동대구역을 노선에 포함하기로 했습니다. 지 도상에 상위 5개 역의 위치 좌표를 찍어보았습니다. 오른쪽 위에 영천시가 위치하며, 지도에서 영천시로 가는 경로상 반월당역을 출발지로 선정하였고, 동대구역을 경유지로 선정했습니다.
![Untitled (7)](https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/b458a397-b08f-40b7-8f49-c50b4df95fda)


경상북도에서 두 개의 노선을 선정하기 위해 인구수가 많은 지역을 분석하였습니다. 또, 렛 츠런파크 부산의 주요 관광객이 40-50대라는 점 또한 참고했습니다. 행정안전부 지역별, 성 별, 연령별 주민등록 인구수 데이터를 활용하여 경상북도 주요 시군구 두 지역을 추출해보았 습니다. 전체 인구수를 기준으로 보았을 때와 주 타겟층인 40-50대 인구수를 기준으로 보았 을 때 동일하게 상위 2개의 지역으로 구미시, 포항시 북구로 확인되었습니다. 더 세부적인 노선을 짜기 위해 각 시군구에서 인구수가 많은 읍면동을 세 개씩 추출했을 때, 구미시는 인 동동, 양포동, 선주원남동 순으로 많았고, 포항시 북구는 장량동, 흥해읍, 우창동 순으로 많았 습니다.
구미시 노선 선정을 위해 교통카드 빅데이터 사이트에서 제공하는 구미시 최다 승차 정류장 을 참고했습니다. 상위 4개의 구미역, 상모농협앞, 인동초등학교, 금오산사거리 정류장을 지 도에 좌표를 찍어보았을 때 인동동, 선주원남동, 양포동은 아니지만 그 중심에 위치해 있으 며 교통이 편리한 구미역을 출발지로 선정하였고 세 지역 중 인구수가 가장 많은 인동동에 위치한 인동초등학교를 경유지로 선정했습니다.
<img width="581" alt="Untitled (8)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/97e3d700-f806-47b1-a710-6b6cf5896fa7">


포항시 북구는 장량동, 흥해읍, 우창동 중 장량동이 두 지역에 비해 우세하게 인구수가 많은 것을 확인했습니다. 인터넷 조사를 통해 포항시에서 시내 교통체증을 해소하기 위해 흥해읍
에 환승센터를 설치한 것을 파악했습니다. 이곳을 포항시 북구 셔틀의 출발지로 선정하고, 인구수가 우세하게 많은 장량동의 행정복지센터를 경유지로 선정했습니다.
![Untitled (9)](https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/36de8bfe-fe74-44fd-a7a1-cc5da6f31970)


결과적으로, 저희가 선정한 3개의 셔틀버스 노선은 아래와 같습니다.
<img width="821" alt="Untitled (10)" src="https://github.com/younkyungkim/Utilization-of-Public-Data-in-yc/assets/141793731/f533fecc-ef2a-40d3-a570-38d87bbc32cf">

