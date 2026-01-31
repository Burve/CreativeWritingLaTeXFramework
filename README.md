# 📖 Creative Writing LaTeX Framework

A beginner-friendly LaTeX template for writing novels, with automatic version control between original and edited drafts.

**Perfect for authors who want professional-quality book formatting without learning complex LaTeX commands.**

---

## ✨ Features

- **Simple Setup** — Edit a few clearly-marked files to configure your book
- **Original/Edited Workflow** — Write in "Original" files, let editors work in "Edited" files, switch between versions with one setting
- **Multiple Book Formats** — Instantly switch between A5 novel, A4 draft, US Letter, 6×9 trade paperback, or 5×8 pocket book
- **Chapter Parts System** — Break long chapters into manageable parts
- **Professional Styling** — Drop caps, scene breaks, character dialogue formatting built-in

---

## 🚀 Quick Start for Authors

### Step 1: Get Your Own Copy

**Option A: Fork on GitHub (Recommended)**
1. Click the **Fork** button at the top-right of this page
2. This creates your own copy under your GitHub account
3. Clone your fork to your computer (see below)

**Option B: Use as Template**
1. Click the green **"Use this template"** button
2. Name your new repository (e.g., "MyNovel")
3. Clone to your computer

**Option C: Download ZIP**
1. Click the green **"Code"** button → **Download ZIP**
2. Extract to a folder on your computer
3. (Optional) Create a new GitHub repository and upload the files

### Step 2: Clone to Your Computer

```bash
git clone https://github.com/Burve/CreativeWritingLaTeXFramework.git
```

