<div align="center">

# 🎮 Kick Chat Tool

<img src="https://media.discordapp.net/attachments/1412417122956607509/1468060693046493204/image.png?ex=6982a590&is=69815410&hm=8573322de0e6d5cc7b1ee0323fd9cea63d9876b2a76af0659adcc7590f4321b2&=&format=webp&quality=lossless&width=388&height=600" width="200" alt="Kick Tool Logo"/>
<img src="https://media.discordapp.net/attachments/1412417122956607509/1468061113487724747/image.png?ex=6982a5f4&is=69815474&hm=75eca067fcc9f6643868e1c06989928dd69ae425ca74d28eff604302be4df8ed&=&format=webp&quality=lossless&width=384&height=600" width="200" alt="Kick Tool Logo"/>

**A premium, modern chat automation tool for Kick.com**

[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows)](https://microsoft.com)

</div>

---

## ✨ Features
- ⌨️ **Realistic Typing**: Simulates human typing behavior for natural messaging.
- 🔀 **Shuffle & Loop**: Randomize message order and loop your queue.
- 🙂 **Auto-Emotes**: Append random popular Kick emotes to your messages.
-  **Auto-Fetch**: Automatically detect chatroom IDs from channel names.
- � **Live Console**: Real-time event logging and progress tracking.
- � **Persistence**: All your settings are saved automatically.

---

## 🚀 Setup & Installation

1. **Download**: Get the latest `KickTools.exe` from the [Releases](https://github.com/216-Team/kick-chat-tool/releases) page.
2. **Run**: Double-click the `.exe` to start. (No installation required!)
3. **Login**: Open the app and paste your **Bearer Token** (see below).

---

## � How to get your Bearer Token

1. Open [kick.com](https://kick.com) in your browser and log in.
2. Press **F12** to open Developer Tools.
3. Click on the **Console** tab.
4. Paste the following command and press **Enter**:

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
    console.log('%c📡 Interceptor Active! Refresh the page (F5) to catch your token.', 'color: #A855F7; font-weight: bold;');
})();
```

5. **Refresh (F5)** the page.
6. The token will appear in the console and be **automatically copied** to your clipboard!

---
⭐ 10 - Add multipal Account Support
⭐ 50 - Nuck Chat with Bypass Cooldown
⭐ 100 - Add Live Viewer Support 1k-3k Viewers
⭐ 500 - Add Live Viewer Support Proxy 10K Viewers
<div align="center">

**Made with 💜 by +216_B.I.G**

</div>
