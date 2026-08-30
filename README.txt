DIGITAL HERITAGE RECONSTRUCTION SYSTEM
========================================

FOLDER STRUCTURE
------------------
Digital-Heritage-Reconstruction-System/
│
├── index.html                  -> the website itself (open this)
│
├── assets/
│   └── models/                 -> the five 3D reconstructions (runtime files
│                                   used directly by the website)
│       ├── charminar.glb
│       ├── gateway-of-india.glb
│       ├── lotus-temple.glb
│       ├── qutub-minar.glb
│       └── sanchi-stupa.glb
│
├── blender-source-files/       -> original project source files for each
│                                   monument, kept for reference and to show
│                                   the modelling process behind each model
│       ├── Charminar.blend
│       ├── GatewayOfIndia.blend
│       ├── LotusTemple.blend
│       ├── QutubMinar.blend
│       └── SanchiStupa.blend
│
└── README.txt                  -> this file

HOW TO RUN THE WEBSITE
-------------------------
Modern browsers block 3D model files from loading when an HTML file is
opened by double-clicking it directly (a security restriction). Serve the
folder through a small local server instead — this takes about ten seconds:

Option A — Python (usually pre-installed):
  1. Open a terminal in this folder.
  2. Run:      python -m http.server 8000
     (or:      python3 -m http.server 8000)
  3. Open a browser and visit:   http://localhost:8000

Option B — VS Code:
  1. Install the "Live Server" extension.
  2. Right-click index.html -> "Open with Live Server".

Option C — Node.js:
  1. Run:      npx serve .
  2. Open the URL it prints.

An internet connection is needed the first time the page loads, since fonts,
the 3D viewer engine, and the reference photographs load from the web.

WHAT'S INSIDE THE WEBSITE
----------------------------
- Five fully interactive 3D reconstructions, one per monument, each set
  against a real photographic backdrop of its actual surroundings.
- History        — when, where, how each monument was built, and the story
                    behind it.
- Architecture   — a breakdown of each monument's key architectural
                    features, each with a "Focus View" button that moves
                    the 3D camera to that feature, plus audio narration.
- Gallery        — reference photography for every monument.
- Preservation   — current protection status and conservation efforts.
- Current Status — what the site looks like and how it's used today.
- Guided Tour    — a step-by-step walkthrough of each monument, launchable
                    directly on the 3D model with a dedicated on-screen
                    panel (Next/Previous navigation between waypoints).
- Quiz           — a short knowledge check for every monument.
- Audio Guide    — every major section can be read aloud using the
                    browser's built-in narrator (the speaker icons).
- View controls  — reset view, toggle auto-rotation, cycle daylight /
                    sunset / night lighting, and a fullscreen mode.

CUSTOMISING CONTENT
----------------------
All monument text, camera viewpoints, image links, tour steps and quiz
questions live in one place — the MONUMENTS array near the top of the
<script> section in index.html. Edit the fields there to correct facts,
add a viewpoint, or extend the quiz.

CREDITS
---------
Photographic references: public archival collections (Wikimedia Commons).
