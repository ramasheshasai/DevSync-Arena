# How to Run DevSync Arena on Your Laptop

## Prerequisites
Make sure you have these installed on your laptop:
- **Node.js** (version 14 or higher) - Download from [nodejs.org](https://nodejs.org/)
- **npm** (comes with Node.js)

## Step-by-Step Setup

### 1. Download/Clone the Project
```bash
# If you have git installed
git clone <your-repo-url>
cd realtime-code-editor

# OR download the ZIP file and extract it
```

### 2. Install Dependencies
Open terminal/command prompt in the project folder and run:
```bash
npm install
```

### 3. Add Logo Image (Optional)
- Add a `code-sync.png` file to the `public` folder
- Or replace the logo references in the code with your own image

### 4. Run the Application

#### Option A: Run Both Frontend and Backend Together (Recommended)
```bash
npm run dev
```

#### Option B: Run Frontend and Backend Separately
**Terminal 1 (Backend):**
```bash
npm run server:dev
```

**Terminal 2 (Frontend):**
```bash
npm run start:front
```

### 5. Access the Application
- Open your browser and go to: `http://localhost:3000`
- The backend server runs on: `http://localhost:5000`

## How to Use

1. **Create a Room**: 
   - Click "new room" to generate a unique room ID
   - Enter your username
   - Click "Join"

2. **Join an Existing Room**:
   - Get a room ID from someone
   - Enter the room ID and your username
   - Click "Join"

3. **Start Collaborating**:
   - Type code in the editor
   - See other users' cursors and changes in real-time
   - Copy room ID to invite more people

## Troubleshooting

### Common Issues:

1. **Port 3000 or 5000 already in use**:
   ```bash
   # Kill processes using these ports (Windows)
   netstat -ano | findstr :3000
   taskkill /PID <PID_NUMBER> /F
   
   # Kill processes using these ports (Mac/Linux)
   lsof -ti:3000 | xargs kill -9
   lsof -ti:5000 | xargs kill -9
   ```

2. **Dependencies not installing**:
   ```bash
   # Clear npm cache and reinstall
   npm cache clean --force
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **Socket connection failed**:
   - Make sure both frontend and backend are running
   - Check if firewall is blocking the ports
   - Ensure `.env` file has correct backend URL

### Development Tips:
- Use `npm run server:dev` for backend development (auto-restart on changes)
- Use `npm run start:front` for frontend development (hot reload)
- Check browser console for any JavaScript errors
- Check terminal for server errors

## Production Deployment
```bash
npm run build
npm run server:prod
```

## Need Help?
- Check the browser console for errors
- Check the terminal where the server is running for backend errors
- Make sure all dependencies are installed correctly