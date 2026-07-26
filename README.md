# Awarizon Bot Scripts 🚀

This collection of Python scripts automates tasks on the Awarizon Testnet — a blockchain-based node activation and social rewards platform. The scripts handle wallet authentication, node activation, daily check-ins, and social account connections.

🔗 Register: [Awarizon Testnet](https://testnet.awarizon.com?ref=5C4D0606)

## ✨ Features Overview

### General Features

- **Multi-Account Support**: Reads private keys from `pvkey.txt` to perform actions across multiple accounts.
- **Colorful CLI**: Uses `colorama` for visually appealing output with box-drawing borders and colored icons.
- **Asynchronous Execution**: Built with `asyncio` for efficient concurrent task processing using semaphore-based threading.
- **Error Handling**: Comprehensive error catching for API failures and rate limits.
- **Bilingual Support**: Supports both English and Vietnamese output.
- **Proxy Support**: Supports HTTP, HTTPS, SOCKS4, and SOCKS5 proxies via `proxies.txt`.

### Included Scripts

✨ **Node Activation** (`node.py`)

- ✅ Wallet authentication via nonce/sign/verify
- ✅ Node activation via signed message
- ✅ Displays node info (level, title, score, reputation, progress)
- ✅ Shows user stats (total/weekly/referral points, global rank)
- ✅ Referral stats display
- ✅ Multi-wallet parallel execution with proxy support

✨ **Daily Check-in** (`checkin.py`)

- ✅ Auto-authenticate and check node status
- ✅ Daily check-in via `POST /nodes/check-in`
- ✅ Shows streak, points earned, and level-up status
- ✅ Skips if already checked in today
- ✅ Multi-wallet parallel execution with proxy support
- ✅ Displays node level and score before check-in

✨ **Social Connect** (`connect.py`)

- ✅ Connect social accounts (TWITTER, TELEGRAM, DISCORD)
- ✅ Reads usernames from `username.txt` (twitter|telegram|discord per line)
- ✅ Skips already-connected platforms
- ✅ Fetches activity rewards to show points earned (+200 each)
- ✅ Multi-wallet parallel execution with proxy support

## 🛠️ Prerequisites

Before running the scripts, ensure you have the following installed:

- **Python 3.8+**
- **pip** (Python package manager)
- **Dependencies**: Install via `pip install aiohttp aiohttp-socks eth-account colorama`
- **pvkey.txt**: Add private keys (one per line) for wallet automation
- **username.txt**: Add social usernames for social connect (one per line, format: `twitter|telegram|discord`)
- **proxies.txt** (optional): Add proxy addresses for network requests

## 📦 Installation

1. **Clone or download this repository:**
   ```sh
   git clone https://github.com/thog9/Awarizon-testnet.git
   cd Awarizon-testnet
   ```

2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Prepare Input Files:**

   Create `pvkey.txt` with your private keys (one per line):
   ```
   0x1234567890abcdef...
   0xabcdef1234567890...
   ```

   Create `username.txt` for social connect (one per line, matching pvkey.txt order):
   ```
   twitterUser|telegramUser|discordUser
   twitterUser2|telegramUser2|discordUser2
   ```

   Create `proxies.txt` (optional) — one proxy per line:
   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ip:port:user:pass
   ```

4. **Run:**
   ```sh
   python main.py
   ```
   - Choose a language (Vietnamese / English).
   - Select the script you want to run.

**Language Selection:**
- Choose between Vietnamese (Tiếng Việt) and English.
- All scripts support bilingual output.

---

## 📁 Project Structure

```
Awarizon-testnet/
├── main.py                # Central menu system
├── pvkey.txt              # Private keys file
├── username.txt           # Social usernames file
├── proxies.txt            # Proxies file (optional)
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── scripts/               # Individual scripts
    ├── node.py            # Node activation & stats
    ├── checkin.py         # Daily check-in
    └── connect.py         # Social account connection
```

---

## 📨 Contact

Connect with us for support or updates:

- **Telegram**: [thog099](https://t.me/thog099)
- **Channel**: [CHANNEL](https://t.me/thogairdrops)
- **Group**: [GROUP CHAT](https://t.me/thogchats)
- **X**: [Thog](https://x.com/thog099)

---

## ☕ Support Us

Love these scripts? Fuel our work with a coffee!

🔗 BUYMECAFE: [BUY ME CAFE](https://buymecafe.vercel.app/)

🔗 WEBSITE: [BUY SCRIPTS](https://thogtoolhub.com/)
