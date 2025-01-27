# Focus Desaturate

Forked from https://github.com/scaryrawr/gnome-focus

A GNOME Shell extension that desaturates inactive windows, helping you focus on your active window. This extension provides a clean and distraction-free desktop environment by reducing the visual impact of background windows.

## Features

- Automatic desaturation of inactive windows
- Configurable desaturation levels
- Special focus list for custom window handling
- Ignore list for windows that should remain unaffected
- Easy-to-use preferences window

## Installation

### From GNOME Extensions Website
Visit [GNOME Extensions - Focus Desaturate](https://extensions.gnome.org/extension/3924/focus-desaturate/) and toggle the switch to install.

### Manual Installation
```bash
yarn package:install
```

After installation, restart GNOME Shell:
- Press Alt+F2
- Type 'r' and press Enter

## Configuration

### Extension Preferences
Access the extension settings through:
1. GNOME Extensions app
2. Select "Focus Desaturate" settings

### Special Focus List
Create a file at `~/.config/FocusDesaturate/special_focus_desaturate.json`:

```json
[
    "Code",
    "Firefox",
    "Terminal"
]
```

Windows in this list will have custom desaturation settings that can be adjusted in preferences.

### Ignore List
Create a file at `~/.config/FocusDesaturate/ignore_focus_desaturate.json`:

```json
[
    "Toolkit",
    "zoom"
]
```

Windows in this list will never be desaturated, regardless of focus state.

## Development

### Prerequisites
- Node.js
- Yarn
- GNOME Shell

### Building
```bash
# Install dependencies
yarn install

# Build the extension
yarn build

# Package for distribution
yarn build:package

# Install locally
yarn package:install
```

### Finding Window Classes
To find a window's WM_CLASS (needed for special focus or ignore lists):
```bash
xprop | grep WM_CLASS
```
Then click on the window you want to identify.

## License
MIT

## Author
Frieser

## Contributing
Contributions are welcome! Feel free to submit issues and pull requests on GitHub.