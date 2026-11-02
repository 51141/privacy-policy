# Multi-App Privacy Policy Hub

A centralized, responsive, and lightweight privacy policy portal hosted with GitHub Pages. Designed to host compliance documentation for all your Android and iOS applications in one single place.

---

## 📁 Repository Structure

```text
privacy-policies/
├── index.html               # Main Hub: lists all your apps with cards and links
├── box-launcher/
│   └── index.html           # Box Launcher's offline privacy policy
├── template/
│   └── index.html           # Starter boilerplate for your future apps
└── README.md
```

---

## 🚀 Setup Guide: Host on GitHub Pages (Step-by-Step)

### Step 1: Create a New GitHub Repository
1. Go to [github.com/new](https://github.com/new).
2. Repository name: `privacy-policies` (or `policies`).
3. Set visibility to **Public** (required for free GitHub Pages).
4. Do **not** initialize with a README, .gitignore, or license (we already have everything here).
5. Click **Create repository**.

### Step 2: Push This Folder to GitHub
Open your terminal (PowerShell or Bash) and run:

```powershell
# Navigate into the privacy-repo folder
cd f:\apps\box-launcher\playstore-assets\privacy-repo

# Initialize Git
git init -b main

# Add all files
git add .

# Commit
git commit -m "Initial commit: privacy hub and Box Launcher policy"

# Link to your new GitHub repository (replace with your GitHub username)
git remote add origin https://github.com/<your-username>/privacy-policies.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. On your GitHub repository page, click **Settings** (top bar).
2. On the left sidebar under *Code and automation*, click **Pages**.
3. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**.

Within 1 minute, your site will be live at:
```
https://<your-username>.github.io/privacy-policies/
```

---

## 🔗 Your Play Store URLs

| App | Play Store Privacy Policy URL |
| :--- | :--- |
| **Main Hub (All Apps)** | `https://<your-username>.github.io/privacy-policies/` |
| **Box Launcher** | `https://<your-username>.github.io/privacy-policies/box-launcher/` |
| **Future App** | `https://<your-username>.github.io/privacy-policies/<app-slug>/` |

---

## ➕ How to Add a New App in the Future

1. **Duplicate the template folder:**
   Copy the `template/` folder and rename it to your new app's slug (e.g. `weather-box/`):
   ```powershell
   Copy-Item -Recurse template weather-box
   ```
2. **Edit `weather-box/index.html`:**
   Update the title, permissions, and details for the new app.
3. **Add a card in the root `index.html`:**
   Uncomment and customize the app card inside `index.html`.
4. **Push the changes:**
   ```powershell
   git add .
   git commit -m "Add Weather Box privacy policy"
   git push
   ```
   GitHub Pages will update your live site automatically!
