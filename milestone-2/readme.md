# 📈 Revenue, Occupancy and Guest Analysis

## 📌 Overview

The goal is to build an interactive hotel performance dashboard that provides business insights into revenue, occupancy, booking channels, and customer behavior.

## 🧱 Data Model Extension

Fact Table (Bookings / Raw_Fact)
Booking_ID
Guest_ID
Hotel_ID / Branch
Room_Type
Booking_Source (Direct / OTA)
Check-in Date
Check-out Date
Length of Stay
Rooms Booked
Revenue
Dimension Tables
Date
Hotel / Branch
Room Type
Guest

## 📐 DAX Measures

1️⃣ Rooms Sold:  Rooms Sold = SUM ( Bookings[Rooms Booked] )
2️⃣ Rooms Available:  Rooms Available = SUM ( Hotels[Total Rooms] )
3️⃣ Occupancy % : DIVIDE ( [Rooms Sold], [Rooms Available], 0 )
4️⃣ Total Revenue: Total Revenue = SUM ( Bookings[Revenue] )
5️⃣ Average Daily Rate (ADR): ADR = DIVIDE ( [Total Revenue], [Rooms Sold], 0 )
6️⃣ Revenue per Available Room (RevPAR): RevPAR = DIVIDE ( [Total Revenue], [Rooms Available], 0 )
Direct Revenue = CALCULATE ( [Total Revenue], Bookings[Booking Source] = "Direct" )

OTA Revenue = CALCULATE ( [Total Revenue], Bookings[Booking Source] = "OTA")

## 🎛️ Interactive Slicers

### Implemented slicers for:

	Room Type
	Hotel Branch / Location
	Booking Source
	Date Range
All slicers interact dynamically with all visuals.

### 👥 Guest Classification Metrics

Guest Measures ::
Total Bookings per Guest = COUNT ( Bookings[Booking_ID] )
Total Spend per Guest = SUM ( Bookings[Revenue] )
Guest Segmentation Column :  Guest Segment = SWITCH ( TRUE(), [Total Spend per Guest] >= 50000, "High Spender", [Total Bookings per Guest] >= 3, "Loyal Guest", [Total Bookings per Guest] = 1, "First-time Guest", "Regular Guest" )

## ✅ Final Outcome:

This dashboard provides:
Clear visibility into hotel revenue and occupancy
Comparison of Direct vs OTA performance
Deep understanding of guest behavior and Actionable customer segmentation.
Fully interactive decision-making experience

## 🎯 Business Value
Identify high-performing hotels and room types.
Optimize pricing and occupancy strategies.
Improve direct booking share.
Target loyal and high-spending guests effectively.

