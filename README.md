# Revenue Insights in Hospitality Domain

## Project Overview

Developed an interactive hospitality analytics dashboard to analyze hotel booking and revenue data using Power BI, SQL, Excel, and DAX. The project focused on monitoring revenue performance, booking trends, customer behavior, occupancy metrics, ADR, and RevPAR to support data-driven business decisions and revenue optimization strategies.

---

# Tools & Technologies

- Power BI
- SQL
- Excel
- DAX
- Power Query

---

# Dataset Details

Analyzed hotel booking data containing:

- Hotel Type
- Booking Status
- Revenue
- ADR (Average Daily Rate)
- Customer Information
- Room Types
- Market Segment
- Distribution Channels
- Cancellation Data
- Stay Duration
- Guest Information

---

# Project Workflow

## Data Collection

- Imported hotel booking data from Excel/CSV files.

## Data Cleaning & Transformation

Performed data preprocessing using Excel and Power Query:

- Removed duplicate records
- Handled missing values
- Corrected data types
- Created calculated columns:
  - Total Nights
  - Total Guests
  - Revenue

---

# SQL Database Creation

Created SQL database and table structure for hospitality analytics.

## SQL Table Creation

```sql
CREATE TABLE hotel_bookings (
Hotel_Type VARCHAR(100),
is_canceled INT,
lead_time INT,
arrival_date_year INT,
arrival_date_month VARCHAR(20),
arrival_date_week_number INT,
arrival_date_day_of_month INT,
Weekend_Nights INT,
Week_Nights INT,
adults INT,
children INT,
babies INT,
meal VARCHAR(20),
Country VARCHAR(100),
Market_Segment VARCHAR(100),
distribution_channel VARCHAR(50),
is_repeated_guest INT,
previous_cancellations INT,
previous_bookings_not_canceled INT,
reserved_room_type VARCHAR(20),
assigned_room_type VARCHAR(20),
booking_changes INT,
deposit_type VARCHAR(50),
agent FLOAT,
company FLOAT,
days_in_waiting_list INT,
customer_type VARCHAR(50),
ADR FLOAT,
required_car_parking_spaces INT,
total_of_special_requests INT,
Booking_Status VARCHAR(50),
reservation_status_date DATE,
Total_Nights INT,
Revenue FLOAT,
Total_Guests INT);

```

---

# SQL Analysis

Performed SQL queries for:

## Revenue Analysis

- Total Revenue
- Total Bookings
- Total Guests
- RevPAR
- Cancellation Rate
- Average ADR

## Booking Analysis

- Cancellation Rate
- Booking Status Analysis
- Lead Time Analysis

## Customer Analysis

- Market Segment Performance
- Distribution Channel Analysis
- Customer Type Analysis

---

# Power BI Dashboard

Designed a multi-page interactive dashboard for hospitality performance analysis.

## Page 1 — Executive Overview

### KPIs

- Total Revenue
- Total Bookings
- ADR
- RevPAR
- Cancellation Rate

### Visualizations

- Revenue Trend Analysis
- Revenue by Hotel Type
- Booking Status Distribution

<img width="1170" height="661" alt="overview" src="https://github.com/user-attachments/assets/6c6d1910-a3ea-41ad-b98e-b095ecd22974" />


---

## Page 2 — Customer Analysis

### Visualizations

- Revenue by Country
- Market Segment Analysis
- Distribution Channel Performance
- Customer Type Analysis


<img width="1169" height="663" alt="customer analysis" src="https://github.com/user-attachments/assets/cc3ee049-3ca6-48f3-b1cb-0b2e61d91da0" />

---

## Page 3 — Room & Stay Analysis

### Visualizations

- Revenue by Room Type
- Weekend vs Weekday Stay Analysis
- Lead Time Analysis
- Deposit Type Analysis
- Special Requests Analysis

<img width="1421" height="746" alt="Room and stay analysis" src="https://github.com/user-attachments/assets/989ea63a-0e93-446e-8a05-ae869b07e3be" />

---

# DAX Measures

## Total Revenue

```DAX
Total Revenue = SUM(hotel_bookings[Revenue])
```

## Total Bookings

```DAX
Total Bookings = COUNTROWS(hotel_bookings)
```

## Average ADR

```DAX
Average ADR = AVERAGE(hotel_bookings[ADR])
```

## Cancellation Rate

```DAX
Cancellation Rate =
DIVIDE(
COUNTROWS(
FILTER(hotel_bookings,
hotel_bookings[is_canceled]=1)),
COUNTROWS(hotel_bookings)
)*100
```

## RevPAR

```DAX
RevPAR =
DIVIDE(
[Total Revenue],
[Total Bookings]
)
```

---

# Key Business Insights

- City hotels generated higher revenue compared to resort hotels.
- Online travel agencies contributed the highest number of bookings.
- Cancellation rates increased during peak seasons.
- Deluxe room types generated the highest ADR.
- Specific countries contributed significantly to overall revenue.

---

# Dashboard Features

- Interactive slicers
- Dynamic filtering
- KPI cards
- Trend analysis
- Customer segmentation
- Revenue optimization insights

---

# Project Outcomes

- Monitored hotel performance effectively
- Analyzed customer booking behavior
- Identified high-revenue segments
- Supported pricing optimization strategies
- Improved operational decision-making

```

---

# Author

**Alappa gari Susmitha**  
