# HTTP

- 클라이언트 서버 구조
- 무상태 프로토콜(stateless), 비연결성
- HTTP Message
- 간결함, 확장성 

---
1. 클라이언트 서버 구조
> Request Response 구조( 요청 - 응답)

---
2. Stateless 프로토콜
>서버가 클라이언트의 상태를 보존 X  
서버 확장성 증가 (Scale Out)    
클라이언트가 추가 데이터 전송

---
3. HTTP Message
>HTTP 요청 메세지    
GET /search?q=hello&hl=ko HTTP/1.1  
Host: www.github.com

>HTTP 응답 메세지   
>GET /search?q=hello&hl=ko HTTP/1.1
Host: www.github.com

