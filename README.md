# 🏥 EHR vs DB Data Analysis

This project analyzes discrepancies between **Electronic Health Records (EHR)** and the **Imported DB Data** to identify **missing encounters**, **CPT code mismatches**, and patterns across providers and dates.

> 🔍 Objective: Ensure data integrity between client-side EHR and the backend database by identifying missing or unimported encounters and CPT codes.

---

## 📂 Dataset Overview

| Dataset       | Rows  | Description                                |
|---------------|-------|--------------------------------------------|
| EHR Data      | 25,956| Closed encounters from client’s EHR        |
| DB Data       | 6,482 | Encounters imported into backend database  |

### 📊 Data Columns

**EHR Data**:
- `Patient Name`
- `Provider Name`
- `Date of Service`
- `CPT Code`
- `Unique ID`

**DB Data**:
- `Patient Name`
- `Provider Name`
- `from_date_range`
- `cpt_codes` (comma-separated)

---

## ✅ Key Metrics Summary

| Metric                                 | Value   |
|----------------------------------------|---------|
| Total EHR Encounters                   | 25,956  |
| Total DB Imported Encounters           | 6,482   |
| Total Missing Encounters               | 1,352   |
| 🔑 Unique Missing Encounters           | 283     |

---

## 📦 CPT Code Import Audit

| Metric                            | Value   |
|----------------------------------|---------|
| 🔢 Total CPT Codes in EHR        | 31      |
| 📥 Total CPT Codes in DB         | 20      |
| ❌ CPT Codes Never Imported       | 11      |

### 🚫 CPT Codes Never Imported
1, NORCM, SP, SP$110, SP$90, SP110, SP90, TOS, TOS115, sp120, sp90
