# Java Socket Client-Server Chat Application

## Overview

This project is a simple **Java TCP socket-based client-server chat application**.  
It demonstrates how two Java programs (a server and a client) can communicate with each other in real time using:

- Socket and ServerSocket
- Multithreading
- Input/Output streams

Both the client and the server can send and receive messages simultaneously.

This project is useful for learning:

- Java networking fundamentals
- Blocking I/O
- Thread-based communication
- Basic real-time messaging concepts

this is medium blog which explains it all step by step : https://medium.com/nerd-for-tech/create-a-chat-app-with-java-sockets-8449fdaa933

---

## Technologies Used

- Java (Standard Edition)
- TCP Sockets (`java.net`)
- Multithreading (`java.lang.Thread`)
- I/O Streams (`java.io`)

---

## How It Works

### Server

- Starts a `ServerSocket` on port **5000**
- Waits for a client connection using `accept()`
- Creates two threads:
  - **Sender Thread** → Sends messages from server console to client
  - **Receiver Thread** → Receives messages from client and prints them

### Client

- Connects to server at `127.0.0.1:5000`
- Creates two threads:
  - **Sender Thread** → Sends messages from client console to server
  - **Receiver Thread** → Receives messages from server and prints them

This allows bi-directional communication at the same time.

---

## How to Run

### Step 1 : Compile — Step 2 : Run server then client

```bash
javac Server.java
javac Client.java

java Server
java Client


