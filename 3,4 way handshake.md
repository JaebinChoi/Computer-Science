# [TCP] 3 way handshake / 4 way handshake
#### 연결을 성립하고 해제하는 과정

## 3 way handshake (연결 성립)
#### TCP는 정확한 전송을 보장해야 한다.
#### 따라서 통신하기에 앞서, 논리적인 접속을 성립하기 위해 3 way handshake 과정을 진행한다.

![image](https://user-images.githubusercontent.com/51224070/108304203-d5e87780-71ea-11eb-877b-b74434d27336.png)

1. 클라이언트가 서버에게 SYN 패킷을 전송 (SEQUENCE = X)
2. 서버가 SYN(X)을 받고, 클라이언트로부터 받았다는 신호인 ACK와 SYN 패킷을 전송 (SEQUENCE = Y, ACK = X+1)
3. 클라이언트는 ACK(X+1), SYN(Y)을 받고, ACK(Y+1)를 전송

## 4 way handshake (연결 해제)
#### 연결 성립 후 모든 통신이 끝났다면 해제한다.

![image](https://user-images.githubusercontent.com/51224070/108305807-2e6d4400-71ee-11eb-8367-ffa53655e953.png)

1. 클라이언트는 연결을 종료한다는 FIN 패킷을 전송
2. 서버는 FIN을 받고, ACK를 전송 (데이터를 모두 전송할 때까지 대기)
3. 데이터를 모두 전송했다면, 연결을 종료한다는 FIN 패킷을 전송
4. 클라이언트는 FIN을 받고, ACK를 전송
5. 서버는 ACK를 받고, 소켓 연결을 CLOSE
6. 클라이언트는 서버로부터 받지 못한 데이터가 있을 것을 대비해 기다리는 과정을 거친다.(TIME_WAIT)
