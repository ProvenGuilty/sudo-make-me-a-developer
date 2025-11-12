# Chapter 1 (Windows): Bootstrap Yourself

> **Mission:** Set up your development environment and take your first steps into the world of AI-assisted coding.

> **On macOS?** Start with **[Chapter 1 (macOS): Bootstrap Yourself](./CHAPTER-1-macos.md)** instead.

**Time Required:** 1-2 hours  
**Prerequisites:** A Windows computer, an email address, and willingness to learn  
**What You'll Learn:** GitHub, Windsurf IDE, version control basics, and WSL installation

---

## 📖 Table of Contents

1. [Before You Begin](#before-you-begin)
2. [Step 1: Create Your GitHub Account](#step-1-create-your-github-account)
3. [Step 2: Fork This Repository](#step-2-fork-this-repository)
4. [Step 3: Create Your Windsurf Account](#step-3-create-your-windsurf-account)
5. [Step 4: Understanding Your IDE](#step-4-understanding-your-ide)
6. [Step 5: Install WSL with AI Help](#step-5-install-wsl-with-ai-help)
7. [Verification & Celebration](#verification--celebration)
8. [What's Next](#whats-next)

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

## Step 3: Create Your Windsurf Account

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

#### 3.1 Download Windsurf

- [ ] Go to: **https://codeium.com/windsurf**
- [ ] Click "Download for Windows"
- [ ] Wait for the download to complete (it's about 100-200 MB)

#### 3.2 Install Windsurf

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

#### 3.3 Launch Windsurf

- [ ] Find Windsurf in your Start Menu
- [ ] Click to launch it
- [ ] Wait for it to open (first launch takes a moment)

#### 3.4 Sign In or Create Account

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

## Step 4: Understanding Your IDE

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

#### 4.1 Open Your Fork in Windsurf

- [ ] In Windsurf, click "File" → "Open Folder"
- [ ] Navigate to where you want to store your projects (e.g., `C:\Users\YourName\Projects`)
- [ ] Create a new folder called "Projects" if you don't have one
- [ ] Click "Select Folder"

**Wait!** You haven't downloaded your fork yet. Let's do that:

#### 4.2 Clone Your Fork

"Cloning" means downloading your GitHub repository to your computer.

- [ ] In Windsurf, press `Ctrl+Shift+P` (opens the Command Palette)
- [ ] Type "Git: Clone" and press Enter
- [ ] Paste your fork's URL: `https://github.com/YOUR-USERNAME/sudo-make-me-a-developer`
- [ ] Choose where to save it (your Projects folder)
- [ ] Click "Open" when asked if you want to open the cloned repository

**What just happened?** You downloaded your fork from GitHub to your computer. Now you can edit it!

#### 4.3 Explore the Interface

- [ ] Click on different files in the Explorer (left sidebar)
- [ ] Notice how they open in the editor
- [ ] Try opening multiple files (they appear as tabs)
- [ ] Click the Source Control icon (looks like a branch) to see Git integration

#### 4.4 Meet Your AI Assistant

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

## Step 5: Install WSL with AI Help

### What is WSL?

**WSL** = Windows Subsystem for Linux

It's a way to run Linux on your Windows computer without:
- Dual-booting
- Virtual machines
- Replacing Windows

**Why do you need it?**
- Many development tools work best on Linux
- It's what most servers run
- You'll learn commands that work everywhere
- It's industry-standard

**Think of it as:** Having a Linux computer inside your Windows computer.

### The AI-Assisted Way

Here's where it gets cool. Instead of following a long list of commands, you're going to **ask the AI to help you install WSL**. This teaches you:
1. How to work with AI assistants
2. How to troubleshoot when things go wrong
3. The actual workflow of modern developers

### Action Items

#### 5.1 Open the Terminal in Windsurf

- [ ] In Windsurf, press `` Ctrl+` `` (that's Ctrl and the backtick key)
- [ ] Or click "Terminal" → "New Terminal" from the menu
- [ ] You should see a terminal panel at the bottom

#### 5.2 Ask the AI for Help

- [ ] Open the AI assistant panel (`Ctrl+L`)
- [ ] Type this prompt:

```
I need to install WSL (Windows Subsystem for Linux) on my Windows computer. 
I'm a complete beginner. Can you guide me through the process step-by-step?
Please check if WSL is already installed first, and then help me install it if needed.
```

- [ ] Press Enter and read the AI's response

#### 5.3 Follow the AI's Instructions

The AI will likely tell you to:

1. **Check if WSL is already installed:**
   - [ ] Run the command the AI suggests (probably `wsl --status` or `wsl -l -v`)
   - [ ] Copy the output and share it with the AI

2. **Install WSL if needed:**
   - [ ] The AI will give you a command like: `wsl --install`
   - [ ] Copy the command
   - [ ] Paste it in the terminal
   - [ ] Press Enter
   - [ ] **Important:** You'll need to run the terminal as Administrator

3. **Run Terminal as Administrator:**
   - [ ] Close Windsurf
   - [ ] Right-click on Windsurf in the Start Menu
   - [ ] Click "Run as Administrator"
   - [ ] Open the terminal again
   - [ ] Run the install command

4. **Wait for Installation:**
   - [ ] WSL will download (this can take 5-15 minutes)
   - [ ] You may need to restart your computer
   - [ ] After restart, open Windsurf again

5. **Set Up Ubuntu (or your chosen Linux distribution):**
   - [ ] After installation, Ubuntu will launch automatically
   - [ ] Create a username (all lowercase, no spaces)
   - [ ] Create a password (you won't see it as you type—this is normal!)
   - [ ] Confirm your password

#### 5.4 Verify WSL is Working

- [ ] In Windsurf's terminal, type: `wsl --version`
- [ ] You should see version information
- [ ] Type: `wsl` to enter the Linux environment
- [ ] You should see a Linux prompt (looks like `username@computername:~$`)
- [ ] Type: `ls` (lists files)
- [ ] Type: `pwd` (shows current directory)
- [ ] Type: `exit` to return to Windows

### 🎓 What You Just Learned

- **How to use a terminal** - You ran actual commands!
- **How to work with AI** - You asked for help and followed instructions
- **How to troubleshoot** - You probably hit a snag and figured it out
- **Linux basics** - You ran Linux commands
- **Administrator privileges** - You learned about permissions

### ✅ Checkpoint

You should now:
- Have WSL installed
- Be able to enter the Linux environment with `wsl`
- Have run basic Linux commands
- Understand how to ask AI for help

**Stuck?** This is the most complex step. Common issues:
- Need to enable virtualization in BIOS
- Windows version too old (need Windows 10 version 2004+ or Windows 11)
- Need to update Windows first

**Ask the AI!** Paste any error messages into the AI chat and ask for help.

---

## Step 6: Connect via SSH & Sign the Guestbook

You now have all the core tools. Next, you'll configure secure access to GitHub and make your first contribution to this project by signing the guestbook.

### Why SSH?

- 🔐 Secure login to GitHub without typing your password every time
- 🚀 Required for pushing code changes from Windsurf/WSL
- 🪪 Confirms you control your GitHub identity

### Action Items

#### 6.1 Open Your WSL Terminal

- [ ] In Windsurf, press `` Ctrl+` `` to open the terminal (make sure it says `username@...` in a Linux prompt)
- [ ] If you see a Windows prompt (e.g., `C:\`), type `wsl` and press Enter to switch into Linux

#### 6.2 Check for Existing SSH Keys

- [ ] Run: `ls ~/.ssh`
- [ ] If you see files like `id_ed25519` and `id_ed25519.pub`, you may already have keys—skip to **6.4**
- [ ] If the folder doesn't exist or is empty, continue to the next step

#### 6.3 Generate a New SSH Key (Recommended: ed25519)

- [ ] Run: `ssh-keygen -t ed25519 -C "your_email@example.com"`
  - Replace the email with the one tied to your GitHub account
- [ ] When prompted for a file location, press **Enter** to accept the default (`/home/yourname/.ssh/id_ed25519`)
- [ ] When prompted for a passphrase, press **Enter** to leave it blank (or set one if you prefer extra security)

#### 6.4 Start the SSH Agent & Add Your Key

- [ ] Run: `eval "$(ssh-agent -s)"`
- [ ] Run: `ssh-add ~/.ssh/id_ed25519`

#### 6.5 Copy Your Public Key

- [ ] Run: `cat ~/.ssh/id_ed25519.pub`
- [ ] Highlight the entire line that starts with `ssh-ed25519` and copy it (right-click → Copy in Windsurf)
- 💡 Tip: You can also run `clip.exe < ~/.ssh/id_ed25519.pub` to copy straight to the Windows clipboard

#### 6.6 Add the Key to GitHub

- [ ] Visit: **https://github.com/settings/ssh/new**
- [ ] Title it something memorable (e.g., "Windsurf on Laptop")
- [ ] Paste the public key, click **Add SSH key**
- [ ] Confirm with your GitHub password or 2FA if prompted

#### 6.7 Test the Connection

- [ ] Back in WSL, run: `ssh -T git@github.com`
- [ ] Type `yes` if asked to confirm the fingerprint
- [ ] Success looks like: `Hi YOUR-USERNAME! You've successfully authenticated...`

#### 6.8 Sign the Guestbook 🎉

- [ ] In Windsurf, open `GUESTBOOK.md`
- [ ] Add your entry **at the top** of the list using the template provided in the file
- [ ] Example:
  ```markdown
  - [2025-11-12] Neo The Learner — Austin, TX — "sudo vibes activated"
  ```
- [ ] Ask the AI assistant to guide you through staging, committing, and pushing your change, or run:
  ```bash
  git add GUESTBOOK.md
  git commit -m "Add <your name> to guestbook"
  git push origin main
  ```
  (If `main` doesn't exist yet in your fork, Windsurf/AI will help you create it.)
- [ ] Open your fork on GitHub and make sure the guestbook entry appears in your branch
- [ ] Optional: open a pull request back to the main project to share your success

### ✅ Checkpoint

You should now:
- Have an SSH key connected to GitHub
- Be able to push code directly from Windsurf/WSL
- See your name in `GUESTBOOK.md`
- Understand how to create commits and interact with GitHub via SSH

---

## Verification & Celebration

### Let's Confirm Everything Works

Run through this checklist:

#### GitHub
- [ ] I can log into GitHub
- [ ] I can see my forked repository
- [ ] I understand what version control is (tracking changes)
- [ ] I've added an SSH key to GitHub
- [ ] I signed the guestbook via a commit and push

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
