# 💬 Assignment 2 – Simple Chatroom (using Go RPC)

## 🧠 Overview
This project is a **Simple Chatroom** implemented using **Go’s `net/rpc` package**.  
It demonstrates how a client and server communicate using Remote Procedure Calls (RPC).  

The **server** coordinates messages between multiple clients by storing them in a list, while the **client** connects to the server, sends messages, and retrieves the full chat history.

---

## 🎥 Running Project Recording
📎 **Video Link:** https://drive.google.com/file/d/1ckNe0_CZnIec6J65vgF7rYqGEk64p4o2/view?usp=drive_link
---

## 📁 Project Structure
├── client.go # Client-side code that connects to the server and sends messages
├── server.go # RPC server that receives, stores, and returns chat history
└── README.md # Documentation of the project

## ⚙️ How It Works

### 🖥️ Server (`server.go`)
- Listens on `127.0.0.1:1234` using TCP.
- Registers the `ChatService` type as an RPC service.
- Receives a message string from the client.
- Appends it to the server’s internal message list.
- Returns the entire chat history (all sent messages) back to the client.
- Displays each received message in the server terminal.


### 💬 Client (client.go)
- Connects to the server
- Reads user input with bufio.NewReader(os.Stdin) to capture full lines (including spaces).
- Sends each entered message to the server
- Displays the full chat history after every sent message.
- Exits when the user types exit.






