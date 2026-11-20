# NoteVerse📝

🎉 A just-for-fun personal project · Built with HTML, CSS & JavaScript · Zero backend

A browser-based, themed notes app built with plain HTML, CSS and JavaScript. Write notes, lock them with a PIN, stick them on a board, track your mood and writing streak, and take a break with mini-games, jokes and a magic 8-ball. Pick one of five themes and the whole app changes its look, fonts, shapes and falling emojis.

## ✨ Features

- 🔐 Local accounts (sign up, login, password reset), all stored in your own browser
- 📝 Notes with search, pinning, moods, and PIN-locked notes
- 🗂️ Sticky Board view: drag your notes around like real sticky notes
- ✅ Markdown and checklists: `**bold**`, `# heading`, `- [ ] task`
- 🎤 Voice notes in English or বাংলা
- 📅 Mood calendar showing your most-used mood for each day
- 🔥 Writing streaks and unlockable badges
- ⏳ Focus timer (5, 10 or 25 minutes) and a built-in calculator
- 🎮 Mini-games:
  - ❌⭕ Tic-Tac-Toe (you vs. a bot)
  - 🔢 Guess the number
  - ⚽ Penalty shootout
- 🎲 Fun corner: random jokes, procrastination excuses and a magic 8-ball
- 🎨 5 themes, each with its own look and falling emojis:
  - ⚽ Football
  - ⚡ Hogwarts
  - 🦄 Unicorn
  - 🤖 Cyberpunk
  - 🌿 Forest
- ⬇️⬆️ Export and import your notes as JSON
- 📲 Installable as an app and works offline (PWA)

## 🛠️ Built With

- HTML5 and CSS3 (CSS variables power the theme system)
- Vanilla JavaScript, no frameworks and no build step
- `localStorage` to save accounts, notes and settings
- Web Crypto API (SHA-256) to hash passwords and PINs
- Web Speech API for voice notes
- Service Worker and Web App Manifest for offline use and installing
- Google Fonts: Cinzel, Nunito, Orbitron, Fredoka

## 📋 Requirements

- Any modern browser (Chrome, Edge, Safari or Firefox)
- No installation and no external libraries needed
- Voice notes work in Chrome, Edge and Safari only
- Internet is only needed the first time, to load the Google Fonts (the app has fallback fonts)

## ▶️ How to Run

**Option 1: Open it directly**

1. Clone this repository:

```
git clone https://github.com/<Noon131>/noteverse.git
cd noteverse
```

2. Open `index.html` in your browser.

**Option 2: Run a local server** (needed to test install and offline mode)

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

**Option 3: Host it free on GitHub Pages**

1. Go to **Settings → Pages**.
2. Choose **Deploy from a branch** → `main` → `/ (root)` → **Save**.
3. Visit `https://<Noon131>.github.io/noteverse/` after a minute.

## 💻 How to Use

| Action | What it does |
|--------|--------------|
| Sign up / Login | Create a free local account and enter the app |
| Theme dropdown | Switch between the 5 themes |
| Save note | Saves the heading, mood and content you wrote |
| 🗂 Board / 📋 List | Switch between sticky board and list view |
| 👁 Preview | Shows your Markdown and checklists nicely |
| 🎤 Mic | Type with your voice (choose EN or বাংলা first) |
| 🔒 Lock | Protects a note with your PIN |
| ⬇ Export / ⬆ Import | Back up or restore your notes (JSON) |
| 📲 Install | Add the app to your home screen or desktop |

### Sidebar tabs

| Tab | What it does |
|-----|--------------|
| 🧮 Calc | A simple calculator |
| 🎮 Games | Tic-Tac-Toe, Guess the number, Penalty shootout |
| ⏳ Focus | Countdown timer for distraction-free writing |
| 📅 Mood | Monthly mood calendar |
| 🎲 Fun | Jokes, excuses and the magic 8-ball |

### Note format example

```
# Today's plan
- [ ] Finish the report
- [x] Drink water
This is **important**!
```

## 🧠 How It Works (Simple Explanation)

1. Everything runs inside your browser. There is no server and no database.
2. When you sign up, your password is hashed (SHA-256) and saved with your notes in `localStorage`.
3. Each theme is just a set of CSS variables (colours, fonts, shapes). Changing the theme swaps those variables, which is why the whole app changes instantly.
4. Notes are saved as small JSON objects (heading, text, mood, pinned, locked, position on the board).
5. Locked notes need your PIN, which is also stored only as a hash.
6. The streak counter checks the date of your last note and counts how many days in a row you wrote.
7. A service worker caches the app files, so it keeps working even when you are offline.

## 📁 Project Structure

```
noteverse/
├── index.html            # The whole app (HTML + CSS + JS)
├── manifest.webmanifest  # Makes the app installable
├── sw.js                 # Service worker for offline use
├── icon-192.png          # App icon
├── icon-512.png          # App icon (large)
├── .nojekyll             # Tells GitHub Pages to serve files as-is
├── LICENSE
└── README.md             # This file
```

## 🚧 Known Limitations

- Data is saved only in your browser, so clearing browser data deletes your notes (use Export for backups)
- Accounts are local to one device and are not synced anywhere
- This is a fun project, so don't store real passwords or sensitive information in it
- Voice notes depend on your browser's speech recognition support
- The Tic-Tac-Toe bot is not very smart (yet)

## 🔮 Future Improvements

- [ ] More themes (cricket, anyone? 🏏)
- [ ] More mini-games
- [ ] Cloud backup and sync across devices
- [ ] Tags and folders for notes
- [ ] Note sharing

## 👥 Authors

- **Mubas Sera Noon**

## 📄 License

This project is open for learning and fun. Feel free to fork it, modify it, and build on top of it. See [LICENSE](LICENSE) (MIT).

---

<div align="center">

### Developed with ❤️ by Noon

*If you liked it, drop a ⭐ on the repo!*

</div>
