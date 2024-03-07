# Spring Boot with Socket.IO

![SpringBoot](https://img.shields.io/badge/Spring_Boot-18181b?style=for-the-badge&logo=springboot)
![ApacheKafka](https://img.shields.io/badge/Socket.IO-fff?style=for-the-badge&logo=socketdotio&logoColor=010101)

An example Spring Boot project built with [Netty Socket.IO](https://github.com/mrniko/netty-socketio)

## Setup

`application.yml` expose your socket server

`socket-server.host` should be a static ip to expose for other client beside local client

in this case, it is local client only

```yaml
socket-server:
  port: 8085
  host: 127.0.0.1
```

Run the project with maven or on your ide

```bash
./mvnw.cmd
```

## Demonstration

### Client 1

Create a Socket.IO request using either [Postman](https://www.postman.com/) or socket.io client of your choice

- url `ws://localhost:8085?room=1`

- listening event `get_message`

- message with event name `send_message`
```json
{
    "room": "1",
    "type": "CLIENT",
    "message": "hello, this is from client 1"
}
```

### Client 2

Create a Socket.IO request using either [Postman](https://www.postman.com/) or socket.io client of your choice

- url `ws://localhost:8085?room=1`

- listening event `get_message`

- message with event name `send_message`
```json
{
    "room": "1",
    "type": "CLIENT",
    "message": "hello, this is from client 2"
}
```

## Meta

Hourmeng Khy