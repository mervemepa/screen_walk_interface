# Desktop Documentary

A nostalgic Windows 95-style web application that creates automated visual collages by opening multiple windows in a cascade pattern across your desktop. Experience the aesthetic of classic computing while creating artistic digital compositions.

![Desktop Documentary Demo](demo-screenshot.png)

## ✨ Features

- **Authentic Windows 95 UI**: Complete with retro styling, taskbar, desktop icons, and classic window controls
- **Smart Collage System**: Intelligent positioning algorithm that creates visually appealing layouts
- **Automated Window Sequence**: Opens windows containing images and videos in timed intervals
- **Built-in Screen Recording**: Capture your desktop documentary as it unfolds
- **Responsive Design**: Adapts to different screen sizes while maintaining the retro aesthetic
- **Mixed Media Support**: Handles both images (JPG, PNG) and videos (MP4)
- **Real-time Clock**: Working taskbar clock that displays current time

## 🚀 Quick Start

1. **Clone or download** this repository
2. **Add your media files** to the `materials/` folder
3. **Update the media configuration** in `index.html` (line 137)
4. **Open `index.html`** in a modern web browser
5. **Click "▶ Start"** to begin your desktop documentary
6. **Optional**: Click "⏺ Record" to capture the experience

## 📁 Project Structure

```
Desktop Documentary/
├── index.html          # Main application file
├── materials/          # Your media files go here
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
└── README.md          # This file
```

## 🎮 Controls

- **▶ Start**: Begin the automated window opening sequence
- **🔄 Reset**: Close all windows and reset to initial state
- **⏺ Record**: Start/stop screen recording (saves as .webm file)

## ⚙️ Configuration

Edit the `mediaFiles` array in `index.html` to customize your documentary:

```javascript
const mediaFiles = [
  {
    name: "img1.jpg",
    type: "image",
    duration: 3000,
    path: "materials/img1.jpg",
  },
  {
    name: "video1.mp4",
    type: "video",
    duration: 5000,
    path: "materials/video1.mp4",
  },
  // Add more files...
];
```

### Parameters:

- **name**: Display name in the window title
- **type**: 'image' or 'video'
- **duration**: How long to wait before opening the next window (milliseconds)
- **path**: Relative path to your media file

## 🎨 Customization

### Window Timing

Adjust opening intervals by modifying the `duration` values or the delay calculation in the `openNextWindow()` function.

### Window Sizes

The system randomly assigns three size classes:

- `small`: max-width 300px
- `medium`: max-width 400px
- `large`: max-width 500px

### Desktop Theme

Modify the CSS variables in the `<style>` section to change colors, fonts, or layout.

## 🖥️ Browser Requirements

- **Chrome/Edge**: Full support including screen recording
- **Firefox**: Full support including screen recording
- **Safari**: Basic functionality (screen recording may be limited)

### Required Browser Features:

- ES6+ JavaScript support
- CSS Grid and Flexbox
- MediaRecorder API (for screen recording)
- Display Media API (for screen capture)

## 📸 Screen Recording

The built-in screen recorder:

- Captures your entire screen or selected window
- Saves as high-quality WebM video
- Includes audio if available
- Auto-downloads when recording stops

**Note**: Your browser will prompt for screen sharing permissions when you first start recording.

## 🎯 Use Cases

- **Digital Art**: Create unique desktop compositions
- **Presentations**: Demonstrate software or concepts with retro flair
- **Nostalgia Projects**: Recreate the Windows 95 experience
- **Video Content**: Record desktop documentaries for social media
- **Interactive Installations**: Use in galleries or exhibitions

## 🔧 Troubleshooting

**Windows not opening?**

- Check that your media files exist in the `materials/` folder
- Verify file paths in the `mediaFiles` configuration
- Check browser console for error messages

**Recording not working?**

- Ensure you're using HTTPS (required for screen recording)
- Grant screen sharing permissions when prompted
- Try a different browser if issues persist

**Performance issues?**

- Reduce the number of simultaneous windows
- Optimize large image/video files
- Close other browser tabs to free up memory

## 🤝 Contributing

Feel free to submit issues, feature requests, or pull requests! Some ideas for enhancements:

- Additional retro OS themes (Windows 98, Mac OS Classic)
- Sound effects and background music
- More window animation styles
- Export options (GIF, MP4)
- Drag and drop file uploading

## 📄 License

This project is open source. Feel free to use, modify, and distribute as needed.

## 🙏 Acknowledgments

Inspired by the aesthetic and user experience of Windows 95 and early desktop computing environments.

---

**Desktop Documentary** - Bringing retro computing aesthetics to modern web experiences.
