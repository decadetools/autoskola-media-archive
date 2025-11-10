# 📦 Autoškola Media Archive (App Distribution via GitHub Releases)

This repository exists **only to host the latest version of the app (ZIP file)** for public download.  
The actual app code is stored elsewhere — this repo is just for **distributing pre-built updates** to users.

---

## 🧠 What This Repo Is For

- Provide a **public download link** that anyone can access  
- Use **GitHub Releases** to host the ZIP file cheaply (free)  
- Keep one simple place where users (or the app itself) can fetch the newest version

---

## 🚀 How It Works

1. Each time you upload a new ZIP through **GitHub Releases**,  
   GitHub automatically serves it via its global CDN.

2. The download link looks like this:

https://github.com/decatetools/autoskola-media-archive/releases/download/v1.0/autoskola-media.zip

yaml
Zkopírovat kód

3. Anyone can download it — no authentication needed.

---

## 🔁 How To Upload a New Version

Every time the app changes and you generate a new `.zip` file:

### 🖱️ Option 1: Web UI
1. Go to the repo  
→ **Releases** → **Draft a new release**  
→ or open directly:  
https://github.com/decatetools/autoskola-media-archive/releases/new

markdown
Zkopírovat kód
2. Enter:
- **Tag version:** e.g. `v1.1`  
- **Title:** short note (e.g. “App update 2025-11-10”)  
- **Description:** what’s new (optional)
3. **Drag your ZIP** (`autoskola-media.zip`) into the upload area
4. Click **Publish release**
5. Done — your new ZIP is now publicly downloadable 🎉

### 💻 Option 2: Command Line (faster)
If you have the GitHub CLI installed:
```bash
gh release create v1.1 autoskola-media.zip -t "App update 2025-11-10" -n "Minor fixes and improvements"
That automatically creates the release and uploads your ZIP.

🔗 How To Share The Download Link
Use the direct latest release link format:

arduino
Zkopírovat kód
https://github.com/decatetools/autoskola-media-archive/releases/latest/download/autoskola-media.zip
💡 The latest tag always points to the newest release —
so you don’t need to update the link every time!

Example (yours):

arduino
Zkopírovat kód
https://github.com/decatetools/autoskola-media-archive/releases/latest/download/autoskola-media.zip
Share that anywhere (website, app updater, etc.).

🧰 Notes & Tips
File size limit: 2 GB per ZIP

Bandwidth: Free and CDN-delivered globally

Don’t push large binaries into Git — always upload via Releases

Keep version tags consistent (v1.0, v1.1, v1.2, …)

Optionally delete old releases to stay tidy

🧭 Why We’re Doing This
GitHub Releases are:

💸 Free CDN hosting for large files

🌍 Fast and globally cached

🧱 Reliable for long-term download links

🔗 Perfect for distributing app binaries or updates

This repo’s purpose is to stay lightweight and serve as a public download endpoint for the Autoškola app — nothing else.

🧩 Summary for Future Me
“Hey future me — remember:
this isn’t the app source code — it’s our delivery bucket.
When the app changes, make a new autoskola-media.zip,
upload it as a new GitHub release,
and share the /releases/latest/download/autoskola-media.zip link.” 💾
