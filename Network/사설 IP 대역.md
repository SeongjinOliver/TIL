# 사설 IP 대역

인터넷 기술 표준을 정의하는 IETF의  RFC 1918 문서에 따르면, 전 세계 공통으로 다음과 같은 주소들이 사설 IP 주소 대역임을 정의하고 있다. (공인 IP로 사용 불가능한 대역, 사설 IP 대역으로만 사용)

- 단일 A 클래스 사설 네트워크 대역
  - 10.0.0.0 ~ 10.255.255.255 (10.0.0.0/8 (255.0.0.0))
- 16개의 인접합 B 클래스 사설 네트워크 대역
  - 172.16.0.0 ~ 172.31.255.255 (172.16.0.0/12 (255.240.0.0))
- 256개의 인접한 C 클래스 사설 네트워크 대역
  - 192.168.0.0 ~ 192.168.255.255 (192.168.0.0/16 (255.255.0.0))