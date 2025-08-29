# AI Agent Instructions for Video Player Project

## Project Overview
This project implements web-based video players for multiple platforms (YouTube, Twitch) with a focus on simplicity and user experience.

### Architecture
- Standalone HTML files for each platform player (`youtube_player.html`, `twitch_player.html`)
- Self-contained design: CSS and JavaScript included within each HTML file
- No external dependencies besides platform-specific APIs

## Key Components

### YouTube Player (`youtube_player.html`)
- Embedded iframe player with custom controls
- Local storage for view history and preferences
- Responsive design with mobile support
- Key features:
  - Video recommendations system
  - Playback controls (prev/next/replay)
  - Keyboard shortcuts
  - Loading states and error handling

### File Organization
```
player/
├── .github/
│   └── copilot-instructions.md
├── youtube_player.html
└── twitch_player.html
```

## Development Patterns

### HTML Structure
- Root container with flex layout
- Player wrapper with absolute positioning for controls
- Recommendation area with horizontal scrolling

### CSS Conventions
- Reset styles at the top
- Mobile-first responsive design
- BEM-like class naming (e.g., `rec-item`, `rec-title`)
- Use of CSS variables for theming
- Flexbox for layouts

### JavaScript Patterns
- Event-driven architecture
- Local storage for persistence
- Error handling with user feedback
- URL state management
- History tracking for recommendations

## Common Tasks

### Adding New Features
1. Locate the relevant section in the HTML file
2. Add CSS in the `<style>` section following existing patterns
3. Implement JavaScript logic in the `<script>` section
4. Test across different screen sizes

### Testing
- Manual testing in browsers
- Test keyboard shortcuts
- Verify error handling
- Check responsive design
- Validate local storage functionality

## Integration Points
- YouTube Embed API
- Browser Local Storage API
- URL History API

## Known Patterns
- Video ID validation regex: `/^[\w-]{11}$/`
- Error message timeout: 3000ms
- Player parameters: `autoplay=1&rel=0&modestbranding=1&showinfo=0&iv_load_policy=3`