Or use [GitHub Desktop](https://desktop.github.com/) for a visual interface.

---

## 🛠️ Required Software

### 1. LaTeX Distribution

Install a LaTeX distribution for your operating system:

| OS | Recommended Distribution |
|----|-------------------------|
| Windows | [MiKTeX](https://miktex.org/download) or [TeX Live](https://tug.org/texlive/) |
| macOS | [MacTeX](https://tug.org/mactex/) |
| Linux | TeX Live (`sudo apt install texlive-full`) |

### 2. Code Editor with LaTeX Support

**Recommended: [Visual Studio Code](https://code.visualstudio.com/)** with the **LaTeX Workshop** extension.

#### Installing LaTeX Workshop:
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "LaTeX Workshop"
4. Click **Install**

#### Building Your Book:
- Open `main.tex` in VS Code
- Press **Ctrl+Alt+B** to build (or save the file — it auto-builds)
- The PDF appears in the same folder

---

## 📁 Project Structure

```
YourNovel/
├── Author/                      ← 📝 YOU EDIT THESE
│   ├── book-settings.tex        ← Title, author, format settings
│   ├── chapters.tex             ← List of your chapters
│   └── frontmatter.tex          ← Characters, dedication, etc.
│
├── Chapters/                    ← 📝 YOUR CHAPTER CONTENT
│   ├── chapter1.tex             ← Chapter definition (title, parts)
│   ├── chapter2.tex
│   └── Parts/
│       ├── Original/            ← Your original writing
│       │   ├── ch01_part01.tex
│       │   └── ch02_part01.tex
│       └── Edited/              ← Editor's corrections
│           ├── ch01_part01.tex
│           └── ch02_part01.tex
│
├── Commands/                    ← ⚙️ Mostly system files
│   ├── characters.tex           ← 📝 YOUR character name shortcuts
│   └── additional_commands.tex  ← 📝 Add custom styling commands
│
├── Context/                     ← 📋 Reference materials (notes, profiles)
└── main.tex                     ← ⚙️ System file (don't edit)
```

---

## 📝 How to Use

### Configure Your Book

Edit **`Author/book-settings.tex`**:

```latex
% Your book's title
\def\bookTitle{My Amazing Novel}

% Author name
\def\bookAuthor{Your Name}

% Page format: a5novel, a4paper, usletter, 6x9book, 5x8book
\def\pageFormat{a5novel}

% Version: "edited" or "original"
\def\chapterVersion{edited}
```

### Add Chapters

1. **Create chapter content** in `Chapters/Parts/Original/`:
   - Copy an existing file like `ch01_part01.tex`
   - Rename it (e.g., `ch02_part01.tex`)
   - Write your content

2. **Create chapter definition** in `Chapters/`:
   - Copy `chapter1.tex` → `chapter2.tex`
   - Update the chapter name and part references

3. **Register the chapter** in `Author/chapters.tex`:
   ```latex
   \subfile{Chapters/chapter1.tex}
   \subfile{Chapters/chapter2.tex}
   ```

### Writing Content

In your chapter part files (`Chapters/Parts/Original/ch01_part01.tex`), you can use:

```latex
% Regular paragraph
This is normal narrative text.

% Character dialogue
\say{Alice}{Hello, how are you?}
\say{Bob}[whispering]{I'm fine, thanks.}

% Character thoughts
\thought{Alice}{I wonder what he's hiding.}

% Scene break
\sceneBreak

% Sound effect
\sfx{BOOM!}
```

### Character Name Shortcuts

Define shortcuts for character names in **`Commands/characters.tex`**:

```latex
% Define character shortcuts
\NewDocumentCommand{\mc}{}{Alice}      % Main character
\NewDocumentCommand{\villain}{}{Lord Darkness}
\NewDocumentCommand{\sidekick}{}{Bob}
```

Then use them in your writing:
```latex
\mc{} walked into the room. \say{\villain}{I've been expecting you.}
```

### Custom Commands

Add your own styling commands or paste commands from external sources in **`Commands/additional_commands.tex`**. This file already includes useful commands like `\sceneBreak` and `\sfx{}`.

---

## 🔄 Original vs Edited Workflow

This framework supports a **dual-file workflow** for authors and editors:

1. **Author writes** in `Chapters/Parts/Original/` files
2. **Editor copies** the file to `Chapters/Parts/Edited/` and makes corrections
3. **When compiling**, the system automatically uses:
   - Edited version (if it exists)
   - Original version (as fallback)

To force using only original files, change in `Author/book-settings.tex`:
```latex
\def\chapterVersion{original}
```

---

## 💾 Saving Your Work with Git

Git tracks all changes to your book, letting you:
- See what changed and when
- Restore previous versions
- Collaborate with editors

### Basic Commands

```bash
# Save your progress
git add .
git commit -m "Finished chapter 3"

# Push to GitHub
git push

# Get latest changes (if collaborating)
git pull
```

### Using GitHub Desktop

1. Open GitHub Desktop
2. Your changes appear automatically
3. Write a summary (e.g., "Added chapter 3")
4. Click **Commit to main**
5. Click **Push origin**

---

## 📐 Available Page Formats

| Format | Size | Best For |
|--------|------|----------|
| `a5novel` | 148×210 mm | Novels, fiction (default) |
| `a4paper` | 210×297 mm | Drafts, manuscripts |
| `usletter` | 8.5×11 in | US standard printing |
| `6x9book` | 6×9 in | Trade paperbacks |
| `5x8book` | 5×8 in | Pocket books |

---

## ❓ Troubleshooting

**PDF not generating?**
- Make sure you have a LaTeX distribution installed
- In VS Code, check the "Output" panel → LaTeX Workshop for errors

**Missing packages?**
- MiKTeX will prompt to install missing packages automatically
- TeX Live: run `tlmgr install <package-name>`

**Characters look wrong?**
- Ensure your file is saved as UTF-8 encoding

---

## 📄 License

This template is free to use for your creative projects. Modify it as you wish!

---

## 🌐 Community

Need help? Want to connect with other authors using this framework?

Join the **[Burve Story Lab](https://skool.com/burve-story-lab-5890)** community on Skool! It's a space for:
- Getting help with setup and troubleshooting
- Sharing tips and workflows
- Discussing creative writing and LaTeX formatting
- Connecting with fellow authors

---

## 🤝 Contributing

Found a bug or have an improvement? Pull requests are welcome!
