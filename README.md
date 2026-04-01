# Apollo Lead Extraction System

A lightweight automation workflow that extracts verified B2B leads from Apollo and structures them into usable datasets using n8n and APIs.

---

## 🚀 Problem

Teams using Apollo for lead generation still face friction:

- manual exporting and filtering of contacts  
- inconsistent data quality  
- time spent cleaning and organizing leads  
- lack of structured pipeline for storing results  

This slows down outreach workflows and reduces efficiency.

---

## ⚙️ Solution

Designed a workflow that:

1. Takes a filtered Apollo search URL as input  
2. Extracts verified contact data using Apify  
3. Structures and standardizes lead information  
4. Automatically stores results into Google Sheets  

---

## 🧠 System Flow

Input → Extraction → Structuring → Storage

- **Input:** Apollo search URL + result limit  
- **Extraction:** Fetch lead data via Apify Apollo scraper  
- **Processing:** Filter and map only relevant fields (verified emails, roles, company data)  
- **Output:** Clean, structured lead dataset stored in Google Sheets  

---

## 🔧 Tech Stack

- n8n (workflow orchestration)  
- Apify (Apollo scraper actor)  
- Google Sheets API  
- HTTP APIs  

---

## 📌 Key Features

- Extracts only **verified emails** to ensure data quality  
- Fully automated flow from input → structured output  
- Dynamic sheet creation for different datasets  
- Eliminates manual export and cleaning effort  

---

## ⚠️ Note

Requires valid Apollo search URLs and configured API credentials. Some configurations may need updates depending on API limits or changes.

---

## 👤 Author

Shobhit Mandal
Contact: shobhitmandal0209@gmail.com
