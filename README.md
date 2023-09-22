# a3_webproject
### 개요
```
수년간 쌓인 야구 통계 자료를 이용하여 야구 기록을 분석하는 세이버메트릭스가 있다.

야구가 유난히 다른 스포츠에 비해 데이터 분석이 발달한 가장 큰 이유는 경기가 연속적이지 않다는 것으로 볼 수 있을 것이다. 타 스포츠에 비해 야구는 아웃 카운트가 3개가 되면 이닝이 종료되고 공수 교대가 이뤄진다. 타석과 다음 타석 사이에도 경기의 흐름이 정지되는 순간들도 존재한다. 한 타석의 결과가 정리되고 나면 다음 타석이 시작될 때까지는 경기 상황으로 인정되지 않는다. 

이렇게 정지된 상황들이 존재하기에, 변화의 정도와 원인을 파악하여 분석할 수 있게 된다.
```
[참고자료](https://about.ncsoft.com/news/article/baseball-data-analytics-21-20190718)

### 데이터 선정 이유
```
야구는 게임 중 발생하는 모든 이벤트가 기록지에 남겨지는 스포츠이자 기록만으로도 경기 내용이 유추가 가능한 스포츠이다. 
⇒ 평소 흥미롭게 생각한 야구 데이터를 직접 분석해보면서 도출해낼 수 있는 인사이트에 대해 고민을 해보고자 데이터를 선정하게 되었다.
```

### 데이터 추출
```
- MLB와 달리 KBO(Korea Baseball Organization)는 데이터셋을 api로 제공해주지 않기 때문에 직접 **웹 스크래핑**을 하여 데이터를 추출해야 한다.
- KBO 리그의 각종 야구 기록에 세이버메트릭스를 전문적으로 도입한 최초의 통계 사이트 중 하나인 **스태티즈(statiz)**의 데이터를 스크래핑하였다.
```

### <가설 설정>
### 1 :  2015~2018년 시즌보다 2019년 이후의 시즌은 타율, 출루, 장타는 감소하였으며 삼진, 병살은 증가하였을 것이다.
### 배경 : 타고투저(타자가 유리하고 투수는 불리한 경향)에 따라 공인구의 반발 계수가 낮아 2018년 공인구의 반발계수를 낮추었는데 이러한 변화는 타격 지표에 악영향을 끼쳤을 것이다.
### 2 : 2020년 KBO 리그는 다른 시즌에 비해 빅볼(2루타, 홈런 등 장타)의 비율이 높다.
 ### 보통 시즌이 3,4월 초에 시즌이 시작되는 다른 연도에 비해 2020년에는 코로나로 인해 5월에 시즌이 시작되게 되었다. 5월에 시즌이 시작되었다는 점이 야구 경기 혹은 선수들이 플레이하는 것에 어떤 영향이 있을 것이다.
### 3:  키움(전 넥슨) 히어로즈의 2016년 경기장 이전으로 인한 타격 지표의 변화
### 기존의 목동 구장에서 고척돔으로 옮기면서 달라진 구장에 관련하여 지표가 어떻게 달라졌는지 알아보자.
