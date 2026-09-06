# 🛡️ Discord HypeSquad Badge Claimer (Console Script)

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Discord API](https://img.shields.io/badge/Discord-API-5865F2?style=for-the-badge&logo=discord&logoColor=white)
![Open Source](https://img.shields.io/badge/Open%20Source-Yes-brightgreen?style=for-the-badge)

A quick, lightweight JavaScript snippet to claim any Discord HypeSquad badge (Bravery, Brilliance, or Balance) directly from your browser's console, even if the official in-app program/quiz has ended.

This script works by hooking into Discord's internal Webpack chunks to access the `HTTPUtils` module, allowing it to send an authenticated request to the `/hypesquad/online` API endpoint using your active browser session.

---

## ⚠️ Important Disclaimer (READ BEFORE USING)

> **Automating user accounts or sending unauthorized API requests violates [Discord's Terms of Service](https://discord.com/terms).** 
> 
> Even though this script simply sends a standard request to an active API endpoint (without "hacking" or exploiting vulnerabilities), **there is still a risk of your account being warned or banned.** 
> 
> **Use this script at your own risk.** I am not responsible for any actions taken against your account. This is provided for educational purposes only.

---

## ✨ The Houses

Choose your preferred house by changing the ID in the script:

| ID | House | Description |
| :---: | :--- | :--- |
| `1` | 🟣 **Bravery** | The universe needs people to lead the charge with confident optimism. |
| `2` | 🔴 **Brilliance** | It takes patience and discipline to become a vital member of the universe. |
| `3` | 🟢 **Balance** | Harmony and equilibrium are necessary to create a successful universe. |

---

## 🚀 How to Use (Step-by-Step)

No downloads or Node.js installations are required. You execute this directly inside Discord's web client.

1. **Log in to Discord:** Open your browser and go to [discord.com/app](https://discord.com/app).
2. **Open Developer Tools:** Press `F12` (or `Ctrl + Shift + I` / `Cmd + Option + I` on Mac) and navigate to the **Console** tab.
3. **Bypass the Warning:** Discord blocks pasting code by default to protect users from Self-XSS attacks. Type `allow pasting` in the console and hit `Enter` to enable it.
4. **Copy the Script:** Copy the code from [`HypeSquadScript.js`](HypeSquadScript.js) in this repository.
5. **Select Your Badge:** Before hitting enter, look at the last line of the code:
   ```javascript
   api.post({ url: "/hypesquad/online", body: { house_id: 1 } });
