# 🔥 Burner Chat

**Real-time, anonymous, ephemeral chat rooms** - No login, no database, no trace.

![Burner Chat Demo](https://img.shields.io/badge/Status-Active-brightgreen) ![Node.js](https://img.shields.io/badge/Node.js-18+-green) ![React](https://img.shields.io/badge/React-18-blue) ![Socket.io](https://img.shields.io/badge/Socket.io-4.7-yellow)

## ✨ Features

- 🚀 **Instant Room Creation** - One click to create a unique chat room
- 👤 **Custom Usernames** - Enter your display name before joining
- 💬 **Real-time Messaging** - Powered by Socket.io
- 🔒 **No Login Required** - Completely anonymous
- 💨 **Ephemeral Messages** - Messages vanish when you leave (server memory only)
- 🎨 **Dark Hacker Aesthetic** - Sleek neon green UI

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React 18 + Vite |
| Styling | Tailwind CSS |
| Backend | Node.js + Express |
| Real-time | Socket.io |
| Routing | React Router v6 |

## 📁 Project Structure

```
Gossips/
├── server/                # Backend
│   ├── package.json
│   ├── .env              # Environment config
│   └── index.js          # Express + Socket.io server
│
└── client/               # Frontend
    ├── package.json
    ├── vite.config.js
    ├── tailwind.config.js
    ├── index.html
    └── src/
        ├── main.jsx
        ├── App.jsx
        ├── index.css
        ├── socket.js     # Socket.io client config
        └── components/
            ├── LandingPage.jsx
            └── ChatRoom.jsx
```

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ installed
- npm or yarn

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd Gossips
```

### 2. Start the Backend

```bash
cd server
npm install
npm run dev
```

Server runs on `http://localhost:3001`

### 3. Start the Frontend

```bash
cd client
npm install
npm run dev
```

App runs on `http://localhost:5173`

### 4. Open in Browser

Visit `http://localhost:5173` and click **"Create New Room"**!

## 💡 How It Works

1. **Create a Room** - Click "Create New Room" on the homepage
2. **Enter Your Name** - Choose a display name for the chat
3. **Share the Link** - Send the room URL to others
4. **Chat!** - Messages are real-time and ephemeral

## 🔧 Configuration

### Server Environment Variables (`.env`)

```env
PORT=3001
CLIENT_URL=http://localhost:5173
```

### Socket.io Client Config (`client/src/socket.js`)

```javascript
const SOCKET_SERVER_URL = 'http://localhost:3001';
```

## 📝 API Events

### Client → Server

| Event | Payload | Description |
|-------|---------|-------------|
| `join_room` | `{ roomId, username }` | Join a chat room |
| `send_message` | `{ message }` | Send a message |

### Server → Client

| Event | Payload | Description |
|-------|---------|-------------|
| `user_joined` | `{ username, userCount }` | Confirmation of joining |
| `receive_message` | `{ id, sender, message, timestamp }` | New message |
| `user_activity` | `{ type, message, userCount }` | Join/leave notifications |

## 🎨 Customization

### Change Theme Colors

Edit `client/tailwind.config.js`:

```javascript
colors: {
  'neon': {
    green: '#00ff00',  // Change this for different accent color
  }
}
```

## 📄 License

MIT License - Feel free to use and modify!

---

<p align="center">
  Made with 💚 by <strong>NSM</strong>
</p>
