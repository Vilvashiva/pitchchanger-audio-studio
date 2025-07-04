# Audio Editor Application

## Overview

This is a full-stack audio editing application built with React, Express, TypeScript, and PostgreSQL. The application allows users to upload audio files, apply pitch and speed modifications, and export the processed audio. It features a modern UI using shadcn/ui components and includes Google Drive integration for file uploads.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Audio Processing**: Web Audio API for real-time audio manipulation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM (Neon serverless)
- **File Storage**: Local file system with multer for uploads
- **Session Management**: Express sessions with PostgreSQL store
- **API Design**: RESTful endpoints for audio file operations

## Key Components

### Audio Processing Pipeline
- **Upload Handler**: Multer-based file upload with MIME type validation
- **Audio Processor**: Web Audio API wrapper for pitch shifting and speed adjustment
- **Waveform Generator**: Real-time waveform visualization
- **Export System**: Client-side audio rendering and download

### Database Schema
- **Audio Files**: Stores metadata including filename, size, duration, and Google Drive integration flags
- **Processing Jobs**: Tracks audio processing tasks with pitch/speed parameters and status
- **Users**: Basic user management schema (currently unused)

### UI Components
- **AudioUpload**: Drag-and-drop file upload with Google Drive integration
- **AudioPlayer**: Full-featured audio player with waveform visualization
- **AudioControls**: Real-time pitch and speed adjustment controls
- **Waveform**: Custom canvas-based waveform visualization

## Data Flow

1. **File Upload**: User uploads audio file via drag-and-drop or file picker
2. **Processing**: Audio is stored locally and metadata saved to database
3. **Loading**: Frontend loads audio file and generates waveform data
4. **Manipulation**: Real-time pitch and speed adjustments using Web Audio API
5. **Export**: Processed audio is rendered client-side and downloaded

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL serverless connection
- **drizzle-orm**: TypeScript-first ORM for database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Headless UI components
- **multer**: File upload middleware
- **react-hook-form**: Form validation and management

### Google Drive Integration
- **Google Drive API**: For cloud file access and downloads
- **OAuth 2.0**: Authentication flow for Google services
- **Environment Variables**: API keys stored as VITE_GOOGLE_CLIENT_ID and VITE_GOOGLE_API_KEY

### Audio Processing
- **Web Audio API**: Native browser audio processing
- **Custom PitchShifter**: Simple pitch shifting implementation (placeholder for advanced algorithms)
- **Canvas API**: Waveform visualization rendering

## Deployment Strategy

### Development Setup
- **Dev Server**: Vite development server with HMR
- **Database**: PostgreSQL with Drizzle migrations
- **File Storage**: Local uploads directory
- **Environment**: NODE_ENV=development with tsx for TypeScript execution

### Production Build
- **Frontend**: Vite build with optimized bundles
- **Backend**: esbuild compilation to ESM format
- **Database**: Drizzle migrations applied via `db:push` command
- **Static Files**: Served via Express static middleware

### Configuration
- **Database URL**: Required environment variable for PostgreSQL connection
- **Google API**: Optional environment variables for Drive integration
- **Port**: Configurable server port (default Express configuration)

## Changelog

- July 04, 2025: Initial setup and core audio player implementation
- July 04, 2025: Fixed runtime errors and made app production-ready
- July 04, 2025: Added Vercel deployment configuration
- July 04, 2025: Integrated PostgreSQL database with Drizzle ORM
- July 04, 2025: Fixed critical audio processing bugs including multiple instance conflicts using singleton pattern
- July 04, 2025: Implemented working pitch shifting with buffer resampling and validation
- July 04, 2025: All core features now functional: speed control, pitch control, stop button, and reset functions
- July 04, 2025: **MAJOR UPDATE**: Successfully implemented advanced audio features:
  - Added reverb and echo effects with real-time parameter control
  - Built frequency spectrum analyzer with dominant frequency detection
  - Enhanced UI with tabbed interface (Basic Controls, Audio Effects, Frequency Analysis)
  - Fixed pitch shifting algorithm to maintain audio timing integrity
  - All audio controls now working reliably including pitch changes and stop functionality
- July 04, 2025: **PROFESSIONAL STUDIO FEATURES**: Implemented comprehensive enhancements:
  - **Project Management**: Save/load complete audio projects with all settings via localStorage
  - **Audio Presets**: Custom effect combinations with instant application
  - **Export Controls**: Professional audio export in WAV/MP3/OGG with quality settings
  - **8-Band Equalizer**: Professional EQ with presets (Rock, Pop, Jazz, Classical, etc.)
  - **Audio Filters**: Low-pass, high-pass, band-pass filters with dynamic range compression
  - **Advanced Visualization**: Real-time spectrum, waveform, and circular visualizations with capture
  - **Audio Recorder**: Built-in microphone recording with level monitoring and direct upload
  - **Audio Engine Settings**: Comprehensive configuration panel with quality presets and advanced options
  - **Enhanced UI**: 9 professional tabs for complete audio production workflow
  - **Complete Studio**: Upload/record → Edit → Apply effects → Visualize → Save projects → Export professionally
- July 04, 2025: **USER AUTHENTICATION & TRACKING SYSTEM**: Added comprehensive user management:
  - **Replit Authentication**: Full user login/logout system with session management
  - **User Profile Integration**: Profile display with avatar and user information in header
  - **Landing Page**: Professional marketing page for non-authenticated users
  - **Google Ads Integration**: Complete tracking setup for advertising and analytics
  - **User Behavior Analytics**: Track user actions, audio processing, project management, and engagement
  - **Conversion Tracking**: Monitor user interactions and feature usage for optimization
  - **Ready for Deployment**: pitchchanger.app domain purchased and configured for production

## User Preferences

Preferred communication style: Simple, everyday language.