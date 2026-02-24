<h1 align="center">
  <img src="./assets/icon.png" alt="MonadScope Logo" width="120" />
  <br>
  MonadScope
</h1>
<p align="center">
  <strong>The Ultimate Monad Validator Tracking Application</strong><br>
  Built natively for Android Devices.
</p>
<p align="center">
  <a href="#features">Features</a> •
  <a href="#installation">Installation</a> •
  <a href="#background-notifications-setup">Background Notifications</a> •
  <a href="#screenshots">Screenshots</a> •
  <a href="#architecture">Architecture</a>
</p>
---
MonadScope is a React Native mobile application built specifically for the **Monad Network (Testnet & Mainnet)**. It allows users to track the lively state of the network, search through active and inactive validators, examine real-time network statuses, and—most importantly—receive **push notifications** whenever their favorited validators experience emergency events such as *Jailing* or *Stake Drops*.
## ✨ Features
- **🌐 Network Overview:** Instant access to real-time Epoch numbers, Total Validators, Active Statuses, Latest Block, and Gas Prices.
- **🔍 Validator Search:** Fast and responsive search functionality to find any validator by Moniker or Operator Address.
- **⭐ Favorites System:** Bookmark your preferred validators to keep a close eye on their performance. (Stored locally).
- **⚠️ Silent Background Tracking:** The app wakes up periodically to verify the safety statuses of your favorited validators.
- **🔔 Smart Push Notifications:** 
  - **Emergency Alerts:** Push warnings if a favorited validator is *Jailed* or its stake suddenly vanishes.
  - **All Safe Summaries:** A bundled hourly report assuring you that your chosen nodes are healthy and actively producing blocks. (Requires specific Android settings, see below).
- **📊 Uptime & Charts (WIP):** Explore visual uptime data representations directly inside the validator detail screen.
- **⚡ Built on React Native & Expo:** Smooth animations, haptic feedback, and a highly responsive bottom tab interface.
---
## 📸 Screenshots
*(Add your screenshots here by replacing the placeholder links with actual GitHub image uploads)*
| Dashboard | Validator Details | Validator Search | Push Notification |
| :---: | :---: | :---: | :---: |
| <img src="URL_TO_DASHBOARD_IMAGE" width="200" /> | <img src="URL_TO_DETAILS_IMAGE" width="200" /> | <img src="URL_TO_SEARCH_IMAGE" width="200" /> | <img src="URL_TO_NOTIFICATION_IMAGE" width="200" /> |
---
## 🚀 Installation
MonadScope is distributed directly as a compiled Android Application Package (`.apk`) so you do not need to build it from the source code.
### 1. Download the App
1. Navigate to the **Releases** tab on this GitHub repository.
2. Download the latest `monadscope_v1.x.apk` file directly to your Android device.
### 2. Install the APK
1. Open your Android file manager and tap on the downloaded `.apk` file.
2. If your phone prompts a security warning, click **Settings** and allow your browser or file manager to **"Install unknown apps"**.
3. Tap **Install** and wait for the process to finish.
4. Open **MonadScope** and start tracking your favorite validators!
*(Note to Developers: If you want to build the app from the Expo source code, clone this repository and run `npm install` followed by `npx expo start` in the `react_native_space` directory).*
---
## 🛠️ Background Notifications Setup (Crucial for Android)
MonadScope relies on the `expo-background-fetch` intent to silently wake up your device every hour, poll the Monad blockchain API, and determine if any of your **Favorite Validators** are in trouble. 
By default, modern Android operating systems implement an aggressive **"Doze Mode"** (Battery Optimization) that forcibly restricts how often background applications can poll for data. If you leave the default settings on, Android may delay your hourly validator checks to run only every 3-6 hours.
### To Enable True Hourly Guaranteed Notifications:
If you want the MonadScope daemon to run unimpeded over 24 hours to secure your node investments, you must tell Android to exclude it from battery sleeping routines.
1. Open your Android device **Settings**.
2. Go to **Apps** -> **See all apps**.
3. Search for and select **MonadScope**.
4. Scroll down and tap on **Battery** or **App battery usage**.
5. Change the setting from *Optimized* (or *Restricted*) to **Unrestricted** (Sınırlandırma Yok).
Once this is set, flip the **Push Notification toggle** in the MonadScope App Settings screen. The application will immediately register a High-Priority background task.
---
## 🏗️ Architecture & APIs
MonadScope avoids heavy backend middleware components by directly fetching states via public sources, ensuring lightning-fast updates:
- **Validator State & Epoches:** `https://www.gmonads.com/api/v1/public`
- **RPC (Gas / Block Num):** `https://rpc.monad.xyz`
- **Local Storage:** `AsyncStorage` + `zustand/middleware/persist`
## 🤝 Contributing
Contributions, issues, and feature requests are welcome!
## 📜 License
[MIT](LICENSE)
