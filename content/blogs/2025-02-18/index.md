---
title: "剁手手系列 - 開箱「小米盒子S」2代"
date: 2025-02-18T00:00:00+08:00
draft: false
github_link: ""
author: "Kevin"
tags:
  - 開箱
  - 小米
  - Android
  - Google TV
  - 剁手手系列
image: /images/2025-02-18/cover.jpg
description: ""
toc:
---

## 開箱體驗

小米盒子 S 2代的包裝採用了醒目的橘色外盒，打開後內含以下配件：

- 遙控器
- 10.5W DC 變壓器（接口尺寸：4.0mm x 1.7mm）
- HDMI 連接線（1 公尺長）
- 小米盒子本體
- 使用說明書

![小米盒子本體](/images/2025-02-18/01.jpg)

可惜的是，盒內並未附帶遙控器所需的兩顆 AAA 電池。

![遙控器](/images/2025-02-18/02.jpg)

## 使用體驗

實際使用中，小米盒子的表現讓我非常滿意。測試中播放 4K@60fps 的 YouTube 影片毫無卡頓，遙控器在導覽時也十分流暢。小米盒子 S 2代搭載 Google TV 系統，內建多種應用程式，如 YouTube、Netflix、Spotify 等，還可透過 Google Play 商店安裝更多應用程式。

在設定 Google TV 時必須強制登入 Google 帳號，這讓我略感不便，因為我並不希望 Google 追蹤我的觀看內容。不過這個問題可透過安裝第三方的 YouTube 應用程式來解決。

![主畫面](/images/2025-02-18/10.png)

![螢幕保護程式](/images/2025-02-18/11.png)

## 配件

以下 USB 配件我測試過能用：

- USB 網卡
- USB 音效卡
- USB 滑鼠
- USB 滑鼠
- USB 相機
- USB 硬碟
- USB Hub

## 客製化

### SideLoad 應用程式

小米盒子運行基於 Android 的 Google TV 系統，因此可以 SideLoad 安裝第三方應用程式。

1. 在小米盒子上啟用「開發人員選項」。
2. 在電腦上，先使用以下指令透過 Wi-Fi 連接小米盒子：

   ```bash
   adb connect <tv_ip_address>
   ```

3. 執行以下指令安裝 apk 檔案：

   ```bash
   adb install <apk_file_path>
   ```

若成功安裝，終端機會輸出：

```bash
Performing Streamed Install
Success
```

以下列出我測試過的應用程式，來源包含 Google Play 與 APK：

- [NewPipe](https://newpipe.net)：無廣告的第三方 YouTube 應用程式
- [LocalSend](https://play.google.com/store/apps/details?id=org.localsend.localsend_app&hl=en-US&pli=1)：Wi-Fi 檔案傳輸程式
- [VLC](https://play.google.com/store/apps/details?id=org.videolan.vlc&hl=en-US)：影音播放器
- [Spotify](https://play.google.com/store/apps/details?id=com.spotify.music&hl=en-US)：音樂串流服務
- [ProtonVPN](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en-US)：VPN 服務
- [CX File Explorer](https://play.google.com/store/apps/details?id=com.cxinventor.file.explorer&hl=en-US)：檔案管理器
- [Droid-ify](https://github.com/Droid-ify/client)：F-Droid 客戶端
- [SmartTube](https://github.com/yuliskov/smarttube)：無廣告的第三方 YouTube 應用程式
- Firefox：瀏覽器（不會在主畫面顯示）
- Kiwi Browser：瀏覽器（不會在主畫面顯示）
- Files by Google：檔案管理器（不會在主畫面顯示）
- Fossify File Manager：開源檔案管理器（不會在主畫面顯示）

![SideLoad 應用程式](/images/2025-02-18/03.png)

![SideLoad 應用程式](/images/2025-02-18/07.png)

![SideLoad 應用程式](/images/2025-02-18/08.png)

![SideLoad 應用程式](/images/2025-02-18/09.png)

下列應用程式則無法使用：

- Aurora Store  
- Brave Browser

### 移除主畫面推薦內容

![大量推薦影片](/images/2025-02-18/04.png)

小米盒子的主畫面預設會顯示大量推薦影片區塊，但這部分內容可以透過以下設定關閉：

1. 打開「設定」
2. 前往「帳戶與登入」
3. 選擇「使用者名稱」
4. 啟用「僅限應用程式模式」

完成設定後，主畫面推薦內容便會消失。

![移除主畫面推薦內容](/images/2025-02-18/05.png)

### 防止誤觸遙控器的「Xiaomi TV+」按鈕

1. 打開「設定」
2. 前往「應用程式」
3. 分別選擇「PatchWall」和「Xiaomi TV+」
4. 選擇「停用」

這樣一來，遙控器上的「Xiaomi TV+」按鈕就不會再啟動 Xiaomi TV+ 應用程式。

![防止誤觸遙控器的「Xiaomi TV+」按鈕](/images/2025-02-18/06.png)
