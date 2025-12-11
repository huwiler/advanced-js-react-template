# Website Project (Vite + React + Bootstrap)

This folder contains your **React marketing website** for Advanced JavaScript with React.

For the website portion (Weeks 1–3), you'll build a modern React site using:

- **Vite** (for fast bundling & dev server)
- **React** (for UI)
- **Bootstrap 5** (for layout & UI helpers)

---

## Step 1 — Create your Vite project (React template)

From the root of your repo:

```bash
cd website
npm create vite@latest .
```

Choose:

```
Select "Ignore files and continue" to keep your README.md in the website directory.
Select a framework: › React
Select a variant: › JavaScript
Select "No" when asked to use rolldown-vite
```

Install dependencies:

```bash
npm install
```

---

## Step 2 — Install Bootstrap

```bash
npm install bootstrap
```

---

## Step 3 — Import Bootstrap into your main entry file

Open `src/main.jsx` and add:

```js
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap'; // optional JS components
```

You can now use Bootstrap classes and JavaScript components.

---

## Step 4 — Run the development server

```bash
npm run dev
```

Visit the local server URL Vite prints out.

---

## Step 5 — Build for production (important!)

This is how you create deployable files for Starfruit:

```bash
npm run build
```

The output will be created in:

```
website/dist/
```

You will later write a deployment script that uploads this folder to your personal `public_html` on Starfruit using `rsync`.

---

## Why React on the website?

- Reinforces React fundamentals before the mobile app  
- Reuses familiar patterns between web and mobile  
- Keeps the toolchain modern and fast with Vite  
- Lets you practice production builds and deployments with React  

---

## Important Notes

- Never install dependencies at the root of the repository  
- Always run commands inside `website/`  
- Do not commit `dist/`  
