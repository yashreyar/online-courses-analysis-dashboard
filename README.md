# online-courses-analysis-dashboard# Online Courses Analytics Dashboard (Power BI)

A dynamic, data-driven Power BI dashboard built to analyze e-learning course performance, student engagement metrics, and content distribution patterns. This project transforms raw operational data from online courses into actionable executive-level insights, helping educational platforms optimize their content strategies and track audience engagement.

## 📊 Live Dashboard Preview
Below is the final polished production view of the interactive analytics dashboard:

![Online Courses Dashboard](https://github.com/yashreyar/online-courses-analysis-dashboard/blob/main/Online%20courses%20dashboard.jpg?raw=true)

---

## 💡 Business Case & Objectives
Managing an expansive online learning curriculum requires deep visibility into product traction. This dashboard answers critical business questions to streamline catalog management:
* **Market Demand:** Which core subject categories and sub-categories attract the most massive viewer densities?
* **Product Mix Analysis:** Do consumers favor specialized structural career tracks (Specializations) or flexible single-course formats (Courses)?
* **Localization Impact:** How heavily does subtitle language diversity impact global scale and retention?
* **Performance Benchmarking:** Who are the high-performing instructors across different technical tracks?

---

## 🛠️ Technical Stack & Skills Demonstrated
* **BI Platform:** Microsoft Power BI Desktop
* **Data Modeling:** Normalized data architecture handling multi-level categorical hierarchies (Category $\rightarrow$ Sub-Category).
* **Data Cleaning & ETL (Power Query):** Cleaned decimal over-precision on high-volume metrics, forced explicit rounding logic, and added localized thousands separators for high scannability.
* **UI/UX Design Strategy:** Containerized dashboard layouts using unified border tracking, dynamic cross-filtering, and an executive-summary banner featuring standard corporate spacing grids.

---

## 📐 Advanced DAX Expressions
Rather than relying on default implicit column counting, explicit DAX measures were built to ensure accurate dynamic behavior during multi-slicer filtering:

### 1. Total Catalog Depth
Tracks the true scale of distinct educational products available on the platform:
```DAX
Total Courses = DISTINCTCOUNT('Online_Courses'[Course ID])
