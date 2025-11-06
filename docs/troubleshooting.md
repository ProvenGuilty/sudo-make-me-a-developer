# Troubleshooting Guide

> **When things don't go as planned** 🔧

Don't panic! Every developer spends time troubleshooting. This is normal and part of the learning process. This guide covers common issues and how to fix them.

---

## 🎯 General Troubleshooting Strategy

Before diving into specific issues, try this approach:

1. **Read the error message carefully** - It often tells you what's wrong
2. **Google the error** - Someone else has probably hit this
3. **Ask the AI** - Paste the error into Windsurf's AI assistant
4. **Check your steps** - Did you skip something?
5. **Restart** - Computer, application, or terminal
6. **Ask for help** - Create a GitHub issue with details

---

## GitHub Issues

### Can't Create Account

**Problem:** GitHub won't let me sign up.

**Possible causes:**
- Email already in use
- Password too weak
- Failed verification

**Solutions:**
- Try a different email address
- Use a stronger password (mix of letters, numbers, symbols)
- Complete the CAPTCHA carefully
- Check spam folder for verification email
- Try a different browser

### Can't Find the Fork Button

**Problem:** I don't see a "Fork" button.

**Solutions:**
- Make sure you're logged into GitHub
- Refresh the page
- Try a different browser
- The button is in the top-right corner of the repository page

### Fork Failed

**Problem:** Forking gives an error.

**Solutions:**
- Wait a moment and try again
- Check if you already forked it (look in your repositories)
- Log out and log back in
- Clear browser cache

---

## Windsurf Issues

### Download Won't Start

**Problem:** Clicking download does nothing.

**Solutions:**
- Try a different browser
- Disable ad blockers temporarily
- Check your internet connection
- Try the direct download link from Codeium's website

### Installation Fails

**Problem:** Installer gives an error.

**Possible causes:**
- Insufficient permissions
- Antivirus blocking
- Insufficient disk space
- Corrupted download

**Solutions:**
- Right-click installer → "Run as Administrator"
- Temporarily disable antivirus
- Free up disk space (need ~500MB)
- Re-download the installer
- Check Windows version (need Windows 10+)

### Windsurf Won't Open

**Problem:** Nothing happens when I click Windsurf.

**Solutions:**
- Restart your computer
- Check Task Manager—is it already running?
- Reinstall Windsurf
- Check antivirus logs—is it being blocked?
- Try running as Administrator

### Can't Sign In

**Problem:** Sign-in fails or loops.

**Solutions:**
- Clear browser cache in Windsurf
- Try signing in with GitHub instead of email
- Check if GitHub authorization is blocked
- Restart Windsurf
- Check firewall settings

### AI Assistant Not Responding

**Problem:** The AI doesn't answer my questions.

**Solutions:**
- Check your internet connection
- Sign out and sign back in
- Restart Windsurf
- Try rephrasing your question
- Check if there's a service outage (check Codeium's status page)

---

## WSL Issues

### "WSL command not found"

**Problem:** Terminal says `wsl` is not recognized.

**Possible causes:**
- WSL not installed
- Windows version too old
- Need to enable Windows features

**Solutions:**

1. **Check Windows version:**
   - Press `Win + R`
   - Type `winver` and press Enter
   - Need Windows 10 version 2004+ or Windows 11

2. **Update Windows:**
   - Settings → Update & Security → Windows Update
   - Install all updates
   - Restart

3. **Enable WSL feature:**
   - Open PowerShell as Administrator
   - Run: `wsl --install`
   - Restart computer

### "Virtualization is not enabled"

**Problem:** WSL installation fails with virtualization error.

**Solution:** Enable virtualization in BIOS:

1. Restart computer
2. Press BIOS key during startup (usually F2, F10, Del, or Esc)
3. Find "Virtualization" or "VT-x" or "AMD-V" setting
4. Enable it
5. Save and exit BIOS
6. Try WSL installation again

**Note:** BIOS varies by manufacturer. Google "[your computer model] enable virtualization" for specific steps.

### WSL Installation Hangs

**Problem:** Installation seems stuck.

**Solutions:**
- Be patient—first install can take 10-15 minutes
- Check your internet connection
- Close other programs to free up resources
- If stuck for >30 minutes, restart and try again

### "WslRegisterDistribution failed"

**Problem:** Error during Ubuntu setup.

**Solutions:**
- Run as Administrator
- Disable antivirus temporarily
- Check disk space (need ~1GB free)
- Try: `wsl --unregister Ubuntu` then reinstall

### Can't Remember WSL Password

**Problem:** Forgot the password I set.

**Solution:** Reset it:

1. Open PowerShell as Administrator
2. Run: `wsl -u root`
3. Run: `passwd yourusername` (replace with your username)
4. Enter new password twice
5. Exit: `exit`

### WSL is Slow

