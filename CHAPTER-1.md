# Chapter 1: Bootstrap Yourself

> **Mission:** Set up your development environment and take your first steps into the world of AI-assisted coding.

**Time Required:** 1-2 hours  
**Prerequisites:** A Windows computer, an email address, and willingness to learn  
**What You'll Learn:** GitHub, version control basics, installing Ubuntu 24.04 on WSL 2 before any IDE work, Windsurf fundamentals, and how to add the Memory + Sequential Thinking MCP servers

---

## 📖 Table of Contents

1. [Before You Begin](#before-you-begin)
2. [Step 1: Create Your GitHub Account](#step-1-create-your-github-account)
3. [Step 2: Fork This Repository](#step-2-fork-this-repository)
4. [Step 3: Install Ubuntu 24.04 on WSL 2 (Before Any IDE)](#step-3-install-ubuntu-2404-on-wsl-2-before-any-ide)
5. [Step 4: Create Your Windsurf Account](#step-4-create-your-windsurf-account)
6. [Step 5: Understanding Your IDE](#step-5-understanding-your-ide)
7. [Step 6: Add the Memory + Sequential Thinking MCP Servers](#step-6-add-the-memory--sequential-thinking-mcp-servers)
8. [Verification & Celebration](#verification--celebration)
9. [What's Next](#whats-next)

---

## Before You Begin

### What You're About to Learn

Think of this chapter as setting up your workshop before building anything. Just like you need Microsoft Word installed before writing a document, you need these tools installed before coding.

**The Big Picture:**
- **GitHub** = Google Drive for code (stores and shares your projects)
- **Windsurf** = Microsoft Word for code (where you write and edit)
- **WSL** = A Linux environment on your Windows PC (many dev tools work best here)
- **AI Assistant** = Your coding mentor who never sleeps

### Why This Matters

Modern developers don't memorize everything—they use tools and AI to help them. You're learning the same workflow that professional developers use in 2024 and beyond.

### What You'll Need

- ✅ A Windows 10 or 11 computer
- ✅ Administrator access to your computer
- ✅ An email address
- ✅ About 1-2 hours of focused time
- ✅ A stable internet connection

**Ready? Let's go!**

---

## Step 1: Create Your GitHub Account

### What is GitHub?

GitHub is like Google Drive, but for code. It:
- Stores your projects online
- Tracks every change you make (so you can undo mistakes)
- Lets you collaborate with others
- Hosts millions of open-source projects

### Action Items

#### 1.1 Sign Up for GitHub

- [ ] Go to: **https://github.com/signup**
- [ ] Enter your email address
- [ ] Create a password (make it strong!)
- [ ] Choose a username (this will be public, choose wisely)
- [ ] Complete the verification puzzle
- [ ] Click "Create account"

**Pro Tip:** Your username will be part of your developer identity. Choose something professional or fun, but not embarrassing. You can't easily change it later.

#### 1.2 Verify Your Email

- [ ] Check your email inbox
- [ ] Find the email from GitHub
- [ ] Click the verification link
- [ ] Return to GitHub

#### 1.3 Complete Your Profile (Optional but Recommended)

- [ ] Click your profile picture (top right)
- [ ] Click "Your profile"
- [ ] Click "Edit profile"
- [ ] Add a profile picture
- [ ] Add a short bio (e.g., "Learning to code with AI")

### ✅ Checkpoint

You should now:
- Have a GitHub account
- Be logged into GitHub
- Have verified your email

**Stuck?** Check the [troubleshooting guide](./docs/troubleshooting.md) or ask in GitHub Issues.

---

## Step 2: Fork This Repository

### What is Forking?

"Forking" means making your own copy of someone else's project. Think of it like:
- **Original project** = A recipe in a cookbook
- **Your fork** = Your personal copy where you can make notes and changes

### Why Fork?

By forking this repository, you:
1. Get your own copy to track your progress
2. Can suggest improvements back to the original
3. Practice the workflow that developers use every day

### Action Items

#### 2.1 Fork the Repository

- [ ] Go to: **https://github.com/ProvenGuilty/sudo-make-me-a-developer**
- [ ] Click the "Fork" button (top right of the page)
- [ ] Keep the default settings
- [ ] Click "Create fork"

**What just happened?** You now have your own copy of this project at `github.com/YOUR-USERNAME/sudo-make-me-a-developer`

#### 2.2 Star the Original Repository (Optional)

- [ ] Go back to the original repository
- [ ] Click the "Star" button (top right)

**Why?** Starring is like bookmarking—it shows appreciation and makes it easy to find later.

### ✅ Checkpoint

You should now:
- Have your own fork of this repository
- See it listed under your GitHub profile
- Understand what forking means

---

## Step 3: Install Ubuntu 24.04 on WSL 2 (Before Any IDE)

### Why WSL Comes First

Installing Windows Subsystem for Linux **before** you ever open an IDE keeps every future workspace inside Linux, avoids race conditions with Windows-only terminals, and ensures Windsurf launches directly into Ubuntu. This is where your actual development happens, so we want it stable from the start.

### Action Items

#### 3.1 Update Windows and Enable Virtualization

- [ ] Open **Settings → Windows Update** and install all pending updates
- [ ] Reboot if prompted
- [ ] Press `Ctrl+Shift+Esc`, click the **Performance** tab, and confirm "Virtualization" says **Enabled**
- [ ] If it says Disabled, enter your BIOS/UEFI and enable Intel VT-x / AMD-V (your PC manual shows how)

#### 3.2 Turn On WSL and Virtual Machine Platform

- [ ] Right-click the **Start** button → **Windows Terminal (Admin)**
- [ ] Run each command (press Enter after every line):

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

- [ ] Restart your PC when the commands finish

#### 3.3 Install Ubuntu 24.04 LTS on WSL 2

- [ ] Open **Windows Terminal (Admin)** again
- [ ] Run:

```powershell
wsl --install -d Ubuntu-24.04
wsl --set-default-version 2
wsl --set-default Ubuntu-24.04
```

- [ ] Wait for the download to complete (5–15 minutes depending on bandwidth)
- [ ] When prompted, restart one more time

#### 3.4 Finish the First Boot

- [ ] Launch **Ubuntu 24.04** from the Start Menu
- [ ] Create a lowercase Linux username (e.g., `yourname`)
- [ ] Create a password (characters won't show—totally normal)
- [ ] Update packages so your environment is fresh:

```bash
sudo apt update && sudo apt upgrade -y
```

#### 3.5 Create a Linux-Native Projects Folder

Windows drives mount under `/mnt/c`, but storing code there can cause permission, path, and line-ending issues. Keep projects inside your Linux home directory instead.

- [ ] Inside the Ubuntu terminal run:

```bash
mkdir -p ~/projects && cd ~/projects
pwd
```

- [ ] Confirm the printed path starts with `/home/`

#### 3.6 Verify Everything Is on WSL 2

- [ ] Run `wsl -l -v` in Windows Terminal and confirm Ubuntu-24.04 shows **Version 2**
- [ ] Run `cat /etc/os-release` inside Ubuntu to confirm you're on 24.04
- [ ] Run `df -h .` while inside `~/projects` to double-check you are not on `/mnt/c`

#### 3.7 Bookmark Troubleshooting

- [ ] Skim the [troubleshooting guide](./docs/troubleshooting.md) for BIOS, update, or network issues
- [ ] If anything fails, copy the exact error into an AI assistant (even the built-in Windows Copilot) before moving on

### ✅ Checkpoint

You should now:
- Have Ubuntu 24.04 installed on WSL 2
- Be able to launch Ubuntu from the Start Menu and land in `/home/YOURNAME`
- Have a `~/projects` folder ready for future repos
- Know where to look if WSL throws an error

---

## Step 4: Create Your Windsurf Account

### What is Windsurf?

Windsurf is an **IDE** (Integrated Development Environment). Think of it as:
- **Microsoft Word** = For writing documents
- **Windsurf** = For writing code

But it's way more powerful! It has:
- AI built-in to help you code
- Tools to run and test your code
- Integration with GitHub
- Syntax highlighting (makes code easier to read)

### Why Windsurf?

- ✅ Beginner-friendly
- ✅ AI assistant built-in (this is huge!)
- ✅ Works with GitHub seamlessly
- ✅ Free for personal use
- ✅ Works on Windows, Mac, and Linux

### Action Items

#### 4.1 Download Windsurf

- [ ] Go to: **https://codeium.com/windsurf**
- [ ] Click "Download for Windows"
- [ ] Wait for the download to complete (it's about 100-200 MB)

> 💡 **Optional but appreciated:** If you want to toss a little love back to the maintainer, you can install via this referral URL: [https://windsurf.com/refer?referral_code=qzyamhddt0gky0zj](https://windsurf.com/refer?referral_code=qzyamhddt0gky0zj). If you choose that link, **we both get 250 bonus credits**, yet you still receive the exact same app and can keep using every free-tier model. Totally fine to skip if you prefer the direct download above.

#### 4.2 Install Windsurf

- [ ] Find the downloaded file (usually in your Downloads folder)
- [ ] Double-click the installer
- [ ] Click "Yes" if Windows asks for permission
- [ ] Follow the installation wizard:
  - [ ] Accept the license agreement
  - [ ] Choose installation location (default is fine)
  - [ ] Select "Add to PATH" (important!)
  - [ ] Click "Install"
- [ ] Wait for installation to complete
- [ ] Click "Finish"

#### 4.3 Launch Windsurf

- [ ] Find Windsurf in your Start Menu
- [ ] Click to launch it
- [ ] Wait for it to open (first launch takes a moment)

#### 4.4 Sign In or Create Account

When Windsurf opens:
- [ ] Click "Sign In" or "Get Started"
- [ ] Choose "Sign in with GitHub" (easiest option)
- [ ] Authorize Windsurf to access your GitHub account
- [ ] Complete any additional setup prompts

**Pro Tip:** Signing in with GitHub connects everything together—your code, your IDE, and your AI assistant all know who you are.

### ✅ Checkpoint

You should now:
- Have Windsurf installed
- Be signed into Windsurf
- See the Windsurf welcome screen or editor

---

## Step 5: Understanding Your IDE

> **Why now?** With Ubuntu on WSL 2 already configured, Windsurf detects the Linux environment automatically. That means every terminal, workspace, and AI action you try in this section will run against the correct filesystem by default—no more getting stuck in Windows PowerShell.

### Take a Tour

Before we dive in, let's understand what you're looking at. Windsurf has several main areas:

#### The Layout

```
┌─────────────────────────────────────────────────────┐
│  Menu Bar (File, Edit, View, etc.)                 │
├──────────┬──────────────────────────────────────────┤
│          │                                          │
│ Sidebar  │  Editor Area                            │
│          │  (where you write code)                 │
│ (files,  │                                          │
│  search, │                                          │
│  git)    │                                          │
│          │                                          │
├──────────┴──────────────────────────────────────────┤
│  Terminal / Output Panel                            │
│  (where you run commands and see results)           │
└─────────────────────────────────────────────────────┘
```

### Key Areas Explained

1. **Sidebar (Left):**
   - 📁 **Explorer:** See all your files and folders (like File Explorer)
   - 🔍 **Search:** Find text across all files
   - 🌿 **Source Control:** Manage your Git/GitHub changes
   - 🤖 **AI Assistant:** Your coding buddy (Cascade)

2. **Editor Area (Center):**
   - Where you write and edit code
   - Can have multiple files open in tabs (like browser tabs)
   - Syntax highlighting makes code colorful and easier to read

3. **Terminal (Bottom):**
   - A command-line interface
   - Where you run commands
   - See output and errors

### Action Items

#### 5.1 Open Your Fork in Windsurf

- [ ] In Windsurf, click "File" → "Open Folder"
- [ ] Navigate to where you want to store your projects (e.g., `C:\Users\YourName\Projects`)
- [ ] Create a new folder called "Projects" if you don't have one
- [ ] Click "Select Folder"

**Wait!** You haven't downloaded your fork yet. Let's do that:

#### 5.2 Clone Your Fork

"Cloning" means downloading your GitHub repository to your computer.

- [ ] In Windsurf, press `Ctrl+Shift+P` (opens the Command Palette)
- [ ] Type "Git: Clone" and press Enter
- [ ] Paste your fork's URL: `https://github.com/YOUR-USERNAME/sudo-make-me-a-developer`
- [ ] Choose where to save it (your Projects folder)
- [ ] Click "Open" when asked if you want to open the cloned repository

**What just happened?** You downloaded your fork from GitHub to your computer. Now you can edit it!

#### 5.3 Explore the Interface

- [ ] Click on different files in the Explorer (left sidebar)
- [ ] Notice how they open in the editor
- [ ] Try opening multiple files (they appear as tabs)
- [ ] Click the Source Control icon (looks like a branch) to see Git integration

#### 5.4 Meet Your AI Assistant

- [ ] Look for the AI/Cascade icon in the sidebar (or press `Ctrl+L`)
- [ ] Click it to open the AI chat panel
- [ ] Try asking it a question: "What is an IDE?"
- [ ] Read the response

**Mind = Blown?** You just had a conversation with an AI that understands code!

### ✅ Checkpoint

You should now:
- Have your fork cloned and open in Windsurf
- Understand the basic layout of an IDE
- Know how to access the AI assistant
- Feel comfortable clicking around

---

## Verification & Celebration

### Let's Confirm Everything Works

Run through this checklist:

#### GitHub
- [ ] I can log into GitHub
- [ ] I can see my forked repository
- [ ] I understand what version control is (tracking changes)

#### Windsurf
- [ ] Windsurf is installed and opens
- [ ] I'm signed in
- [ ] I have my fork open in Windsurf
- [ ] I can access the AI assistant

#### WSL
- [ ] I can open a terminal
- [ ] I can type `wsl --version` and see output
- [ ] I can enter WSL with `wsl` command
- [ ] I can run basic Linux commands

#### Understanding
- [ ] I know what an IDE is
- [ ] I know what version control is
- [ ] I know what WSL is
- [ ] I know how to ask AI for help

### 🎉 Congratulations!

If you checked all those boxes, you've completed Chapter 1! You now have:
- A GitHub account and your first fork
- A professional IDE installed and configured
- A Linux environment on your Windows machine
- Experience working with AI assistants

**This is a HUGE accomplishment.** Many people get stuck at this stage. You didn't. You're now equipped with the same tools that professional developers use.

### Document Your Journey

Help the next person by sharing your experience:

- [ ] In your fork, create a file called `my-chapter-1-notes.md`
- [ ] Write down:
  - What was confusing?
  - What helped you succeed?
  - How long did it take?
  - Any tips for others?
- [ ] Commit and push your notes (we'll teach you this in Chapter 2)

---

## What's Next

### Chapter 2: Your First AI-Powered Project

In Chapter 2, you'll:
- Learn Git commands (commit, push, pull)
- Build a real project using AI assistance
- Choose what YOU want to build
- Share your creation with the community

### Before Chapter 2

Take a break! You've earned it. When you're ready:

1. **Explore Windsurf:**
   - Click around
   - Open different files
   - Ask the AI random questions
   - Get comfortable

2. **Practice WSL:**
   - Type `wsl` to enter Linux
   - Try commands: `ls`, `pwd`, `cd`, `mkdir`
   - Type `exit` to leave

3. **Think About What You Want to Build:**
   - A personal website?
   - A simple game?
   - A productivity tool?
   - An automation script?

Chapter 2 will be about YOUR ideas. Start thinking!

### Join the Community

- [ ] Star the original repository
- [ ] Watch the repository for updates
- [ ] Join discussions in GitHub Issues
- [ ] Help others who are stuck on Chapter 1

---

## Quick Reference

### Important URLs
- **GitHub:** https://github.com
- **Your Fork:** https://github.com/YOUR-USERNAME/sudo-make-me-a-developer
- **Windsurf:** https://codeium.com/windsurf

### Key Commands
```bash
# Check WSL version
wsl --version

# Enter WSL
wsl

# Exit WSL
exit

# List files (in WSL)
ls

# Show current directory (in WSL)
pwd
```

### Keyboard Shortcuts (Windsurf)
- `Ctrl+` ` - Toggle terminal
- `Ctrl+L` - Open AI assistant
- `Ctrl+Shift+P` - Command palette
- `Ctrl+P` - Quick file open
- `Ctrl+S` - Save file

---

## Troubleshooting

### "I can't install WSL"
- Ensure Windows is up to date
- Check if virtualization is enabled in BIOS
- Run PowerShell as Administrator
- Ask the AI assistant with your specific error message

### "Windsurf won't open"
- Try restarting your computer
- Check if antivirus is blocking it
- Reinstall Windsurf
- Check system requirements

### "I'm stuck and the AI isn't helping"
- Try rephrasing your question
- Include error messages in your prompt
- Ask the AI to explain like you're five
- Post in GitHub Issues for human help

### "This is taking too long"
- That's normal! First-time setup always takes longer
- Take breaks
- Don't rush
- You're learning a LOT

---

## Additional Resources

- [Glossary](./docs/glossary.md) - Terms explained
- [Troubleshooting Guide](./docs/troubleshooting.md) - Detailed solutions
- [Contributing](./CONTRIBUTING.md) - How to help improve this guide

---

**You did it!** 🎉 Welcome to the world of development. See you in Chapter 2!

---

*Last Updated: November 2025*
