# DREAD ARCHIVE

A horror video game encyclopedia built with Jekyll for GitHub Pages.

![Dread Archive](https://img.shields.io/badge/horror-encyclopedia-8B0000)

## 🎮 Features

- **Games Database**: Catalog of horror games with metadata
- **Reviews**: Gameplay-focused reviews with scores
- **Deep Analysis**: Long-form articles exploring horror themes and symbolism

---

## 🚀 Quick Start (GitHub Pages)

### 1. Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create an account)
2. Click the **+** icon → **New repository**
3. Name it `dread-archive` (or whatever you prefer)
4. Keep it **Public** (required for free GitHub Pages)
5. Click **Create repository**

### 2. Upload These Files

**Option A: GitHub Web Interface (Easiest)**
1. On your new repo page, click **"uploading an existing file"**
2. Drag and drop ALL files from this folder
3. Click **Commit changes**

**Option B: Git Command Line**
```bash
cd dread-archive
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/dread-archive.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (in left sidebar)
3. Under "Source", select **GitHub Actions**
4. Wait 2-3 minutes for the first build
5. Your site will be live at: `https://YOUR_USERNAME.github.io/dread-archive/`

### 4. Update the Config

Edit `_config.yml` and update:
```yaml
url: "https://YOUR_USERNAME.github.io"
baseurl: "/dread-archive"  # Your repo name
```

---

## 📝 Adding Content

### Add a New Game

Create a file in `_games/` folder:

```markdown
---
title: "Resident Evil 4"
year: 2005
developer: "Capcom"
publisher: "Capcom"
platforms:
  - GameCube
  - PlayStation 2
  - PC
tags:
  - Action Horror
  - Survival Horror
description: "A brief description of the game."
cover: /assets/images/games/re4.jpg  # Optional
---

Write additional details about the game here.
This can include history, legacy, gameplay notes, etc.
```

**Filename**: Use lowercase with hyphens, e.g., `resident-evil-4.md`

---

### Add a New Review

Create a file in `_reviews/` folder:

```markdown
---
title: "Resident Evil 4 (2023 Remake)"
date: 2023-04-15
game: "Resident Evil 4"
platform: "PC / PS5 / Xbox Series"
score: 9.2
pros:
  - Stunning visual overhaul
  - Refined controls
  - Expanded story content
cons:
  - Some cut content from original
  - Performance issues on some hardware
cover: /assets/images/reviews/re4-remake.jpg  # Optional
---

Write your full review here.

## Section Header

More review content...
```

**Filename**: Use lowercase with hyphens, e.g., `resident-evil-4-remake.md`

---

### Add a New Analysis

Create a file in `_analyses/` folder:

```markdown
---
title: "Folk Horror and Isolation in Darkwood"
date: 2024-03-10
category: "Folk Horror"
themes:
  - Isolation
  - Folklore
  - Survival
  - Eastern European Horror
reading_time: 12
related_games:
  - "Darkwood"
---

Write your deep analysis here.

## Section Header

More analysis content...
```

**Filename**: Use lowercase with hyphens, e.g., `darkwood-folk-horror.md`

---

## 🖼️ Adding Images

1. Create folders: `assets/images/games/`, `assets/images/reviews/`
2. Add your images there
3. Reference them in your content:
   ```yaml
   cover: /assets/images/games/silent-hill-2.jpg
   ```

---

## 📁 Folder Structure

```
dread-archive/
├── _config.yml          # Site configuration
├── _layouts/            # Page templates
│   ├── default.html
│   ├── home.html
│   ├── game.html
│   ├── review.html
│   └── analysis.html
├── _includes/           # Reusable components
│   ├── nav.html
│   └── footer.html
├── _games/              # ← ADD GAMES HERE
│   └── silent-hill-2.md
├── _reviews/            # ← ADD REVIEWS HERE
│   └── silent-hill-2-remake.md
├── _analyses/           # ← ADD ANALYSES HERE
│   └── silent-hill-2-trauma-analysis.md
├── assets/
│   ├── css/
│   │   └── style.scss
│   └── images/          # ← ADD IMAGES HERE
├── games/
│   └── index.html       # Games listing page
├── reviews/
│   └── index.html       # Reviews listing page
├── analysis/
│   └── index.html       # Analysis listing page
└── index.md             # Homepage
```

---

## 🔄 Updating Your Site

After making changes:

**GitHub Web Interface:**
1. Navigate to the file you want to edit
2. Click the pencil icon to edit
3. Make your changes
4. Click **Commit changes**
5. Site rebuilds automatically (1-2 minutes)

**Git Command Line:**
```bash
git add .
git commit -m "Added new review"
git push
```

---

## 🎨 Customization

### Change Colors

Edit `assets/css/style.scss` and modify the CSS variables:

```css
:root {
    --blood: #8B0000;        /* Primary accent */
    --blood-bright: #B22222; /* Links */
    --void: #0a0a0a;         /* Background */
    --fog: #1a1a1f;          /* Card backgrounds */
    --bone: #e8e4d9;         /* Text */
    --ash: #9a9590;          /* Secondary text */
}
```

### Change Site Title

Edit `_config.yml`:

```yaml
title: "YOUR SITE NAME"
description: "Your site description"
```

---

## 🌐 Custom Domain (Optional)

1. Buy a domain (Namecheap, Porkbun, etc.)
2. In your repo, go to **Settings** → **Pages**
3. Enter your custom domain
4. Add a `CNAME` file to your repo containing just your domain:
   ```
   dreadarchive.com
   ```
5. Configure DNS at your domain registrar (GitHub provides instructions)

---

## 🆘 Troubleshooting

**Site not updating?**
- Check the **Actions** tab for build errors
- Make sure your YAML front matter is valid (no tabs, proper indentation)

**Styling broken?**
- Clear browser cache
- Check that `style.scss` has the `---` at the top

**Pages 404?**
- Verify `baseurl` in `_config.yml` matches your repo name
- Make sure files are in the correct folders

---

## 📜 License

Content is yours. Code is MIT licensed.

---

*Enter at your own risk.* 🩸
