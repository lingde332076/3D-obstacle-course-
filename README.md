# Key Climb

A single-page Three.js obstacle-course game with three vertical stages:

- Stage 1: 100 pastel keys
- Stage 2: 200 pastel keys
- Stage 3: 400 pastel keys

The scene uses `skybox.png` for the ocean-and-sky backdrop, `character-outfit.png` for the avatar outfit, and `head-hair.png` as the long wavy hair reference on the back of the head.

## Run locally

Double-click `index.html` to open the game directly. No localhost server is required.

If you prefer to use a local static server, from this folder run:

```powershell
python -m http.server 8000
```

If `python` is not on your PATH in the Codex workspace, use the bundled runtime instead:

```powershell
& 'C:\Users\lingd\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe' -m http.server 8000
```

The sky and character images are embedded inside the HTML, so no local asset server is required. The page still loads Three.js from jsDelivr, so internet access is required unless you later bundle Three.js into the file too.

## Controls

- Click `Start climbing` to capture the mouse and begin. Press `Esc` to pause and free the cursor.
- `WASD` or arrow keys: move
- `Space`: jump
- Drag on the game: orbit the camera
- `R`: restart the entire run
- On phones: use the virtual joystick to move, tap `JUMP`, and swipe the game view to look around.

White keys appear every ten keys and become spawn points. Falling or stepping on a vanishing key returns you to your last white checkpoint. Red keys return you to the bottom of the current stage and are spaced apart rather than appearing consecutively. Dropping keys fall after you land on them; in the final stage, vanishing keys disappear two seconds after you land on them. Reach the portal at the top of each stage to continue.
