# Screen Walk

A web-based visual performance tool for creating dynamic desktop compositions with images, videos, PDFs, audio, and live text. Built with a Windows 95 aesthetic, Screen Walk enables artists and performers to orchestrate multi-window presentations with precise control over timing, layout, and media playback.

![Screen Walk Interface](materials/screenshot.png)

## License

Screen Walk © 2026 Merve Mepa  
Licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)

You may share this project with attribution, but commercial use and modifications are prohibited.

License details: https://creativecommons.org/licenses/by-nc-nd/4.0/

## Overview

Screen Walk is a single-page web application designed for visual performance and digital art creation. The application opens media files in randomly positioned windows that can be controlled programmatically or manually. Windows maintain their original aspect ratios and are positioned within a safe zone that avoids overlapping control panels.

Key characteristics:

- Client-side processing only (no server required)
- Pure HTML/CSS/JavaScript implementation
- No external dependencies
- Responsive layout with dynamic positioning
- Built-in screen recording capability

## Technical Requirements

### Supported Browsers

- Chrome/Chromium 90+ (recommended)
- Firefox 88+
- Edge 90+
- Safari 14+ (limited MediaRecorder support)

### Required Browser APIs

- File API for file uploads
- Drag and Drop API for file handling
- MediaRecorder API for screen recording
- Display Media API for screen capture
- Local Storage for settings persistence
- Blob API for media URL management

### File Format Support

- Images: JPG, PNG, GIF, WebP (max 100MB)
- Videos: MP4, WebM, MOV (max 100MB)
- PDF: PDF documents (max 100MB)
- Audio: MP3, WAV, OGG, AAC (max 50MB)

## Core Features

### Media Management

- Multi-file upload with format validation
- Drag-and-drop interface for file addition
- Playlist with drag-to-reorder functionality
- Individual item deletion
- Automatic aspect ratio preservation
- Dynamic window sizing based on content dimensions

### Window System

- Chaotic positioning algorithm with clustering
- Safe zone calculation to avoid control panel overlap
- Random size variations with weighted distribution
- Z-index management for window layering
- Draggable windows with titlebar control
- Resizable windows with corner handles
- Window focusing system

### PDF Viewer

- Integrated PDF rendering via iframe
- Zoom controls (25% to 300%)
- Pan functionality when zoomed
- Keyboard shortcuts for zoom control
- Toggle visibility (front/back positioning)
- Persistent window state

### Live Text Performance

- Always-on-top text window
- Toggle between front and back positioning
- Persistent state (does not close)
- Custom blue background (Windows 95 style)
- Monospace font for readability

### Audio Playback

- Background audio with looping
- Single audio file support
- Standard HTML5 audio controls
- Clear audio functionality

### Playback Control

- Adjustable duration per window (1-8 seconds)
- Maximum concurrent windows (3-20)
- Optional seeded randomization for reproducible layouts
- Continuous looping
- Manual start/stop control

### Screen Recording

- MediaRecorder integration
- WebM output format
- Automatic download on stop
- Permission handling for display capture

## Architecture

### File Structure

```
index_test.html        # Main application (self-contained)
README.md             # Documentation
LICENSE.md            # License information
materials/            # Assets (cursors, icons)
  └── playlist.txt    # Configuration data
```

### Key Functions

#### Media Handling

- `addFiles(fileList)` - Validates and processes uploaded files
- `addPdfFiles(files)` - Handles PDF file upload
- `validateFile(file)` - Validates file type and size
- `renderPlaylist()` - Updates playlist UI

#### Window Management

- `createWindow(item, index)` - Creates and positions media windows
- `generateChaoticPosition(index, total)` - Calculates window position within safe zone
- `getChaoticSize()` - Determines random window dimensions
- `fitMediaToRandomWindow(mediaElement)` - Adjusts window to media aspect ratio
- `closeWindow(id, instant)` - Removes window from DOM

#### Text Window

- `toggleTextWindow()` - Toggles text window front/back state
- `openTextWindow()` - Creates text performance window
- `sendTextToBack()` - Moves text window to z-index 50
- `bringTextToFront()` - Moves text window to z-index 9999

#### PDF Window

- `openPdfWindow()` - Creates PDF viewer window
- `initializePdfZoom(pdfWindow)` - Sets up zoom and pan controls
- `sendPdfToBack()` - Moves PDF window to z-index 50
- `bringPdfToFront()` - Moves PDF window to z-index 9999
- `closePdfWindow()` - Closes and cleans up PDF window

#### Layout System

- Safe zone calculation: `screenWidth - controlsPanelWidth - windowWidth`
- Dynamic positioning adjusts to browser dimensions
- Cluster-based random distribution (40% clustering probability)
- Edge preference algorithm (30% probability)

### State Management

#### Global Variables

```javascript
let mediaItems = []; // Visual media queue
let audioItems = []; // Audio files
let pdfItems = []; // PDF documents
let currentPdf = null; // Active PDF
let pdfWindow = null; // PDF window reference
let isPdfWindowOpen = false; // PDF window state
let textWindow = null; // Text window reference
let isTextWindowOpen = false; // Text window state
let openWindows = []; // Currently displayed windows
let isRunning = false; // Playback state
let currentIndex = 0; // Playback position
```

### CSS Architecture

#### Z-Index Hierarchy

- Control panel: 10000+ (increments on click)
- Text window (front): 9999
- PDF window (front): 9999
- Help window: 1000
- Media windows: 100-150 (random)
- Text/PDF window (back): 50
- Desktop: 1

#### Layout System

- Fixed control panel (right side, 240px width)
- Safe zone calculation: viewport width - 280px
- Responsive grid for desktop icons
- Flexbox for control groups
- Dynamic button sizing with flex: 1

