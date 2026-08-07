# Screen Recorder — 100% Offline, Client-Side

A lightweight, client-side screen recorder web app that captures and saves screen recordings directly from your browser — no servers, no uploads, and no internet connection required.

## Key features

- 100% Offline: All recording, processing, and saving happens entirely in your browser. No data leaves your machine.
- Client-side only: Single-page, lightweight HTML app — no backend required.
- Simple workflow: Start recording, stop recording, and download the file locally.
- Privacy-first: Your screen recordings are saved to your device only.

## Files

- `index.html` — The entire app is implemented as a client-side HTML file (and related assets if included).

## How to use (offline)

1. Download or clone this repository to your computer:

   git clone https://github.com/Manuuuu21/screen-recorder.git

2. Serve the app locally (recommended) or open the file directly:

   - Recommended (works reliably): Run a local static server and open in your browser:

     - Python 3: `python -m http.server 8000`
     - Then open `http://localhost:8000` in your browser.

   - Direct file open: Double-click `index.html` to open via `file://` — note that some browsers restrict screen capture on `file://` pages. If screen capture is blocked, use the local server option above.

3. In the page, click the "Start recording" button. Your browser will prompt you to choose a screen, window, or tab to share.
4. Click "Stop recording" when finished.
5. Click the provided download/save button to save the recording as a file on your computer.

Note: The browser will always ask for permission before sharing your screen. This app does not send or upload recordings anywhere.

## Browser compatibility

- Works best in modern Chromium-based browsers (Chrome, Edge) and Firefox.
- Safari support may be limited depending on the macOS/iOS version.
- The app uses the Web Screen Capture API (getDisplayMedia); a secure context (HTTPS) or `localhost` is required in many browsers — serving locally via `http://localhost` is an offline-safe way to meet this requirement.

## Privacy & Security

- Offline-first: No network requests are necessary for recording or saving files.
- Local-only: Recordings are created and offered as downloads — they are never uploaded by the app.
- Permissions: The browser controls access to screen capture; only the user can grant it.

## Development

- The project is implemented with plain HTML (and client-side JavaScript). Look for `index.html` and any accompanying assets.
- To make changes, edit the files locally and reload the page in your browser.

## Troubleshooting

- If the screen selection prompt doesn't appear or capture is blocked:
  - Ensure you are using a recent browser version.
  - Serve the app via `http://localhost` rather than `file://` if needed.
  - Check browser settings and extensions that may block screen capture.
- If audio is not recorded, check the app UI for microphone toggles and your browser's site permissions.

## Contributing

Contributions are welcome. Open an issue or submit a pull request with improvements, bug fixes, or new features. Keep in mind the offline design goal — prefer client-side solutions.

## License

No license file is included in this repository by default. If you'd like to license this project, add a `LICENSE` file (for example, MIT) or specify your preferred license.

---

Made with privacy and simplicity in mind — your recordings stay on your device.