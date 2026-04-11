# 📄 md2web

> A minimal, elegant Markdown document viewer — just write in `doc.md`, open `index.html`, and you're done.

This project turns your Markdown file into a beautifully styled web page. No build step, no terminal commands — just a static HTML file powered by [Showdown.js](https://github.com/showdownjs/showdown).

## ✨ Features

| Feature | Description |
| --- | --- |
| 📝 Real‑time rendering | `index.html` reads `doc.md` and converts it on the fly |
| 🎨 Beautiful defaults | Clean typography and readable layout out of the box |
| 🪶 Zero build step | No npm, no bundler — runs directly in the browser |
| 📱 Responsive | Looks good on desktop, tablet, and mobile |
| 🌐 Offline-ready | Can be configured to work without an internet connection |

## 🚀 Quick Start

1. **Clone or download** this repository
2. **Edit** `doc.md` — write your content in Markdown
3. **Open** `index.html` in any modern browser

That's it. Every time you refresh the page, it pulls the latest content from `doc.md`.

## 🗂️ Project Structure

```
.
├── index.html      # Main viewer (uses Showdown.js via CDN)
├── doc.md          # Your content — edit this
└── README.md       # This file
```

## 🛠️ How It Works

- `index.html` fetches `doc.md` using the Fetch API
- [Showdown.js](https://github.com/showdownjs/showdown) converts Markdown → HTML
- A minimal CSS stylesheet makes the result pleasant to read

## 📝 Example

Write this in `doc.md`:

```markdown
# Hello, World

This is **bold** and this is *italic*.
```

…and `index.html` will display a properly formatted heading and paragraph.

## 📦 About Showdown.js

By default, `index.html` loads Showdown.js from a CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js"></script>
```

This works out of the box with no extra steps.

### 🔧 Switching to a Local Copy (Offline Use)

If you want to use this project without an internet connection, you can download Showdown.js locally:

#### Step 1: Download the file

**Option A — Using curl (Linux/macOS/Git Bash):**
```bash
curl -O https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js
```

**Option B — Using wget:**
```bash
wget https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js
```

**Option C — Manual download:**
Open this link in your browser and save the file:
https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js

#### Step 2: Place the file

Put `showdown.min.js` in the **same folder** as `index.html`.

#### Step 3: Update `index.html`

Change the script tag from:

```html
<script src="https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js"></script>
```

to:

```html
<script src="showdown.min.js"></script>
```

That's it! Now you can open `index.html` without an internet connection.

### 📂 Local Setup Project Structure

After switching to local Showdown.js:

```
.
├── index.html
├── doc.md
├── showdown.min.js   # <-- downloaded locally
└── README.md
```

## 🙏 Acknowledgments

This project uses [Showdown.js](https://github.com/showdownjs/showdown) by ShowdownJS.  
Showdown is released under the MIT License:

> MIT License  
> Copyright (c) 2018,2021 ShowdownJS  
> https://github.com/showdownjs/showdown

Special thanks to the ShowdownJS team for creating such a robust and easy‑to‑use Markdown converter.

## 📄 License

**My own code** in this project is dedicated to the public domain under the [Unlicense](https://unlicense.org/).  
You may use, copy, modify, distribute, and sell it for any purpose, without restriction.

*Showdown.js remains under its original MIT License as noted in the Acknowledgments section above.*

---

⭐️ Star this repo if you find it useful.