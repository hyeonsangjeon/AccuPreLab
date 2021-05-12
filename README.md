# AccuPreLab


# System 구성
![](img/sysArch.png)



# 데이터 설명
* 입금, 출금, 대출, 지불, 송금등의 거래에서 이행행위에 대한 데이터
## Column Desc
|no|컬럼명           | 설명                                                                    |Type |
|--|-----------------|-------------------------------------------------------------------------|-----|
|0|id             | 고객의 고유 ID                                                                |int64 |
|1|Gender           | 성별                                                                   |object|
|2|Age         | 나이                                                                        |int64|
|3|Driving_License   |  0 - 운전면허 미보유, 1 - 운전면허 보유                                                |int64|
|4|Region_Code   | 고객 지역의 고유 코드                                                               |float64|
|5|Previously_Insured  | 1 - 자동차 보험 가입, 0 - 자동차 보험 미가입                                       |int64|
|6|Vehicle_Age   | 차량의 년식                                                                |object|
|7|Vehicle_Damage   | 1 - 사고 이력 있음. 0 - 사고 이력 없음                                             |object|
|8|Annual_Premium          | 고객이 연도에 보험료로 지불해야하는 금액                                         |float64|
|9|Policy_Sales_Channel          | 고객에게 연락하는 채널. 다른 상담원, 우편, 전화, 직접 방문 등                   |float64|
|10|Vintage          | 고객이 회사와 연결된 일 수                                                                  |int64|
|11|Response          | 1 - 관심을 보임, 0 - 관심을 보이지 않음.                                                 |int64|


# 분석 시나리오
* 외부 시스템에서 S3에 데이터를 계속 저장하고 있다.
* AccuInsight+ Pipe를 통해 S3에 저장된 데이터를 전처리 한다.
* AccuInsight+ Pipe에서 전처리한 데이터는 hdfs에 저장한다.                      (EDA에서는 S3사용 혹은 PC에 다운로드)
* AccuInsight+ Modeler를 통해 이상행위 판별 모델을 생성한다.
* AccuInsight+ Modeler에 RestFul 웹서비스로 FDS의 이상행위 탐지 모델을 구현한다.
* Asset화 하여 향후 타부서 사용할 수 있게 한다.
* 단, 외부 시스템(데이터 수집서버, Client)등은 구현하지 않는다.


# 1.EDA
* [1.EDA로 이동](./1.EDA/README.md)

# 2.Load And Preprocessing
* [2.LoadAndPreprocessing로 이동](./2.LoadAndPreprocessing/README.md)

# 3.Modeling
* [3.Modeling로 이동](./3.Modeling/README.md)

# 4.Asset
* [4.Asset로 이동](./4.Asset/README.md)
