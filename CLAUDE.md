# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML application for YouTube channel analysis and management. The project consists of one main file (`youtube_analyzer_complete.html`) that creates a comprehensive dashboard for analyzing YouTube channels.

## Application Architecture

### Single-File Structure
- **Complete HTML Application**: All functionality contained in `youtube_analyzer_complete.html`
- **Frontend-Only**: Pure HTML/CSS/JavaScript with no backend dependencies
- **External APIs**: Uses YouTube Data API v3 and optional Apify API for enhanced features

### Key Components

1. **API Management**
   - YouTube Data API v3 integration for channel data retrieval
   - Apify API integration for subtitle/transcript extraction (optional)
   - API keys stored in localStorage for persistence

2. **Channel Management**
   - Channel list management with local storage persistence
   - Bulk channel operations (add, update, delete)
   - Channel data caching and automatic updates

3. **Analytics Dashboard**
   - Real-time channel statistics and metrics
   - Chart.js integration for data visualization
   - Performance tracking and growth analysis

4. **Data Export/Import**
   - JSON export for channel data and analytics
   - Local storage backup and restore functionality

### Core Functions

#### API Functions
- `saveApiKey()` / `testApiKey()` - YouTube API key management
- `saveApifyApiKey()` / `testApifyApiKey()` - Apify API key management
- `getChannelInfo(channelId)` - Fetch channel data from YouTube API
- `extractChannelId(url)` - Extract channel ID from various YouTube URL formats

#### Channel Management
- `addChannelToList()` - Add new channel to tracking list
- `updateAllChannels()` - Bulk update all tracked channels
- `updateSingleChannel(channelId)` - Update specific channel data
- `removeChannel(channelId)` - Remove channel from tracking

#### Data Persistence
- `saveToStorage()` - Save all data to localStorage
- `loadSavedData()` - Load saved data on application start
- `exportData()` / `importData()` - JSON export/import functionality

### Development Notes

1. **No Build Process**: This is a standalone HTML file that can be opened directly in a browser
2. **External Dependencies**: Chart.js and Axios loaded via CDN
3. **Local Storage**: All data persisted client-side using localStorage
4. **API Requirements**: Requires YouTube Data API v3 key for core functionality

### Testing and Development

To work with this application:
1. Open `youtube_analyzer_complete.html` in a web browser
2. Configure YouTube Data API key in the application settings
3. Optionally configure Apify API key for enhanced features
4. Add YouTube channel URLs to start tracking

### Key Features

- **Multi-Channel Tracking**: Monitor multiple YouTube channels simultaneously
- **Real-time Analytics**: Live channel statistics and performance metrics
- **Data Visualization**: Charts and graphs for trend analysis
- **Export Capabilities**: JSON export for data backup and analysis
- **Responsive Design**: Mobile-friendly interface with modern styling