# Advanced JavaScript with React – Course Starter Template

Welcome to **Advanced JavaScript with React** at Champlain College!

This repository serves as your **project foundation** for the entire course.  
Throughout Weeks 1–7, you will build two related deliverables:

1. **A marketing website for your app** (Vite + React)  
2. **A mobile app** (React Native + Expo)  

Both projects will live inside this single repository, mirroring modern **monorepo** workflows used in industry.

---

## Repository Structure

```
root/
├── website/   → Your Vite-based marketing site (Weeks 1–3)
├── mobile/    → Your Expo mobile app (Weeks 4–7)
├── scripts/   → Deployment or utility scripts created later
├── README.md  → You are here
├── .gitignore → Preconfigured to avoid common issues
└── package.json → Warns you *not* to install dependencies at root
```

---

## Getting Started

### Before you start: Git setup

- Confirm Git is installed: `git --version` (install Xcode Command Line Tools on macOS with `xcode-select --install`, or Git for Windows from git-scm.com if missing).
- Configure your identity so commits are attributed correctly:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

- Sign in before your first push. GitHub no longer accepts account passwords over HTTPS—use a browser-based login or token:
  - Easiest: run `gh auth login` and follow the prompts (select HTTPS and “Login with a web browser”). Install GitHub CLI if needed: macOS `brew install gh`, Windows `winget install GitHub.cli`, Ubuntu `sudo apt install gh`.
  - Alternatively, on your first `git push`, use the browser prompt. If asked for a password in terminal, paste a Personal Access Token instead of your GitHub password.

### 1. Create your own personal repository

**Do not work in the class template directly.**  
After cloning, you will create a brand-new GitHub repo that belongs to you.

```bash
git clone https://github.com/huwiler/advanced-js-react-template.git my-project
cd my-project

# remove template remote
git remote remove origin

# Go to GitHub website -> New Repository -> name it (Do NOT initialize with README or gitignore) -> Create.  This gives you the
# HTTPS URL to your repo, which you will need for the next step.

# add your own new GitHub repo
git remote add origin <YOUR_NEW_REPO_HTTPS_URL>
git push -u origin main
```

### Install Node.js and npm

Install the current LTS release (npm comes with Node):

- macOS: `brew install node` (or use the installer from nodejs.org if you don’t use Homebrew).
- Windows: `winget install OpenJS.NodeJS.LTS` (or grab the LTS installer from nodejs.org).
- Linux (Debian/Ubuntu): `sudo apt update && sudo apt install -y nodejs npm` (or use nvm/nodesource for newer versions).

Verify your setup:

```bash
node -v
npm -v
```

---

## Setting up your Website project (Weeks 1–3)

See /website/README.md

---

## Setting up your mobile app (Weeks 4-7)

See /mobile/README.md

---

## Important Rules

### 1. **Do not install dependencies at the root of the repository.**
Always install inside:

- `website/`
- `mobile/`

### 2. **Do not commit `node_modules` or build artifacts.**
This repo includes a `.gitignore` tailored for Vite + Expo.

### 3. **Keep your repo clean and organized.**
Consistency is part of your grade.

---

## Optional Enhancements

As you progress, you may:

- Add a shared component library
- Add a shared assets folder
- Add deployment scripts in `/scripts`
- Apply industry patterns such as monorepo organization

---

## Have fun and build something great!

This repo will evolve with you throughout the course.  
If you have questions, please ask early — small issues get big fast in React projects.

Good luck, and welcome to **Advanced JavaScript with React**!
