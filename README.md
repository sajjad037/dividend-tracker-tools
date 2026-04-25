# Dividend Tracker Tools Suite

A professional automation suite for managing Canadian brokerage dividend data in Google Sheets.

## 📁 Repository Structure
* **/wealthsimple**: Supports Wealthsimple Monthly Statements (PDF-to-CSV) and Activity Tab exports.
* **/td-web-broker**: Production-grade importer for TD Activity CSVs, featuring tax matching and description scrubbing.

## 📂 System Management & Maintenance
### Internal Log Sheets (`Import_..._DoNotDelete`)
Both tools utilize hidden log sheets that act as a database index.
* **Idempotency:** Every transaction is assigned a unique fingerprint. If you upload the same CSV twice, the script will skip any previously processed entries.
* **Warning:** Do not delete these sheets unless you wish to reset your entire import history.

### Ticker Mapping (`Config_TD`)
The TD tool maintains a persistent mapping sheet to handle complex institutional security names.
* **Manual Override:** If the API provides an incorrect ticker, edit the "Mapped Ticker" column in this sheet. The script will always prioritize your manual entry for all future imports.

## 🚀 Setup
1. Copy the `.gs` scripts into your Spreadsheet's Apps Script editor.
2. Ensure each portfolio tab has the **Account ID** in **Row 1**.
3. Use the unified custom menus to process your CSV exports.