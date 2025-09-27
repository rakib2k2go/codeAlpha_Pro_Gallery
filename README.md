#Pro Gallery
_An elegant, Google-Photos–style image gallery — zero installs, runs locally, keeps your photos private._

**Photos — Pro Gallery** is a single-page, mobile-first photo viewer you can open by double-clicking `index.html`.  
Load an entire folder of pictures, add individual files, or just drag & drop. It remembers what you viewed recently, and the viewer feels like Google Photos with smooth zoom, swipe, slideshow, and a clean one-corner control cluster.

---

## ✨ Features
- **Click-to-run:** static HTML file — no build, no dependencies.
- **Upload Folder** _(recursive)_: load a whole photo folder at once (Chromium browsers).
- **Add Images** + **Drag & Drop** + **Paste**: import pictures however you like.
- **Masonry grid**: responsive, rounded tiles with lazy-loaded thumbnails.
- **Search & Sort**: name search; sort by **Newest / Oldest / Name ↑↓**.
- **Recents rail**: quick access to recently viewed images (stored in `localStorage`).
- **Viewer** (Google Photos vibe):
  - Single, **top-right** controls: **◀ ▶ ✕** (no duplicates)
  - **Back** button on the left
  - **Slideshow**, **Fullscreen**, **Download**
  - **Zoom** (double-click/double-tap), **pinch-to-zoom**, **pan**
  - **Swipe** on mobile, **Arrow keys** on desktop
- **Responsive**: on phones, the top bar hides and a bottom action bar shows **Prev / Next / Close**.
- **Privacy-first**: everything stays on your device — no uploads or analytics.

> Supported formats depend on your browser (e.g. `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`, `.heic` on supported engines).

---

## 🚀 Quick Start
1. Download or clone the repo.
2. Double-click **`index.html`** to open it in your browser.
3. Load photos via:
   - **Add images** (multi-select)
   - **Add folder** (Chromium browsers, recursive)
   - **Drag & drop** images/folders
   - **Paste** an image (Ctrl/Cmd-V)
4. Click any tile to open the viewer; use arrows/swipe to navigate.

> You’ll see a few built-in sample images so the page isn’t blank on first open.

---

## ⌨️ Keyboard Shortcuts
- **← / →** — Previous / Next  
- **Esc** or **✕** — Close viewer  
- **Space** — Play / Pause slideshow  
- **Double-click** — Zoom in/out (also double-tap on mobile)

---

## 🧠 How it Works (high-level)
- Uses the **File API** to create temporary **Blob URLs** for selected files.
- Generates **thumbnails** in-memory via `<canvas>` for a snappy grid.
- Stores a compact **Recents** list in `localStorage` (name + tiny preview/URL).
- Pure-CSS **masonry** layout (multi-column) — no layout JS library.
- All logic is client-side; there are **no network requests**.

---

## 🛠 Customization
Open `index.html` and tweak:
- **Grid density** — change `column-width` in the `.masonry` CSS rule.
- **Slideshow speed** — adjust the interval in `startSlide()` (default `2500ms`).
- **Recents size** — update `MAX_RECENTS` (default `24`).
- **Theme & radii** — edit CSS variables at the top of the `<style>` block.

---

## 🌐 Browser Support
- **Chrome / Edge**: full support (including **Add folder** via `webkitdirectory`).
- **Firefox**: supported (folder import via drag-and-drop; file picker is per-file).
- **Safari**: supported; folder import varies by version (drag-and-drop recommended).
- **Mobile**: Chrome/Edge on Android, Safari/Chrome on iOS (file-picker UX varies by OS).

---

## ⚠️ Limitations
- Folder uploads rely on non-standard `webkitdirectory` (Chromium only); drag-and-drop folders as a fallback.
- Very large folders may take time to thumbnail on first load.
- “Recents” lives in the current browser profile; clearing site data resets it.

---

## 🗺️ Roadmap (nice-to-haves)
- [ ] EXIF date sorting & camera filters
- [ ] Favorites/tags & albums
- [ ] HEIC/RAW fallbacks via optional codecs
- [ ] Light/Dark theme switcher
- [ ] Export/Import of “Recents” data

---

## 🤝 Contributing
Issues and PRs are welcome! Please keep it dependency-free and test on both mobile and desktop.

---

## 🛡️ License
MIT — use freely, keep the notice.

---

## 📸 Screenshots
<img width="1222" height="661" alt="image" src="https://github.com/user-attachments/assets/27c7d03e-c267-4de9-b27e-7bee775ca095" />

