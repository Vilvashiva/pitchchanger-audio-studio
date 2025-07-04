# Audio Editor Web Application

A modern web-based audio player with pitch and speed controls, built with React and Express.js.

## Features

- **Audio File Upload**: Drag-and-drop support for MP3, WAV, and OGG files
- **Audio Player**: Full-featured player with waveform visualization
- **Pitch Control**: Adjust pitch by ±12 semitones (half-steps)
- **Speed Control**: Change playback speed from 0.5x to 2.0x
- **Real-time Processing**: Instant audio manipulation using Web Audio API
- **Export Functionality**: Download processed audio as WAV files
- **Responsive Design**: Clean, modern UI that works on all devices

## Technology Stack

### Frontend
- **React** with TypeScript
- **Vite** for fast development and optimized builds
- **shadcn/ui** components with Tailwind CSS
- **TanStack Query** for server state management
- **Web Audio API** for audio processing
- **Wouter** for lightweight routing

### Backend
- **Express.js** with TypeScript
- **Multer** for file upload handling
- **In-memory storage** for development
- **RESTful API** design

## Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <your-repo-url>
cd audio-editor
```

2. Install dependencies
```bash
npm install
```

3. Start the development server
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Deployment

### Deploy to Vercel

1. Install Vercel CLI
```bash
npm i -g vercel
```

2. Deploy to Vercel
```bash
vercel
```

3. Follow the prompts to configure your deployment

### Manual Deployment

1. Build the project
```bash
npm run build
```

2. The built files will be in the `dist` directory
3. Deploy the `dist` directory to your hosting provider

## API Endpoints

- `POST /api/upload` - Upload audio file
- `GET /api/audio-files` - Get all audio files
- `GET /api/audio-files/:id` - Get specific audio file
- `GET /api/audio-files/:id/stream` - Stream audio file
- `DELETE /api/audio-files/:id` - Delete audio file

## Audio Processing

The application uses the Web Audio API for real-time audio processing:

- **Pitch Shifting**: Currently uses a simple implementation (placeholder for advanced algorithms)
- **Speed Control**: Uses the native playbackRate property
- **Waveform Visualization**: Generated from audio buffer data
- **Export**: Renders processed audio using OfflineAudioContext

## File Support

Supported audio formats:
- MP3 (audio/mpeg)
- WAV (audio/wav) 
- OGG (audio/ogg)

Maximum file size: 50MB

## Browser Compatibility

- Chrome 66+
- Firefox 60+
- Safari 14+
- Edge 79+

(Requires Web Audio API support)

## Future Enhancements

- Advanced pitch shifting algorithms (PSOLA, phase vocoder)
- Google Drive integration (currently disabled)
- YouTube link support
- Additional audio effects (reverb, EQ, filters)
- Batch processing
- User accounts and cloud storage

## License

MIT License - feel free to use this project for personal or commercial purposes.