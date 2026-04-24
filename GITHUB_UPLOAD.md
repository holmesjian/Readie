# How to Upload to GitHub

Follow these steps to get Readie on GitHub.

## 📂 Repository Contents

```
readie/
├── README.md              # Main documentation
├── LICENSE                # MIT License
├── CONTRIBUTING.md        # Contribution guidelines
├── SETUP.md              # Detailed setup instructions
├── DEMO.md               # Hackathon demo script
├── .gitignore            # Files to ignore
└── readie.html           # The complete app (single file!)
```

## 🚀 Method 1: GitHub Web Interface (Easiest)

### Step 1: Create Repository

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `readie`
3. Description: `Stop prepping. Start Readie. AI-powered meeting prep in seconds.`
4. Choose: **Public** (for hackathon visibility)
5. **Do NOT** initialize with README (we have our own)
6. Click **Create repository**

### Step 2: Upload Files

1. On the empty repository page, click **uploading an existing file**
2. Drag ALL files from this folder into the upload area:
   - README.md
   - LICENSE
   - CONTRIBUTING.md
   - SETUP.md
   - DEMO.md
   - .gitignore
   - readie.html
3. Commit message: `Initial commit - Readie v1.0`
4. Click **Commit changes**

### Step 3: Done! ✅

Your repo is now live at: `github.com/YOUR-USERNAME/readie`

## 🚀 Method 2: Command Line (For Git Users)

### Prerequisites
- Git installed
- GitHub account
- Command line access

### Steps

```bash
# 1. Navigate to the repository folder
cd path/to/readie

# 2. Initialize git
git init

# 3. Add all files
git add .

# 4. First commit
git commit -m "Initial commit - Readie v1.0"

# 5. Add GitHub remote (replace YOUR-USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/readie.git

# 6. Push to GitHub
git branch -M main
git push -u origin main
```

## 📝 Customize Before Upload

Update these files with your info:

### README.md
Find and replace:
- `[Your Name]` → Your actual name
- `[your@email.com]` → Your email
- `[https://github.com/yourusername/readie]` → Your actual repo URL

### LICENSE
Update the year if needed (currently 2026)

## 🎯 After Upload

### 1. Add Topics

On GitHub, click ⚙️ next to "About" and add topics:
- `ai`
- `meeting-prep`
- `productivity`
- `claude-api`
- `hackathon`
- `single-file`

### 2. Add Description

In the "About" section:
```
Stop prepping. Start Readie. AI-powered meeting prep that translates your week into tailored briefs for any audience. 🚀
```

### 3. Enable GitHub Pages (Optional)

For a live demo:
1. Settings → Pages
2. Source: Deploy from branch
3. Branch: `main` → `/` → Save
4. Your demo will be at: `https://YOUR-USERNAME.github.io/readie/readie.html`

### 4. Create a Release

1. Click **Releases** → **Create a new release**
2. Tag: `v1.0.0`
3. Title: `Readie v1.0 - Push-to-Prod Hackathon`
4. Description:
   ```
   Initial release for Push-to-Prod Hackathon 2026
   
   Features:
   - AI-powered brief generation
   - Gmail integration (in claude.ai)
   - Multiple meeting types
   - PDF export
   - Single-file deployment
   ```
5. Attach: `readie.html`
6. Click **Publish release**

## 🏆 For Hackathon Judges

Add this badge to README.md (top of file):

```markdown
![Hackathon](https://img.shields.io/badge/hackathon-Push%20to%20Prod%202026-orange)
```

## 📊 Optional: Add a Demo GIF

Create a quick screen recording:
1. Record yourself using Readie
2. Convert to GIF (use https://ezgif.com)
3. Upload to repository
4. Add to README.md:
   ```markdown
   ![Readie Demo](demo.gif)
   ```

## ✅ Verification Checklist

Before submitting to hackathon:

- [ ] All files uploaded
- [ ] README.md has your contact info
- [ ] Repository is public
- [ ] Topics added
- [ ] Description added
- [ ] `readie.html` works when downloaded
- [ ] LICENSE file present
- [ ] No API keys committed (check .gitignore)

## 🔗 Share Your Repo

After upload, share at:
- Hackathon submission portal
- Twitter/X: "Just shipped Readie - AI meeting prep in a single HTML file 🚀"
- LinkedIn: Post about your hackathon project
- Dev.to: Write a blog post about building it

## 🎉 You're Done!

Your Readie repository is now:
- ✅ On GitHub
- ✅ Open source (MIT License)
- ✅ Ready for hackathon judging
- ✅ Ready for contributions
- ✅ Ready to help people prep for meetings!

**Good luck at the hackathon! 🚀**
