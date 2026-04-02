# Customer Database Cleaning for Outreach

## 🧾 Project Overview
This project demonstrates how to clean and transform a messy customer dataset into a structured, professional call list using Python. The goal is to improve data quality, ensure consistency, and make the dataset usable for outreach campaigns.

---

## The Problem
The original dataset was noisy and unreliable:
- Duplicate customer records  
- Inconsistent name formatting  
- Messy phone numbers  
- Unstructured address data  
- Irrelevant columns  
- Customers marked as “Do Not Contact” still included  

This would lead to inefficient outreach, poor user experience, and wasted resources.

---

## Data Cleaning Steps

### 1. Removing Duplicates
Duplicate entries (e.g. the same customer appearing multiple times) were identified and removed.

**Result:**  
Each customer now appears only once → ensuring data integrity.

---

### 2. Column Pruning
Irrelevant columns that added no business value were removed.

**Example:**  
`Not_Useful_Column` (random True/False values)

**Result:**  
Cleaner dataset with only meaningful fields.

---

### 3. Name Sanitization
Last names contained special characters and inconsistent formatting.

**Before:**
- `/Baggins`
- `Holmes...`
- `_Skywalker`

**After:**
- `Baggins`
- `Holmes`
- `Skywalker`

**Result:**  
Professional and standardized naming.

---

### 4. Phone Number Standardization 
Phone numbers were inconsistent and sometimes invalid.

**Before:**
- `123|456|7890`
- `123.456.7890`
- `NaN`

**After:**
- `123-456-7890`

**Actions Taken:**
- Removed non-numeric characters  
- Applied consistent format  
- Cleared invalid entries  

**Result:**  
Reliable and dial-ready phone numbers.

---

### 5. Address Parsing 
Addresses were stored as a single unstructured string.

**Before:**

123 Shire Lane, Shire, 12345


**After:**
- Street Address  
- State  
- Zip Code  

**Result:**  
Improved readability and easier filtering.

---

### 6. Categorical Uniformity
Inconsistent labels in categorical columns were standardized.

**Before:**
- Yes / No  
- Y / N  

**After:**
- Y  
- N  

**Result:**  
Cleaner and more consistent data.

---

### 7. Strategic Filtering 
Business rules were applied to remove irrelevant records.

**Removed:**
- Customers marked as **Do Not Contact**  
- Customers without valid phone numbers  

**Result:**  
A high-quality, actionable call list.

---

### 8. Final Formatting
After all transformations, the dataset index became inconsistent.

**Before:**
- Index jumps (e.g. 1 → 4 → 7)

**After:**
- Reset to a clean sequential index starting from 0  

**Result:**  
Neat and easy-to-navigate dataset.

---

## Final Outcome
A fully cleaned dataset that is:
- Consistent  
- Professional  
- Easy to use  
- Ready for outreach campaigns  

---

## Tools Used
- Python  
- Pandas  

---

## Key Takeaways
- Small inconsistencies can significantly impact data usability  
- Data cleaning is a critical step in any data analysis workflow  
- Structured data leads to better decision-making and efficiency  

---


This project is part of my journey to becoming a Data Analyst, where I focus on building practical, real-world projects.

