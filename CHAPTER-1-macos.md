# Chapter 1 (macOS): Bootstrap Yourself

> **Mission:** Set up your macOS development environment and take your first steps into AI-assisted coding.

> **On Windows?** Start with **[Chapter 1 (Windows): Bootstrap Yourself](./CHAPTER-1.md)** instead.

**Time Required:** 1-2 hours  
**Prerequisites:** A Mac running macOS 12 (Monterey) or newer, an email address, and willingness to learn  
**What You'll Learn:** GitHub, Windsurf IDE, version control basics, Xcode Command Line Tools, and Homebrew setup

---

## 📖 Table of Contents

1. [Before You Begin](#before-you-begin)  
2. [Step 1: Create Your GitHub Account](#step-1-create-your-github-account)  
3. [Step 2: Fork This Repository](#step-2-fork-this-repository)  
4. [Step 3: Install Windsurf on macOS](#step-3-install-windsurf-on-macos)  
5. [Step 4: Get Comfortable with Your IDE](#step-4-get-comfortable-with-your-ide)  
6. [Step 5: Install Xcode Command Line Tools and Homebrew](#step-5-install-xcode-command-line-tools-and-homebrew)  
7. [Verification & Celebration](#verification--celebration)  
8. [What's Next](#whats-next)

---

## Before You Begin

### What You're About to Learn

Think of this chapter as preparing your workshop. Before you can build anything, you need a space, tools, and a guide.

**The Big Picture:**
- **GitHub** = Google Drive for code (stores and shares your projects)
- **Windsurf** = Microsoft Word for code (where you write and edit)
- **Xcode Command Line Tools** = Essential developer utilities (Git, compilers, etc.)
- **Homebrew** = A package manager that installs additional software with one command
- **AI Assistant** = Your tireless coding mentor

### Why This Matters

Modern developers rely on smart tools and automation. By learning how to set up a professional environment on macOS, you're matching the workflow used by engineers worldwide.

### What You'll Need

- ✅ A Mac running macOS 12 (Monterey) or newer  
- ✅ Administrator access to the Mac (you should know the login password)  
- ✅ An email address  
- ✅ 1-2 hours of focused time  
- ✅ A reliable internet connection

**Ready? Let's go!**

---

## Step 1: Create Your GitHub Account

This is identical to the Windows guide, so follow the same steps:

- [Chapter 1 (Windows) → Step 1](./CHAPTER-1.md#step-1-create-your-github-account)

Make sure you complete the checkboxes there before moving on.

---

## Step 2: Fork This Repository

Forking creates your personal copy of this project, so you can track progress and make improvements.

- [Chapter 1 (Windows) → Step 2](./CHAPTER-1.md#step-2-fork-this-repository)

Once you have your fork, return here for macOS-specific setup.

---

## Step 3: Install Windsurf on macOS

### Why Windsurf?

Windsurf is your coding cockpit. It combines a code editor, integrated terminal, and AI assistant in one place.

### Action Items

#### 3.1 Download Windsurf for macOS

- [ ] Visit **https://codeium.com/windsurf**  
- [ ] Click **Download for macOS**  
- [ ] Wait for the `.dmg` file to finish downloading (~150 MB)

#### 3.2 Install Windsurf

- [ ] Double-click the downloaded `.dmg` file  
- [ ] Drag the **Windsurf** icon into the **Applications** folder  
- [ ] Eject "Windsurf" from Finder after installation (optional but tidy)

#### 3.3 First Launch (Gatekeeper Warning)

The first time you open Windsurf, macOS may warn you that it's downloaded from the internet.

- [ ] Open **Launchpad** or **Finder → Applications**  
- [ ] Right-click (or Control-click) **Windsurf**  
- [ ] Select **Open**  
- [ ] Click **Open** again when prompted (this whitelists the app)

#### 3.4 Sign In or Create an Account

- [ ] Launch Windsurf  
- [ ] Click **Sign In** or **Get Started**  
- [ ] Choose **Sign in with GitHub** for seamless integration  
- [ ] Authorize Windsurf to access your GitHub account  
- [ ] Complete any onboarding prompts

**Checkpoint ✅**
- Windsurf is installed in Applications  
- You can open it without macOS warnings  
- You're signed in and see the main editor window

---

## Step 4: Get Comfortable with Your IDE

Windsurf on macOS looks just like the Windows version. Let’s make sure you know where everything lives.

### Key Areas

- 📁 **Explorer**: Shows your files and folders  
- 🔍 **Search**: Finds text within your project  
- 🌿 **Source Control**: Git & GitHub management  
- 🤖 **AI Assistant**: Your built-in coding partner  
- 💻 **Editor Area**: Where you read and write files  
- 🖥️ **Terminal**: Runs commands at the bottom of the window

### Action Items

#### 4.1 Clone Your Fork

- [ ] In Windsurf, press `⌘⇧P` (Command + Shift + P) to open the Command Palette  
- [ ] Type "Git: Clone" and press Enter  
- [ ] Paste your fork URL: `https://github.com/YOUR-USERNAME/sudo-make-me-a-developer`  
- [ ] Choose a folder (e.g., `~/Projects`) to store the repository  
- [ ] Click **Open** when Windsurf offers to open the cloned repo

#### 4.2 Explore Windsurf

- [ ] Click different files in the Explorer  
- [ ] Observe how they open as tabs  
- [ ] Click the Source Control tab to see pending changes  
- [ ] Press `⌃`` (Control + backtick) or use **View → Terminal** to open the terminal

#### 4.3 Meet the AI Assistant

- [ ] Click the AI icon in the sidebar or press `⌘L` (Command + L)  
- [ ] Ask: "Explain what an IDE is like I'm new to coding."  
- [ ] Read the assistant's response

**Checkpoint ✅**
- Repository cloned locally  
- Comfortable navigating Windsurf  
- Able to open and use the terminal  
- Successfully chatted with the AI assistant

---

## Step 5: Install Xcode Command Line Tools and Homebrew

Windows needed WSL. macOS already runs Unix-style commands, but we still need developer tools and a package manager.

### Part A: Install Xcode Command Line Tools

These tools include Git and compilers. Many developer utilities expect them.

#### 5.1 Use Spotlight to Open Terminal

- [ ] Press `⌘Space` to open Spotlight  
- [ ] Type **Terminal** and press Enter

#### 5.2 Ask AI for Help (Optional but Recommended)

- [ ] In Windsurf AI, ask:

```
I need to install Xcode Command Line Tools on macOS. 
Please guide me step-by-step and help me verify the installation.
```

#### 5.3 Run the Installation Command

- [ ] In the Terminal, run: `xcode-select --install`  
- [ ] Click **Install** when prompted  
- [ ] Agree to license terms  
- [ ] Wait for the download (can take 5-10 minutes)

#### 5.4 Verify Installation

- [ ] Run: `xcode-select -p`  
  - ✅ If it prints a path like `/Library/Developer/CommandLineTools`, you're good  
- [ ] Run: `git --version`  
  - ✅ If you see a version number, Git is ready

### Part B: Install Homebrew (Optional but Highly Recommended)

Homebrew makes installing developer tools on macOS easy.

#### 5.5 Install Homebrew with AI Guidance

- [ ] Ask the AI: "How do I install Homebrew on macOS Ventura?"  
- [ ] Follow the steps (usually involves running a command starting with `/bin/bash -c ...`)

#### 5.6 Update Your Shell Environment

- [ ] After installation, follow any prompts to add Homebrew to your PATH  
  - Typically: `echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile`  
  - Then: `eval "$(/opt/homebrew/bin/brew shellenv)"`

#### 5.7 Verify Homebrew

- [ ] Run: `brew --version`  
- [ ] Run: `brew doctor` and follow any recommendations

### Part C: Terminal Comfort

- [ ] Practice running commands: `pwd`, `ls`, `mkdir test-folder`, `cd test-folder`  
- [ ] Use `rm -rf test-folder` to clean up (careful—this deletes without confirmation)

**Checkpoint ✅**
- Xcode Command Line Tools installed  
- Git works (`git --version`)  
- Homebrew installed (optional but recommended)  
- Comfortable running commands in the macOS Terminal

---

## Step 6: Connect via SSH & Sign the Guestbook

This final step ensures you can contribute back to the project using secure GitHub access.

### Why SSH on macOS?

- 🔐 Secure authentication without typing your password repeatedly
- 🚀 Required for pushing changes from Windsurf/Terminal
- 🪪 Confirms your identity when collaborating

### Action Items

#### 6.1 Check for Existing SSH Keys

- [ ] In Terminal, run: `ls ~/.ssh`
- [ ] If you see `id_ed25519` and `id_ed25519.pub`, skip to **6.4**
- [ ] Otherwise, continue below

#### 6.2 Generate a New SSH Key

- [ ] Run: `ssh-keygen -t ed25519 -C "your_email@example.com"`
- [ ] Press **Enter** to accept the default location (`/Users/you/.ssh/id_ed25519`)
- [ ] Press **Enter** again to skip a passphrase (optional)

#### 6.3 Start the SSH Agent & Add Your Key

- [ ] Run: `eval "$(ssh-agent -s)"`
- [ ] Run: `ssh-add ~/.ssh/id_ed25519`

#### 6.4 Copy Your Public Key

- [ ] Run: `pbcopy < ~/.ssh/id_ed25519.pub`
- [ ] This copies the key to your clipboard automatically
- [ ] (If `pbcopy` isn't available, run `cat ~/.ssh/id_ed25519.pub` and copy manually)

#### 6.5 Add the Key to GitHub

- [ ] Visit: **https://github.com/settings/ssh/new**
- [ ] Name it (e.g., "MacBook Windsurf")
- [ ] Paste the key and click **Add SSH key**
- [ ] Confirm with your password/2FA if requested

#### 6.6 Test the Connection

- [ ] Run: `ssh -T git@github.com`
- [ ] Type `yes` if asked to confirm the fingerprint
- [ ] You should see: `Hi YOUR-USERNAME! You've successfully authenticated...`

#### 6.7 Sign the Guestbook 🎉

- [ ] In Windsurf, open `GUESTBOOK.md`
- [ ] Add your entry at the top using the template in the file
- [ ] Example:
  ```markdown
  - [2025-11-12] Trinity Learner — Brooklyn, NY — "🚀 First AI-assisted commit!"
  ```
- [ ] Stage, commit, and push your change. Ask the AI assistant for help, or run:
  ```bash
  git add GUESTBOOK.md
  git commit -m "Add <your name> to guestbook"
  git push origin main
  ```
- [ ] Verify the change on your fork in GitHub
- [ ] Optional: open a pull request back to the main project

### ✅ Checkpoint

You now:
- Have SSH keys linked to GitHub
- Can push changes from macOS Terminal/Windsurf
- See your guestbook entry in your fork
- Understand how to collaborate securely

---

## Verification & Celebration

### GitHub
- [ ] Logged into GitHub  
- [ ] Personal fork exists  
- [ ] Understand the concept of version control  
- [ ] Added an SSH key to GitHub  
- [ ] Signed the guestbook via a commit and push

### Windsurf
- [ ] Windsurf launches from Applications  
- [ ] Signed in with GitHub  
- [ ] Repository cloned locally  
- [ ] AI assistant responds to questions

### macOS Terminal
- [ ] `xcode-select -p` returns a path  
- [ ] `git --version` shows a version number  
- [ ] `brew --version` works (if installed)  
- [ ] Comfortable with `ls`, `pwd`, `cd`

### Understanding
- [ ] Know what an IDE does  
- [ ] Understand version control basics  
- [ ] Know how to ask AI for help  
- [ ] Ready to start building in Chapter 2

**🎉 Congratulations!**

You've built a professional-grade macOS development environment with AI as your co-pilot. That's a big deal.

### Document Your Journey

- [ ] In your fork, create `my-chapter-1-macos-notes.md`  
- [ ] Write what was confusing, what helped, and tips for others  
- [ ] Commit and push (coming in Chapter 2!)

---

## What's Next

### Chapter 2: Your First AI-Powered Project

You'll learn Git commands, collaborate with AI, and start building your own idea.

### Before Chapter 2

- Experiment in Windsurf  
- Try installing a tool with Homebrew (e.g., `brew install tree`)  
- Think about what project you want to build  
- Join community discussions and help others

---

## Quick Reference

### Important URLs
- **GitHub:** https://github.com  
- **Your Fork:** https://github.com/YOUR-USERNAME/sudo-make-me-a-developer  
- **Windsurf:** https://codeium.com/windsurf  
- **Homebrew:** https://brew.sh

### Key Commands (macOS)
```bash
# Install Xcode Command Line Tools (if not already installed)
xcode-select --install

# Verify installation
xcode-select -p

# Check Git version
git --version

# Install Homebrew (from https://brew.sh)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Add Homebrew to your shell
(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"

# Verify Homebrew
brew --version
```

### Keyboard Shortcuts (macOS)
- `⌘S` – Save file  
- `⌘P` – Quick file open  
- `⌘⇧P` – Command palette  
- `⌃`` – Toggle terminal  
- `⌘L` – Open AI assistant

---

## Troubleshooting (macOS)

### Can't Install Xcode Command Line Tools
- Make sure the pop-up isn't hidden behind other windows  
- Try running the command again  
- Restart your Mac and retry  
- Ask the AI assistant with any error messages

### Gatekeeper Blocking Windsurf
- Right-click the app and choose **Open** the first time  
- Or go to **System Settings → Privacy & Security** and click **Open Anyway** under security alerts

### Terminal Says "Permission Denied"
- Make sure you typed commands correctly  
- Use quotes around paths with spaces  
- Double-check case sensitivity (`Desktop` ≠ `desktop`)

### Homebrew Installation Errors
- Run `brew doctor` for diagnostics  
- Ensure you have Rosetta installed on Apple Silicon (`softwareupdate --install-rosetta`)  
- Check that `/opt/homebrew` has the right permissions

---

## Need Help?

- Ask the AI assistant inside Windsurf (include error messages for better answers)  
- Search the troubleshooting guide  
- Open a GitHub issue: https://github.com/ProvenGuilty/sudo-make-me-a-developer/issues  
- Ask in Discussions (coming soon!)

---

**You did it!** 🎉 Welcome to the macOS dev world. On to Chapter 2 when you're ready!

---

*Last Updated: November 2025*
