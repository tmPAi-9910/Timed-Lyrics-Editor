# Timed Lyrics Editor

A completely static, browser-based timed lyrics editor with a minimal editor-style design for creating and editing synchronized lyrics (LRC format) for music tracks.

## Features

- **Minimal Editor-Style Design**: High contrast grayscale interface with clean lines and minimal rounded corners
- **1-Column Layout**: Streamlined single-column layout for focused editing
- **4-Tab Interface**: Organized interface with Lyric, Syncer, Preview, and Settings tabs
- **Clickable Progress Bar**: Seek to any position by clicking the progress bar
- **Icon-Only Playback Controls**: Clean icon-based music controls (Play/Pause, Stop, Rewind, Forward)
- **Audio Playback**: Load and play audio files (MP3, WAV, OGG, etc.)
- **LRC Import/Export**: Read and write LRC format lyrics files
- **Direct Text Editing**: Large textarea in Lyric tab for direct LRC content editing
- **Sync Mode**: Set timestamps using keyboard shortcuts (T/Enter keys)
- **Empty Timing Support**: Insert timestamp-only lines for instrumental breaks (Y key)
- **Animated Preview**: Live preview with fade-in, smooth scroll, and glow effects
- **Dark Mode**: Toggle between light and dark themes (grayscale focused)
- **Tab Synchronization**: Changes in one tab automatically reflect in others
- **Full Keyboard Control**: Complete keyboard shortcut support for efficient workflow
- **Auto-Highlight**: Current playback position automatically highlights in lyrics
- **requestAnimationFrame Loop**: Smooth 20fps updates for UI and playback
- **No Build Required**: Pure HTML/CSS/JavaScript - no dependencies or build tools needed

## Usage

### Getting Started

Simply open `index.html` in a modern web browser (Chrome, Firefox, Edge, Safari).

### Tabs Overview

The editor is organized into four tabs:

1. **Lyric Tab** - Large textarea for direct LRC content editing (pure text editor behavior)
2. **Syncer Tab** - Display lyrics with timestamp column, use T key to set timestamps
3. **Preview Tab** - Animated preview with fade-in, smooth scroll, and glow effects
4. **Settings Tab** - Configure app settings, view keyboard shortcuts, and manage local data

### Basic Workflow

1. **Load Audio**: Click the "Audio" button to load an audio file
2. **Edit Lyrics**: Use the Lyric tab to edit LRC content directly or load an existing LRC file
3. **Sync Timestamps**: In the Syncer tab, play audio and press T when lyrics start
4. **Empty Timing**: Press Y to insert timestamp-only lines for instrumental breaks
5. **Preview**: Check the Preview tab to see synchronized lyrics with animations
6. **Export**: Click "Export" or press Ctrl+S to save LRC file

### Keyboard Shortcuts

#### Global (all tabs)
| Key | Action |
|-----|--------|
| `Space` / `K` | Play/Pause |
| `←` / `→` | Rewind/Forward 5 seconds |
| `Ctrl + ←` / `→` | Previous/Next tab |
| `Ctrl + 1/2/3/4` | Switch to Lyric/Syncer/Preview/Settings tab |
| `Ctrl + S` | Export LRC file |
| `Ctrl + D` | Toggle dark mode |
| `Esc` | Close modal |

#### Lyric Tab
Standard text editor behavior only (Enter, Backspace, Ctrl+Z, etc.)

#### Syncer Tab
| Key | Action |
|-----|--------|
| `T` / `Enter` | Set timestamp to current line and move to next |
| `Y` | Insert Empty Timing (timestamp only) and move to next |
| `↑` / `↓` | Move to previous/next line |

#### Preview Tab
Read-only only

#### Settings Tab
None

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
[01:00.00]
```

Note: Lines with only a timestamp (e.g., `[01:00.00]`) are "Empty Timing" lines used for instrumental breaks, section separators, or paragraph breaks.

## Design

### Color Scheme

The editor uses a high contrast grayscale design:

- **Light Mode**: `#e3e3e3` / `#333333` (text)
- **Dark Mode**: `#1a1a1a` / `#e3e3e3` (text)
- **Minimal rounded corners**: 4px for buttons, minimal for panels
- **Clean lines**: Sharp editor-style aesthetics

### UI Components

- **Progress Bar**: Clickable seek bar with smooth fill animation
- **Playback Controls**: Icon-only buttons (24x24 Material Symbols SVGs)
- **Tab Navigation**: Rounded minimal tabs with active indicators
- **Lyric Tab**: Large monospace textarea for direct editing
- **Syncer Tab**: Grid layout with line number, timestamp, and text columns
- **Preview Tab**: Animated lyrics with fade-in, smooth scroll, and glow effects

## Browser Compatibility

Works in all modern browsers that support:
- HTML5 Audio API
- File API
- ES6+ JavaScript
- requestAnimationFrame

Tested on: Chrome, Firefox, Edge, Safari

## Technical Details

- **No External Dependencies**: Pure vanilla JavaScript
- **Single File**: All HTML, CSS, and JavaScript in one `index.html` file
- **4-Tab Architecture**: Clean separation with Lyric, Syncer, Preview, and Settings tabs
- **Tab Synchronization**: Real-time sync between tabs
- **LocalStorage**: Dark mode preference is persisted
- **File API**: Uses FileReader and Blob for file operations
- **requestAnimationFrame Loop**: 20fps (50ms) updates for smooth playback highlighting
- **Responsive**: Adapts to different screen sizes
- **Accessibility**: Full ARIA support for tabs and controls
- **Minimal Editor-Style**: High contrast grayscale with sharp lines

## License

MIT License
