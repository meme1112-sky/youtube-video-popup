# YouTube Clone - React Native Web App

A modern, responsive YouTube clone built with React Native that runs seamlessly on both mobile and web platforms. This application provides a YouTube-like experience with video browsing, search functionality, and an intuitive user interface.

## 🚀 Features

### Core Functionality
- **Video Discovery**: Browse popular YouTube videos with real-time data
- **Advanced Search**: Search for videos using YouTube's API
- **Infinite Scroll**: Automatic loading of more videos as you scroll
- **Category Filtering**: Filter content by categories (Music, Comedy, History, etc.)
- **Responsive Design**: Optimized for both desktop and mobile viewing

### User Interface
- **Modern Header**: Clean search bar with voice search and app launcher
- **Video Grid**: Card-based layout with hover effects and video previews
- **Interactive Elements**: Watch later, add to queue, and more options
- **Live Streaming Support**: Special indicators for live content
- **Loading States**: Smooth loading animations and error handling

### Technical Features
- **Cross-Platform**: React Native with Web support via react-native-web
- **TypeScript**: Full type safety and better development experience
- **Custom Hooks**: Reusable data fetching logic with `useYouTubeData`
- **API Integration**: Direct integration with YouTube Data API v3
- **Responsive Layout**: Adaptive grid system for different screen sizes

## 📱 Screenshots

The app features a clean, modern interface similar to YouTube with:
- Header with search functionality and user controls
- Horizontal category filter bar
- Responsive video grid with hover effects
- Video cards showing thumbnails, titles, channel info, and metadata

## 🛠️ Technology Stack

- **Frontend**: React Native 0.72.6
- **Web Support**: react-native-web
- **Language**: TypeScript
- **Bundling**: Webpack 5
- **API**: YouTube Data API v3
- **State Management**: React Hooks
- **Styling**: React Native StyleSheet

## 📋 Prerequisites

Before running this application, ensure you have:

- **Node.js**: Version 16 or higher
- **npm**: Package manager
- **YouTube API Key**: Get one from [Google Cloud Console](https://console.developers.google.com/)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp env.example .env.local
   ```
   
   Edit `.env.local` and add your YouTube API key:
   ```env
   REACT_APP_YOUTUBE_API_KEY=your_youtube_api_key_here
   ```

4. **Get YouTube API Key**
   - Go to [Google Cloud Console](https://console.developers.google.com/)
   - Create a new project or select existing one
   - Enable YouTube Data API v3
   - Create credentials (API Key)
   - Copy the API key to your `.env.local` file

## 🚀 Running the Application

### Web Development
```bash
npm run web
```
The app will open at `http://localhost:3000`

### Web Production Build
```bash
npm run web:build
```

### Mobile Development

#### Android
```bash
npm run android
```

#### iOS
```bash
npm run ios
```

### Other Commands
```bash
# Start Metro bundler
npm start

# Type checking
npm run type-check

# Linting
npm run lint

# Testing
npm test

# Clean cache
npm run clean
```

## 📁 Project Structure

```
frontend/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── CategoryFilter.tsx
│   │   ├── ModernHeader.tsx
│   │   ├── VideoCard.tsx
│   │   ├── VideoGrid.tsx
│   │   └── VideoHoverPopup.tsx
│   ├── hooks/               # Custom React hooks
│   │   └── useYouTubeData.ts
│   ├── services/           # API services
│   │   └── YouTubeService.ts
│   ├── config/             # Configuration files
│   │   └── environment.ts
│   └── assets/             # Static assets
├── web/                    # Web-specific files
│   ├── index.html
│   ├── index.tsx
│   └── WebApp.tsx
├── android/                # Android-specific code
├── ios/                    # iOS-specific code
├── App.tsx                 # Main app component
├── package.json
└── webpack.config.js       # Webpack configuration
```

## 🔌 API Integration

The app integrates with YouTube Data API v3 to provide:

- **Popular Videos**: Fetch trending content
- **Search Results**: Search for specific videos
- **Video Details**: Thumbnails, duration, view counts, channel info
- **Pagination**: Load more results with next page tokens

### API Endpoints Used
- `GET /videos` - Popular videos
- `GET /search` - Search videos
- `GET /channels` - Channel information

## 🎨 Customization

### Adding New Categories
Edit the categories array in `web/WebApp.tsx`:
```typescript
const categories = [
  'All',
  'Your New Category',
  // ... existing categories
];
```

### Styling
All styles are defined using React Native's StyleSheet API. Modify component styles directly in their respective files.

### API Configuration
Update API settings in `src/config/environment.ts`:
```typescript
export const YOUTUBE_API_KEY = "your_api_key";
```

## 🐛 Troubleshooting

### Common Issues

1. **API Key Issues**
   - Ensure your YouTube API key is valid
   - Check that YouTube Data API v3 is enabled
   - Verify the API key has proper permissions

2. **Build Issues**
   - Clear cache: `npm run clean`
   - Delete node_modules and reinstall: `rm -rf node_modules && npm install`

3. **Web Development Issues**
   - Ensure port 3000 is available
   - Check webpack configuration

## 📝 Development Notes

- The app uses React Native's cross-platform components
- Web-specific features are handled via platform detection
- All API calls are made through the custom `YouTubeService`
- State management is handled with React hooks
- TypeScript provides type safety across the codebase

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔗 Links

- [React Native Documentation](https://reactnative.dev/)
- [YouTube Data API](https://developers.google.com/youtube/v3)
- [React Native Web](https://github.com/necolas/react-native-web)

## 📞 Support

For support and questions, please contact the development team or create an issue in the repository.

---

**Built with ❤️ using React Native and TypeScript**
