## 🏨 Atliq Hotel Chain Booking Analysis

### 📌 Project Overview
This project analyzes booking data from a Hotel Chain business to uncover insights into guest behavior, platform performance, and revenue trends. Using Pandas Library, I cleaned, transformed, and explore over **130,000+ booking records** across multiple dimension tables to support data-driven decision-making.

---

### 📂 Dataset Summary

| Table Name                    | Description                                      |
|------------------------------|--------------------------------------------------|
| `fact_bookings.csv`          | Core booking data with guest, revenue, and status |
| `dim_date.csv`               | Date dimension for time-based analysis           |
| `dim_hotels.csv`             | Hotel metadata including category and city       |
| `dim_rooms.csv`              | Room category details                            |
| `fact_aggregated_bookings.csv` | Aggregated booking metrics by property and date |

---

### 🧼 Data Cleaning & Transformation

- **Missing Values & Outliers:**
  - Detected negative values in `no_guests` → filtered out invalid entries.
  - Nulls in `ratings_given` handled via imputation or exclusion based on context.

- **Date Parsing:**
  - Converted `booking_date`, `check_in_date`, and `checkout_date` to datetime format.
  - Merged with `dim_date` for enriched time-based analysis.

- **Revenue Logic:**
  - Compared `revenue_generated` vs `revenue_realized` to assess booking success.
  - Flagged discrepancies due to cancellations and no-shows.

- **Dimensional Joins:**
  - Merged `fact_bookings` with `dim_hotels` to extract hotel category and city.
  - Integrated `dim_rooms` for room type segmentation.
  - Linked `fact_aggregated_bookings` to validate booking capacity vs actuals.

---

### 📊 Key Insights

- **Hotel Category Distribution:**
  - `Luxury` hotels dominate the dataset (16 out of 25 properties).
  - Cities like Mumbai and Hyderabad show higher booking volumes.

- **Platform Performance:**
  - Top platforms: `others`, `makeyourtrip`, `logtrip`
  - Direct bookings yield higher revenue realization.

- **Booking Status Breakdown:**
  - Majority are `Checked Out`, followed by `Cancelled` and `No Show`.

- **Room Category Trends:**
  - `RT1` is the most booked room type across properties.

---

### 🧠 Skills Demonstrated

- Advanced Pandas for cleaning, merging, and transformation  
- EDA using `groupby`, `value_counts`, and descriptive statistics  
- Business logic interpretation for revenue and booking status  
- Dimensional modeling and join operations  
- Notebook structuring for clarity and reproducibility  

---

<h3>📁 Folder Structure</h3>
<pre style="text-align: left;">
Project-Hospitality-Domain/
│
├── datasets/
│   ├── fact_bookings.csv
│   ├── dim_date.csv
│   ├── dim_hotels.csv
│   ├── dim_rooms.csv
│   └── fact_aggregated_bookings.csv
├── Project-Hospitality-Domain.ipynb
└── README.md
</pre>


