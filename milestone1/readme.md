# 🏨 Hotel Analytics & Revenue Optimization (Power BI)
This project analyzes hotel operational and financial performance using a structured Star Schema data model and Power BI dashboards.
The objective is to understand **occupancy trends, revenue drivers, guest behavior.
## 📊 Dataset Description
The dataset represents daily and monthly hotel performance metrics, covering bookings, revenue, guests, operations, and external factors.
# 📅 Time-Based Attributes
Date: Recorded date
Month: Numeric month (1–12)
Day of the Week: Numeric day (1–7)
Season: Winter, Spring, Summer, Fall
Public Holiday: Binary (0/1)
## 🏨 Booking & Guest Information
Booking Source (Direct, OTA)
Guest Type (Leisure, Business)
Nationality
Repeat Guests (%)
Group Bookings (0/1)
Booking Lead Time
Booking Cancellations (%)
🛏 Room & Pricing
Room Rate
Average Daily Rate (ADR)
Discounts and Promotions
Maintenance Issues
## 📈 Revenue Metrics
Room Revenue
Food & Beverage Revenue
Other Services Revenue
Total Revenue for the Month
Previous Month Revenue
Year-over-Year Revenue
RevPAR (Revenue per Available Room)
## 🧱 Data Modeling (Star Schema)
The model follows best practices for analytical performance and scalability.

⭐ Fact Table

Fact_Bookings

Occupancy Rate

ADR

RevPAR

Booking Lead Time

Booking Cancellations

Room Revenue

F&B Revenue

Other Services Revenue

Total Revenue

Marketing Spend

Profit Metrics

🔵 Dimension Tables:

Dim_Date: Date, Month, Day, Season, Holiday

Dim_Guest: Guest Type, Nationality, Repeat Guests

Dim_Room: Room Rate, Discounts, Maintenance

Dim_Market: Booking Source, Promotions

Dim_External: Weather, Economic Indicators, Events

## 📐 Key Calculated Metrics
Occupancy Rate

ADR (Average Daily Rate)

RevPAR Profit = Total Revenue – Total Cost Year-over-Year Revenue Growth.

## 🔍 Key Observations
1.Seasonal demand significantly impacts occupancy and ADR.

2.OTA bookings increase volume but reduce margins.

3.Repeat guests contribute higher lifetime value.
4.Promotions increase occupancy but may reduce ADR.

5.External factors (weather, local events) strongly influence demand.

## 📌 Future Enhancements
1.Predictive occupancy forecasting

2.Price optimization models

3.Competitor benchmarking dashboards
