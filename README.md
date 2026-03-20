<div align="center">

<img src="https://img.shields.io/badge/TikTok--Downloader-Latest-010101?style=for-the-badge&logo=tiktok&logoColor=white" alt="TikTok-Downloader Latest" />

# 🎵 TikTok Downloader

### Download TikTok videos, audio, and slideshows — no watermark, no account needed.

[![Node.js](https://img.shields.io/badge/Node.js-18.x+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/Advay254/TikTok-Downloder/pulls)
[![Deploy on Render](https://img.shields.io/badge/Deploy%20on-Render-46E3B7?style=flat-square&logo=render&logoColor=white)](https://render.com)

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank">
  <img src="https://img.shields.io/badge/Support%20Me-%E2%98%95%20Buy%20Me%20a%20Coffee-010101?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white" alt="Support Me" />
</a>

<br/><br/>

> Paste a TikTok link. Get your media. No watermark, no sign-up, ever.

<br/>

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=010101&center=true&vCenter=true&width=500&lines=Download+TikTok+Videos+%F0%9F%8E%AC;Save+TikTok+Audio+as+MP3+%F0%9F%8E%B5;Download+TikTok+Slideshows+%F0%9F%96%BC%EF%B8%8F;No+Watermark.+No+Account.+Always+Free.)

</div>

---

## ✨ Features

<img align="right" width="380" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="coding gif"/>

- 🎬 **TikTok video downloads** — full quality, no watermark
- 🎵 **Audio extraction** — save TikTok audio as MP3
- 🖼️ **Slideshow downloads** — save TikTok photo slideshows
- 📱 **Full PWA** — installable on Android and iOS
- 📲 **Android APK** — native app experience, no browser bar
- ⚡ **Fast and lightweight** — no bloat, no tracking
- 🔒 **Secure** — no data stored, no login required
- 🚀 **Deploy anywhere** — Render, Railway, Fly.io, any Node.js host

<br clear="right"/>

---

## 🗂️ Project Structure

```
TikTok-Downloader/
├── index.js          # Launcher — fetches and starts the core engine
├── package.json      # Launcher dependencies only
├── .env.example      # Environment variable reference
├── version.txt       # Current release version
└── .gitignore
```

> The core application is loaded securely at runtime. This keeps the source lean and the deployment simple.

---

## 🚀 Quick Start

### 1. Fork or clone the repo

```bash
git clone https://github.com/Advay254/TikTok-Downloder.git
cd TikTok-Downloder
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

```bash
cp .env.example .env
```

Edit `.env` with your values:

```env
SITE_URL=http://localhost:3000
OWNER_API_KEY=your_owner_api_key_here
RAPIDAPI_SECRET=your_rapidapi_secret_here
```

### 4. Run

```bash
npm start
```

Visit `http://localhost:3000` — you're live. 🎉

---

## 🔑 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `SITE_URL` | ✅ **Yes** | Full production domain. Example: `https://yoursite.onrender.com` |
| `OWNER_API_KEY` | ✅ **Yes** | Owner key that protects internal API endpoints |
| `RAPIDAPI_SECRET` | ✅ **Yes** | Secret for RapidAPI proxy authentication |
| `AD_BANNER_URL` | Optional | Banner ad URL — leave blank to disable |
| `AD_CDN_URL` | Optional | Ad CDN URL — leave blank to disable |
| `AD_POPUNDER_URL` | Optional | Popunder ad URL — leave blank to disable |
| `AD_SMARTLINK_URL` | Optional | Smartlink ad URL — leave blank to disable |
| `PORT` | Auto | Set automatically by Render — do not set manually |

---

## 🌐 Deploying to Production

### Render (recommended)

<img align="right" width="300" src="https://media.giphy.com/media/RbDKaczqWovIugyJmW/giphy.gif" alt="deploy gif"/>

1. Fork this repo to your GitHub account
2. Go to [render.com](https://render.com) and create a new **Web Service**
3. Connect your forked repo
4. Set **Build Command:** `npm install`
5. Set **Start Command:** `npm start`
6. Add your environment variables under **Environment**
7. Click **Deploy**

> Render free tier sleeps after 15 minutes of inactivity. Use [cron-job.org](https://cron-job.org) to ping your site every 10 minutes to keep it awake.

<br clear="right"/>

### Railway

```bash
npm install -g @railway/cli
railway login && railway init && railway up
```

Add your environment variables in the Railway dashboard under **Variables**.

### Any VPS (Ubuntu/Debian)

```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
git clone https://github.com/Advay254/TikTok-Downloder.git
cd TikTok-Downloder && npm install
npm install -g pm2
pm2 start index.js --name tiktok-downloader
pm2 save && pm2 startup
```

---

## 🛠️ How It Works

```
User deploys TikTok Downloader
        ↓
Launcher starts and fetches the core engine securely at runtime
Core engine extracts and installs its own dependencies
        ↓
App starts — ready to accept TikTok URLs
        ↓
User pastes a TikTok video, audio, or slideshow URL
        ↓
Server fetches media metadata and resolves download links
        ↓
User downloads video, audio or slideshow
No watermark. No account. No hassle.
```

---

## 📊 Tech Stack

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)

</div>

---

## 🔄 Updates

Check `version.txt` for the latest release version. Sync your fork and redeploy on Render to get the latest update automatically.

---

## 🤝 Contributing

1. Fork the repo
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit: `git commit -m 'Add your feature'`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## ⚠️ Disclaimer

TikTok Downloader is an independent open-source project and is **not affiliated with, endorsed by, or connected to TikTok or ByteDance** in any way.

This tool is intended for downloading your own content or content you have the right to download. Users are responsible for complying with TikTok's terms of service and copyright laws in their country.

---

## 📄 License

MIT © 2026 Advay — free to use, modify, and distribute.

---

<div align="center">

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=Advay254.TikTok-Downloder)

**If TikTok Downloader saved you time, drop a ⭐ — it helps others find the project.**

<br/>

<a href="https://www.buymeacoffee.com/advay254" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

</div>
