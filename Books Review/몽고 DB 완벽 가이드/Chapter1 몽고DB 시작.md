# Part1 몽고DB 시작



### 1.1 손쉬운 사용

몽고DB는 관계형 데이터베이스(relational database)가 아니라 **도큐먼트 지향** 데이터베이스(document- oriented database)다. 관계형 모델을 사용하지 않는 주된 이유는 분산 확장(scale-out)을 쉽게 하기 위함이지만 다른 이점도 있다.

도큐먼트 지향 데이터베이스에서는 행 개념 대신에 보다 유연한 모델인 도큐먼트를 사용한다. 내장 도큐먼트와 배열을 허용함으로써 도큐먼트 지향 모델은 복잡한 계층 관계를 하나의 레코드로 표현할 수 있다. 이 방식은 최신 객체 지향 언어를 사용하는 개발자의 관점에 매우 적합하다.

또한 몽고DB에서는 도큐먼트의 키와 값을 미리 정의하지 않는다. 따라서 고정된 스키마가 없다. 고정된 스키마가 없으므로 필요할 때마다 쉽게 필드를 추가하거나 제거할 수 있다. 덕분에 개발 과정을 빠르게 반복할 수 있어서 개발 속도가 향상된다.



### 1.2 확장 가능한 설계

애플리케이션 데이터셋(dataset)의 크기는 놀라운 속도로 증가하고 있다. 가용 대역폭(available bandwidth)과 값싼 스토리지의 증가로 인해 작은 애플리케이션에도 현재 데이터베이스의 한계를 넘어서는 데이터를 저장하게 됐다. 과거에는 흔치 않았던 테라바이트 수준의 데이터도 이제는 꽤 흔하게 접한다.

분산 확장을 염두에 두고 설계돼어 도큐 먼트 지향 데이터 모델은 데이터를 여러 서버에 더 쉽게 분산하게 해준다.



### 1.3 다양한 기능

몽고DB는 범용 데이터베이스로 만들어졌기 때문에 데이터의 생성, 읽기, 변경, 삭제 외에도 데이터베이스 관리 시스템(DBMS)의 대부분의 기능과 더불어 다음과 같은 기능을 제공한다.

- 인덱싱
  몽고DB는 일반적인 보조 인덱스를 지원하며 고유(unique), 복합(compound), 공간 정보, 전문(full-text) 인덱싱 기능도 제공한다. 중첩된 도큐먼트 및 배열과 같은 계층 구조의 보조 인덱스도 지원하며, 개발자는 모델링 기능을 자신의 애플리케이션에 가장 적합한 방식으로 최대한 활용할 수 있다.
- 집계
  몽고DB는 데이터 처리 파이프라인 개념을 기반으로 한 집계 프레임워크를 제공한다. 집계 파이프라인(aggregation pipeline)은 데이터베이스 최적화를 활용해, 서버 측에서 비교적 간단한 일련의 단계로 데이터를 처리함으로써 복잡한 분석 엔진(anlytics engine)을 구축하게 해준다.
- 특수한 컬렉션 유형
  몽고DB는 로그와 같은 최신 데이터를 유지하고자 세션이나 고정 크기 컬렉션(제한 컬렉션 - capped collection)과 같이 특정 시간에 만료해야 하는 데이터에 대해 유효 시간(TTL - Time to Live) 컬렉션을 지원한다. 또한 기준 필터(criteria filter)와 일치하는 도큐먼트에 한정된 부분 인덱스(partial index)를 지원함으로써 효율성을 높이고 필요한 저장 공간을 줄인다.
- 파일 스토리지
  몽고DB는 큰 파일과 파일 메타데이터를 편리하게 저장하는 프로토콜을 지원한다.



### 1.4 고성능

몽고DB는 강력한 성능을 제공하면서도 관계형 시스템의 많은 기능을 포함한다. 하지만 관계형 데이터베이스의 작업을 전부 하려는 것은 아니다. 일부 기능의 경우 데이터베이스 서버는 처리와 로직을 클라이언트 측에 오프로드한다.(드라이버 또는 사용자의 애플리케이션 코드에 의해 처리된다) 이러한 간소한 설계 덕분에 몽고DB는 뛰어난 성능을 발휘한다.



### 1.5 몽고DB의 철학

몽고DB 프로젝트의 주 관심사는 확장성이 높으며 유연하고 빠른, 즉 완전한 기능을 갖춘 데이터 스토리지를 만드는 일이다.