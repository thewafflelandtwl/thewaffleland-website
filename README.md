# The Waffle Land - Website

This is a premium, static single-page web application built for **The Waffle Land** (Specializing in Waffles, Mini Pancakes, and Real Fruit Ice Creams). Designed to be hosted on **GitHub Pages** with custom domain integration (`thewaffleland.co.in`).

## ✨ Features

- **Premium Cocoa Theme**: Built using clean HSL dark colors, golden/amber glow, warm typography, and glassmorphic cards.
- **Hero Image Carousel**: Smooth fading slider showcase featuring authentic product images.
- **Interactive Menu**: Instantly filter products by category (Waffles, Mini Pancakes, Brownies, Real Fruit Ice Creams).
- **Interactive Waffle Customizer Widget**: Interactive lab where visitors select waffle base, drizzles, and toppings with real-time price updates and visual feedback overlays.
- **Instagram Social Integration**: Integrated gallery grid linking directly to Instagram profile `@thewaffleland`.
- **Responsive Layout**: Fluid experience tailored for desktop, tablet, and mobile browsers.

## 🚀 How to Run Locally

Since this is a static webpage with pure HTML, CSS, and JS, no compilation is needed!

1. Double-click `index.html` to open it directly in your browser.
2. Alternatively, start a simple local server inside this folder:
   ```bash
   # If you have Python installed:
   python3 -m http.server 8000
   ```
   Open `http://localhost:8000` in your web browser.

---

## 🌐 Deploying to GitHub Pages

1. **Create a GitHub Repository**:
   - Go to GitHub and create a new repository (e.g., `thewaffleland-website`).
   - Push these codebase files to your repository's `main` or `master` branch.

2. **Enable GitHub Pages**:
   - Go to your repository **Settings** -> **Pages** (in the sidebar).
   - Under **Build and deployment**, set the source to **Deploy from a branch**.
   - Choose your branch (e.g., `main` or `/root`) and click **Save**.

---

## 🏷️ Setting up Custom Domain in GoDaddy

Since this project has a custom domain (`thewaffleland.co.in`), follow these steps to link it:

1. **GitHub Custom Domain settings**:
   - In GitHub repository **Settings** -> **Pages**, scroll to the **Custom domain** section.
   - Enter `thewaffleland.co.in` and click **Save** (this will verify the `CNAME` file inside the repository).

2. **GoDaddy DNS Configuration**:
   - Log into your **GoDaddy Control Panel**.
   - Select your domain (`thewaffleland.co.in`) and click **Manage DNS**.
   - Add/Update the following records:

#### A Records (Points your apex domain to GitHub's servers)
Create **four A records** with host `@` pointing to:
- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

#### CNAME Record (Points www subdomain to your GitHub domain)
Create/Update a **CNAME record**:
- **Name/Host**: `www`
- **Value/Target**: `<your-github-username>.github.io`
- **TTL**: `1 Hour` (or default)

*Note: DNS changes can take a few minutes to 24 hours to propagate worldwide.*

---

## 📸 Updating Images (Real Fruit Ice Cream & Classic Pancakes)

Currently, Waffles, Brownies, Waffle Pizzas, and Triple Chocolate Pancakes are linked to your provided real images. Other items (like Alphonso Mango Shell, Real Coconut Shell, and Classic Maple Pancakes) use clean CSS icon placeholders.

To replace any remaining placeholders:
1. Save your photo in the `assets/` directory (e.g., `assets/alphonso_mango_shell.jpg`).
2. Open `index.html`.
3. Locate the menu card for that item, look for the placeholder image element:
   ```html
   <div class="menu-img-container placeholder-img">
     <svg>...</svg>
   </div>
   ```
4. Replace that block with a standard image element pointing to your new photo:
   ```html
   <div class="menu-img-container">
     <img src="assets/alphonso_mango_shell.jpg" alt="Alphonso Mango Shell" class="menu-img">
   </div>
   ```
5. Commit and push the changes.

