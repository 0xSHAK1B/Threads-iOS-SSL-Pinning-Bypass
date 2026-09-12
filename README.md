<div align="center">

# 🔓 Threads iOS SSL Pinning Bypass

#### Intercept, capture & analyze Threads HTTPS traffic on iPhone & iPad — 2026 working build

<br>

[![Download IPA](https://img.shields.io/badge/⬇_Download_IPA_(v446.1.0.30.67)-000000?style=for-the-badge&logo=threads&logoColor=white)](../../releases/latest)
[![Telegram](https://img.shields.io/badge/Chat_on_Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/MUH4MM4DSH4KIB)

![iOS](https://img.shields.io/badge/iOS_14.0+-000000?style=flat-square&logo=apple&logoColor=white)
![ARM64](https://img.shields.io/badge/arm64-blue?style=flat-square)
![Version](https://img.shields.io/badge/Threads-v446.1.0.30.67-000000?style=flat-square&logo=threads&logoColor=white)
![Updated](https://img.shields.io/badge/Updated-Regularly-brightgreen?style=flat-square)

</div>

---

<div align="center">

> **Bypass SSL/TLS certificate pinning** in Threads for iOS and pipe the full HTTPS stream — including login, feed, and post flows — into **Burp Suite · mitmproxy · Reqable · Proxypin.**

</div>

---

## 🎥 Proof of Concept

<div align="center">

<img width="590" height="1280" alt="Image" src="https://github.com/user-attachments/assets/ed31d7a1-bc9a-4df2-bdf8-1145d33f7219" />

> Live capture — Threads iOS HTTPS traffic intercepted in cleartext. **v446.1.0.30.67**.

</div>

---

## 📦 Supported Version

| App | Bundle ID | Version | Arch | Status |
|-----|-----------|:-------:|:----:|:------:|
| Threads for iOS | `com.burbn.barcelona` | **446.1.0.30.67** | `arm64` | ✅ [**Download**](../../releases/latest) |

> Grab the patched IPA from the [**Releases**](../../releases/latest) section. Need the newest build or another version? [Message me on Telegram](https://t.me/MUH4MM4DSH4KIB).

---

## 🎯 What You Can Capture

Full visibility into Threads' API surface (shares Meta/Instagram backend infrastructure):

- **Login via Instagram** — auth token exchange and session handling
- **Feed & timeline** — for-you / following ranking and GraphQL queries
- **Posts & replies** — create, like, repost, and quote endpoints
- **Profile & follows** — profile data and follow-graph requests
- **Media** — image/video upload and CDN delivery
- **Notifications & presence**
- **Analytics & telemetry** — device telemetry and A/B assignments

---

## ⚙️ Requirements

### iOS Device — iOS 14.0+

| Install / signing method | Notes |
|---|---|
| [**TrollStore**](https://github.com/opa334/TrollStore) | Best option (iOS 14.0 – 16.6.1 / 17.0). Permanent install, no expiration, no re-sign. |
| **KravaSign** / paid **Apple Developer** cert | For newer iOS (17.1+, 18, 26). Stable, longer-lived signing. |
| [**Sideloadly**](https://sideloadly.io/) / [**AltStore**](https://altstore.io/) + Apple ID | Works, but a **free** Apple ID signature expires after **7 days** and must be re-signed to keep working. |

### MITM Proxy Tool

- [**Burp Suite**](https://portswigger.net/burp) — industry-standard security testing proxy
- [**mitmproxy**](https://mitmproxy.org/) — open-source, scriptable HTTPS proxy
- [**Reqable**](https://reqable.com) — modern cross-platform HTTP debugger
- [**Proxypin**](https://proxypin.com) — lightweight proxy with mobile support

---

## 🚀 How to Bypass — Step by Step

**1. Get the patched IPA** — download from [**Releases**](../../releases/latest) (or [Telegram](https://t.me/MUH4MM4DSH4KIB) for the newest build).

**2. Install on your device**
- *TrollStore:* open TrollStore → **+** → select the IPA → **Install** (permanent).
- *Sideloadly / AltStore:* sign the IPA with your certificate, then trust the profile under **Settings → General → VPN & Device Management**.

> If the official Threads app is installed, uninstall it first — signatures conflict.

**3. Configure your proxy**
1. Export your proxy's **CA certificate**
2. Install & **fully trust** it: open the `.crt`/`.pem` → **Settings → General → VPN & Device Management → Install Profile**, then **Settings → General → About → Certificate Trust Settings → enable full trust**
3. Set the Wi-Fi proxy: **Settings → Wi-Fi → (network) → Configure Proxy → Manual**

**4. Capture traffic** — launch Threads and use it normally; decrypted HTTPS streams into your proxy in real time.

> Both steps matter: CA installed **and** full trust enabled — miss either and decryption fails silently.

---

<div align="center">

## 💼 Need a Custom Bypass?

**Custom SSL pinning bypass · automated patching scripts · full reverse-engineering projects** — for any iOS or Android app.

[![Request Custom Work](https://img.shields.io/badge/Message_me_on_Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/MUH4MM4DSH4KIB)

</div>

---

## ⚠️ Disclaimer

This project is provided **for educational and security-research purposes only**. It is **not affiliated with, endorsed by, or connected to Meta, Threads, Instagram, or their subsidiaries**. All trademarks belong to their respective owners. You are solely responsible for complying with your local laws and the app's Terms of Service, and should only analyze traffic on **accounts and devices you own or are authorized to test**. Provided **"as is", without warranty of any kind**.

---

## 🔗 Related Projects

| App | Platform | Repository |
|-----|----------|------------|
| TikTok | iOS | [**TikTok iOS SSL Pinning Bypass**](https://github.com/0xSHAK1B/TikTok-iOS-SSL-Pinning-Bypass) |
| Instagram | iOS | [**Instagram iOS SSL Pinning Bypass**](https://github.com/0xSHAK1B/Instagram-iOS-SSL-Pinning-Bypass) |
| Facebook | iOS | [**Facebook iOS SSL Pinning Bypass**](https://github.com/0xSHAK1B/Facebook-iOS-SSL-Pinning-Bypass) |
| Threads | Android | [**Threads SSL Pinning Bypass**](https://github.com/0xSHAK1B/Threads-SSL-Pinning-Bypass) |
| Instagram | Android | [**Instagram SSL Pinning Bypass**](https://github.com/0xSHAK1B/Instagram-SSL-Pinning-Bypass) |
| Facebook | Android | [**Facebook SSL Pinning Bypass**](https://github.com/0xSHAK1B/Facebook-SSL-Pinning-Bypass) |
| Messenger | Android | [**Messenger SSL Pinning Bypass**](https://github.com/0xSHAK1B/Messenger-SSL-Pinning-Bypass) |
| X (Twitter) | Android | [**X (Twitter) SSL Pinning Bypass**](https://github.com/0xSHAK1B/Twitter-SSL-Pinning-Bypass) |

---

## 💖 Support This Project

If this saved you time or helped your research, please **⭐ star the repo** — it helps others find it and keeps the builds coming. Contributions toward keeping bypasses updated as apps release new versions are appreciated:

| Currency | Address |
|:---------|:--------|
| **BTC** | `131NaAJooX2XYq5QUFmKsTuLQXcGNayYPJ` |
| **ETH** | `0xea9a566a5123c3a1b8d60f8bdd845835716668f0` |
| **USDT (TRC-20)** | `THssAZhUQEEsw15211rAaRLGRjSWXMX4PW` |

Thank you! 🙏

---

<div align="center">

### 📬 Contact & Latest Builds

Newest IPAs · support · custom work

[![Telegram](https://img.shields.io/badge/@MUH4MM4DSH4KIB-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/MUH4MM4DSH4KIB)

⭐ **Star the repo if it helped your research!**

</div>
