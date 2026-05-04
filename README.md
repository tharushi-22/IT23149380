# ITPM Assignment 1 - Test Automation

This repository contains a Python script that automates frontend translation test execution for the [Pixels Suite Chat Translator](https://www.pixelssuite.com/chat-translator) website using 50 test cases from an Excel workbook and writing actual results and test status back into the file.


## 🎯 Prerequisites

- Python 3.11 or 3.12
- playwright
- openpyxl
- Google Chrome


## 🚀 Setup Instructions

### 1. Clone the repository

```powershell
git clone https://github.com/tharushi-22/IT23149380_ITPM_Assignment1.git
cd IT23149380_ITPM_Assignment1
```

### 2. Install dependencies

```powershell
python -m pip install --upgrade pip 
pip install playwright openpyxl
playwright install
```

### 3. Run the script

```powershell
python IT23149380.py --excel "IT23149380/IT23149380.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 6000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```


## 📝 Notes

- The script will auto-detect input and expected result columns from the Excel header row using common names.
- If the actual output or status columns are missing, they are created automatically.
- Use `--output` to preserve the original workbook.