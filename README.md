# DevSync Arena - Realtime Code Editor

A collaborative real-time code editor that allows multiple developers to code together in the same room with live synchronization.

## Features

- 🚀 **Real-time Collaboration** - Multiple users can edit code simultaneously
- 👥 **Live User Presence** - See who's currently in the room
- 🎨 **Syntax Highlighting** - JavaScript syntax highlighting with Dracula theme
- 📋 **Room Management** - Create or join rooms with unique IDs
- 🔄 **Auto-sync** - Code changes are instantly synchronized across all clients
- 📱 **Responsive Design** - Works on desktop and mobile devices

## Tech Stack

- **Frontend**: React.js, CodeMirror, Socket.io-client
- **Backend**: Node.js, Express.js, Socket.io
- **Styling**: CSS3

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd realtime-code-editor
```

2. Install dependencies
```bash
npm install
```

3. Start the development server
```bash
npm run server:dev
```

4. In another terminal, start the React app
```bash
npm run start:front
```

5. Open your browser and navigate to `http://localhost:3000`

### Production Deployment

```bash
npm start
```

This will build the React app and start the production server.

## How to Use

1. **Create a Room**: Click "new room" to generate a unique room ID
2. **Join a Room**: Enter an existing room ID and your username
3. **Start Coding**: Begin typing and see real-time collaboration in action
4. **Share Room**: Copy the room ID to invite others
5. **Leave Room**: Click the "Leave" button when done

## Project Structure

```
src/
├── components/
│   ├── Client.js      # User avatar component
│   └── Editor.js      # CodeMirror editor wrapper
├── pages/
│   ├── Home.js        # Landing page
│   └── EditorPage.js  # Main editor interface
├── Actions.js         # Socket event constants
└── socket.js          # Socket.io client setup
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source and available under the MIT License.