**Problem:** Commands take forever.

**Solutions:**
- Close other programs
- Restart WSL: `wsl --shutdown` then `wsl`
- Check Windows Defender—exclude WSL directories
- Increase WSL memory allocation (advanced)

---

## Terminal Issues

### Terminal Won't Open in Windsurf

**Problem:** Nothing happens when I press Ctrl+`.

**Solutions:**
- Try menu: Terminal → New Terminal
- Restart Windsurf
- Check keyboard layout (backtick key location varies)
- Try Ctrl+Shift+` instead

### Commands Don't Work

**Problem:** Typing commands gives errors.

**Possible causes:**
- Wrong environment (Windows vs WSL)
- Typos in command
- Missing software

**Solutions:**
- Check if you're in WSL: prompt should show `username@computername`
- Type `wsl` to enter WSL if needed
- Copy/paste commands carefully
- Check for typos

### "Permission Denied" Errors

**Problem:** Commands fail with permission errors.

**Solutions:**
- In WSL, try adding `sudo` before the command
- Example: `sudo apt update`
- Enter your WSL password when prompted
- In Windows, run as Administrator

---

## Git/GitHub Issues

### Can't Clone Repository

**Problem:** Cloning fails or times out.

**Solutions:**
- Check internet connection
- Try HTTPS URL instead of SSH
- Check if repository URL is correct
- Try cloning to a different folder
- Restart Windsurf

### "Authentication Failed"

**Problem:** Can't push/pull from GitHub.

**Solutions:**
- Sign in to GitHub in Windsurf
- Generate a Personal Access Token on GitHub
- Use token as password
- Check if you have permission to access the repository

---

## Performance Issues

### Everything is Slow

**Problem:** Computer is sluggish.

**Solutions:**
- Close unnecessary programs
- Restart computer
- Check disk space
- Check for Windows updates
- Scan for malware

### Windsurf is Laggy

**Problem:** Windsurf responds slowly.

**Solutions:**
- Close unused files/tabs
- Disable unused extensions
- Restart Windsurf
- Check if indexing is running (wait for it to finish)
- Increase system resources

---

## Common Error Messages

### "Access is denied"

**Meaning:** You don't have permission.

**Fix:**
- Run as Administrator
- Check file/folder permissions
- Close programs that might be using the file

### "File not found"

**Meaning:** The file or path doesn't exist.

**Fix:**
- Check spelling and path
- Use absolute paths (full path from C:\)
- Check if file was moved or deleted

### "Connection refused" or "Timeout"

**Meaning:** Can't connect to a service.

**Fix:**
- Check internet connection
- Check if service is down (GitHub status, etc.)
- Disable VPN temporarily
- Check firewall settings

---

## When All Else Fails

### Nuclear Options (Last Resort)

1. **Restart everything:**
   - Close all programs
   - Restart computer
   - Try again

2. **Reinstall:**
   - Uninstall Windsurf
   - Delete leftover files
   - Reinstall fresh

3. **Reset WSL:**
   ```bash
   wsl --unregister Ubuntu
   wsl --install
   ```

4. **Ask for help:**
   - Create a detailed GitHub issue
   - Include error messages
   - Describe what you tried
   - Include screenshots

---

## Getting Help

### Information to Include When Asking for Help

1. **What you were doing:**
   - "I was following Step 3.2 in Chapter 1"

2. **What happened:**
   - Exact error message (copy/paste it!)
   - Screenshot if relevant

3. **Your environment:**
   - Windows version: `winver`
   - WSL version: `wsl --version`
   - Windsurf version: Help → About

4. **What you tried:**
   - List troubleshooting steps you attempted

### Where to Get Help

- **AI Assistant:** Ask in Windsurf (fastest for simple issues)
- **GitHub Issues:** https://github.com/ProvenGuilty/sudo-make-me-a-developer/issues
- **Google:** Search the exact error message
- **Stack Overflow:** For specific technical questions

---

## Prevention Tips

### Avoid Common Issues

1. **Keep Windows updated** - Many issues are fixed in updates
2. **Read error messages** - They often tell you what's wrong
3. **Follow steps in order** - Don't skip ahead
4. **Save your work** - Commit changes regularly
5. **Take breaks** - Fresh eyes catch mistakes

### Good Habits

- ✅ Read instructions carefully
- ✅ Copy/paste commands to avoid typos
- ✅ Keep notes on what works
- ✅ Ask questions early
- ✅ Don't be afraid to experiment

---

## Remember

- **Errors are normal** - Every developer deals with them
- **Google is your friend** - Most errors have been solved before
- **AI can help** - Paste errors into the AI assistant
- **Community is here** - Don't hesitate to ask for help
- **You're learning** - Troubleshooting is a valuable skill

**You've got this!** 💪

---

*Last Updated: November 2025*
