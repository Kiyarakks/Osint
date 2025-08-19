# Web Data Finder 🔍

**Web Data Finder** is a Python script that searches the web for a given query, detects URLs, and analyzes webpage content to find relevant links based on text similarity. It uses **Google search**, **BeautifulSoup**, and **fuzzy matching** to identify links containing the requested information.  

---

## ✨ Features
- Performs Google searches for any query.  
- Detects URLs from search results and prints them in the terminal.  
- Extracts webpage titles.  
- Finds relevant links using fuzzy text matching between link text and URLs.  
- Highlights when requested data is found in a link.  
- Colored terminal output for better readability (via `colorama`).  

---

## 🛠️ Requirements
- Python 3.8+  
- Install dependencies using your **`requirements.txt`** file:  
```bash
pip install -r requirements.txt
```
Your `requirements.txt` should include:  
```
requests
beautifulsoup4
colorama
google
fuzzywuzzy
python-Levenshtein
```

---

## 🚀 Usage
1. Run the script:  
```bash
python main.py
```
2. Enter your search query at the prompt:  
```
Find > example query
```
3. The script will display:  
   - URLs detected from Google search  
   - Page titles  
   - Links containing requested data or text matching the URL  

---

## ⚡ How It Works
1. Uses `googlesearch` to fetch up to 100 search results.  
2. Requests each page with `requests.get`.  
3. Parses the HTML with `BeautifulSoup`.  
4. Compares link text and URLs using `fuzzywuzzy` to find relevant matches.  
5. Prints results with colored terminal output using `colorama`.  

---

## 📝 Notes
- Timeout for requests is set to 1 second to avoid slow loading pages.  
- Only HTTP/HTTPS links are considered.  
- Make sure your terminal supports ANSI color codes for proper coloring.  
