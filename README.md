# AR-game

# Pocket Portal

Pocket Portal is a small, mobile-friendly AR treasure hunt. Find a surface, place a glowing portal, and collect five floating crystals. If your device does not support AR, play in Practice mode instead.

## Play

### Practice mode

Open `index.html` in a modern browser and choose **Practice mode**. Tap each crystal to collect it. Choose **New hunt** to play again.

### AR mode

AR requires a compatible phone and browser with WebXR immersive AR and hit-test support. The page must be served from a **secure context**: use HTTPS, or `localhost` while developing. Opening the file directly or serving it over plain HTTP will not enable AR.

1. Host the project on an HTTPS web server and open the page on your phone.
2. Allow camera and motion permissions if prompted.
3. Choose **Start AR** and slowly move the phone to scan a floor or table.
4. When a surface is found, choose **Place game**.
5. Tap crystals or move close to them to collect them. Watch your surroundings while playing.

## Run a local web server

From the project directory, start any static-file server and open its address in your browser. For example, with Node.js installed:

```powershell
npx --yes http-server . -p 8080
```

Open `http://localhost:8080` on the same computer. This is suitable for Practice mode and local development. For AR on a phone, use an HTTPS deployment; a phone's `localhost` refers to the phone itself, not your computer.

## Requirements and implementation

- A modern browser with WebGL support.
- Internet access to load Three.js from jsDelivr.
- AR additionally requires a WebXR-compatible phone/browser, HTTPS, camera access, and hit-test support.
- The game is a single `index.html` file; it has no build step or local package installation.

If AR is unavailable, the game displays a message and Practice mode remains playable.
