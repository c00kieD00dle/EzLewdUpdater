# EzLewdUpdater

A simple **Playnite Generic Plugin** that checks for game updates by comparing the local version (from the game name) against the latest version available on linked **F95** pages. Notifications are shown in Playnite if updates are found.

---
## Important!
- Games must be in format: ```gamename [version]```
- Games need to have a valid f95 threadlink, named ```f95```
---

## ✅ Features
- Adds a **"Check Game Updates"** option to the Playnite main menu.
- Compares the version in your game name (e.g., `[v1.2]`) to the version found on the linked page.
- Uses **customizable regex** to detect version numbers.
- Option to **exclude keywords** (e.g., `completed`, `final`) or specific games.
- Clickable notifications that open the linked page in your browser.
- Logs update results to `update_log.txt` in the plugin folder.

---

## 🛠 Requirements
- **Playnite** 10.37 (or newer)
- **Playnite SDK** 6.12

---

## 🔍 How It Works
1. When you click **Check Game Updates**, the plugin:
   - Scans all games in your Playnite library.
   - Skips games with excluded keywords or names.
   - Looks for a version string in the game name using your configured **Regex**.
   - Checks if the game has an **F95 link** (Link name must be named `f95`).
   - Fetches the HTML page title from the F95 thread.
   - Extracts the online version using the same **Regex**.
2. If the local and online versions differ, you get a **Playnite notification** with a direct link to the game page.
3. Results are appended to `update_log.txt`.

---

## ⚙️ Settings
Accessible under **Add-ons → Extensions settings → Generic → EzLewdUpdater**:

- **Regex Pattern**  
  Default:  
  ```\[(?:v)?[\d][^\]]*\]```
- **Excluded Keywords**  
  Default:  
  ```completed, final```
- **Excluded Games**  
