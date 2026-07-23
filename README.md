# Hospital Management Dashboard | Power BI

## Overview
A 3-page interactive Power BI dashboard analyzing hospital 
operations across appointments, revenue, and doctor performance. 
Built using a relational dataset of 5 tables structured as a 
star schema data model.

---

## Dataset
| Table | Description |
|-------|-------------|
| appointments | Patient appointment records with status and doctor info |
| billing | Payment records with amount, method and payment status |
| doctors | Doctor profiles with specialization, branch and experience |
| patients | Patient demographics and insurance information |
| treatments | Treatment types and costs linked to appointments |

---

## Data Model
- Designed a **star schema** with appointments as the central fact table
- Connected all 5 tables using proper one-to-many relationships
- Relationships: appointments → doctors, appointments → patients, 
  billing → patients, billing → treatments, treatments → appointments

---

## Tools Used
- Power BI Desktop
- Power Query (data transformation)
- DAX (calculated measures)
- Power BI Data Modeling (star schema)

---

## DAX Measures Created
- **Collection Rate** — % of billed revenue successfully collected
- **No-Show Rate** — % of appointments that resulted in no-show
- **Failed Revenue** — total revenue from failed payments
- **Pending Revenue** — total revenue yet to be collected
- **Avg Doctor Experience** — average years of experience across doctors

---

## Dashboard Pages

### Page 1 — Executive Overview
- KPI Cards: Total Revenue, Collection Rate, 
  Total Appointments, Pending Revenue
- Appointments per Month (line chart)
- Appointments by Treatment Type (bar chart)
- Appointments by Status (donut chart)
- Cost per Treatment Type (bar chart)
- Key Insights text box

### Page 2 — Revenue & Billing
- KPI Cards: Total Revenue, Revenue Collected, 
  Failed Revenue, Pending Revenue
- Revenue Trend by Month (line chart)
- Collection Rate Trend (line chart)
- Revenue by Payment Status (bar chart)
- Revenue by Payment Method (bar chart)
- Key Insights text box

### Page 3 — Doctor & Patient Performance
- KPI Cards: Total Doctors, Total Patients, 
  Total Specializations, Avg Experience
- Doctor Performance Summary (table)
- Patients by Insurance Provider (bar chart)
- No-Show Rate by Doctor (bar chart)
- Appointments by Doctor (bar chart)
- Key Insights text box

---

## Key Insights
- Only 31% of total billed revenue is collected — 
  failed payments (193K) exceed collected revenue (173K)
- 49% of appointments result in no-show or cancellation — 
  a significant operational gap
- Chemotherapy drives the highest appointment volume 
  and cost across all treatment types
- Sarah Taylor handles the highest patient load with 
  the highest no-show rate — workload redistribution 
  may be needed
- MedCare Plus covers 18 out of 50 patients — 
  a key insurance dependency

---

## Features
- Page navigation buttons for seamless storytelling
- 6 interactive slicers: Month, Gender, Payment Status, 
  Status, Treatment Type, Payment Method
- Key Insights text box on every page
- Star schema data model for optimized performance


