# E-commerce Customer Profiling and Data Consolidation Project

## Problem Statement
An e-commerce startup, following a successful first month, seeks to better understand its customer base and purchasing behaviors. The primary challenges are:
- Identifying and profiling customers across disparate data sources:
  - **Customer database**: Records online account sign-ups.
  - **CRM system**: Tracks phone and non-online customer interactions.
  - **Raw transaction data**: Includes guest purchases without formal customer records.
- Addressing overlapping entries and duplicates caused by customers interacting with multiple systems.

This project aims to integrate, clean, and analyze customer data to enable actionable insights into customer demographics and purchasing patterns.

---

## Goals
1. **Data Consolidation**  
   Integrate customer information across all data sources into a unified dataset.

2. **Data Deduplication**  
   Identify and resolve duplicate records using exact and fuzzy matching techniques.

3. **Customer Identification**  
   Create a flexible data model to uniquely identify and profile each customer.

4. **Data Validation**  
   Ensure data completeness and reliability by identifying inconsistencies.

5. **Solution Documentation**  
   Provide a well-documented schema to support future demographic and behavioral analysis.

---

## Methodology

### 1. Data Exploration
- Analyzed datasets for inconsistencies, missing values, and data overlaps.
- Created columns to identify guest checkouts and verified data source integrity.

### 2. Data Cleaning
- Standardized string columns (e.g., names and postcodes).
- Validated unique customer IDs and resolved duplicates.

### 3. Data Integration
- Merged datasets (Purchases, CRM, Customer Database) while maintaining lineage for each record.
- Identified customer overlaps using both exact and fuzzy matching techniques.

### 4. Deduplication
- Employed fuzzy matching for similar entries (e.g., typos in names).
- Merged duplicate customer IDs into main records for accurate profiling.

### 5. Final Schema
- Created a unified dataset with columns: `customer_id`, `first_name`, `surname`, `postcode`, `age`, `is_guest`, `in_purchase_data`, `in_crm_data`, `in_customer_data`, and deduplication metadata.

---

## Results
- **Unified Dataset**: Integrated 35,395 records across all sources.
- **Unique Customers**: Identified 27,395 unique/main customer records.
- **Guest Checkouts**: Represented ~25% of purchase data.
- **Fuzzy Matching Success**: Enabled linkage of ~7,148 additional records based on name, surname, and postcode similarity.

---

## Challenges and Key Insights
- **Data Overlap**: ~2,134 customers existed only in CRM or customer databases without purchase history.
- **Fuzzy Matching Success**: Improved deduplication for records with minor discrepancies (e.g., typos or formatting).
- **Guest Behavior**: Guests constituted a significant portion of transactions, emphasizing the need for conversion strategies.

---

## Future Considerations
1. **Enhance Fuzzy Matching**: Explore advanced ML techniques for improved record linkage.
2. **Customer Behavior Segmentation**: Use the unified dataset to analyze purchasing trends and demographics.
3. **Marketing Insights**: Tailor campaigns based on consolidated profiles and spending habits.