## Usage

### Basic Setup

1. Open `index_test.html` in a modern browser
2. Upload media files via "Upload Media" button
3. Configure duration and max windows settings
4. Click "Start" to begin automated playback

### PDF Integration

1. Click "Upload PDF" to select PDF file
2. PDF opens automatically in viewer window
3. Use zoom controls (+, -, 1:1) or Ctrl+scroll
4. Click and drag to pan when zoomed
5. Click "Send Back" to move behind other windows
6. Click again to bring to front

### Live Text Performance

1. Click "Live Text Box" to open text window
2. Window opens at z-index 9999 (always on top)
3. Type content in real-time
4. Click "Send Back" to move behind other windows
5. Click again to bring to front
6. Window persists until explicitly closed

### Recording Workflow

1. Click "Record" button
2. Grant screen sharing permission
3. Select entire screen or window
4. Click "Start" to begin media playback
5. Perform live text input if desired
6. Click "Record" again to stop and download

### Advanced Configuration

#### Seeded Randomization

Enter a numeric seed in "Random Seed" field for reproducible layouts. Same seed produces identical positioning across sessions.

#### Custom Duration

Adjust "Duration (s)" slider (1-8 seconds) to control time between window openings.

#### Window Limits

Set "Max Windows" (3-20) to control concurrent window count. Oldest windows close automatically when limit reached.

## Performance Considerations

### Optimization Recommendations

- Limit file count to 20-30 for optimal performance
- Keep individual files under 10MB
- Use compressed video formats (H.264)
- Close unnecessary browser tabs during recording
- Disable browser extensions if experiencing lag

### Memory Management

- Blob URLs created for all media files
- URLs revoked when items deleted
- Windows removed from DOM on close
- Automatic cleanup on reset

### Browser-Specific Issues

#### Chrome/Edge

- Full feature support
- Recommended for recording
- Hardware acceleration enabled by default

#### Firefox

- Full feature support
- May require manual hardware acceleration enable
- Recording quality may vary

#### Safari

- Limited MediaRecorder support
- PDF rendering may differ
- Some keyboard shortcuts may conflict

## Keyboard Shortcuts

| Shortcut    | Action                        |
| ----------- | ----------------------------- |
| Ctrl+T      | Toggle text window front/back |
| Ctrl++      | Zoom in (PDF)                 |
| Ctrl+-      | Zoom out (PDF)                |
| Ctrl+0      | Reset zoom (PDF)              |
| Ctrl+scroll | Zoom at cursor (PDF)          |

## Troubleshooting

### Media Not Displaying

- Verify file format compatibility
- Check file size limits (100MB)
- Inspect browser console for errors
- Try different file formats

### Windows Overlapping Control Panel

- Resize browser window to recalculate safe zone
- Manually drag windows to desired positions
- Click control panel to bring to front

### Recording Failures

- Confirm screen sharing permission granted
- Use Chrome/Edge for best results
- Close other applications to free resources
- Check available disk space

### PDF Not Rendering

- Verify PDF is not corrupted
- Try different PDF file
- Check browser PDF plugin settings
- Use alternate browser

### Text Window Not Responding

- Click window to focus
- Check z-index with browser inspector
- Refresh page if window becomes unresponsive

## Security and Privacy

All media processing occurs client-side. No data is transmitted to external servers. Files are converted to blob URLs for display and are not stored permanently unless explicitly saved by the user.

### Data Storage

- Local Storage: Control panel dimensions and settings
- Session Storage: None
- Cookies: None
- External Requests: None (except demo image URLs)

## Development

### Extending Functionality

#### Adding New Media Types

1. Update `validateFile()` function with new MIME type
2. Create handling logic in `addFiles()`
3. Modify `createWindow()` to support new content type
4. Update UI to reflect new capabilities

#### Custom Positioning Algorithms

Modify `generateChaoticPosition()` function to implement alternative distribution patterns:

- Grid-based layouts
- Spiral patterns
- Specific coordinate mapping
- Edge-aligned positioning

#### Theme Customization

CSS variables defined in `:root` control color scheme:

```css
--bar: #c0c0c0 /* Window chrome */ --bar2: #dfdfdf /* Window chrome gradient */
  --blue: #000080 /* Title bars */;
```

## API Reference

### Core Methods

#### start()

Begins automated media playback with configured settings. Loops continuously until stopped.

#### reset()

Stops playback, closes all windows, resets state.

#### createWindow(item, index)

Creates media window with random positioning and sizing.

- Parameters: `item` (media object), `index` (playback position)
- Returns: DOM element reference

#### toggleTextWindow()

Toggles text window between front (z-index 9999) and back (z-index 50).

#### toggleRecording()

Starts or stops screen recording using MediaRecorder API.

## Version History

### Version 2.0 (February 2026)

- Renamed project to Screen Walk
- Implemented persistent text window with front/back toggle
- Added PDF front/back toggle functionality
- Implemented dynamic safe zone positioning
- Added aspect ratio preservation for media
- Removed demo button
- Updated button styling (monochrome except Record)
- Reorganized control panel layout
- Added clickable control panel (bring to front)
- Updated text box background color (#000080)

### Version 1.0 (2025)

- Initial release as Desktop Documentary
- Basic media playback
- Text performance window
- Screen recording
- PDF viewer with zoom/pan

## Credits

Screen Walk © 2026 Merve Mepa

## Contact

For technical issues or feature requests, consult the browser console for detailed error messages and use standard web development debugging tools.

## Contact

For technical issues or feature requests, consult the browser console for detailed error messages and use standard web development debugging tools.
