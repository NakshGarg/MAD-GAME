🎮 Drive Mad – Web Game (HTML + WASM)

Drive Mad is a browser-based physics driving game built using WebAssembly (WASM) and rendered via HTML5 Canvas.
This repository contains an HTML wrapper that loads and runs the game using assets hosted on a CDN.

The project demonstrates how modern web games compiled from native code (C/C++) can be executed efficiently in the browser using Emscripten.

🚀 Live Preview

If deployed correctly, the game runs directly in the browser with no installation required.

🧠 Tech Stack

HTML5 – Page structure and layout

CSS – UI styling and loading screen

JavaScript – Game bootstrapping and runtime logic

WebAssembly (WASM) – High-performance game execution

Canvas API – Rendering engine

Emscripten – Compiles native code to WebAssembly

Poki SDK – Game lifecycle hooks (ads, pause/resume)

📂 Project Structure
Drive-Mad/
│
├── index.html              # Main HTML entry point
├── webapp/
│   ├── fancade.css         # Game UI & layout styles
│   ├── index.js            # Auto-generated Emscripten loader
│   ├── source_min.js       # Game-specific logic
│   ├── cover.jpg           # Game cover image
│   └── favicon.ico         # Favicon
│
├── poki-sdk.js              # Poki platform SDK
└── README.md                # Project documentation

⚙️ How It Works (High Level)

The browser loads index.html

<base> tag redirects all assets to the CDN

JavaScript initializes a fake Poki environment

Emscripten loader (index.js) downloads the .wasm file

Game renders inside an HTML5 <canvas>

User input is captured and processed in real time

This approach allows near-native performance directly in the browser.

🖥️ How to Run Locally
Method 1: Using Live Server (Recommended)

Install VS Code

Install Live Server extension

Right-click index.html → Open with Live Server

Method 2: Using Python HTTP Server
python -m http.server 8000


Then open:

http://localhost:8000


⚠️ Important:
Opening the file directly (file://) may cause WASM loading issues. Always use a local server.

📱 Mobile Support

Fully responsive

Touch controls supported

Optimized viewport settings

Zoom disabled for better gameplay

⚠️ Disclaimer

This project is for educational and learning purposes only.

Assets and game logic belong to their respective owners

Not intended for commercial redistribution

Demonstrates WASM-based game embedding and hosting techniques

If you plan to build your own game, use this project as a technical reference, not a production template.

📚 Learning Outcomes

By exploring this project, you’ll understand:

How WebAssembly games are loaded in browsers

How Emscripten-generated JS works

Canvas-based rendering pipelines

Game bootstrapping and asset loading

CDN-based hosting strategies

🧩 Future Improvements

Clean HTML structure (remove nested documents)

Add CSP & security headers

Replace external dependencies with local assets

Improve accessibility

Modularize JS logic

👤 Author

Naksh Garg
B.Tech CSE | Web Development & System Design
GitHub: https://github.com/NakshGarg
