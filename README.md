# Resonance: Core — Trello Power-Up Importer

Adds an **"Import Resonance: Core"** button to your board. Click it, authorize once, and import each part of the board with one click.

## Setup (about 10 minutes)

### 1. Host it on GitHub Pages
1. Make a new **public** GitHub repo, e.g. `rc-trello-powerup`.
2. Upload every file in this folder to the repo root.
3. Repo **Settings → Pages →** Source: *Deploy from a branch*, Branch: `main`, folder `/ (root)`. Save.
4. Your URL will be `https://YOUR-USERNAME.github.io/rc-trello-powerup/`

### 2. Create the Power-Up
1. Go to https://trello.com/power-ups/admin → **New**.
2. Pick the workspace your board is in. You need to be a workspace admin.
3. **Iframe connector URL:** your GitHub Pages URL from step 1.
4. Fill in name, email, support contact, and click **Create**.
5. **Capabilities tab:** turn on **Board buttons**, **Authorization status**, and **Show authorization**.
6. **API Key tab:** generate/copy your **API key**. Under **Allowed origins**, add `https://YOUR-USERNAME.github.io`.

### 3. Add your key
Open `config.js` in the repo and replace `PASTE_YOUR_API_KEY_HERE` with your API key. Commit. (The key is safe to be public. Never put a token in any file.)

### 4. Use it
1. Make a new empty board named **Resonance: Core**.
2. Board menu → **Power-Ups → Custom** → add **Resonance: Core Importer**.
3. Click **Import Resonance: Core** in the board header → **Authorize** → **Import** Part 1.
4. Later: Part 2 after the Arc 1 finale, Part 3 as each Dark World arc starts.

The importer remembers which parts it already imported on that board and warns before importing duplicates.

## Updating the board content
Edit `resonance_core_trello.json` in the repo. New imports use the updated file.

## If something breaks
Copy the red error line from the importer's log and send it back to Claude.
