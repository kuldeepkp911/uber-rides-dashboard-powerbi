


# 🚗 Uber Rides Analytics Dashboard — Power BI

A multi-page interactive Power BI dashboard for analyzing Uber ride data across bookings, revenue, vehicle performance, and customer behavior.

---

##  Dashboard Overview

The report is structured across **4 pages**, each focused on a distinct analytical domain:

| Page | Description |
|------|-------------|
| **Home** | Landing page with navigation to all report sections |
| **Overview** | High-level KPIs and trends across all rides |
| **Vehicle** | Performance breakdown by vehicle type |
| **Bookings & Revenue** | Deep-dive into booking patterns and revenue analysis |

---

##  Pages & Visuals

###  Home
- Branded landing page with the Uber logo and page navigation buttons
- Acts as the entry point for the report

---

###  Overview
Key metrics and trend analysis at a glance.

**KPI Cards:**
- Total Completed Bookings
- Total Lost Bookings
- Total Booking Value
- Total Distance Covered
- Average Distance per Ride
- Customer Count

**Charts & Visuals:**
-  **Area Chart** — Completed bookings trend over time (Date Axis)
-  **Clustered Column Chart** — Monthly booking comparison
-  **Donut Charts (×3)** — Booking status breakdown (Complete, Lost, etc.)
-  **Clustered Bar Chart** — Bookings by Pickup Location
-  **Multi-Row Cards** — Pickup & Drop location summaries
-  **Slicers** — Filter by Date and image-based vehicle categories

---

### 🚙 Vehicle
Performance metrics segmented by vehicle type.

**KPI Cards (×6):**
- Complete Bookings per Vehicle
- Lost Bookings per Vehicle
- Booking Value per Vehicle
- Total Distance per Vehicle
- Average Distance per Vehicle
- Vehicle-specific count metrics

**Charts & Visuals:**
-  **Clustered Bar Chart** — Booking value by vehicle type (`uber.Vec_Type`)
-  **Table** — Detailed vehicle-level data (Customer ID, Booking Status, Vehicle Type)
-  **Vehicle Type Images** — Visual cards for each vehicle category (e.g., Intercity Comfort)

---

###  Bookings & Revenue
In-depth revenue and booking funnel analysis.

**KPI Cards (×5+):**
- Total Booking Value
- Complete Bookings
- Lost Bookings
- Booking Count by Drop Location
- Contribution % (`Cont%`)

**Charts & Visuals:**
-  **Area Chart** — Revenue over time
-  **Clustered Column Chart** — Monthly booking value
-  **Clustered Bar Chart** — Bookings by Drop Location
-  **Donut Chart** — Payment Method distribution
-  **Funnel Chart** — Booking conversion funnel (Complete → Lost)
-  **Slicer** — Filter by date / image category

---

##  Data Model

### Tables

| Table | Description |
|-------|-------------|
| `uber` | Core fact table with ride-level transaction data |
| `_Measure` | DAX measures table |
| `image` | Vehicle type lookup with images |

### Key Columns — `uber` Table

| Column | Description |
|--------|-------------|
| `Booking Status` | Ride outcome (Completed / Cancelled / etc.) |
| `Pickup Location` | Origin of the ride |
| `Drop Location` | Destination of the ride |
| `Vehicle Type` | Type of Uber vehicle used |
| `Vec_Type` | Vehicle type category (used in vehicle analysis) |
| `Customer ID` | Unique customer identifier |
| `Customer Rating` | Rating given by the customer |
| `Driver Ratings` | Rating given to the driver |
| `Booking_Value` | Fare amount for the ride |
| `Payment Method` | Mode of payment used |
| `Lost_Booking` | Flag for cancelled/lost rides |

### Key DAX Measures — `_Measure` Table

| Measure | Description |
|---------|-------------|
| `Complete_Booking` | Count of successfully completed rides |
| `Lost_Booking` | Count of cancelled or lost rides |
| `Booking_Value` | Total revenue from bookings |
| `Booking_count` | Total number of bookings |
| `Total_Distance` | Sum of all ride distances |
| `Avg_Distance` | Average distance per ride |
| `Customer_Count` | Distinct count of customers |
| `Vec_Type` | Vehicle type aggregation measure |
| `Quarter` | Quarter-level time grouping |

---

## 🛠️ Tools & Technologies

- **Tool:** Microsoft Power BI Desktop
- **File Format:** `.pbix`
- **Theme:** Custom Uber-branded theme
- **Power BI**

---

##  Getting Started

### Prerequisites
- [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free download)

### Steps
1. Clone or download this repository
2. Open `uber_dashboard.pbix` in Power BI Desktop
3. If prompted, refresh the data source connection
4. Use the **Home** page navigation to explore each report section
5. Use slicers to filter by **date range** or **vehicle category**

---

##  Repository Structure

```
 uber-powerbi-dashboard
 ┣  uber_dashboard.pbix       # Main Power BI report file
 ┗  README.md                 # This file
```

---

##  Key Insights the Dashboard Enables

- Track **booking completion vs. cancellation rates** over time
- Compare **revenue contribution by vehicle type**
- Identify **high-demand pickup and drop locations**
- Analyze **payment method preferences** among customers
- Monitor **driver and customer rating trends**
- Understand **monthly and quarterly distance and revenue patterns**

---

