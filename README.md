# Pole Simulator Web

This folder contains the web-hostable version of the Pole Climbing 360 Simulator. It is separate from the stable V3 project and is intended for GitHub Pages or any other HTTPS static host.

## Included files

- `index.html` – the simulator UI and logic
- `vendor/` – local Three.js and MediaPipe dependencies
- `.nojekyll` – prevents GitHub Pages from processing folders with underscores or special paths

## GitHub Pages setup

1. Create a GitHub repository or use an existing one.
2. Upload the contents of this folder to the repository root, or to a branch used by GitHub Pages.
3. In GitHub, open Settings → Pages.
4. Set the source to the branch and folder used for the site.
5. Publish the site.
6. The app will be available at a URL like:
   `https://your-user-name.github.io/your-repo-name/`

## Local testing

You can also run it locally in a browser with a static HTTP server:

```bash
python -m http.server 8000
```

Then open:

`http://localhost:8000/`

## Usage

- Click the video picker and choose a local 360° MP4 file from your computer or USB drive.
- The app keeps the video local to your computer; nothing is uploaded.
- Enable webcam tracking and calibrate your neutral head position.
- Use the sliders to adjust smoothing, range, and centre calibration as needed.

## Limitations

- Webcam/head tracking requires browser camera permission at the target site.
- This is a static HTTPS site; it does not upload your video files anywhere.
- GitHub Pages does not provide server-side logic; if you need a custom server or backend later, that would require a different hosting solution.
- Local file selection is still browser-controlled and may be restricted by device/browser security policies, but the standard HTTPS page flow is the correct path for Edge/Chrome on work laptops.

