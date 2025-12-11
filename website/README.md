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

This starts the automatically installs and starts vite server.  Stop the server for now by holding Control and pressing C.

```
CTRL^C
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

This starts a local dev server (default: http://localhost:5173). Open that URL to see the Vite placeholder page render in the browser.

- Stop the server: press `Ctrl+C` in the terminal running Vite.
- Start it again (from `website/`): `npm run dev`

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

- In order for your react site to work on starfruit, make the following change to website/vite.config.js:

```
export default defineConfig({
    base: '/~your-username/', // <-- Add this line substiting your username
    plugins: [react()],
})
```

- Never install dependencies at the root of the repository  
- Always run commands inside `website/`  
- Do not commit `dist/`  

## Deployment

When you are ready to deploy changes to starfruit, read scripts/README.md to learn how AI can assist in automating the deployment process.
