# 📧 Remote PC Control via Gmail

A lightweight **remote computer control system using Gmail**.  
This project allows users to send commands through email to remotely control a Windows machine. The application listens for incoming emails from an authorized Gmail account, parses the commands, executes them on the target machine, and sends back the execution results via email.

The project was developed as a **practice project for socket programming and client-server architecture**, focusing on remote command execution and email-based communication.

---

# ✨ Features

- 📩 **Email-based command control**  
  Send commands from an authorized Gmail account to control the remote computer.

- ⚙️ **Remote system actions**  
  Execute various operations such as:
  - Launch applications
  - Control system settings
  - Run predefined commands

- 📤 **Execution feedback**  
  The system sends an email response containing the result of the executed command.

- 🔐 **Authorized sender verification**  
  Only predefined Gmail accounts are allowed to send control commands.

---

# 🧠 How It Works

The system works using a simple **email command pipeline**:

1. The server application monitors an inbox via Gmail.
2. When a new email arrives, the program:
   - verifies the sender
   - parses the command in the email
3. The command is executed on the target machine.
4. The result of the execution is sent back to the sender via email.

This architecture allows **remote control without requiring a dedicated web server or remote desktop connection**.

---

# 🏗️ System Architecture

Authorized Gmail User
        │
        ▼
   Gmail Server
        │
        ▼
   Email Listener
        │
        ▼
Sender Verification
        │
        ▼
   Command Parser
        │
        ▼
  Command Executor
        │
        ▼
Windows System Actions
        │
        ▼
   Result Generator
        │
        ▼
    Email Sender
        │
        ▼
Authorized Gmail User

---

# 📦 Requirements

Make sure the following tools and libraries are installed before running the project:

## Development Tools

- **Visual Studio (latest version)**  
  Used for building and running the application.

## Libraries

- **OpenCV**  
  Used for image processing tasks if the project requires screen capture or image-based operations.

- **EASendMail**  
  Used for sending emails programmatically between the client and server.

---

# ⚙️ Installation

## 1. Clone the repository

git clone https://github.com/trongtz/control-pc-by-email.git
cd control-pc-by-email
## 2. Open the project

Open the solution file in Visual Studio.

## 3. Install required libraries

Make sure the following libraries are properly linked:

OpenCV

EASendMail

Configure library paths if needed.

## 4. Configure Gmail credentials

Update the configuration with:

Gmail account

App password

Authorized sender email

# 🚀 Usage

1. Start the server application on the target computer.

2. Send an email from the authorized Gmail account containing a command.

3. The system will:

- read the email

- execute the command

- send the result back via email.

# 🔒 Security Considerations

1. Only authorized Gmail accounts can send commands.

2. Gmail App Passwords should be used instead of normal passwords.

3. It is recommended to:

- restrict allowed commands

- validate email input

- log all executed actions.
