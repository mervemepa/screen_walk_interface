# Desktop Documentary - Complete User Guide

A nostalgic Windows 95-style web application for creating automated visual collages and live text performances. Transform your media collection into artistic desktop documentaries with authentic retro aesthetics.

![Desktop Documentary Demo](demo-screenshot.png)

## 🎯 What is Desktop Documentary?

Desktop Documentary creates **automated visual performances** by opening multiple windows containing your images and videos in intelligent cascade patterns across a virtual desktop. Perfect for:

- **Performance Art**: Live text performances with visual backgrounds
- **Digital Art**: Creating unique desktop compositions
- **Content Creation**: Recording artistic desktop experiences
- **Nostalgia Projects**: Experiencing classic Windows 95 computing

---

## ✨ Complete Feature List

### 🖼️ **Media Management**

- **File Upload**: Select multiple images (JPG, PNG, GIF, WebP) and videos (MP4, WebM, MOV)
- **Drag & Drop**: Drag files directly onto the desktop
- **Demo Mode**: Quick start with 5 sample images from Picsum
- **Dynamic Playlist**: Resizable media list with scroll support
- **Individual Delete**: Remove items with trash icon (🗑️)
- **Drag Reordering**: Reorganize playlist by dragging items

### 🎮 **Playback Controls**

- **Smart Timing**: Adjustable delays between windows (1-8 seconds)
- **Window Limits**: Control maximum open windows (3-20)
- **Seeded Random**: Reproducible layouts using custom seeds
- **Automatic Looping**: Continuous playback for extended performances
- **Manual Controls**: Start, Reset, and individual window management

### 📝 **Text Performance**

- **Live Text Window**: Resizable notepad-style window for real-time typing
- **Performance Ready**: Type during recordings for multimedia art
- **Keyboard Shortcuts**: `Ctrl+T` to toggle, `Ctrl+Shift+C` to clear text
- **Classic Styling**: Authentic Windows 95 notepad appearance
- **Draggable**: Position text window anywhere on screen

### 🎥 **Recording & Capture**

- **Built-in Screen Recording**: Capture your entire performance
- **High Quality**: WebM format with audio support
- **Auto-download**: Saves recording when stopped
- **Browser Permissions**: Handles screen sharing requests

### 🖱️ **Window Interaction**

- **Draggable Windows**: Move any window by dragging titlebar
- **Window Controls**: Minimize (transparency), maximize, and close
- **Smart Positioning**: Intelligent grid-based layout with organic variation
- **Size Variety**: Random small/medium/large window sizes

### 🔧 **Interface Customization**

- **Resizable Panel**: Drag left edge to expand control panel (200px-500px)
- **Resizable Playlist**: Drag bottom-right corner to expand media list (60px-300px)
- **Persistent Settings**: Remembers your preferred panel sizes
- **Responsive Design**: Adapts to different screen sizes

---

## 🚀 Quick Start Guide

### **1. Initial Setup**

1. Open `index_test.html` in a modern web browser (Chrome recommended)
2. You'll see the classic Windows 95 desktop with control panel on the right

### **2. Add Media**

**Option A - Upload Files:**

- Click **"📥 Medya Ekle"**
- Select multiple images/videos from your computer
- Files appear in the playlist below

**Option B - Demo Mode:**

- Click **"✨ Demo"** for 5 sample images
- Perfect for testing and learning

**Option C - Drag & Drop:**

- Drag files directly from your computer onto the desktop
- Multiple files supported

### **3. Configure Settings**

- **Süre (Duration)**: Adjust time between window openings
- **Maks Pencere**: Set maximum simultaneous windows
- **Rastgele Tohum**: Enter number for consistent layouts (leave blank for random)

### **4. Start Your Documentary**

- Click **"▶ Başlat"** to begin the automated sequence
- Windows will open in timed intervals with your media
- **Automatic Looping**: Starts over when all media played

### **5. Add Live Text Performance** _(Optional)_

- Click **"📝 Text"** to open text performance window
- Type live during playback for multimedia performances
- Resize and position the text window as needed

### **6. Record Your Performance** _(Optional)_

- Click **"⏺ Kayıt"** to start screen recording
- Grant screen sharing permission when prompted
- Click again to stop and download recording

### **7. Interactive Controls**

- **Drag Windows**: Click and drag any window titlebar to reposition
- **Window Controls**: Use `_`, `□`, `×` buttons in window corners
- **Reset**: Click **"🔄 Reset"** to close all windows and stop

---

## 🎨 Advanced Usage

### **Creating Reproducible Layouts**

```
1. Load your media files
2. Enter a number in "Rastgele Tohum" (e.g., 12345)
3. Start documentary
4. Same seed = same layout every time
```

### **Performance Art Setup**

```
1. Load artistic images/videos
2. Open text window (📝 Text button)
3. Position text window for visibility
4. Start recording (⏺ Kayıt)
5. Begin documentary (▶ Başlat)
6. Type live text during playback
7. Stop recording when complete
```

### **Long Performance Sessions**

```
1. Set higher "Maks Pencere" (15-20)
2. Use shorter "Süre" intervals (1-2 seconds)
3. Documentary will loop automatically
4. Text window stays open for continuous performance
```

### **Custom Timing Per File**

- Each file type has default timing (images: 3s, videos: 4s)
- Modify timing in playlist if needed
- Videos play their full length regardless of timing setting

