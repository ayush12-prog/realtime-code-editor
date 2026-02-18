# 🚀 Realtime Code Editor

A powerful real-time collaborative code editor built with the MERN stack (MongoDB not included) that enables multiple developers to write, edit, and compile code together in real-time.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Node.js](https://img.shields.io/badge/Node.js-18.x-green.svg)
![React](https://img.shields.io/badge/React-18.x-blue.svg)
![Socket.io](https://img.shields.io/badge/Socket.io-4.x-purple.svg)

## ✨ Features

### 🔄 Real-Time Collaboration
- **Live Code Synchronization**: See changes from other users in real-time
- **Room-Based System**: Create or join rooms with unique IDs for collaborative sessions
- **User Presence**: See who's currently in the room

### 📝 Code Editor
- **Monaco Editor**: Same editor that powers VS Code
- **Syntax Highlighting**: Support for multiple languages
- **Dark Theme**: Easy on the eyes with VS Code's dark theme

### 💻 Multi-Language Support
- JavaScript
- Python
- Java
- C++

### ⚡ Code Execution
- **Integrated Compiler**: Run your code directly in the browser
- **Input/Output**: Provide stdin input and view stdout output
- **Piston API**: Powered by the Piston code execution engine

### 👥 User Management
- Join rooms with custom usernames
- See list of users in the current room
- Typing indicators
- Leave room functionality

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **Socket.io** - Real-time bidirectional communication

### Frontend
- **React** - UI library
- **Vite** - Build tool
- **Monaco Editor** - Code editor component
- **Socket.io Client** - Client for real-time communication
- **UUID** - Unique ID generation

## 📋 Prerequisites

- Node.js (v18 or higher)
- npm or yarn

## 🚦 Installation & Setup

### 1. Clone the Repository

```
bash
git clone https://github.com/ayush12-prog/realtime-code-editor.git
cd realtime-code-editor
```

### 2. Install Dependencies

Install all required packages:

```
bash
# Install root dependencies
npm install

# Install frontend dependencies (if not automatically installed)
cd frontend
npm install
```

### 3. Run the Application

#### Development Mode (with auto-reload):
```
bash
npm run dev
```

#### Production Mode:
```
bash
npm run build
npm start
```

The application will be available at `http://localhost:5000`

## 📖 Usage Guide

### Creating a Room
1. Open the application in your browser
2. Click "create id" to generate a unique room ID
3. Enter your name
4. Click "Join Room"

### Joining an Existing Room
1. Open the application in your browser
2. Enter the Room ID (shared by another user)
3. Enter your name
4. Click "Join Room"

### Writing and Running Code
1. Select a programming language from the dropdown
2. Write your code in the editor
3. (Optional) Enter input in the input console
4. Click "Execute" to run your code
5. View the output in the output console

### Sharing Your Room
1. Click "Copy Id" to copy the room ID
2. Share the room ID with other users

## 🔧 Project Structure

```
realtime-code-editor/
├── backend/
│   └── index.js          # Express server & Socket.io setup
├── frontend/
│   ├── src/
│   │   ├── App.jsx       # Main React component
│   │   ├── App.css       # Styling
│   │   └── main.jsx      # React entry point
│   ├── public/           # Static assets
│   ├── package.json      # Frontend dependencies
│   ├── vite.config.js   # Vite configuration
│   └── index.html       # HTML template
├── package.json          # Root dependencies
└── README.md            # This file
```

## 🌐 API Reference

### Socket Events

| Event | Description | Payload |
|-------|-------------|---------|
| `join` | Join a room | `{ roomId, userName }` |
| `codeChange` | Broadcast code changes | `{ roomId, code }` |
| `languageChange` | Change programming language | `{ roomId, language }` |
| `compileCode` | Execute code | `{ code, roomId, language, version, input }` |
| `typing` | Broadcast typing status | `{ roomId, userName }` |
| `leaveRoom` | Leave current room | - |

### Socket Listeners

| Event | Description | Payload |
|-------|-------------|---------|
| `codeUpdate` | Receive code updates | `code` |
| `userJoined` | Update user list | `users[]` |
| `userTyping` | Show typing indicator | `userName` |
| `languageUpdate` | Update language | `language` |
| `codeResponse` | Receive code output | `response` |

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Monaco Editor](https://microsoft.github.io/monaco-editor/) - Code editor
- [Piston](https://piston.rs/) - Code execution engine
- [Socket.io](https://socket.io/) - Real-time communication

## 📧 Contact

For any questions or suggestions, please open an issue on GitHub.

---

<p align="center">Made with ❤️ by Ayush</p>
