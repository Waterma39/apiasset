項目名稱：跨資產動態追蹤與視覺化系統 (Multi-Asset Tracking & Visualization App)

系統架構與 API 整合說明 (System Architecture & API Integration)
本專案為一款跨平台（Web / Android）輕量級資產管理應用，核心功能著重於多源數據整合（Multi-Source Data Aggregation）與即時視覺化分析。

外部 API 與 Google Sheets API 數據整合：

動態資料庫管道 (Dynamic Pipeline)：系統透過 RESTful API / Google Sheets API 作為後端輕量化資料源，實現資產數據（股票、加密貨幣、法幣）的無縫同步與動態載入。

環境變數與資安隔離 (Security & Mock Data)：嚴格遵循資安最佳實踐，抽離敏感憑證與個人資產數據，提供開放式 Demo Sheet ID 與環境變數設定檔（.env），支援使用者自主替換個人化資料源。

數據處理與商業邏輯 (Data Processing & Business Logic)：

多策略覆蓋處理 (Multi-Strategy Overwrite)：內建數據衝突與優先級決策邏輯，當多個數據源（API 與試算表）出現重複或衝突時，可自動執行策略覆蓋與清洗。

跨資產動態合併 (Dynamic Data Merging)：自動將不同計價單位（如 USD、NTD、BTC）與資產類別進行即時匯率換算與正規化（Normalization）。

前端與跨平台封裝 (Frontend & Cross-Platform)：

視覺化呈現：採用 Chart.js 進行多維度資產比例與歷史走勢之動態圖表渲染。

技術棧：HTML5 / JavaScript (ES6+) 原生架構，並透過 Android Studio (WebView / TWA) 進行模組化打包，實現 Web 與 Android 雙端一致的使用者體驗。
