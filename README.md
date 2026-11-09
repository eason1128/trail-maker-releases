# Trail Maker：Mac 安裝與使用

Trail Maker 把爬山的 GPX 軌跡變成可以 3D 列印的地形模型。這份說明給在自己 Mac 上使用的人看，不需要懂程式，也不用打任何指令。

適用：Apple Silicon（M1 以後）的 Mac，macOS 12 以上。

## 第一次安裝

1. **下載**：<https://github.com/eason1128/trail-maker-releases/releases/latest/download/Trail-Maker-mac.zip>
2. **解壓縮**：在「下載項目」裡雙擊 `Trail-Maker-mac.zip`，會出現 `Trail Maker`。
3. **搬進「應用程式」**：把 `Trail Maker` 拖到 Finder 左邊的「應用程式」。
4. **第一次打開要多一步**：Trail Maker 沒有經過 Apple 的付費簽章，所以 macOS 第一次會擋下來。
   - **macOS 15（Sequoia）以後**：
     1. 雙擊 `Trail Maker`，跳出「無法確認…是否包含惡意軟體」，按「完成」。
     2. 打開「系統設定 → 隱私權與安全性」，往下捲到「安全性」，會看到「已阻擋 Trail Maker」，按「強制打開」。
     3. 再按一次「強制打開」，輸入 Mac 的登入密碼。
   - **macOS 12–14**：在 `Trail Maker` 上按右鍵（或 Control + 點一下）→「打開」→ 再按「打開」。

   之後都直接雙擊就好，不會再問。
5. **等它準備好**：第一次會跳出「正在下載並安裝 Trail Maker」的視窗。它會自動下載需要的東西（約 100 MB，裝好約佔 400 MB 空間），**需要網路，大約 2–5 分鐘**。完成後瀏覽器會自動打開 Trail Maker 的頁面。

## 平常使用

- **開始**：雙擊「應用程式」裡的 `Trail Maker`，瀏覽器會自動打開頁面。
- **使用中**：畫面上會有一個「Trail Maker 執行中」的小視窗，不要關掉它。
  - 不小心關掉瀏覽器分頁的話，按小視窗的「打開網頁」就能回來。
- **結束**：在小視窗按「停止」。
- **產生的檔案**：在頁面上直接下載。

如果電腦有安裝 [Bambu Studio](https://bambulab.com/zh-tw/download/studio)（放在「應用程式」裡），頁面右上角會顯示「Bambu Studio 已連線」，可以直接切片估算時間、下載設定好的 Bambu 專案檔。沒有安裝也能用，只是少了這些功能。

## 更新

打開 Trail Maker 時，如果有新版本，會跳出「有新版本 vX，要更新嗎？」，下面會寫這一版改了什麼：

- 按「**更新**」：自動下載並換成新版，通常幾秒到一分鐘。
- 按「**稍後**」：這次先用舊版，下次打開會再問。

如果新版本打不開，Trail Maker 會自動退回原本的版本，並告訴你。

## 遇到問題

- **打不開、或一直沒出現頁面**：先在小視窗按「停止」（如果有），再打開一次。
- **出現錯誤訊息**：按訊息上的「打開紀錄」，把 `logs` 資料夾裡的 `launcher.log` 和 `server.log` 傳給 Eason。
- **第一次安裝失敗**：通常是網路中斷，確認網路後再打開一次就會繼續。

## 移除

1. 把「應用程式」裡的 `Trail Maker` 丟到垃圾桶。
2. 在 Finder 按「前往 → 前往檔案夾…」，輸入 `~/Library/Application Support/`，把裡面的 `Trail Maker` 資料夾也丟到垃圾桶。這個資料夾裝的是程式、地形圖資的快取和產生過的模型。

產生過的模型會保留 30 天，之後自動清掉。
