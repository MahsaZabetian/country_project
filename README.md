# country_project
Create tool that can automatically correct typos in geographic names
# 🌍 Country Name Standardization Tool

This tool automatically detects and corrects typos in country names using data from the [GeoNames API](http://www.geonames.org/export/web-services.html) and fuzzy matching via `rapidfuzz`. It is designed to help standardize geographic names in datasets, especially those using controlled vocabularies like [BOLD](http://www.boldsystems.org/).

---

## 🚀 Features

- ✅ Fetches official country names using GeoNames
- ✅ Corrects misspelled or alternate country names
- ✅ Saves standardized results to a JSON file
- ✅ Easy to extend for other BOLD fields like continent, habitat, etc.

---

## 🧠 How It Works

1. **Fetch Country List**  
   Connects to the GeoNames API using your GeoNames username and retrieves valid country names.

2. **Typo Correction with Fuzzy Matching**  
   Uses `rapidfuzz.process.extractOne()` to find the best match among valid countries.

3. **Output to JSON**  
   Saves both the original and corrected country names in a clean `.json` format.

---

## 💾 Example

Input country names with typos:

```python
["Untied States", "UK", "Russsia", "Venzuela", "South Corea"]

Output saved as corrected_countries.json:
[
  {"original": "Untied States", "corrected": "United States"},
  {"original": "UK", "corrected": "United Kingdom"},
  {"original": "Russsia", "corrected": "Russia"},
  {"original": "Venzuela", "corrected": "Venezuela"},
  {"original": "South Corea", "corrected": "South Korea"}
]
Requirements:
Python 3.6+
rapidfuzz
Install dependencies:
pip install rapidfuzz requests

How to Use:
1) Get a GeoNames username
Register for free at https://www.geonames.org/login

2) Edit the script
Set my username in the Python file:
username = "your_geonames_mahsazabetian"

3) Run the script:
python fetch_and_correct.py

4) Check output

Console: corrected results printed

File: corrected_countries.json created in your directory

Project Structure:
country_project/
├── fetch_and_correct.py         # main script
├── corrected_countries.json     # sample output
└── README.md                    # this file

redits
Created by Mahsa Zabetian as part of a project for standardizing biodiversity data using open APIs and Python tools.

Special thanks to:

GeoNames

RapidFuzz

BOLD Systems


[corrected_countries.json](https://github.com/user-attachments/files/20825252/corrected_countries.json)


