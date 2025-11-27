# Chapter 2: Build Your First App with AI

> **Mission:** Choose your idea. Build it with AI. Ship it to production.

**Time Required:** 3-4 hours  
**Prerequisites:** Chapter 1 completed  
**What You'll Build:** A working web app that solves a real problem  
**End Goal:** Live web app → Mobile app (Ch 3) → App Store (Ch 4-6)

---

## 🎯 Choose Your Adventure

**This chapter teaches you to build a web app. But what app?**

**That's up to you!**

You could build:
- 📊 Budget tracker
- 📝 Habit tracker
- 🍳 Recipe organizer
- 💪 Workout logger
- 📚 Book club manager
- 🐾 Pet care tracker
- 🎯 Goal planner
- 📅 Event organizer
- Or literally anything else!

**The Example: peasant**

Throughout this chapter, I'll show examples from building **peasant** - a budget tracker that's part of a larger financial super app.

> **peasant** - "Everything a modern peasant needs" 💰

But you should build YOUR idea. The skills are the same, the outcome is yours.

**👉 [Check out peasant on GitHub](https://github.com/ProvenGuilty/peasant)** to see the full vision.

---

## 📖 Table of Contents

1. [The Big Picture](#the-big-picture)
2. [What We're Building](#what-were-building)
3. [Git Workflow Mastery](#git-workflow-mastery)
4. [Set Up Your Project](#set-up-your-project)
5. [Build the Core Features](#build-the-core-features)
6. [Deploy Your App](#deploy-your-app)
7. [What's Next](#whats-next)

---

## The Big Picture

### Why Build an App?

**You're not just learning to code. You're learning to:**
- Solve real problems
- Build products people actually use
- Ship to production
- Use AI as your co-pilot
- Think like an entrepreneur

### The Example: peasant Budget Plugin

**My Problem:**
- Most people live paycheck to paycheck
- Bi-monthly pay periods are confusing
- Subscriptions silently drain money
- Budgeting apps are too complicated

**My Solution: peasant budget plugin**
An AI-powered budget tracker that:
- ✅ Tracks spending by pay period (bi-monthly)
- ✅ AI categorizes transactions automatically
- ✅ Detects subscription bleed
- ✅ Shows budget vs actual in real-time
- ✅ Provides AI insights and recommendations

### 💭 Your Turn: What Problem Will You Solve?

Before we start coding, think about:
- What frustrates you daily?
- What do you wish existed?
- What would make your life easier?
- What would help others?

**Write it down:**
- **My Problem:** _____________________
- **My Solution:** _____________________
- **Key Features:** _____________________

Don't overthink it! You can always change it later.

### The Journey Ahead

```
Chapter 2: Web App (Your Idea)
    ↓
Chapter 3: Mobile App (React Native)
    ↓
Chapter 4-6: Polish & Launch
    ↓
🎉 YOUR APP IN THE APP STORE!
```

### What You'll Learn in Chapter 2

- ✅ **Git workflow** - Branches, commits, pull requests
- ✅ **React fundamentals** - Components, state, hooks
- ✅ **AI integration** - OpenAI API for smart features
- ✅ **Data handling** - Forms, validation, storage
- ✅ **Modern CSS** - Tailwind for beautiful UI
- ✅ **Deployment** - Ship to production

**Time Investment:** 3-4 hours  
**Outcome:** Live web app you can actually use!

**peasant example:** Budget tracker with AI categorization  
**Your app:** Whatever you want to build!

---

## What We're Building

### Your App's Core Features

Every good app needs:
1. **Data Entry** - Add/edit/delete items
2. **Data Display** - Show items in a useful way
3. **Smart Features** - AI makes it better
4. **Visual Feedback** - Charts, progress, insights
5. **Simple Dashboard** - Overview at a glance

### Example: peasant Budget Plugin

Here's what I'm building for peasant:

#### 1. Transaction Entry 💰
- Add income and expenses
- Date, amount, description
- AI suggests category automatically

#### 2. Bi-Monthly Pay Period View 📅
- Toggle between 1st-15th and 16th-end of month
- See income vs expenses for each period
- Visual progress bars

#### 3. Subscription Detector 🔍
- AI identifies recurring charges
- Shows total monthly subscription cost
- Highlights "subscription bleed"

#### 4. Budget Tracker 📊
- Set budget by category
- See actual vs budget
- AI provides insights when over budget

#### 5. Simple Dashboard 📈
- Current period summary
- Spending by category
- AI-powered insights

### 💭 Your Turn: What Features Do You Need?

Based on your app idea, what 3-5 core features do you need?

**My core features:**
1. _____________________
2. _____________________
3. _____________________
4. _____________________
5. _____________________

Keep it simple! You can always add more later.

### What We're NOT Building Yet

These come in later chapters:
- ❌ Bank statement import (Chapter 4)
- ❌ Debt snowball calculator (Chapter 4)
- ❌ Due date optimizer (Chapter 4)
- ❌ Savings goals (Chapter 4)
- ❌ Mobile app (Chapter 3)

**Focus:** Get the core working first!

### Tech Stack

- **Frontend:** React + Vite (fast, modern)
- **Styling:** Tailwind CSS (beautiful UI, fast)
- **AI:** OpenAI API (categorization, insights)
- **Storage:** LocalStorage (simple, no backend yet)
- **Hosting:** Vercel (free, easy)
- **Charts:** Recharts (data visualization)

**Why these choices?**
- Beginner-friendly
- AI assistants know them well
- Free to use
- Industry-standard
- Easy to convert to mobile later

---

## Git Workflow Mastery

Before we code, let's learn Git properly. This is the workflow professional developers use every day.

### Understanding Git

**What is Git?**
Think of Git as a time machine for your code:
- Save snapshots (commits) of your work
- Try new ideas safely (branches)
- Collaborate with others (pull requests)
- Never lose work (version history)

**Real-world analogy:**
- **Git** = Track Changes in Microsoft Word
- **GitHub** = Google Drive for code
- **Commit** = Save with a note about what changed
- **Branch** = Make a copy to experiment
- **Merge** = Combine your changes back

### The Git Workflow

```
1. Create a branch (for new feature)
2. Make changes (write code)
3. Commit changes (save snapshot)
4. Push to GitHub (backup online)
5. Create Pull Request (ask to merge)
6. Merge to main (add to main codebase)
```

### Hands-On: Your First Git Workflow

#### Step 1: Create Repository

- [ ] Open Windsurf
- [ ] Open terminal (Ctrl+`)
- [ ] Navigate to your projects folder:
```bash
cd ~/Projects
# or wherever you keep projects
```

- [ ] Create new directory:
```bash
mkdir my-app
cd my-app
```

**💭 Your Turn:** Choose your project name!
- peasant example: `peasant-budget`
- Your app: `my-app` or whatever you want!

- [ ] Initialize Git:
```bash
git init
git branch -M main
```

#### Step 2: Create on GitHub

- [ ] Go to https://github.com/new
- [ ] Repository name: Your project name (e.g., `my-app`)
- [ ] Description: Brief description of your app
- [ ] Public repository
- [ ] **Don't** initialize with README
- [ ] Click "Create repository"

**peasant example:**
- Name: `peasant-budget`
- Description: `AI-powered budget tracker for bi-monthly pay periods`

#### Step 3: Connect Local to GitHub

- [ ] Copy the commands GitHub shows you, or use these:
```bash
git remote add origin git@github.com:YOUR-USERNAME/your-app-name.git
```

Replace `YOUR-USERNAME` and `your-app-name` with your actual values.

#### Step 4: Create Your First Branch

- [ ] Create a branch for setup:
```bash
git checkout -b setup-project
```

**What just happened?**
- `checkout -b` creates a new branch and switches to it
- You're now on `setup-project` branch
- Changes won't affect `main` until you merge

#### Step 5: Understanding Branches

```
main branch:      A---B---C
                       \
setup-project:          D---E
```

- `main` is your production code (always working)
- `setup-project` is where you experiment
- If experiment works, merge it back
- If it fails, delete branch and start over

### Git Commands You'll Use

```bash
# See current branch
git branch

# Create and switch to new branch
git checkout -b feature-name

# See what changed
git status

# Add files to commit
git add .

# Commit with message
git commit -m "Add transaction entry form"

# Push to GitHub
git push origin branch-name

# Switch branches
git checkout main

# Pull latest changes
git pull origin main

# Merge branch into current branch
git merge feature-name
```

### ✅ Checkpoint

You should now:
- [ ] Have `payflow` directory
- [ ] Git initialized
- [ ] Connected to GitHub
- [ ] On `setup-project` branch
- [ ] Understand branches and commits

---

## Set Up Your Project

### Part 1: Create React App with Vite

Vite is a modern tool that creates React apps super fast.

#### Ask AI to Help

- [ ] Open AI assistant in Windsurf (Ctrl+L)
- [ ] Use this prompt:

```
I'm in an empty directory called 'payflow'. I want to create a React app using Vite.
Please give me the exact commands to:
1. Create a new Vite + React project
2. Install dependencies
3. Start the development server
4. Verify it's working

I'm a beginner, so explain what each command does.
```

- [ ] Follow AI's instructions
- [ ] You should see a welcome page at http://localhost:5173

**Expected commands (AI will explain these):**
```bash
npm create vite@latest . -- --template react
npm install
npm run dev
```

#### What Just Happened?

- **Vite** created a React project structure
- **npm install** downloaded all dependencies
- **npm run dev** started a development server
- You can now edit code and see changes instantly!

### Part 2: Install Additional Dependencies

We need a few more tools:

- [ ] Stop the dev server (Ctrl+C in terminal)
- [ ] Ask AI:

```
I need to install these packages for my budget app:
- Tailwind CSS (for styling)
- Recharts (for charts)
- date-fns (for date handling)
- lucide-react (for icons)

Please give me the commands to install and configure these.
```

- [ ] Follow AI's instructions

**Expected commands:**
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm install recharts date-fns lucide-react
```

### Part 3: Set Up Tailwind CSS

- [ ] Ask AI:

```
I just installed Tailwind CSS. Please help me:
1. Configure tailwind.config.js
2. Update my CSS file to include Tailwind
3. Verify it's working with a simple test

Show me exactly what to put in each file.
```

- [ ] Follow AI's instructions
- [ ] Restart dev server: `npm run dev`

### Part 4: Clean Up Starter Files

- [ ] Ask AI:

```
I have a fresh Vite + React project. Please help me:
1. Clean up the default App.jsx to be empty and ready for my budget app
2. Remove unnecessary starter files
3. Create a basic structure for my Peasant app

Keep it simple - just a header that says "Peasant" for now.
```

- [ ] Follow AI's instructions

### Part 5: First Commit!

- [ ] Check what changed:
```bash
git status
```

- [ ] Add all files:
```bash
git add .
```

- [ ] Commit:
```bash
git commit -m "Initial setup: Vite + React + Tailwind"
```

- [ ] Push to GitHub:
```bash
git push origin setup-project
```

### ✅ Checkpoint

You should now have:
- [ ] React app running on localhost:5173
- [ ] Tailwind CSS working
- [ ] Clean App.jsx ready to build
- [ ] First commit pushed to GitHub
- [ ] Basic "Peasant" header showing

**Stuck?** Ask the AI assistant! Paste any error messages and ask for help.

---

## Build the Core Features

Now the fun part - building your app! We'll use AI to help write most of the code.

### Part 1: Project Structure

First, let's organize our code:

- [ ] Ask AI:

```
I'm building a budget app called Peasant. Please help me create a good folder structure:

src/
  components/  (reusable UI components)
  pages/       (main app pages)
  utils/       (helper functions)
  hooks/       (custom React hooks)

Create empty folders and explain what each is for.
```

### Part 2: Transaction Entry Form

This is the heart of the app - where users add income and expenses.

- [ ] Create a new branch:
```bash
git checkout -b feature-transaction-form
```

- [ ] Ask AI:

```
I need to build a transaction entry form for my budget app. It should have:

Fields:
- Date (date picker)
- Amount (number input with $ symbol)
- Description (text input)
- Type (Income or Expense - toggle or select)
- Category (dropdown - AI will suggest based on description)

Features:
- Clean, modern UI with Tailwind
- Form validation
- Submit button
- Clear form after submit

Please create a TransactionForm component in src/components/TransactionForm.jsx

Make it beautiful and user-friendly!
```

- [ ] Copy the code AI provides
- [ ] Create the file
- [ ] Import and use it in App.jsx

**Test it:**
- [ ] Fill out the form
- [ ] Submit (should log to console for now)
- [ ] Form should clear after submit

### Part 3: AI Category Suggestion

Now let's add AI to suggest categories!

- [ ] Ask AI:

```
I want to add AI-powered category suggestions to my transaction form.

When user types a description like "Starbucks", AI should suggest category "Food & Dining".
When they type "Netflix", suggest "Subscriptions".

Please help me:
1. Set up OpenAI API integration
2. Create a function that suggests categories based on description
3. Show the suggestion in the form
4. Let user accept or change it

I'll need to get an API key from OpenAI. Guide me through that too.
```

**Getting OpenAI API Key:**
- [ ] Go to https://platform.openai.com/api-keys
- [ ] Sign up or log in
- [ ] Create new API key
- [ ] Copy it (you won't see it again!)

**Storing API Key Safely:**
- [ ] Ask AI:

```
I have my OpenAI API key. How do I store it safely in my React app?
I need to use environment variables and not commit the key to GitHub.
```

- [ ] Follow AI's instructions (will use `.env` file)
- [ ] Add `.env` to `.gitignore`

**Test AI Categorization:**
- [ ] Type "Starbucks" in description
- [ ] AI should suggest "Food & Dining"
- [ ] Try other descriptions
- [ ] Adjust categories if needed

### Part 4: Transaction List

Display all transactions:

- [ ] Ask AI:

```
Create a TransactionList component that:
- Shows all transactions in a nice table or card layout
- Displays date, description, category, amount
- Color codes: green for income, red for expenses
- Shows icons for each category
- Has a delete button for each transaction
- Responsive design (works on mobile)

Use Tailwind CSS and lucide-react icons.
```

### Part 5: Bi-Monthly Pay Period Selector

This is a key feature!

- [ ] Ask AI:

```
Create a PayPeriodSelector component that:
- Lets user toggle between two pay periods:
  * 1st-15th of current month
  * 16th-end of current month
- Shows which period is currently selected
- Highlights the active period
- Filters transactions to show only current period

Use date-fns library for date calculations.
```

### Part 6: Budget Summary Dashboard

Show the numbers!

- [ ] Ask AI:

```
Create a BudgetSummary component that shows:
- Total income for current pay period
- Total expenses for current pay period
- Remaining budget (income - expenses)
- Progress bar showing spending
- Color coded: green if under budget, red if over

Make it visually appealing with Tailwind.
```

### Part 7: Subscription Detector

AI finds recurring charges:

- [ ] Ask AI:

```
Create a SubscriptionDetector that:
- Analyzes all transactions
- Uses AI to identify recurring charges (Netflix, Spotify, etc.)
- Shows list of detected subscriptions
- Calculates total monthly subscription cost
- Highlights "subscription bleed" if too high

Use OpenAI API to detect patterns and recurring charges.
```

### Part 8: Category Breakdown Chart

Visualize spending:

- [ ] Ask AI:

```
Create a CategoryChart component using Recharts that:
- Shows spending by category as a pie chart or bar chart
- Color coded by category
- Shows percentage of total spending
- Interactive (hover to see details)
- Only shows current pay period

Make it beautiful and easy to understand.
```

### Part 9: AI Insights

Smart recommendations:

- [ ] Ask AI:

```
Create an AIInsights component that:
- Analyzes spending patterns
- Uses OpenAI to generate personalized insights like:
  * "You spent 30% more on dining this period"
  * "Consider canceling unused subscriptions"
  * "You're on track to save $X this month"
- Shows 3-5 actionable insights
- Updates when transactions change

Make insights helpful and encouraging, not judgmental.
```

### Part 10: Data Persistence

Save data locally:

- [ ] Ask AI:

```
I need to save all transactions to localStorage so they persist when page refreshes.

Please help me:
1. Create a custom hook called useLocalStorage
2. Save transactions array to localStorage
3. Load transactions on app start
4. Update localStorage when transactions change

Explain how localStorage works.
```

### Part 11: Put It All Together

- [ ] Ask AI:

```
Help me organize my App.jsx to use all these components:
- TransactionForm at the top
- PayPeriodSelector below that
- BudgetSummary showing key numbers
- CategoryChart for visualization
- TransactionList showing all transactions
- SubscriptionDetector in a sidebar
- AIInsights at the bottom

Create a clean, organized layout with Tailwind CSS.
Make it responsive (works on mobile and desktop).
```

### ✅ Checkpoint

Your app should now:
- [ ] Accept transaction entries
- [ ] AI suggests categories
- [ ] Show transactions by pay period
- [ ] Display budget summary
- [ ] Detect subscriptions
- [ ] Show spending charts
- [ ] Provide AI insights
- [ ] Save data locally
- [ ] Look professional

**Test everything:**
- [ ] Add 10-15 sample transactions
- [ ] Mix of income and expenses
- [ ] Include some subscriptions (Netflix, Spotify, etc.)
- [ ] Switch between pay periods
- [ ] Check that AI insights make sense

### Commit Your Work

- [ ] Check status:
```bash
git status
```

- [ ] Add all changes:
```bash
git add .
```

- [ ] Commit:
```bash
git commit -m "Add core budget features: transactions, AI categorization, insights"
```

- [ ] Push:
```bash
git push origin feature-transaction-form
```

---

## Deploy Your App

Time to make it live!

### Part 1: Prepare for Deployment

- [ ] Ask AI:

```
I want to deploy my React app to Vercel. 
Please help me:
1. Create a vercel.json config if needed
2. Make sure environment variables are set up correctly
3. Prepare for production build

What do I need to check before deploying?
```

### Part 2: Deploy to Vercel

- [ ] Go to https://vercel.com
- [ ] Sign up with GitHub
- [ ] Click "New Project"
- [ ] Import your `payflow` repository
- [ ] Configure:
  - Framework Preset: Vite
  - Root Directory: ./
  - Build Command: `npm run build`
  - Output Directory: `dist`
- [ ] Add environment variable:
  - Name: `VITE_OPENAI_API_KEY`
  - Value: Your OpenAI API key
- [ ] Click "Deploy"

### Part 3: Wait for Build

- [ ] Watch the build process
- [ ] Should take 1-2 minutes
- [ ] If errors, read them and ask AI for help

### Part 4: Your App is Live!

- [ ] Vercel gives you a URL: `payflow-xxx.vercel.app`
- [ ] Click it to see your live app
- [ ] Test all features
- [ ] Share with friends!

### Part 5: Custom Domain (Optional)

- [ ] Ask AI:

```
I want to add a custom domain to my Vercel app.
How do I:
1. Buy a domain (where's cheapest?)
2. Connect it to Vercel
3. Set up SSL certificate

Guide me through the process.
```

### ✅ Checkpoint

You should now have:
- [ ] Live app at a public URL
- [ ] All features working online
- [ ] Environment variables configured
- [ ] App accessible from any device

**Celebrate!** 🎉 You built and deployed a real web app!

---

## What's Next

### Immediate Next Steps

1. **Use Your App**
   - [ ] Add your real transactions
   - [ ] Track your actual budget
   - [ ] See if it helps your finances

2. **Get Feedback**
   - [ ] Share with friends/family
   - [ ] Ask what's confusing
   - [ ] Note feature requests

3. **Improve It**
   - [ ] Fix bugs you find
   - [ ] Improve UI based on feedback
   - [ ] Add small features

### Chapter 3 Preview: Mobile App

Next chapter, we'll convert this to a mobile app:
- React Native + Expo
- Camera to scan receipts
- Push notifications for bills
- Works offline
- Test on your phone

### Chapter 4 Preview: Advanced Features

Then we'll add the power features:
- Import bank statements (CSV)
- Debt snowball calculator
- Due date optimizer
- Savings goal tracker
- Interest savings projections
- Better charts and analytics

### Chapter 5 Preview: Production Ready

Make it professional:
- Data encryption
- Security hardening
- Automated testing
- Error tracking
- Performance optimization

### Chapter 6 Preview: App Store

Finally, launch it:
- Submit to Apple App Store
- Submit to Google Play Store
- Marketing and launch
- Get real users!

---

## Troubleshooting

### Common Issues

#### "npm command not found"
- Node.js not installed
- Install from https://nodejs.org
- Restart terminal

#### "OpenAI API errors"
- Check API key is correct
- Check you have credits ($5 free to start)
- Check .env file is loaded

#### "App won't deploy"
- Check build runs locally: `npm run build`
- Check environment variables in Vercel
- Read error messages carefully

#### "AI suggestions are weird"
- Improve your prompts
- Add more context
- Try different models (gpt-4 vs gpt-3.5)

#### "Styling looks broken"
- Check Tailwind is configured
- Check CSS imports
- Clear browser cache

### Getting Help

- **AI Assistant:** Ask in Windsurf (paste error messages)
- **GitHub Issues:** https://github.com/ProvenGuilty/sudo-make-me-a-developer/issues
- **Vercel Docs:** https://vercel.com/docs
- **React Docs:** https://react.dev
- **OpenAI Docs:** https://platform.openai.com/docs

---

## Key Learnings

### What You Accomplished

- ✅ Built a real, useful web application
- ✅ Learned React fundamentals
- ✅ Integrated AI (OpenAI API)
- ✅ Mastered Git workflow
- ✅ Deployed to production
- ✅ Created something you can actually use

### Skills Gained

**Technical:**
- React components and hooks
- State management
- API integration
- Data visualization
- Form handling
- Local storage
- Deployment

**Professional:**
- Git branching and merging
- Code organization
- Problem-solving with AI
- Reading documentation
- Debugging

**Mindset:**
- You CAN build real apps
- AI is a powerful tool
- Breaking big problems into small steps
- Learning by doing

---

## Reflection Questions

- [ ] What was the hardest part?
- [ ] What surprised you?
- [ ] What would you do differently?
- [ ] What feature do you want to add next?
- [ ] How will you use this app in real life?

---

## Share Your Success!

- [ ] Tweet your live app URL
- [ ] Post on LinkedIn
- [ ] Show friends and family
- [ ] Add to your portfolio
- [ ] Star the sudo-make-me-a-developer repo

---

**Congratulations!** 🎉

You're no longer a beginner. You're a developer who ships.

See you in Chapter 3 where we turn this into a mobile app!

---

*Last Updated: November 2025*
