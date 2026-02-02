# AppPortal 🚀

A sleek, "glassmorphism" style dashboard to serve as a home screen for your collection of Single Page Apps (SPAs). It runs entirely from a single file—no build steps or database required.

## Features

* **📂 Unified Dashboard:** Access all your tools from one place.
* **🖼️ App Viewer:** Apps open in a seamless overlay window (iframe) so you never leave the portal.
* **🔙 Smart Navigation:** Integrated with browser history—use your browser's "Back" button to close apps.
* **⭐ Favorites:** Pin your most-used tools (saved automatically to your browser's Local Storage).
* **🔍 Instant Search:** Filter apps by title or description in real-time.
* **📱 Responsive:** Works on mobile, tablet, and desktop.

## 📂 Project Structure

Just drop the `index.html` in your root folder and organize your apps in subfolders.

```text
/my-portfolio
├── index.html          # The dashboard (contains all logic and config)
└── apps/               # Folder containing your sub-projects
    ├── data-viz/
    │   └── index.html
    ├── task-manager/
    │   └── index.html
    └── my-game/
        └── index.html
```

## ⚙️ Configuration

To add or remove apps, simply open index.html in any text editor and scroll to the APPS_CONFIG section (around line 140).

Add a new object to the list for each app:

```json
const APPS_CONFIG = [
    {
        id: 'unique-id-1',
        title: 'My Cool App',
        description: 'A brief description of what this tool does.',
        path: 'apps/my-cool-app/index.html', // Relative path to your app
        category: 'Productivity',            // Used for filter tabs
        icon: '🚀',                          // Emoji or text icon
        color: 'from-blue-500 to-cyan-500'   // Tailwind gradient colors
    },
    // ... add more apps here
];
```

## 🌍 Deployment

1. This project is ready for GitHub Pages.

2. Push your code to a GitHub repository.

3. Go to Settings > Pages in your repository.

4. Select the `main` branch as the source and save.

5. Your portal will be live at `https://your-username.github.io/repo-name/`.

## 🛠️ Local Development

Because this uses an `<iframe>` to display apps, it works best when running on a local server rather than just opening the file directly (due to browser security policies).

VS Code: Right-click `index.html` and select "Open with Live Server".

Python: Run `python -m http.server` in the terminal and go to `localhost:8000`.