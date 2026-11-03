# RAVAND CAFE 2

An offline-capable café table and receipt web app. It is a static Progressive Web App (PWA): no build step or external runtime dependencies are required.

## Install for offline use

The app must first be opened online from an HTTPS site so the browser can install it and cache its files. Once installed and opened at least once, it can work offline. Orders and settings are stored locally in that browser on that device; they are not synchronized between devices. Use the app's backup and restore controls to move data.

### iPhone and iPad

1. Open [the hosted app](https://qaidar-7.github.io/ravand-cafe/) in Safari while online.
2. Tap **Share**, then **Add to Home Screen**.
3. Open the new home-screen icon once while online. The app can then be launched offline.

### Windows

1. Open [the hosted app](https://qaidar-7.github.io/ravand-cafe/) in Microsoft Edge or Google Chrome while online.
2. Use the app's **Install App** button when it appears, or choose the browser's **Install this site as an app** option.
3. Launch the installed app once while online before using it offline.

Browser storage can be cleared by device or browser settings. Keep a backup if the café data is important.

## Run from a downloaded copy

Download the repository ZIP from GitHub and extract it. Do not open `index.html` directly as a `file://` URL: service workers, which provide offline support, require HTTPS or a local development server.

On Windows, open PowerShell in the extracted app folder and run:

```powershell
py -m http.server 8000 --bind 127.0.0.1
```

Then open <http://localhost:8000> in a browser. Stop the server with `Ctrl+C`.

## Publish with GitHub Pages

The public repository is [qaidar-7/ravand-cafe](https://github.com/qaidar-7/ravand-cafe), and GitHub Pages is enabled. The included GitHub Actions workflow deploys the static app whenever changes are pushed to the `main` branch.

The hosted app is <https://qaidar-7.github.io/ravand-cafe/>. To publish future updates, push the changed app files to the repository's `main` branch; the workflow at `.github/workflows/pages.yml` will deploy them automatically. If you fork the project, select **GitHub Actions** under **Settings → Pages** in the fork.

The page's café phone number and location are visible in the public source and hosted app.
