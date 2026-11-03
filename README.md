# Your Fullstack Project Starts Here

**Everything you need before you write your first line of code:** install Visual Studio Code, add the extensions that actually matter, and learn from the best free resources — in one place, in about 30 minutes.

> **Visual Studio Code (VS Code)** is the free code editor used in this course. It is **not** "Visual Studio" (Microsoft's C# IDE) — different product, similar name, similar logo. If someone tells you to install "Visual Studio" for a frontend course, they mean **VS Code**.

- **Cost:** $0 — every tool and resource in this README is free.
- **Time:** ~30 minutes for the full setup, once, on your machine.
- **Works on:** Windows 10/11, macOS 12+, and Linux.

---

## Table of contents

1. [What you need before you start](#1-what-you-need-before-you-start)
2. [Install Visual Studio Code](#2-install-visual-studio-code)
3. [Install the extensions](#3-install-the-extensions)
4. [Configure VS Code once, then forget it](#4-configure-vs-code-once-then-forget-it)
5. [Your first project in 5 minutes](#5-your-first-project-in-5-minutes)
6. [Learning resources that are actually worth your time](#6-learning-resources-that-are-actually-worth-your-time)
7. [How this repo is organized](#7-how-this-repo-is-organized)
8. [How to submit your work](#8-how-to-submit-your-work)
9. [Troubleshooting](#9-troubleshooting)
10. [Keyboard shortcuts worth memorizing](#10-keyboard-shortcuts-worth-memorizing)
11. [How we review your work](#11-how-we-review-your-work)
12. [Get help](#12-get-help)

---

## 1. What you need before you start

| Requirement | Details |
| --- | --- |
| Operating system | Windows 10 or 11 (64-bit) · macOS 12.0 or later · Linux (x64, Arm32, Arm64) |
| Free disk space | ~500 MB for the editor, ~100 MB per extension set |
| RAM | 4 GB works fine; 8 GB is comfortable |
| A browser | Any modern one — Chrome, Edge, Firefox, or Safari |
| Git | Optional for week one, required from the first commit — [download](https://git-scm.com/downloads) |
| Node.js | Not needed for plain HTML/CSS/JS. Install it when we reach JavaScript tooling — [download](https://nodejs.org/en/download) |
| Your account | A free GitHub account — [github.com/signup](https://github.com/signup) |

**You do not need to pay for anything.** If a tutorial tells you to buy a tool, pick a different tutorial.

---

## 2. Install Visual Studio Code

### Windows 10 / 11

1. Open the official download page: **https://code.visualstudio.com/download**
2. Under **Windows**, download the **User Installer (x64)** — it installs for your user account and does **not** require administrator rights. (The *System Installer* is only for machine-wide installs on shared computers.)
3. Run the installer and tick these two boxes before you continue:
   - ☑ **Add to PATH** — lets you run `code .` from any terminal. Tick this one; it saves you pain later.
   - ☑ **Add to Windows Explorer context menu** — optional, gives you "Open with Code" on any folder.
4. Finish the install and launch **Visual Studio Code**.

### macOS 12+

1. Open **https://code.visualstudio.com/download**
2. Download the **Universal (Apple Silicon and Intel)** `.dmg`.
3. Double-click the `.dmg`, then drag **Visual Studio Code** into your **Applications** folder.
4. Launch it from Applications. If macOS blocks the first launch ("cannot be opened because it is from an unidentified developer"), right-click the app → **Open** → **Open** again. This is a one-time Gatekeeper prompt, not a problem.

### Linux

Pick the package that matches your distribution:

```bash
# Ubuntu / Debian / Mint — .deb
sudo apt update && sudo apt install code

# Fedora / RHEL / openSUSE — .rpm
sudo dnf install code

# Any Linux — Snap (works everywhere, slightly slower startup)
sudo snap install code --classic
```

If you prefer no package manager, grab the **.tar.gz** build from the download page (available for x64, Arm32, and Arm64) and extract it anywhere you like.

### Verify the installation

1. Open VS Code → **Help → About**. You should see the version, the commit hash, and the platform. If the window opens, the install worked.
2. Open a terminal (Windows Terminal / PowerShell / Git Bash on Windows, Terminal on macOS and Linux) and run:

```bash
code --version
```

You should see three lines: version, commit, and architecture.

**If `code` is not recognized**, the `code` command is not on your PATH yet:

- **Windows:** re-run the installer and tick **Add to PATH**, or simply skip the terminal for now — you can still use VS Code's own terminal (`Ctrl+``).
- **macOS / Linux:** open VS Code, press `Ctrl+Shift+P` (macOS: `Cmd+Shift+P`), type **"Shell Command: Install 'code' command in PATH"**, and run it. Then reopen your terminal.

---

## 3. Install the extensions

VS Code ships with excellent built-in support for HTML, CSS, JavaScript, and JSON — syntax highlighting, IntelliSense, and Emmet (the HTML/CSS abbreviation engine that lets you type `!` and get a full HTML skeleton) are **already included**. You do not need an extension for those.

The extensions below are the ones that make your day-to-day work faster and your code consistent.

### Install them in one click

This repo ships a recommended list. After you open the project folder in VS Code, a yellow banner appears at the top right:

> **Do you want to install the recommended extensions for this workspace?**

Click **Install All**. That installs everything in `.vscode/extensions.json` — the exact same list every student has, so nobody's setup drifts.

### Or install them manually

Press `Ctrl+Shift+X` (macOS: `Cmd+Shift+X`) to open the Extensions panel, search by name or by the ID in the table, and click **Install**.

| Extension | Marketplace ID | Why you want it |
| --- | --- | --- |
| **Live Server** | `ritwickdey.liveserver` | Starts a local server and refreshes the browser when you save. You see your changes instantly — no "open the file again" loop. |
| **Prettier** | `esbenp.prettier-vscode` | Formats your code the same way every time, on every machine. Kills "why does my spacing look different" reviews. |
| **HTML CSS Support** | `ecmel.vscode-html-css` | Completes your CSS `class` and `id` names while you are writing HTML, and jumps from a class to its rule. |
| **Path Intellisense** | `christian-kohler.path-intellisense` | Autocompletes file paths when you link to an image, script, or stylesheet. |
| **Material Icon Theme** | `PKief.material-icon-theme` | Gives each file type its own icon — instantly readable file tree. |
| **ESLint** | `dbaeumer.vscode-eslint` | Marks JavaScript problems as you type (unused variables, undefined names). *Note: this extension is a bridge — it needs the `eslint` package installed in the project. We set that up together in the JavaScript module.* |
| **Auto Close Tag** | `formulahendry.auto-close-tag` | Closes HTML tags for you as you type. (Optional — VS Code's built-in Emmet usually covers this.) |
| **Code Spell Checker** | `streetsidesoftware.code-spell-checker` | Catches typos in comments and documentation. (Optional) |
| **Live Share** | `ms-vsliveshare.vsliveshare` | Lets two people edit the same file at the same time — perfect for pair sessions with your classmates. (Optional) |
| **EditorConfig** | `editorconfig.editorconfig` | Applies the repository's `.editorconfig` rules automatically. Keeps everyone's formatting identical. (Optional) |
| **GitLens** | `eamodio.gitlens` | Shows who changed each line and when. (Optional — useful once you work in a team.) |
| **Markdown All in One** | `yzhang.markdown-all-in-one` | Preview and edit Markdown comfortably — useful if you keep notes or a study journal in the repo. (Optional) |
| **Tailwind CSS IntelliSense** | `bradlc.vscode-tailwindcss` | Autocomplete for Tailwind classes. (Optional — only when we reach Tailwind.) |

### Or install them from the command line

Open a terminal in this folder and run:

```bash
code --install-extension ritwickdey.liveserver
code --install-extension esbenp.prettier-vscode
code --install-extension ecmel.vscode-html-css
code --install-extension christian-kohler.path-intellisense
code --install-extension PKief.material-icon-theme
code --install-extension dbaeumer.vscode-eslint
code --install-extension formulahendry.auto-close-tag
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension ms-vsliveshare.vsliveshare
code --install-extension editorconfig.editorconfig
code --install-extension eamodio.gitlens
code --install-extension yzhang.markdown-all-in-one
code --install-extension bradlc.vscode-tailwindcss
```

Extensions update themselves — you never have to reinstall them.

---

## 4. Configure VS Code once, then forget it

Open the settings file with **`Ctrl+Shift+P`** → type **"Preferences: Open User Settings (JSON)"** and paste:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.fontSize": 16,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "editor.rulers": [80, 120],
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": "active",
  "editor.minimap.enabled": false,
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,
  "emmet.showSuggestionsAsSnippets": true,
  "workbench.iconTheme": "material-icon-theme"
}
```

What each group does:

- **`editor.formatOnSave` + `defaultFormatter`** — every save reformats the file with Prettier. Your code stays clean without you thinking about it.
- **`editor.fontSize: 16`** — larger than the default; easier to read while learning.
- **`editor.tabSize: 2` + `insertSpaces`** — the HTML/CSS convention.
- **`editor.rulers: [80, 120]`** — faint vertical guides that show where lines get too long.
- **`files.autoSave`** — saves your work automatically after a short delay. Never lose code again.
- **`emmet.showSuggestionsAsSnippets`** — makes Emmet expand on `Tab`.

If you want Arabic comments to be comfortable to read, add your Arabic-capable font on top of a monospace font:

```json
{
  "editor.fontFamily": "'IBM Plex Sans Arabic', Consolas, 'Courier New', monospace"
}
```

---

## 5. Your first project in 5 minutes

The `starter/` folder in this repo is a working mini project. Do the following:

1. **Clone or download this repo**, then open the folder in VS Code: `File → Open Folder…`, or run `code .` in the folder.
2. Open **`starter/index.html`**.
3. Right-click anywhere in the editor → **Open with Live Server**.
4. Your default browser opens at `http://127.0.0.1:5500/starter/`. Edit the HTML, press `Ctrl+S`, and watch the page update instantly.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My first page</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <main class="card">
    <h1>Hello, frontend!</h1>
    <p>I edited this file and pressed <kbd>Ctrl</kbd> + <kbd>S</kbd>.</p>
    <button id="my-button" type="button">Click me</button>
  </main>
  <script src="script.js"></script>
</body>
</html>
```

Two rules that prevent 90% of beginner bugs:

- **Use relative paths** in `src` and `href` (`style.css`, `images/logo.png`) — never `/style.css`, which points to the server root and returns 404.
- **Link your files** — an `index.html` with no `<link>` to your CSS shows an unstyled page, and a missing `<script src>` is the usual reason "my button does nothing".

---

## 6. Learning resources that are actually worth your time

**Do not collect ten courses.** Pick **one** course, keep **MDN** open as your reference, and use **one** practice site. That combination beats an abandoned pile of bookmarks.

### Reference — the authority, use it daily

| Resource | Link | Use it for |
| --- | --- | --- |
| **MDN Web Docs — HTML** | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/HTML) | Every HTML element and attribute |
| **MDN Web Docs — CSS** | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/CSS) | Every CSS property and value |
| **MDN Web Docs — JavaScript** | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript) | Every JS builtin and syntax rule |
| **MDN Learn Web Development** | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn_web_development) | A guided learning path through HTML → CSS → JS |
| **HTML Living Standard (WHATWG)** | [html.spec.whatwg.org](https://html.spec.whatwg.org/multipage/) | The actual specification — when you need the truth, not a tutorial |
| **Can I Use** | [caniuse.com](https://caniuse.com/) | "Does this work in Safari / Firefox / old browsers?" |

### Courses — pick one and finish it

| Resource | Link | Format |
| --- | --- | --- |
| **javascript.info** | [javascript.info](https://javascript.info/) | The best JavaScript book on the internet. Free, with exercises in every chapter. |
| **web.dev Learn** | [web.dev/learn](https://web.dev/learn) | Short, focused lessons on HTML, CSS, and accessibility |
| **freeCodeCamp — Responsive Web Design** | [freecodecamp.org/learn](https://www.freecodecamp.org/learn/) | A long, project-heavy curriculum |
| **roadmap.sh — Frontend** | [roadmap.sh/frontend](https://roadmap.sh/frontend) | The map of the whole field, so you know what comes next |
| **Wael Habbal Dev (Arabic)** | [youtube.com/@waelhabbaldev](https://www.youtube.com/@waelhabbaldev) | Live lessons and recorded sessions in Arabic |

### Practice — where the skill actually forms

| Resource | Link | What you train |
| --- | --- | --- |
| **Flexbox Froggy** | [flexboxfroggy.com](https://flexboxfroggy.com/) | Flexbox, level by level — 24 puzzles |
| **CSS Grid Garden** | [cssgridgarden.com](https://cssgridgarden.com/) | CSS Grid — 28 puzzles |
| **Frontend Mentor** | [frontendmentor.io](https://www.frontendmentor.io/) | Real design briefs you build from a screenshot |
| **Exercism** | [exercism.org](https://exercism.org/) | JavaScript exercises with human mentor feedback |
| **CSS-Tricks** | [css-tricks.com](https://css-tricks.com/) | Article series on every modern CSS technique |
| **W3Schools** | [w3schools.com/html](https://www.w3schools.com/html/html_intro.asp) | Quick syntax lookups — use it as a cheat sheet, not as the source of truth |

### Git and GitHub — required from your first commit

| Resource | Link | Use it for |
| --- | --- | --- |
| **Git downloads** | [git-scm.com/downloads](https://git-scm.com/downloads) | Installing Git on your OS |
| **Pro Git (free book)** | [git-scm.com/book/en/v2](https://git-scm.com/book/en/v2) | Learning Git properly, chapter by chapter |
| **GitHub Docs** | [docs.github.com](https://docs.github.com/en) | Forking, pull requests, Actions |
| **GitHub CLI** | [cli.github.com](https://cli.github.com/) | The optional `gh` command line tool |

> **Dead link?** Open an issue on this repo — links rot, and fixing them takes one minute from anyone.

---

## 7. How this repo is organized

```
frontend-starter-kit/
├── README.md              ← you are reading it
├── LICENSE
├── .gitignore              ← keeps node_modules and junk out of Git
├── .vscode/
│   ├── extensions.json     ← the recommended extension list
│   └── settings.json       ← shared formatting rules for the whole class
├── starter/                ← your first project: open this folder and run it
│   ├── index.html
│   ├── style.css
│   └── script.js
├── exercises/              ← your assignments go here
│   └── README.md
└── tools/
    └── validate_repo.py    ← checks every link and extension ID in this README
```

**Your own work goes in `exercises/`.** Create a new folder per assignment: `exercises/01-profile-card/`.

**Before you publish:** run `python3 tools/validate_repo.py` from the repo root. It checks that every link in this README still resolves and that every recommended extension still exists on the Marketplace — so broken links get fixed instead of rotting.

---

## 8. How to submit your work

We use the standard GitHub flow: **fork → clone → branch → commit → push → pull request.**

```bash
# 1. Fork this repo on GitHub (the "Fork" button, top right), then clone YOUR fork
git clone https://github.com/<your-username>/frontend-starter-kit.git
cd frontend-starter-kit

# 2. Create a branch for your assignment
git checkout -b feature/01-profile-card

# 3. Do your work in VS Code, then commit
git add exercises/01-profile-card
git commit -m "feat: add profile card with responsive layout"

# 4. Push your branch to your fork
git push -u origin feature/01-profile-card
```

Then open a **Pull Request** from your branch to the main repository. You can do the whole thing from VS Code: open the **Source Control** panel (`Ctrl+Shift+G`) — it shows changes, commit messages, push, and **Create Pull Request**.

**Commit message style we use:** a short prefix plus a description — `feat:` for a new feature, `fix:` for a bug fix, `docs:` for documentation, `chore:` for housekeeping. Example: `fix: correct relative path to style.css`.

**Keep each pull request small.** One assignment, one PR. It is easier for you to review and much easier for us to read.

---

## 9. Troubleshooting

| Symptom | Cause | Fix |
| --- | --- | --- |
| `code` is not recognized as a command | Not on PATH | Windows: re-run the installer and tick **Add to PATH**. macOS/Linux: Command Palette → **Shell Command: Install 'code' command in PATH** |
| Live Server: "Port 5500 is already in use" | Another server is using the port | Right-click the HTML file → **Change Live Server Port**, or set `"liveServer.settings.port": 5501` in your settings |
| The page opens but looks completely unstyled | The CSS file is not linked, or the path is absolute | Add `<link rel="stylesheet" href="style.css">` and use a **relative** path — never `/style.css` |
| My button does nothing | The script is not linked, or the script is below the button in the file | Add `<script src="script.js"></script>` before `</body>`, or select the element with `document.querySelector` after the DOM is ready |
| An extension will not install | Network, proxy, or company policy blocking the marketplace | Try again later, or download the `.vsix` file from the extension's Marketplace page and install it via the Extensions panel → **⋯ → Install from VSIX** |
| ESLint shows nothing | The extension is installed, but the `eslint` package is not in the project | Run `npm install -D eslint` in the project folder — the extension is only the editor bridge |
| Prettier and ESLint argue about formatting | Two formatters fighting over the same file | Let Prettier own formatting (`"editor.defaultFormatter": "esbenp.prettier-vscode"`) and let ESLint own correctness rules only |
| Git: `fatal: could not read Username for 'https://github.com'` | Git is not authenticated | Install [GitHub CLI](https://cli.github.com/) and run `gh auth login`, or use a personal access token as your password |
| PowerShell: "running scripts is disabled on this system" | Windows execution policy | `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned` |
| Arabic comments look wrong or disconnected | The editor font lacks Arabic glyphs | Set `"editor.fontFamily": "'IBM Plex Sans Arabic', Consolas, monospace"` (see section 4) |
| Extensions look different on a classmate's machine | Different versions or a missing recommended list | Open the project folder and click **Install All** in the recommended-extensions banner |

---

## 10. Keyboard shortcuts worth memorizing

| Action | Windows / Linux | macOS |
| --- | --- | --- |
| Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Quick Open (open a file) | `Ctrl+P` | `Cmd+P` |
| Toggle terminal | ``Ctrl+` `` | ``Cmd+` `` |
| Toggle sidebar | `Ctrl+B` | `Cmd+B` |
| Format the file | `Shift+Alt+F` | `Shift+Option+F` |
| Toggle line comment | `Ctrl+/` | `Cmd+/` |
| Select the next occurrence of the word | `Ctrl+D` | `Cmd+D` |
| Move the current line up / down | `Alt+↑` / `Alt+↓` | `Option+↑` / `Option+↓` |
| Rename a variable or tag everywhere | `F2` | `F2` |
| Toggle word wrap | `Alt+Z` | `Option+Z` |
| Go to a line number | `Ctrl+G` | `Cmd+G` |
| Extensions panel | `Ctrl+Shift+X` | `Cmd+Shift+X` |
| Source Control panel | `Ctrl+Shift+G` | `Cmd+Shift+G` |

---

## 11. How we review your work

When we look at a pull request, this is what we check — in this order:

1. **It runs.** The page loads with no console errors, and the layout holds at mobile and desktop widths.
2. **The HTML is semantic.** Real `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>` — not a wall of `<div>`.
3. **The CSS is organized.** Related rules next to each other, meaningful class names (`card-title`, not `blue-box-3`).
4. **It is formatted.** Run Prettier (it runs on save) before you push.
5. **The commits tell a story.** `feat:` then `fix:` reads like a real developer.
6. **It is your own work.** If you used an AI assistant or copied a tutorial, say so in the pull request and explain what you changed. We grade the understanding, not the first draft — and we do not accept code you cannot explain line by line.

**A note on AI assistants:** using them is fine. What is not fine is submitting output you cannot explain. Be ready to walk us through any line you submitted.

---

## 12. Get help

- **Stuck on a setup step?** Open an **Issue** on this repo with the error message and your OS. Screenshot is better than a description.
- **Stuck on an assignment?** Ask in class first, then open a **Discussion** — questions there help the next student too.
- **Pair debugging?** Use the **Live Share** extension and let a classmate join your editor.

---

## License

Released under the [MIT License](LICENSE) so you can reuse, remix, and build on it.

## Credits

- [Visual Studio Code](https://code.visualstudio.com/) — Microsoft
- [MDN Web Docs](https://developer.mozilla.org/) — Mozilla & contributors
- [javascript.info](https://javascript.info/) — Ilya Strebkov
- [web.dev](https://web.dev/learn) — Google
- [Flexbox Froggy](https://flexboxfroggy.com/) & [CSS Grid Garden](https://cssgridgarden.com/) — Thomas J. Bradley & Andy Bell
- [Wael Habbal Dev](https://www.youtube.com/@waelhabbaldev) — course videos and live sessions
