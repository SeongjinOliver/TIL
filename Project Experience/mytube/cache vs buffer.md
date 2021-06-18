# cache vs buffer



- Cache와 Buffer은 서로 바꿔 쓸 수 있는 단어
- Buffer는 전통적으로 연산 속도가 서로 다른 객체 사이에 임시로 데이터를 저장하는 저장소 지칭
  - 연산 속도가 빠른 쪽이 불필요하게 대기하지 않도록 도와 성능 향상에 도움을 줌
  - 작은 데이터 조각들을 모아서 한번에 움직일 수 있게 도와줌
  - 적어도 한 객체는 버퍼의 존재를 알아야함
- Cache는 보이지 않고 또한 두 객체 모두 그 존재를 알 필요가 없음
  - 같은 데이터를 여러 번 읽으려고 할 때 상대적으로 빠른 방법(느린 네트워크 요청 대신에 로컬 메모리에 저장된 것을 바로 돌려주는 등)을 제공하여 성능 향상에 도움을 줌