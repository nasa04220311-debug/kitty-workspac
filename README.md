# kitty-workspac
🏢 台灣房地產市場與總體經濟自動化分析系統
基於 Python 與大型語言模型（Groq API）的房產新聞輿情與總體經濟月度自動化分析工具。

📌 專案背景與目的
本專案旨在解決傳統房地產市場研究中，人工蒐集新聞、彙整數據與撰寫分析報告耗時費力的大量痛點。透過自動化爬蟲技術抓取近期房產與總體經濟新聞，並結合 Groq LLM 的強大語意理解與生成能力，自動產出具備商業價值的月度專業分析報告，適合應用於金融授信、資產管理及市場研究。

🛠️ 技術堆疊 (Tech Stack)
程式語言：Python

資料處理：Pandas, Openpyxl (pd.read_excel)

網路爬蟲：Requests, BeautifulSoup, Selenium

人工智慧與 NLP：Groq API (openai SDK, openai/gpt-oss-20b)

文件自動化：python-docx（可擴充套件自動產出 Word 格式報告）

⚙️ 核心功能模組
智能數據過濾與截斷：自動讀取 Excel 格式的原始新聞資料，進行空值處理、字串轉換，並具備智慧文本長度截斷防護，確保不超過 API Token 限制。

結構化 AI 提示詞工程 (Prompt Engineering)：

宏觀政策與金融風向（央行利率、房市調控、稅務影響）。

市場供需與價格趨勢（豪宅佔比、租金行情、買賣方心態）。

熱點區域與產品焦點、潛在風險警訊、首購剛需市場評估。

金融級專業語氣輸出：採用嚴格的 system role 設定，強制要求模型輸出量化數據與結構化表格，確保產出內容符合金控授信與資產管理高層的審閱標準。

🚀 快速開始與使用方式
1. 環境安裝
請確保你的電腦已安裝 Python，並執行以下指令安裝必要套件：

Bash
pip install pandas requests beautifulsoup4 openai python-docx openpyxl
2. 設定環境變數（安全性最佳實踐）
為確保 API 金鑰安全，請在你的系統環境變數中設定 GROQ_API_KEY，或在執行環境中指定：

Bash
# Windows (命令提示字元)
set GROQ_API_KEY="你的_Groq_API_Key"

# Mac / Linux
export GROQ_API_KEY="你的_Groq_API_Key"
3. 執行程式
將你的新聞資料放置於指定路徑（例如 d:\新聞類\POST.xlsx），即可直接執行主程式產出分析月報。

💡 專案亮點 (Resume Highlights)
自動化與效率提升：實現從「非結構化新聞數據」到「專業結構化月報」的端到端（End-to-End）自動化流程。

資安意識：嚴格落實程式碼與機密金鑰（API Key）的分離管理，採用環境變數確保程式碼公開時的安全性。
