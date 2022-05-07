# 인터넷 네트워크

- IP(Internet Protocol)
- TCP, UDP
- PORT
- DNS
---
1. Internet Protocol

> 지정한 IP Address에 데이터 전달.           
> 패킷이라는 통신 단위로 데이터 전달.

비연결성:
패킷을 받을 대상이 없거나 서비스 불능 상태여도 패킷 전송

비신뢰성: 중간에 패킷이 사라지거나 순서대로 오지 않을 경우 전송문제 발생

### 인터넷 프로토콜 스택의 4계층
L4. Application Layer - HTTP, FTP

L3. Transport Layer - TCP, UDP

L2. Internet Layer - IP

L1. Netwrok Access Layer



---
2. TCP(Transport Contrl Protocol)

> 연결지향 - TCP 3 way handshake(가상 연결).    
> 데이터 전달 보장.  
> 순서 보장.    
<u>(1.SYN 2.SYN + ACK 3.ACK)</u>

3. UDP(User Datagram Protocol)
> IP와 기능이 유사하다.     
> PORT, checksum 부가기능 App에서 추가 작업 필요.

---
4. PORT
> 0 ~ 65535 할당 가능
> FTP - 20, 21
> TELNET - 23
> HTTP - 80
> HTTPS - 443

---
5. DNS 

|도메인명|IP Address|비고|
|------|---|---|
|naver.com|223.130.195.95|None|
|google.com|172.217.161.46|None|
|github.com|52.78.231.108|None|

