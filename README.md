# Real-Time Chat App — Spring Boot + WebSockets

A minimal real-time chat app using Spring Boot (STOMP over WebSocket) with a tiny HTML/vanilla-JS client. Good for learning WebSocket handshakes, message flow, and basic presence handling.

## Quick start

```bash
git clone <repo-url>
cd factor-4
./mvnw spring-boot:run    # Windows: mvnw.cmd spring-boot:run
# Open http://localhost:8080
```

## What it does

Clients connect via WebSocket, send chat messages to `/app/chat`, and receive broadcasts on `/topic/messages`. Includes connect/disconnect listeners to track presence.

## Tech stack

* Java + Spring Boot (WebSocket + STOMP)
* Maven
* HTML + vanilla JavaScript (SockJS/STOMP client)

## Project layout

```
factor-4/
├─ src/        # Java code + static HTML/JS (usually under src/main/resources/static/)
├─ pom.xml
├─ mvnw, mvnw.cmd
└─ .gitignore
```

## Important endpoints (check your config)

* WebSocket endpoint: `/ws`
* Send (app destination): `/app/chat`
* Subscribe (topic): `/topic/messages`



---

If you want, I can also add an **MIT LICENSE** snippet and a sample `docker-compose.yml` for running with RabbitMQ — tell me which one and I’ll add it to the same file.
