# 빅데이터 분석을 위한 스파크 2 프로그래밍 
빅데이터 분석을 위한 스파크 2 프로그래밍 서적의 소스코드입니다.
아래는 소스코드 전반에 대한 설명 및 유의사항, 오류 정정등과 관련된 내용으로 사용하기 전에 반드시 먼저 살펴보시기 바랍니다.



## 로컬 개발 환경 
* 본 프로젝트는 자바7 및 자바8 예제가 동일 소스에 포함되어 있으므로 자바8 설치가 필요합니다.
* 본 도서는 본문에서 Scala IDE를 다루고 있으나 IntelliJ등 어떤 IDE를 사용하여도 무방합니다.
    * 단, 사용하는 IDE에 따라 실제 오류가 아닌 코드를 오류로 인식하는 문제가 발생할 수 있으므로
    * maven 빌드를 수행하여 실제 컴파일 오류인지 IDE의 버그 또는 개발 환경 문제로 인한 것인지 여부를 확인해 보아야 합니다.  
        


## 코드 관련 유의사항 및 오류 내용 안내     
* 본 도서 본문에 실린 예제 코드 중에서 스파크세션(SparkSession) 생성 시 사용한 spark.local.ip, spark.driver.host, spark.sql.warehouse.dir 등은 의미 없거나 매번 지정해야 하는 필수 설정이 아니므로 제공되는 예제 코드에서는 필요한 경우를 제외하고는 이를 사용하지 않는 것으로 수정하여 배포합니다. 
* 데이터프레임등 일부 예제 코드의 경우는 다수의 메서드 사용법에 대한 예제를 하나의 코드에 포함하고 있으므로 각 예제를 메서드로 구분하고 아래와 같이  메인함수 내에 주석으로 처리하여 제공합니다. 따라서 실제 코드 테스트 시에는 원하는 부분의 주석을 해제하고 실행해야 합니다.

``` 
// [예제 실행 방법] 아래에서 원하는 예제의 주석을 제거하고 실행!!
// createDataFrame(spark, spark.sparkContext)
// runBasicOpsEx(spark, sc, sampleDf)
// runColumnEx(spark, sc, sampleDf)
```
* 일부 코드의 경우 코드 상에 본문의 "절 번호"를 포함하였으나 쉽게 판별이 가능한 경우 기록하지 않았습니다. 
* 자바, 스칼라, 파이썬 코드는 거의 대부분 동일한 이름의 파일명, 메서드명을 사용하는 것을 원칙으로 하였으나 일부 언어에 따른 특성 상 일치하지 않는 경우도 있습니다. 
