<div align="center">🚀 StuCode

A Modern Desktop Text Editor & Code Visualizer
Built with Electron ⚡ & Monaco Editor 📝

   



</div>
---

✨ Highlights

🎨 Modern UI → Custom title bar, VS Code-inspired layout, light & dark themes

📂 File Management → Explorer tree, new/open/save, auto-save, live updates

📝 Editor Power → Monaco engine, multi-tabs, syntax highlighting, zoom controls

📊 Visualizations → Flowcharts (Mermaid.js), interactive charts (D3.js), syntax trees (Tree-sitter), execution tracing

💻 Built-in Terminal → xterm.js integration, multiple/split terminals, cross-platform

🔌 Extensions → Custom marketplace, extension API, easy install/manage

⌨️ Productivity → Standard shortcuts, customizable keybindings



---

⚡ Quick Start

Prerequisites

Node.js v16+

npm or yarn


Installation

git clone https://github.com/yourusername/stucode.git
cd stucode
npm install
npm start

Build

npm run build        # Current platform
npm run build:all    # All platforms


---

📂 Project Structure

stucode/
├── main.js                # Electron main process
├── preload.js             # Secure bridge
├── renderer.js            # Renderer process
├── index.html             # UI
├── styles.css             # Styles
├── package.json           # Config & dependencies
├── src/
│   ├── menu/menuBuilder.js
│   ├── file/fileManager.js
│   ├── terminal/terminalManager.js
│   ├── visualization/
│   │   ├── mermaidRenderer.js
│   │   ├── d3Renderer.js
│   │   └── treeSitterParser.js
│   └── extensions/extensionManager.js
├── icons/
└── dist/                  # Production build


---

🛠️ Built With

⚡ Electron – Cross-platform framework

📝 Monaco Editor – Code editing engine

💻 xterm.js – Terminal integration

📊 Mermaid.js – Flowcharts & diagrams

📈 D3.js – Data visualizations

🌳 Tree-sitter – Syntax parsing

👀 Chokidar – File watching



---

💡 Usage

Editing

Open files/folders via menu or drag & drop

Multi-tab editing with syntax highlighting

Save via Ctrl/Cmd + S


Visualization

Flowcharts, syntax trees, and execution flow

Step-by-step algorithm tracing


Terminal

Toggle with `Ctrl + ``

Split into multiple terminals

Run build tasks & commands


Extensions

Browse marketplace

Install/manage easily

Enable/disable on demand



---

🎨 Customization

Themes: Light/Dark switchable in settings

Keybindings: Editable via keybindings.json

Settings: Stored in stucode-settings.json



---

🐛 Troubleshooting

❌ App won’t start → Check Node.js version, reinstall dependencies

❌ Terminal not working → Verify shell config

❌ Extensions failing → Open Developer Tools (View → Toggle DevTools)

❌ File issues → Check permissions



---

📝 FAQ

Is it free? → Yes, MIT licensed

Commercial use? → Allowed

How’s it different from VS Code? → Lightweight, visualization-focused

Languages supported? → All Monaco-supported (JS, TS, Python, Java, C++, etc.)

Updates? → Delivered via GitHub releases



---

🤝 Contributing

We ❤️ contributors!

1. Fork the repo


2. Create a feature branch → git checkout -b feature/amazing


3. Commit changes → git commit -m "Add amazing feature"


4. Push branch → git push origin feature/amazing


5. Open Pull Request




---

📄 License

Licensed under the MIT License.


---

🗺️ Roadmap

Near-term:

More visualization types

Git integration

Advanced debugging


Future:

Plugin system for visualization engines

Collaborative editing

Cloud sync

Mobile companion app



---

<div align="center">✨ Made with passion by the StuCode Team ✨
🌐 [Website] · 📚 [Docs] · ⬇️ [Download]

</div>
