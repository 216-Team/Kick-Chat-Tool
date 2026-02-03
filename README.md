<div align="center">

# 🎮 Kick Chat Tool

<img src="https://media.discordapp.net/attachments/1412417122956607509/1468060693046493204/image.png?ex=6982a590&is=69815410&hm=8573322de0e6d5cc7b1ee0323fd9cea63d9876b2a76af0659adcc7590f4321b2&=&format=webp&quality=lossless&width=388&height=600" width="200" alt="Kick Chat Tool Preview"/>
<img src="https://media.discordapp.net/attachments/1412417122956607509/1468061113487724747/image.png?ex=6982a5f4&is=69815474&hm=75eca067fcc9f6643868e1c06989928dd69ae425ca74d28eff604302be4df8ed&=&format=webp&quality=lossless&width=384&height=600" width="200" alt="Kick Chat Tool Preview"/>

**A modern, premium chat automation tool for Kick.com**

[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows)](https://www.microsoft.com/windows)

</div>

---

## ✨ Features

- ⌨️ **Human‑Like Typing**  
  Simulates real typing delays for natural chat behavior.

- 🔀 **Shuffle & Loop Messages**  
  Randomize message order and loop queues endlessly.

- 🙂 **Auto Emotes**  
  Automatically append random popular Kick emotes.

- 🔎 **Auto Chatroom Fetch**  
  Detects chatroom IDs directly from channel names.

- 🖥️ **Live Console**  
  Real‑time logs, status updates, and event tracking.

- 💾 **Persistent Settings**  
  All configurations are saved automatically.

---

## 🚀 Setup & Installation

1. **Download**  
   Get the latest `KickTools.exe` from the  
   👉 [Releases Page](https://github.com/216-Team/kick-chat-tool/releases)

2. **Run**  
   Double‑click the `.exe` file (no installation needed).

3. **Login**  
   Paste your **Bearer Token** inside the app.

---

## 🔑 How to Get Your Kick Bearer Token

1. Open 👉 [https://kick.com](https://kick.com) and log in.
2. Press **F12** to open Developer Tools.
3. Go to the **Console** tab.
4. Paste the script below and press **Enter**:

```javascript
(function() {
    console.clear();
    const originalFetch = window.fetch;
    window.fetch = async function(...args) {
        const config = args[1] || {};
        const headers = config.headers || {};
        let auth = '';
        if (headers instanceof Headers) auth = headers.get('authorization');
        else auth = headers['Authorization'] || headers['authorization'];

        if (auth && auth.startsWith('Bearer ')) {
            const token = auth.replace('Bearer ', '');
            console.log('%c🔑 KICK TOKEN DETECTED:', 'color: #A855F7; font-weight: bold; font-size: 14px;');
            console.log(token);
            if (typeof copy === 'function') {
                copy(token);
                console.log('%c✅ Token copied to clipboard!', 'color: #22c55e;');
            }
        }
        return originalFetch.apply(this, args);
    };
    console.log('%c📡 Interceptor active! Refresh the page (F5) to capture your token.', 'color: #A855F7; font-weight: bold;');
})();
 ```
Refresh the page (F5).

Your token will appear in the console and be auto‑copied 🎉

🛣️ Roadmap / Future Plans
⭐ 10 Stars – Multi‑Account Support
⭐ 50 Stars – Nuke Chat (Cooldown Bypass)
⭐ 100 Stars – Live Viewer Support (1K–3K)
⭐ 500 Stars – Proxy Live Viewers (Up to 10K)

<div align="center">
Made with 💜 by +216_B.I.G
If you like the project, don’t forget to ⭐ star it!

</div>
