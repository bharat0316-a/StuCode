# StuCode - Desktop Text Editor and Code Visualizer

![StuCode](https://img.shields.io/badge/StuCode-Desktop%20Editor-blueviolet) ![Built with](https://img.shields.io/badge/Built%20with-Electron-47848F) ![Editor](https://img.shields.io/badge/Editor-Monaco-0078D4) ![License](https://img.shields.io/badge/License-MIT-green)

StuCode is a powerful desktop text editor and code visualizer built with Electron and Monaco Editor, designed to provide a VS Code-like experience with advanced visualization capabilities and a completely customizable UI.

## Features

✨ **Modern Interface**
- Custom Title Bar: Completely custom title bar with minimize, maximize, and close buttons
- VS Code-inspired UI: Familiar interface with sidebar, editor area, and status bar
- Theme Support: Light and dark themes with persistence
- Responsive Design: Adapts to different screen sizes and layouts

📁 **File Management**
- Advanced File Operations: New file, new folder, open file, open folder, save, save all, save as
- File Explorer: Tree view of your project structure with icons
- Auto Save: Configurable auto-save functionality
- File Watching: Real-time updates when files change externally

🧩 **Editor Capabilities**
- Monaco Editor: The same editor that powers VS Code
- Syntax Highlighting: Support for multiple programming languages
- Multiple Tabs: Tabbed interface for working with multiple files
- Word Wrap: Configurable word wrapping
- Zoom Controls: Adjust text size with zoom in/out buttons

⚡ **Code Visualization**
- Mermaid.js Integration: Generate flowcharts and diagrams from your code
- D3.js Visualizations: Create interactive data visualizations
- Tree-sitter Parsing: Advanced code parsing for syntax trees and analysis
- Execution Flow: Visualize code execution with tracing

🔧 **Terminal Integration**
- Integrated Terminal: Built-in terminal using xterm.js
- Multiple Terminals: Support for split terminals
- Task Running: Run build tasks and execute code directly
- Platform Support: Works with cmd/PowerShell on Windows and default Linux terminal

🧩 **Extensibility**
- Extension System: Install and manage extensions
- Marketplace: Browse and install extensions from a custom marketplace
- API for Extensions: Well-defined API for extension developers

⌨ **Keyboard Shortcuts**
- Comprehensive Shortcuts: All standard editor shortcuts (Ctrl/Cmd+S, Ctrl/Cmd+Z, etc.)
- Customizable: Configurable keyboard shortcuts
- Menu Integration: All menu actions have associated shortcuts

## Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Installation Steps
1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/stucode.git
   cd stucode
   ```
2. Install dependencies
   ```bash
   npm install
   ```
3. Start the application
   ```bash
   npm start
   ```

### Building for Production
```bash
# Build for current platform
npm run build

# Build for all platforms
npm run build:all
```

## Project Structure
```
stucode/
├── main.js                 # Electron main process
├── preload.js             # Secure bridge between main and renderer
├── renderer.js            # Renderer process logic
├── index.html             # Main UI structure
├── styles.css             # Application styles
├── package.json           # Project configuration and dependencies
├── src/                   # Source code directory
│   ├── menu/
│   │   └── menuBuilder.js # Menu construction and management
│   ├── file/
│   │   └── fileManager.js # File system operations
│   ├── terminal/
│   │   └── terminalManager.js # Terminal management
│   ├── visualization/
│   │   ├── mermaidRenderer.js  # Mermaid.js integration
│   │   ├── d3Renderer.js       # D3.js integration
│   │   └── treeSitterParser.js # Tree-sitter integration
│   └── extensions/
│       └── extensionManager.js # Extension system
├── icons/                  # Application icons
└── dist/                   # Built application (after build)
```

## Usage

### Basic Editing
1. Open a file or folder using the File menu or drag-and-drop
2. Start editing your code with full syntax highlighting
3. Use tabs to switch between multiple files
4. Save your work with Ctrl/Cmd+S or through the File menu

### Code Visualization
1. Write your code in the editor
2. Use the Run menu to select a visualization option:
   - Run with Visualization: Execute code with visual execution flow
   - Show Flowchart: Generate a flowchart of your code structure
   - Show Algorithm: Visualize algorithm execution
   - Show Tracing: See step-by-step code tracing

### Terminal Usage
1. Open the terminal panel with Ctrl+` or through the View menu
2. Use the terminal toolbar to create new terminals or split existing ones
3. Run commands directly or use the Task menu to run build tasks

### Extensions
1. Open the Extensions sidebar
2. Search for extensions in the marketplace
3. Install and manage your extensions
4. Enable/disable extensions as needed

## Customization

### Themes
StuCode supports both light and dark themes. Change the theme through Settings or using the command palette.

### Keybindings
Keyboard shortcuts can be customized through the keybindings.json file in your user settings directory.

### Settings
Application settings are stored in stucode-settings.json and include:
- Editor preferences (font size, word wrap, etc.)
- Theme settings
- File handling options
- Extension configurations

## API Reference

### Extension API
Extensions can interact with StuCode through a well-defined API:

```javascript
// Example extension
module.exports = {
  activate: (context) => {
    // Register commands
    const disposable = vscode.commands.registerCommand('extension.sayHello', () => {
      vscode.window.showInformationMessage('Hello World!');
    });
    
    context.subscriptions.push(disposable);
  },
  
  deactivate: () => {
    // Clean up resources
  }
};
```

**Available API Methods**
- `vscode.commands`: Register and execute commands
- `vscode.window`: Show information, warnings, and errors
- `vscode.workspace`: Access and modify workspace files
- `vscode.languages`: Language-specific features
- `vscode.extensions`: Manage extensions

## License

StuCode is licensed under the MIT License.