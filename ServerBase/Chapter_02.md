# TCP/IP 스택의 계층 구조

# 1. Physical layer (물리계층)  
- 하드웨어를 다루며, 전기 신호를 관리한다.  
- 전화선, 동축 케이블, 광섬유 케이블, 전파 등

# 2. Data Link Layer (데이터 링크 계층)  
- 송신 호스트의 정보를 물리계층을 통해 보낼 수 있는 수단을 제공한다.  
- 신호를 호스트가 수신할 수 있도록 물리적 전기 신호로 변환하는 방법을 정의한다.
- 
- 이더넷, 와이파이 프로토콜, 장거리 무선 프로토콜 (3G, 4G)  

#### 이더넷 패킷 구조
프리앰블/ SFD(0x55 7개 + OxD5 1개) -> 시작을 알린다.  
목적지 MAC주소(네트워크 고유주소/6byte)  
발진지 MAC주소 / 길이/종류(길이는 페이로드의 길이를 바이트 단위 표시, 종류는 이더넷 타입 표시) -> 최대 1500바이트이기때문에 넘으면 종류, 아니면 길이  
페이로드  
프레임 체크 시퀀스 : CRC32  


# 3. Network Layer( 네트워크 계층)
- IP주소를 사용한다.  
- 라우터와 게이트웨이  

### IP 주소 및 패킷 주소
![100504_cisco_figure_3_12b](https://user-images.githubusercontent.com/80669633/223909398-a970f426-f29e-43dc-a7e4-ba14256b9fdc.gif)

identifier : IP 패킷 식별한다.
flag : 패킷 분할 여부 정보를 제공한다.
fragment offset :  재조립시 필요한, 기존 위치 정보를 제공한다.

#### 직접라우팅  
* ARP : MAC 주소 결정 프로토콜, MAC <-> IP주소  
* ![2279CC4552B2CDEE25](https://user-images.githubusercontent.com/80669633/223911319-05982a88-461d-44f9-8d3c-cd8e0603d2cb.jpg)

#### 간접라우팅(CIDR)  
#### 서브넷  
 IP주소와 서브넷 마스크를 비트 AND했을 때 같으면 동일한 네트워크  
 서브넷마스크 이진수 형태의 1의 개수가 IDR  
 
 
 - fragment