---

## 🔧 Technical Details

### **Browser Requirements**

- **Recommended**: Chrome/Edge (full feature support)
- **Compatible**: Firefox (full support)
- **Limited**: Safari (basic features, recording may not work)

### **Required Browser Features**

- File API (for uploads)
- Drag & Drop API
- MediaRecorder API (for screen recording)
- Display Media API (for screen capture)
- Local Storage (for settings)

### **File Format Support**

- **Images**: JPG, JPEG, PNG, GIF, WebP (up to 100MB each)
- **Videos**: MP4, WebM, MOV (up to 100MB each)

### **Performance Tips**

- **Optimal file count**: 5-20 media files
- **Recommended file size**: Under 10MB each for smooth performance
- **Browser memory**: Close other tabs during recording
- **Recording quality**: Use fullscreen mode for best results

---

## 🎮 Keyboard Shortcuts

| Shortcut       | Action                                |
| -------------- | ------------------------------------- |
| `Ctrl+T`       | Toggle text performance window        |
| `Ctrl+Shift+C` | Clear text (when text window focused) |
| `Drag`         | Move windows or resize panels         |
| `Drop`         | Add files to desktop                  |

---

## 🔍 Troubleshooting

### **Media Not Loading**

- Check file formats are supported
- Ensure files are under 100MB
- Try refreshing browser
- Check browser console for errors

### **Windows Not Opening**

- Verify playlist has media items
- Check browser console for JavaScript errors
- Try clearing browser cache
- Ensure no popup blockers active

### **Recording Issues**

- **Chrome/Firefox**: Should work fully
- **Safari**: May have limitations
- **Permissions**: Grant screen sharing when prompted
- **HTTPS**: Some browsers require secure connection
- **Performance**: Close unnecessary browser tabs

### **Performance Issues**

- Reduce "Maks Pencere" setting
- Use smaller image files
- Close other applications
- Try incognito/private browsing mode

### **Panel/Window Issues**

- **Resize not working**: Try dragging from exact edges
- **Windows stuck**: Use Reset button
- **Text window missing**: Click 📝 Text button again

---

## 🎯 Creative Ideas & Use Cases

### **Art Projects**

- **Memory Collages**: Use personal photos with stream-of-consciousness text
- **Poetry Performances**: Write live poetry as images cascade
- **Visual Narratives**: Tell stories through image sequences and live text
- **Abstract Compositions**: Use random seeds for unexpected layouts

### **Educational Uses**

- **Digital Literacy**: Demonstrate how early computer interfaces worked
- **Art History**: Recreate desktop aesthetic movements
- **Media Studies**: Explore relationship between text and image

### **Performance Art**

- **Live Streaming**: Use for Twitch/YouTube creative streams
- **Gallery Installations**: Set up on large screens for public interaction
- **Workshop Activities**: Collaborative storytelling sessions
- **Digital Theater**: Create desktop-based performances

### **Personal Projects**

- **Memory Documentation**: Family photos with live commentary
- **Creative Journaling**: Daily visual and text entries
- **Mood Boards**: Dynamic collections that evolve over time
- **Digital Scrapbooking**: Interactive memory preservation

---

## 💾 Data & Privacy

### **Local Storage Only**

- All files processed locally in browser
- No uploads to servers
- Complete privacy protection
- Data cleared when browser cache cleared

### **File Handling**

- Files converted to blob URLs for display
- Memory cleaned up when items deleted
- No permanent storage without user action
- Recording files downloaded to user's computer

---

## 🔄 Version History & Updates

### **Current Version: 2.0**

- ✅ File upload system
- ✅ Text performance window
- ✅ Automatic looping
- ✅ Resizable interface
- ✅ Individual delete buttons
- ✅ Drag & drop reordering
- ✅ Screen recording
- ✅ Smart positioning algorithm

### **Future Enhancements** _(Ideas)_

- Multiple desktop themes (Mac OS Classic, etc.)
- Sound effects and background music
- Export configurations
- Collaborative sessions
- Mobile touch support
- WebGL effects
- AI-generated content integration

---

## 🤝 Support & Community

### **Getting Help**

- Check this README for common issues
- Use browser developer tools to check console errors
- Try different browsers if problems persist
- Test with demo mode first

### **Contributing Ideas**

- Performance art techniques
- Creative use cases
- Technical improvements
- Interface enhancements
- New feature suggestions

---

## 📄 Technical Implementation

### **Core Architecture**

- **Frontend Only**: Pure HTML/CSS/JavaScript
- **No Dependencies**: No external libraries required
- **Modern APIs**: Uses latest browser capabilities
- **Responsive Design**: CSS Grid and Flexbox
- **Event-Driven**: Clean separation of concerns

### **File Structure**

```
Desktop Documentary/
├── index_test.html     # Complete application (single file)
├── README.md          # This documentation
└── demo-images/       # Optional demo assets
```

### **Key Functions**

- `addFiles()` - Handle file uploads and drag-drop
- `start()` - Begin documentary playback with looping
- `createWindow()` - Generate positioned media windows
- `toggleTextWindow()` - Manage text performance window
- `toggleRecording()` - Handle screen capture recording

---

**Desktop Documentary** - Transform your media into interactive visual performances with authentic Windows 95 nostalgia.

_Last Updated: October 2025 | Version 2.0_
