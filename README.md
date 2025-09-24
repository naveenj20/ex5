## NAME: NAVEEN JAISANKER

# Web Scraping in UiPath

## AIM
To develop a UiPath workflow that scrapes structured data from a website and exports it into an Excel file using Data Scraping and Excel activities.

---

## PROCEDURE

### Step 1: Create Project
- Open **UiPath Studio**.  
- Create a new Process project.  
- Name it **WebScrapingExample**.  

---

### Step 2: Open Website
- Launch a browser (Chrome/Edge/Firefox).  
- Navigate to the website from which data will be extracted (e.g., product listings on Amazon/Flipkart).  
- Ensure the UiPath browser extension is installed and enabled.  

---

### Step 3: Data Scraping Wizard
- In UiPath Studio, go to the **Design** tab → click **Data Scraping**.  
- Select the first element to scrape (e.g., product name).  
- Select a second similar element → UiPath identifies the pattern.  
- (Optional) Add correlated data like **price** or **ratings**.  
- Preview the extracted data → stored in a variable `ExtractDataTable`.  

---

### Step 4: Export to Excel
- Drag a **Write Range** activity (inside a Use Excel File scope).  
- Set file name as `ScrapedData.xlsx`.  
- Write the DataTable variable `ExtractDataTable` into **Sheet1**.  
- Enable **Include Headers** to copy column names.  

---

### Step 5: Run Workflow
- Click **Run** in UiPath Studio.  
- UiPath scrapes data and writes it into `ScrapedData.xlsx`.  
- Verify output by opening the Excel file.  

---

### Step 6: Handle Pagination
- If the website has multiple pages, enable **Pagination** in the Data Scraping wizard.  
- Select the **Next Page** button → UiPath loops through all pages.  

---

## WORKFLOW
Your workflow consists of:  
1. **Browser Scope** – Opens the target website.  
2. **Data Scraping Wizard** – Extracts structured data into a DataTable.  
3. **Excel File Scope** – Creates/opens `ScrapedData.xlsx`.  
4. **Write Range** – Writes the DataTable to Excel.  

---

## OUTPUT

- **Output Excel (after execution):** The scraped data appears in tabular form in `sample.xlsx`.
  
<img width="1163" height="1025" alt="Screenshot 2025-09-24 133810" src="https://github.com/user-attachments/assets/a7f99708-9d3b-47c0-b86e-2467e9c1e3cb" />

---

## RESULT
Thus, the UiPath workflow for scraping data from a website and writing it into an Excel file was executed successfully.
