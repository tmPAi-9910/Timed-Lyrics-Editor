# Timed Lyrics Editor

A completely static, browser-based timed lyrics editor for creating and editing synchronized lyrics (LRC format) for music tracks.

## Features

- **Tabbed Interface**: Organized interface with LRC Editor, Preview, and Settings tabs
- **Audio Playback**: Load and play audio files (MP3, WAV, OGG, etc.)
- **LRC Import/Export**: Read and write LRC format lyrics files
- **Timestamp Editor**: Add, edit, and remove timestamps synchronized with audio
- **Live Preview**: Preview lyrics with automatic highlighting during playback
- **Dark Mode**: Toggle between light and dark themes
- **Keyboard Shortcuts**: Full keyboard control for efficient workflow
- **Auto-Highlight**: Current playback position automatically highlights in lyrics
- **Click-to-Seek**: Click on any timestamp to jump to that position
- **No Build Required**: Pure HTML/CSS/JavaScript - no dependencies or build tools needed

## Usage

### Getting Started

Simply open `index.html` in a modern web browser (Chrome, Firefox, Edge, Safari).

### Tabs Overview

The editor is organized into three tabs:

1. **LRCエディタ (LRC Editor)** - Main editing interface with audio controls and lyrics editor
2. **プレビュー (Preview)** - View lyrics with timestamps, automatically highlights current playback position
3. **設定 (Settings)** - Configure app settings, view keyboard shortcuts, and manage local data

### Basic Workflow

1. **Load Audio**: In the LRC Editor tab, click "📁 音楽ファイル" and select an audio file (required)
2. **Load Lyrics (Optional)**: Click "📝 LRCファイル" to import existing LRC file, or click "➕ 行追加" to create new lines
3. **Play Audio**: Use Space key or the play button to start playback
4. **Add Timestamps**:
   - Select a line by clicking it or using Arrow keys
   - Press Enter when the audio reaches the correct timing
   - Or manually edit the timestamp field
5. **Edit Lyrics**: Click on text fields to edit lyric text
6. **Preview**: Switch to the Preview tab to see your synchronized lyrics with live playback highlighting
7. **Export**: Click "💾 エクスポート" or press Ctrl+S to download LRC file

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play/Pause |
| `Enter` | Set current time as timestamp for selected line |
| `Arrow Up` / `↓` | Select previous/next line |
| `Delete` / `Backspace` | Delete selected line |
| `Ctrl + N` | Add new line |
| `Ctrl + S` | Export LRC file |
| `Ctrl + D` | Toggle dark mode |
| `←` / `→` | Rewind/Forward 5 seconds |
| `Esc` | Close help modal |

### LRC Format

The editor supports standard LRC format:
```
[mm:ss.xx]Lyric text here
```

Example:
```
[00:00.00]First verse begins here
[00:05.23]With the music playing
[00:12.45]Synchronized to the beat
```

## Browser Compatibility

Works in all modern browsers that support:
- HTML5 Audio API
- File API
- ES6+ JavaScript

Tested on: Chrome, Firefox, Edge, Safari

## Technical Details

- **No External Dependencies**: Pure vanilla JavaScript
- **Single File**: All HTML, CSS, and JavaScript in one `index.html` file
- **Tabbed Architecture**: Clean separation of concerns with LRC Editor, Preview, and Settings tabs
- **LocalStorage**: Dark mode preference is persisted
- **File API**: Uses FileReader and Blob for file operations
- **Responsive**: Adapts to different screen sizes
- **Accessibility**: Full ARIA support for tabs and controls

## License

MIT License
