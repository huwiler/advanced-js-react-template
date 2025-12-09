# Advanced JavaScript with React – Course Starter Template

Welcome to **Advanced JavaScript with React** at Champlain College!

This repository serves as your **project foundation** for the entire course.  
Throughout Weeks 1–7, you will build two related deliverables:

1. **A marketing website** (Vite + React)  
2. **A mobile app** (React Native + Expo)  

Both projects will live inside this single repository, mirroring modern **monorepo** workflows used in industry.

---

## 📁 Repository Structure

```
root/
├── website/   → Your Vite-based marketing site (Weeks 1–3)
├── mobile/    → Your Expo mobile app (Weeks 4–7)
├── assets/    → Shared images, icons, logos (optional)
├── scripts/   → Deployment or utility scripts created later
├── README.md  → You are here
├── .gitignore → Preconfigured to avoid common issues
└── package.json → Warns you *not* to install dependencies at root
```

---

## 🚀 Getting Started

### 1. Create your own personal repository

**Do not work in the class template directly.**  
After cloning, you will create a brand-new GitHub repo that belongs to you.

```bash
git clone <TEMPLATE_URL> my-project
cd my-project

# remove template remote
git remote remove origin

# add your own new GitHub repo
git remote add origin <YOUR_NEW_REPO_URL>
git push -u origin main
```

---

## 🧩 Setting up your Website project (Weeks 1–3)

Inside `website/`:

```bash
cd website
npm create vite@latest .
npm install
npm run dev
```

You will build your marketing site here.

---

## 📱 Setting up your Mobile App (Weeks 4–7)

Inside `mobile/`:

```bash
cd mobile
npx create-expo-app .
npm install
npm run start
```

You will build your React Native mobile app here.

---

## 🌐 Deploying Your Website to Starfruit

Later in the course, you’ll write a script to:

1. Build your website (`npm run build`)
2. Upload the result to your Starfruit `public_html` using `rsync`

Deployment examples will be provided during the course.

---

## ❗ Important Rules

### 1. **Do not install dependencies at the root of the repository.**
Always install inside:

- `website/`
- `mobile/`

### 2. **Do not commit `node_modules` or build artifacts.**
This repo includes a `.gitignore` tailored for Vite + Expo.

### 3. **Keep your repo clean and organized.**
Consistency is part of your grade.

---

## 🧪 Optional Enhancements

As you progress, you may:

- Add a shared component library
- Add a shared assets folder
- Add deployment scripts in `/scripts`
- Apply industry patterns such as monorepo organization

---

## 🎉 Have fun and build something great!

This repo will evolve with you throughout the course.  
If you have questions, please ask early — small issues get big fast in React projects.

Good luck, and welcome to **Advanced JavaScript with React**!