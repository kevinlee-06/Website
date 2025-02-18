---
title: "剁手手系列 - 開箱「小米盒子S」2代"
date: 2025-01-01T00:00:00+08:00
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
前幾天，我用樹莓派試了各種電視盒的系統，主要是想取代 Smasnug 電視內建的 Tizen 系統，部分原因是 YouTube 上的廣告太多。我嘗試了 Kodi 和 Android TV，發現 Android TV 系統最適合我。然而樹莓派的解碼性能讓我非常失望，無法流暢播放影片。今天在班會的空堂時剛好在三創看到，就決定購買一台小米盒子 S 2代。

## 開箱體驗

小米盒子 S 2代的包裝採用橘色外盒，打開後裡面包含了以下配件：

- 遙控器
- 10.5W DC 變壓器，接口尺寸為 4.0mm*1.7mm
- HDMI 連接線 1 公尺
- 小米盒子本體
- 使用說明書

![小米盒子本體](/images/2025-02-18/01.jpg)

很可惜的是，盒內並沒有包含遙控器所需的兩顆 AAA 電池。

![遙控器](/images/2025-02-18/02.jpg)

## 使用體驗

實際使用上，小米盒子的表現讓我非常滿意。YouTube 播放 4k@60fps 的影片完全不卡頓，使用遙控器導覽也都很順暢。小米盒子 S 2代搭載 Google TV 系統，內建各種應用程式，例如 YouTube、Netflix、Spotify 等等，也可以透過 Google Play 商店安裝更多應用程式。

設定 Google TV 時需要強制登入 Google 帳號，這讓我有些不滿，因為我不是很想讓 Google 知道我在觀看的內容。不過這個問題可以透過安裝第三方的 YouTube 應用程式來解決。

## 客製化

## SideLoad 應用程式

小米盒子使用基於 Android 的 Google TV 系統，可以透過 adb 指令或 apk 來安裝第三方應用程式。

在電腦上使用 adb connect 來透過 Wi-Fi 連接小米盒子，然後使用 adb install 安裝 apk 檔案。

```bash
adb connect <tv_ip_address>
```

```bash
adb install <apk_file_path>
```

成功的話終端機會輸出

```bash
Performing Streamed Install
Success
```

以下是我測試過的應用程式：

- NewPipe：開源無廣告 YouTube 第三方應用程式
- LocalSend：開源 Wi-Fi 傳檔程式，Play Store 上也有
- Firefox：瀏覽器
- Files by Google：檔案管理器
- Fossify File Manager：開源檔案管理器
- Spotify：音樂串流服務
- VLC：影片播放器
- kiwi browser：瀏覽器

### 移除主畫面廣告

小米盒子的主畫面有一大堆推薦影片的區塊，這個區塊可以在設定關閉

打開設定 -> 帳戶與登入 -> 使用者名稱 -> 僅限應用程式模式 -> 開啟

