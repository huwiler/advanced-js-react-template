# Website Project (Vite + Bootstrap — No React)

This folder contains your **marketing website** for Advanced JavaScript with React.

For the website portion (Weeks 1–3), we will **not** use React.  
Instead, you'll build a modern JavaScript website using:

- **Vite** (for fast bundling & dev server)
- **Bootstrap 5** (for layout & UI)
- **Modular ES6 JavaScript**

This mirrors *real-world static site development* and keeps the React learning focused on the **mobile app**.

---

## Step 1 — Create your Vite project (Vanilla JS template)

From the root of your repo:

```bash
cd website
npm create vite@latest .
```

Choose:

```
✔ Select a framework: › Vanilla
✔ Select a variant: › JavaScript
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

## Step 3 — Import Bootstrap into your main JavaScript file

Open `src/main.js` and add:

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

## Why no React on the website?

- The website is a **static marketing site**, not a dynamic web app  
- Vite + Bootstrap gives you a fast, modern developer experience  
- You learn modular JavaScript without React abstractions  
- React knowledge is saved for the **mobile app**, where it matters most  
- You practice deploying a built static site — exactly how it works in industry  

---

## Important Notes

- Never install dependencies at the root of the repository  
- Always run commands inside `website/`  
- Do not commit `dist/`  