# 血液透析室護理端｜上機前 UFR 安全檢核與血管通路評估 (`hd-nursing-ufr-access`)

專為血液透析室護理師設計的輕量化、純前端單頁互動網頁（Single-Page Application），協助護理人員於上機前快速完成超濾率安全風險篩檢、血管通路物理評估與穿刺輪替定位，並一鍵生成標準化 Focus Charting（DAR）護理紀錄。

## 線上預覽（GitHub Pages）
- 網址：`https://yht5582-source.github.io/hd-nursing-ufr-access/`

## 核心護理功能
1. **上機前 UFR 與體液安全動態檢核**：
   - 即時計算 IDWG（kg 與 %）、淨脫水量、進食與沖管回血總脫水目標，以及超濾率 **UFR（mL/kg/hr）**。
   - 依安全閾值（≤ 10 綠燈、10.1–13 黃燈、> 13 紅燈）結合上機前血壓與臨床症狀，自動提示啟動階梯式脫水曲線（UF Profile）、低溫透析（35.5–36.0°C）與通報醫師檢核。
2. **血管通路評估與互動式 SVG 穿刺圖譜**：
   - 支援 **AVF、AVG 與 Permcath（CVC）** 三種模式切換。
   - 整合視診（Look）、觸診震顫（Thrill）、聽診雜音（Bruit）、抬臂塌陷測試及 AP/VP 機台壓力判讀。
   - 可直接在手臂 SVG 血管圖點選 A 端與 V 端穿刺點，即時換算兩針尖距離（檢核是否 ≥ 5 cm 以預防再循環）並避開假性動脈瘤變薄區。
3. **Focus Charting（DAR）交班紀錄生成器**：
   - 右側即時將所有評估數據、護理處置與通報狀態整理為 `[D] Data / [A] Action / [R] Response` 結構化紀錄，一鍵複製即可貼入醫院 NIS/HIS 護理系統。

## 資安設計
- 100% 純前端本機瀏覽器運算（Zero-Backend / Zero-CDN Dependency），不傳輸或儲存任何病患個資。
