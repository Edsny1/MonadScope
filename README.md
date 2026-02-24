<p align="center">
  <img src="./assets/icon.png" alt="<img width="512" height="512" alt="monadscope_512x512" src="https://github.com/user-attachments/assets/41d65b07-6447-40d2-8eb3-239ec720d12c" />
<img width="512" height="512" alt="monadscope_512x512" src="https://github.com/user-attachments/assets/41d65b07-6447-40d2-8eb3-239ec720d12c" />
" width="140" />
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

## ✨ Features

### 🌐 Network Overview

* Real-time Epoch numbers
* Total Validators
* Active status tracking
* Latest block & gas metrics

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

* Hourly health reports
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

1. Go to the **Releases** tab
2. Download the latest `monadscope_v1.0.0.apk`

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
