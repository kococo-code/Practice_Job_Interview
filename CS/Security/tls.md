# Security

## SSL/TLS 인증 방법에 대해서 설명하시오.
SSL : Secure Socket Layer(보안 소켓 레이어)

TLS : Transport Layer Security(전송 계층 보안)

SSL은 Certificate Authority(CA)로 부터 서버와 클라이언트를 인증하는 절차를 가진다. TLS는 SSL을 표준화하면서 바뀐 이름이다.

상대방과 통신하고자하는 대상이 맞음을 확인하기 위해서 디지털 인증서를 사용하며 모두가 신뢰할수 있는 CA와의 비대칭키 암호화가 필요함.
### 통신 절차

1. 클라이언트가 서버로 통신연결 요청
2. 서버는 CA로부터 받은 인증서를 클라이언트에 전달
3. 클라이언트는 CA로부터 공개키를 요청
4. CA로부터 받은 공개키로 인증서에 있는 공개키와 서버정보를 획득
5. 클라이언트는 인증서속의 공개키로 대칭키를 암호화하여 전송
6. 서버는 개인키를 이용하여 해독후 대칭키를 이용해 안전통신을 진행

### 관련 정보
- 디지털 인증
- HMAC
- X.509
- PKCS

## Reference
- https://b.luavis.kr/server/tls-101
