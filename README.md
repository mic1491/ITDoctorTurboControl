<div align="center">

<img src="assets/icon.png" alt="IT Doctor Turbo Control Icon" width="128" height="128" />

# IT Doctor Turbo Control

**專為 macOS 量身打造的處理器智慧溫控、動態調頻與硬體效能管理中心**

[![macOS](https://img.shields.io/badge/macOS-13.0%2B%20(Ventura%20%7C%20Sonoma%20%7C%20Sequoia)-black?style=for-the-badge&logo=apple)](https://github.com)
[![Architecture](https://img.shields.io/badge/Architecture-Universal%202%20(Intel%20%2B%20Apple%20Silicon)-007AFF?style=for-the-badge)](https://github.com)
[![Swift](https://img.shields.io/badge/Swift-5.9%20%7C%20SwiftUI%20%2B%20AppKit-FA7343?style=for-the-badge&logo=swift)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.5.0-34C759?style=for-the-badge)](https://github.com)

[繁體中文](README.md) · [English Description](#english-overview) · [立即下載最新發行版](#-下載與安裝指引)

</div>

---

## 📖 為什麼需要 IT Doctor Turbo Control？

MacBook 在輕薄機身下運行 Intel 處理器時，原廠 macOS 傾向於在任何微小運算（如開啟 Chrome 分頁、切換視窗）時瞬間將 CPU 頻率超頻拉升（Turbo Boost），導致：
- 🌋 **機身瞬間飆溫**：核心溫度動輒衝破 90°C～100°C，鍵盤與金屬底板極度燙手。
- 🌪️ **風扇狂暴起飛**：散熱風扇經常飆破 5000～6500 RPM，產生刺耳噪聲。
- ⚡️ **電池急速流失**：功耗暴衝使得外出不插電時的續航力腰斬。

**IT Doctor Turbo Control** 是一套純原生、非侵入式、兼具極致美學與硬體底層控制力的專業工具。讓您在保有日常 100% 流暢度的前提下，**一鍵淨降溫 20°C～30°C、消除風扇狂轉、並延長 30%～50% 電池續航力**！

---

## ✨ 核心特色與功能亮點

### 1. 🌬️ 處理器智慧調控 & 一鍵 Turbo 開關
- **Intel 晶片深度支援**：直接通訊 CPU 核心暫存器（MSR `0x1A0`），精確控制 Turbo Boost 啟閉。
- **Apple Silicon 晶片支援**：自適應無縫切換 macOS 原生低耗電模式（P-Core 全速釋放 vs E-Core 節能靜音）。
- **四種情境預設檔**：極限效能、智慧平衡、靜音辦公、極致省電（支援自訂高低溫門檻）。

### 2. 📊 溫控效益智能分析與診斷報告（Thermal Effect Analyzer）
- **雙向實測對比**：自動將歷史取樣切分為「Turbo 開啟前」與「Turbo 關閉後」，並列呈現平均溫度、最高溫、風扇 RPM 與平均時脈。
- **量化成效指標**：直接算出「平均淨降溫」、「降溫幅度 %」與「風扇降噪比例 %」。
- **專家白話文解說**：自動將硬體數據翻譯成流暢的診斷結論，清楚告訴您發熱抑制與節能成效。
- **⚡️ 60 秒基準對比實驗**：一鍵全自動執行 30 秒基準採樣 + 30 秒降溫採樣，快速產出對比報告。

### 3. 💎 純原生 Apple 液態毛玻璃美學（Liquid Frosted Glass）
- 採用純 Swift + SwiftUI + AppKit 原生打造，底層使用系統原生毛玻璃材質（`.regularMaterial`）。
- 嚴格遵循 Apple 人機介面指南（HIG），動態脈衝呼吸徽章、Activity Ring 圓環儀表，完全適配 Light Mode 與 Dark Mode。
- 支援「選單列彈出小窗」與「獨立展開為大視窗」雙向切換。

### 4. ⏱️ 選單列零抖動等寬即時監控（Jitter-Free Menu Bar）
- **徹底告別位移**：全面採用 Unicode 表格數字專用等寬空格（Figure Space `\u{2007}`）與 `.monospacedDigit()`。
- 無論數值從 4% 飆到 100%、或是從 58°C 跳至 85°C，文字長度分毫不差，**完全消除水平拉扯與抖動**。
- 支援多種 Apple 風格外觀（能量膠囊、動態旋轉指針、活動進度環、極簡純字等）。

### 5. 🪟 自由縮放桌面懸浮小工具（Floating HUD）
- **自由無段拖曳縮放**：按住小工具右下角即可任意拉伸長寬（190px～480px）。
- **3 檔官方黃金尺寸一鍵切換**：
  - 🟢 **迷你膠囊（210 × 44）**：單行極簡省空間，即時監控 CPU、頻率與溫度。
  - ⚖️ **標準尺寸（250 × 100）**：三欄硬體讀數與快速控制按鈕。
  - 🖥️ **大螢幕放大（320 × 126）**：適合 4K/5K 高解析度螢幕遠距觀看。
- 具備置頂、穿透、防誤觸位置鎖（🔒）以及多螢幕拔除安全歸位機制。

### 6. 📱 macOS 桌面 WidgetKit 小工具
- 支援放入 macOS 桌面背景或通知中心。
- 提供小型（Small，158×158）、中型（Medium，338×158）與大型（Large，338×354）三種標準規格。

### 7. 🛡️ 智慧電源與安全防護策略
- **拔除充電線自動降耗**：改用電池供電時自動停用 Turbo，即刻延長電池續航 30%～50%。
- **休眠喚醒自動同步（Wake Resync）**：掀開螢幕喚醒後，自動校驗並補償狀態，絕不讓 macOS 悄悄刷回預設值。
- **退出 App 自動安全復原**：結束程式時主動還原原廠處理器狀態。
- **持續高溫推播警報**：溫度過高持續 16 秒時主動發出 macOS 系統橫幅警報。

### 8. ⚡️ 特權分離與「零密碼干擾」架構
- 採用特權分離輔助工具（Privilege Separation Helper）。
- 初次安裝驗證後，日常在背景調節「完全全自動、全靜默執行」，絕不彈出密碼視窗打擾使用者。
- **非侵入式理念**：不改寫系統核心檔案，App 沒開啟時 Mac 即為 100% 原廠出廠狀態。

---

## 💻 系統需求

- **作業系統**：macOS 13.0 (Ventura) 或更新版本（完全相容 macOS 14 Sonoma 與 macOS 15 Sequoia）
- **硬體平台**：Universal 2 雙原生架構
  - 🔹 **Intel 處理器**：MacBook / MacBook Pro / MacBook Air / Mac mini / iMac（完整支援 MSR Turbo 控制）
  - 🔹 **Apple Silicon 晶片**：M1 / M2 / M3 / M4 系列晶片（支援原生低耗電模式無縫調控）
- **記憶體預算**：常駐運行僅消耗約 20MB～28MB，背景 CPU 佔用率接近 0.0%。

---

## 📥 下載與安裝指引

1. 前往本專案右側的 [**Releases 發行版頁面**](https://github.com) 下載最新版本的 `ITDoctorTurboControl-v0.5.0.zip`。
2. 下載完成後解壓縮，將 **`IT Doctor Turbo Control.app`** 拖曳至您的 **「應用程式（Applications）」** 資料夾。
3. 雙擊啟動即可！應用程式會常駐於螢幕頂部的選單列中。

> **💡 初次啟動提示**：
> 若系統提示「無法開啟，因為未識別開發者」：
> 請前往 macOS「系統設定」$\to$「隱私權與安全性」$\to$ 點擊「強制開啟」或「仍要開啟」即可。

---

## ❓ 常見問題（FAQ）

### Q1：點了「關閉 Turbo」之後結束 App，重開機會一直關閉嗎？
**不會！** Intel CPU 的 Turbo Boost 是由核心內部的揮發性暫存器（MSR `0x1A0`）控制的。只要電腦重新開機或斷電，硬體晶片微碼在開機自我檢測時一定會自動復原為原廠的「啟用」狀態。只要您沒打開 App，電腦就是 100% 原廠狀態。

### Q2：關閉 Turbo Boost 會導致電腦變卡嗎？
**日常使用完全無感！** Intel 處理器的基準時脈（例如 2.3 GHz）對於瀏覽數十個網頁、4K YouTube 播放、文書辦公、程式開發綽綽有餘。關閉 Turbo 僅影響極限高負載（如長時間 3D 渲染輸出），但在日常中能換來安靜、涼爽與大幅延長的電池壽命。

### Q3：電腦休眠蓋上螢幕，喚醒後設定會跑掉嗎？
**不會！** 本 App 內建「休眠喚醒自動同步（Wake Resync）」專利機制。掀開螢幕喚醒後，程式會在背景自動校驗處理器狀態，若發現被系統重設，會瞬間自動補寫為您要求的狀態，全程無感維護。

---

## 🌐 English Overview

**IT Doctor Turbo Control** is a modern, native macOS menu bar & dashboard application engineered for Intel MacBooks and Apple Silicon. It provides hardware-level thermal management and CPU frequency tuning without thermal throttling or loud fan noise.

- **Universal 2 Binary**: Native Intel x86_64 & Apple Silicon arm64 support.
- **Instant Temperature Drop**: Lowers CPU temperatures by 20°C–30°C and eliminates annoying fan whines.
- **Smart Thermal Diagnostics**: Generates human-readable thermal effect reports comparing metrics before and after Turbo disabling.
- **Apple Liquid Material Design**: Native SwiftUI & AppKit implementation adhering to Apple Human Interface Guidelines.
- **Jitter-Free Menu Bar**: Uses Unicode figure spaces (`\u{2007}`) for subpixel tabular alignment.
- **Resizable Floating HUD & Desktop Widgets**: Mini capsule, standard, and large sizes with free corner-drag resizing.

---

## 👨‍💻 作者與致謝

- **開發者**：Matt
- **版本**：v0.5.0 (Universal 2)
- **版權聲明**：Copyright © 2026 Matt. All Rights Reserved. 個人免費使用。
