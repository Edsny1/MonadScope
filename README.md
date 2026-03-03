<p align="center">
  <img
    src="https://github.com/user-attachments/assets/41d65b07-6447-40d2-8eb3-239ec720d12c"
    alt="MonadScope Icon"
    width="140"
  />
</p>

<h1 align="center">MonadScope</h1>

<p align="center">
  <strong>The Ultimate Monad Validator Tracking Application</strong><br/>
  Built natively for Android devices.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/framework-React%20Native-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/expo-SDK-000020?style=for-the-badge&logo=expo&logoColor=white" />
  <img src="https://img.shields.io/badge/license-MIT-blue?style=for-the-badge" />
</p>

<p align="center">
  <a href="#whats-new"><b>What's New</b></a> •
  <a href="#features"><b>Features</b></a> •
  <a href="#installation"><b>Installation</b></a> •
  <a href="#background-notifications-setup"><b>Background Notifications</b></a> •
  <a href="#screenshots"><b>Screenshots</b></a> •
  <a href="#architecture"><b>Architecture</b></a>
</p>

---

## 🚀 About MonadScope

**MonadScope** is a high-performance React Native mobile application built specifically for the **Monad Network (Testnet & Mainnet)**.

It helps validators and delegators:

* 🔴 Monitor network health in real time
* 🔎 Instantly find validators
* ⭐ Track favorite validators
* 🚨 Receive critical push alerts

Built with a focus on **speed**, **clarity**, and **zero backend dependency**.

---

## 🆕 What's New in v2.0.0

### ✨ New Features

**📰 Monad Today Screen**
- New dedicated tab with real-time Monad ecosystem news
- Latest YouTube videos from the official Monad channel
- MONAD price widget (live from CoinGecko — USD + 24h change)
- Network status bar showing Mainnet & Testnet active validator counts
- Ecosystem projects with on-chain TVL data (DeFiLlama, Monad-specific)

**🔔 Smarter Push Notifications**
- Hourly reports now show accurate per-network validator status (Mainnet & Testnet separately)
- Eliminated false "All Safe" notifications when a validator was actually inactive
- Fixed composite key bug: same validator on multiple networks now tracked independently
- Notification logs now recorded for audit and deduplication

**🔄 In-App Update System**
- App automatically checks for new versions on launch
- Optional or forced update prompts with release notes
- Direct download link to latest release

### 🐛 Bug Fixes
- **Favorites limit**: "Added to favorites" toast no longer shows when the 2-validator network limit is hit
- **News feed**: Removed low-quality domains (Bitcoinist, CoinGape, CoinPedia, etc.) from news sources; cached articles from blocked sources are cleaned up automatically
- **Duplicate token registration**: Push token is only re-registered when it changes; otherwise only favorites are synced

### 🔒 Security & Maintenance
- Backend URL moved to environment variable (`EXPO_PUBLIC_API_URL`) — no longer hardcoded in source
- Inactive users (30+ days) automatically removed from the database every Monday at 03:00

---

## ✨ Features

### 🌐 Network Overview

* Real-time Epoch numbers
* Total Validators
* Active status tracking
* Latest block & gas metrics

### 📰 Monad Today

* Real-time ecosystem news feed
* Official Monad YouTube videos
* Live MONAD price (USD + 24h change)
* Mainnet & Testnet validator status at a glance
* On-chain TVL data for ecosystem projects

### 🔍 Validator Search

* Lightning-fast search
* Filter by Moniker
* Search by Operator Address

### ⭐ Favorites System

* Bookmark validators
* Local persistent storage
* Quick health monitoring

### ⚠️ Silent Background Tracking

* Periodic safety checks
* Low battery impact
* Fully automatic

### 🔔 Smart Push Notifications

**Emergency Alerts**

* Validator jailed
* Sudden stake drops

**All Safe Summary**

* Hourly health reports per network (Mainnet & Testnet)
* Requires Android battery settings

### 📊 Uptime & Charts (WIP)

* Visual uptime analytics
* Validator performance insights

### ⚡ Built with React Native + Expo

* Smooth animations
* Haptic feedback
* Responsive bottom tabs

---

## 📸 Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/84cddb8a-1129-468a-9289-793956238cd5" width="180" />
  <img src="https://github.com/user-attachments/assets/beda0edf-7e35-43ef-afdb-563f67583c8d" width="180" />
  <img src="https://github.com/user-attachments/assets/22e2729b-7129-4552-9607-e0255c3abfbe" width="180" />
  <img src="https://github.com/user-attachments/assets/5f066e6e-3952-45dc-ace5-96a9e5a42503" width="180" />
</p>

---

## 🚀 Installation

MonadScope is distributed as a compiled Android Application Package (`.apk`).

### 1️⃣ Download

<p align="center">
  <a href="https://github.com/Edsny1/MonadScope/releases/latest/download/MonadScope.apk">
    <img src="https://img.shields.io/badge/Download-Latest%20APK-6C47FF?style=for-the-badge&logo=android&logoColor=white" />
  </a>
</p>

> 💡 This link always points to the **latest release** automatically — no need to update it manually.

### 2️⃣ Install

1. Open the downloaded `.apk`
2. Allow **Install unknown apps** if prompted
3. Tap **Install**
4. Launch **MonadScope**

---

## 🛠️ Background Notifications Setup

MonadScope uses `expo-background-fetch` to wake the device and check validator status.

⚠️ **Important:** Android Doze Mode may delay background tasks.

### ✅ Enable Reliable Hourly Checks

1. Open **Android Settings**
2. Go to **Apps → See all apps**
3. Select **MonadScope**
4. Tap **Battery**
5. Set to **Unrestricted**

Then enable **Push Notifications** inside the app.

---

## 🏗️ Architecture & APIs

MonadScope fetches data directly from public endpoints.

**Validator State & Epochs**
`https://www.gmonads.com/api/v1/public`

**RPC (Gas / Block Number)**
`https://rpc.monad.xyz`

**Price Data**
`CoinGecko API`

**TVL Data**
`DeFiLlama API`

**Local Storage**
`AsyncStorage` + `zustand/middleware/persist`

---

## 🤝 Contributing

PRs, issues, and feature requests are welcome.

If you plan major changes, please open an issue first.

---

## 📜 License

Licensed under the **MIT License**.

---

<p align="center">
  <b>Built for the Monad ecosystem</b> ⚡
</p>
