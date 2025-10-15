# 🧭 Interactive Sales Dashboard for a Mid-Sized Retail Company


## 🧩 How to Use This Dashboard with the Dataset

To explore and interact with the Power BI dashboard using the dataset provided in this repository, follow these steps:

### 🔹 Step 1: Download the Dataset
1. Go to the repository files above.  
2. Locate and download the dataset file:  
   **`SuperMarket Analysis.csv`**
3. Save the file to a convenient location on your computer (e.g., `Documents/PowerBI Projects/`).

---

### 🔹 Step 2: Download the Power BI File
1. In this repository, find and download the Power BI report file:  
   **`Sales Dashboard.pbix`**
2. Save it in the same folder as the dataset for convenience.

---

### 🔹 Step 3: Open in Microsoft Power BI Desktop
1. Open **Microsoft Power BI Desktop**.  
2. Go to **File → Open**, and select the `Sales Dashboard.pbix` file.  
3. When prompted to connect to the dataset:
   - Click **Transform Data → Edit Queries** (if needed).
   - Make sure the file path in the **Source** step points to your downloaded CSV file.  
     For example:
     ```
     Source = Csv.Document(File.Contents("C:\Users\<YourName>\Documents\PowerBI Projects\SuperMarket Analysis.csv"), [Delimiter=",", Columns=...])
     ```
   - Update the file path if necessary, then click **Close & Apply**.

---

### 🔹 Step 4: Explore the Interactive Dashboard
Once the data is loaded:
- Navigate between pages to explore **Sales KPIs, Regional Insights, Product Performance, Customer Behavior**, and **Time Forecasting**.  
- Use slicers and filters to interact with different dimensions of the dataset.

---

✅ **You are now ready to explore the fully functional Power BI dashboard using the dataset from this repository!**


