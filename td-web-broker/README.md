# TD Web Broker Dividend Importer

## 📊 Expected Format: Activity CSV
1. Log in to **TD Web Broker**.
2. Select the account and click the **Activity** tab.
3. Filter the **Date Range** and click the **Download CSV** icon.

## ⚙️ Key Features
* **Tax Matcher:** Automatically identifies `WHTX02` (Withholding Tax) entries and subtracts them from the gross dividend to report true Net Income.
* **Description Scrubbing:** Uses Regex to strip exchange rate noise (e.g., `CONVERT TO CAD @...`) ensuring consistent grouping for stocks like Algonquin.
* **Strict Date Injection:** Injects JavaScript Date Objects into headers to prevent month-misalignment errors.

## 🛠 Configuration
* **Account ID:** Place your TD Account ID (e.g., `46J3Y8K`) in **Row 1** of the target tab.
* **Log Sheet:** Tracks `TD_ID_Ticker_Date_Amount` to prevent duplicates.