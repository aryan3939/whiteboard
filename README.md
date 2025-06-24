# Professional Real-time Collaborative Whiteboard

A Miro-like collaborative whiteboard application built with React, TypeScript, and Socket.io for real-time collaboration.

## Live Demo

[https://whiteboardstry.onrender.com/](https://whiteboardstry.onrender.com/)

## Video Demo

[https://www.youtube.com/watch?v=jHtbhEREMNc](https://www.youtube.com/watch?v=jHtbhEREMNc/)

## Features

### Core Drawing Functionality

- **Infinite Canvas**: Zoom (25%-400%) and pan navigation
- **Drawing Tools**:
  - Freehand pen with adjustable stroke width (2-20px)
  - Basic shapes (rectangle, circle, line, arrow)
  - Text tool with font options
  - Selection tool with transform controls
- **Color System**: Color picker with recent colors history
- **Grid System**: Toggle grid visibility and snap-to-grid functionality
- **Undo/Redo**: Full history management with keyboard shortcuts

### Real-time Collaboration

- **Live Cursors**: See other users' cursor positions in real-time
- **Active Users**: Display list of currently connected users
- **Real-time Updates**: Synchronized drawing across all connected users
- **Auto-reconnection**: Handles connection drops gracefully

### Professional UI

- **Responsive Design**: Works on desktop, tablet, and mobile
- **Keyboard Shortcuts**:
  - V: Select tool
  - P: Pen tool
  - T: Text tool
  - R: Rectangle
  - C: Circle
  - L: Line
  - A: Arrow
  - Ctrl/Cmd + Z: Undo
  - Ctrl/Cmd + Y: Redo
- **Modern Interface**: Clean, intuitive design with proper spacing and typography

## Technology Stack

### Frontend

- **React 18+** with TypeScript
- **Redux Toolkit** for state management
- **Tailwind CSS** for styling
- **Socket.io Client** for real-time communication
- **HTML5 Canvas** for drawing functionality
- **Lucide React** for icons

### Backend

- **Node.js** with Express
- **Socket.io Server** for real-time communication
- **In-memory storage** for room data (can be extended with database)

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/aryan3939/whiteboard
cd whiteboard
```

2. **Install dependencies**

```bash
npm install or npm i
```

3. **Start the development server**

```bash
# Start the frontend (Vite dev server)
npm run dev

# In another terminal, start the backend server
npm run server
```

4. **Open your browser**
   Navigate to `http://localhost:5173`

   The Socket.io server will be running on `http://localhost:3001`

## Architecture

### State Management

The application uses Redux Toolkit for state management with the following structure:

- **Canvas State**: Zoom, pan, grid settings, selected tools
- **Drawing Elements**: All drawn shapes and paths
- **Users**: Connected users and their cursors
- **History**: Undo/redo functionality

### Real-time Communication

Socket.io handles real-time features:

- User presence and cursor tracking
- Element creation, updates, and deletion
- Room-based collaboration
- Automatic reconnection

### Canvas Rendering

Custom canvas utilities handle:

- Element rendering with proper transformations
- Grid system with snap-to-grid
- User cursor visualization
- Zoom and pan transformations

## License

[MIT License](LICENSE) - see the LICENSE file for details
