# 🌐 Web Server Log Analysis (Calgary HTTP Dataset)

## 📌 Project Overview
This project focuses on analyzing real-world web server log data from the Calgary HTTP dataset. The dataset contains approximately one year of HTTP request logs, making it a practical example of handling large-scale, unstructured data.

The objective of this analysis was to transform raw log entries into a structured format and extract meaningful insights related to user behavior, server performance, and traffic patterns.

---

## 📂 Dataset Details
- **Dataset Name:** Calgary HTTP Dataset  
- **Source:** Internet Traffic Archive  
- **Format:** Apache Common Log Format  
- **Records:** ~726,000 HTTP requests  
- **Nature:** Unstructured, real-world log data  

---

## ⚙️ Approach & Methodology

### 🔹 1. Data Loading
- Loaded compressed `.gz` dataset directly using Python  
- Avoided manual extraction for efficiency and reproducibility  
- Stored raw logs into a pandas DataFrame  

---

### 🔹 2. Data Cleaning & Preparation
Handling real-world log data required careful preprocessing:

- Parsed log entries using **regular expressions**
- Extracted structured fields:
  - Host
  - Timestamp
  - Request
  - Status Code
  - Response Size

- Converted timestamp into **datetime format** for time-based analysis  
- Handled missing and inconsistent data:
  - Replaced `"-"` in size column with `0`
  - Labeled missing file extensions as `no_extension`
- Identified and flagged malformed log entries instead of dropping them  
- Created a clean dataset (`df_clean`) for analysis  

---

### 🔹 3. Feature Engineering
- Split request into:
  - Method (GET/POST)
  - Filename
  - Protocol  
- Extracted file extensions for content-type analysis  

---

## 📊 Analysis Performed

The following analytical tasks were completed:

- ✅ Total number of HTTP requests  
- ✅ Unique hosts accessing the server  
- ✅ Date-wise unique filename usage  
- ✅ 404 error count and analysis  
- ✅ Top missing resources (filenames & extensions)  
- ✅ Bandwidth usage trends (July 1995)  
- ✅ Hourly traffic distribution  
- ✅ Most requested resources  
- ✅ HTTP response code distribution  

---

## 📈 Key Insights

- Identified peak traffic hours and usage patterns  
- Detected frequently missing resources (404 errors)  
- Observed bandwidth consumption trends over time  
- Highlighted most popular files requested by users  

---

## 🛠️ Tools & Technologies
- **Python**
- **Pandas**
- **Regular Expressions**
- **Jupyter Notebook**

---

## 💡 Challenges & Learnings

- Handling unstructured log data required precise parsing  
- Managing missing and malformed entries without data loss  
- Understanding real-world data inconsistencies and handling them logically  

---

## 🚀 Conclusion

This project demonstrates the ability to:
- Work with real-world, unstructured datasets  
- Perform data cleaning and transformation effectively  
- Apply analytical techniques to extract actionable insights  

It reflects a practical understanding of data analysis workflows and problem-solving in real-world scenarios.

---

## 👤 Author
**Saurav**

---
