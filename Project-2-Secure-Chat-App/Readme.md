# 🔐 Secure Channel V1: E2EE Chat Application

### 🚀 End-to-End Encrypted Real-Time Communication Platform
**Status:** Production Ready | **Tech Stack:** Python, Flask-SocketIO, SQLite, Cryptography

---

## 🎯 Project Overview:
"Secure Channel V1" is a high-security chat application designed to demonstrate the practical implementation of **End-to-End Encryption (E2EE)**.

While the initial requirement was a basic chat interface, this project was engineered to be a **robust privacy tool**. It features RSA/AES hybrid encryption, ephemeral messaging (no logs stored), and a persistent user authentication
system, ensuring that communication remains private even if the server is compromised.

### 🔑 Key Features:
* **End-to-End Encryption:** Messages are encrypted on the client side using AES; keys are exchanged securely via RSA.
* **Ephemeral Messaging:** Chat logs are transient and disappear after the session, ensuring zero data retention.
* **Secure Authentication:** Custom-built SQLite user management system for secure login/registration.
* **Real-Time Communication:** Powered by `Flask-SocketIO` with patched `eventlet` for handling concurrent encrypted streams.

---

## 📸 Visual Walkthrough:

### 1. Secure Identity Portal
*The hacker-themed login interface enforcing secure user authentication.*
![Login Screen](screenshots/login_page.png)

### 2. Encrypted Channel Interface
*The main chat dashboard showing active units and secure status.*
![Chat Dashboard](screenshots/chat_interface.png)

### 3. Live Secure Communication
*Real-time message exchange in a fully encrypted environment.*
![Active Chat](screenshots/active_chat.png)

### 4. Server-Side Logistics
*Backend logs showing the handling of encrypted payloads and socket events.*
![Server Logs](screenshots/terminal_logs.png)

---

## 🔧 Technical Challenges & Solutions:

* **Concurrency:** Configuring asynchronous communication with Socket.IO caused threading issues. This was resolved by patching the `eventlet` library and managing application contexts carefully.
* **Static Asset Management:** Fixed CSS loading issues caused by case-sensitivity (Static vs. static) and browser caching by restructuring the folder hierarchy and updating templates.

---

## ⚠️ Disclaimer
**This tool is a Proof of Concept for educational purposes.**
The encryption implementation follows standard cryptographic principles but should not be used for critical sensitive communications without a full code audit.
