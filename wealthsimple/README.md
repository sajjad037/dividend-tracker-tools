# Wealthsimple Dividend Importer

## 📊 Expected Formats
* **Monthly Statements:** Download PDF -> Convert to CSV (e.g., via Tabula).
* **Activity Tab:** Filter for "Dividends" -> Download CSV.

## ⚙️ Key Features
* **Regex Ticker Extraction:** Automatically pulls ticker symbols from the "Description" field.
* **Log Sheet:** Maintains an internal registry of processed IDs to allow for overlapping statement uploads without data duplication.

## 📂 System Sheets
* **`Import_Log_DoNotDelete`**: Hidden sheet managing transaction state.