# 🎵 Sonora Music Player

A beautiful full-stack music player application with a distinctive vinyl-inspired aesthetic.

## Features

### Frontend
- **Beautiful UI**: Gradient backgrounds, smooth animations, and a vintage-modern aesthetic
- **Music Library**: Browse your entire music collection
- **Search**: Real-time search across songs, artists, and albums
- **Playlists**: Organize your music into custom playlists
- **Player Controls**: Play, pause, skip, volume control, and progress tracking
- **Responsive Design**: Works on desktop and mobile devices

### Backend API
- **RESTful API**: Complete CRUD operations for songs and playlists
- **File Upload**: Support for MP3, WAV, OGG, and M4A files
- **Search**: Full-text search across song metadata
- **Playlist Management**: Create and manage playlists

## Tech Stack

### Backend
- Node.js
- Express.js
- Multer (file uploads)
- CORS enabled

### Frontend
- React
- Custom CSS with animations
- DM Serif Display & Instrument Sans fonts
- HTML5 Audio API

## Setup Instructions

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

The API will run on `http://localhost:3001`

### Frontend Setup

The frontend is a single React component that can be used in any React application.

1. Copy `music-player.jsx` to your React project's components folder

2. Import and use the component:
```jsx
import MusicPlayer from './components/music-player';

function App() {
  return <MusicPlayer />;
}
```

3. Make sure your React app is running and can connect to the backend API

## API Endpoints

### Songs
- `GET /api/songs` - Get all songs
- `GET /api/songs/:id` - Get single song
- `POST /api/songs` - Add new song (with file upload)
- `PUT /api/songs/:id` - Update song
- `DELETE /api/songs/:id` - Delete song
- `GET /api/search?q=query` - Search songs

### Playlists
- `GET /api/playlists` - Get all playlists
- `POST /api/playlists` - Create new playlist
- `POST /api/playlists/:id/songs` - Add song to playlist

## API Usage Examples

### Add a new song
```bash
curl -X POST http://localhost:3001/api/songs \
  -H "Content-Type: application/json" \
  -d '{
    "title": "New Song",
    "artist": "Artist Name",
    "album": "Album Name",
    "duration": "3:45",
    "url": "https://example.com/song.mp3",
    "coverArt": "https://example.com/cover.jpg"
  }'
```

### Search for songs
```bash
curl http://localhost:3001/api/search?q=jazz
```

### Create a playlist
```bash
curl -X POST http://localhost:3001/api/playlists \
  -H "Content-Type: application/json" \
  -d '{
    "name": "My Favorites",
    "songIds": [1, 2, 3]
  }'
```

## Design Philosophy

The design features:
- **Vintage meets modern**: Inspired by vinyl records and classic hi-fi equipment
- **Smooth animations**: Subtle micro-interactions and transitions
- **Color palette**: Deep blues with gradient accents (coral to turquoise)
- **Typography**: Serif display font for headers, clean sans-serif for body
- **Glassy effects**: Frosted glass blur effects and translucent surfaces
- **Responsive interactions**: Hover states, active states, and visual feedback

## Sample Data

The backend comes pre-loaded with 5 sample songs and 2 playlists for testing purposes.

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Future Enhancements

- User authentication
- Favorites system
- Shuffle and repeat modes
- Lyrics display
- Equalizer
- Social sharing
- Dark/light theme toggle
- Mobile app version

## License

MIT License - feel free to use this project for learning or commercial purposes.
