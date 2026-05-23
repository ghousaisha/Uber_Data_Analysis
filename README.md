# Uber Booking Analysis Dashboard

## Project Overview

This project is an interactive Power BI dashboard created to analyze Uber ride booking data. The dashboard provides insights into booking trends, cancellation analysis, revenue generation, vehicle performance, customer ratings, and operational KPIs.

The purpose of this project is to transform raw ride-booking data into meaningful business insights using data visualization and DAX measures in Power BI.

---

# Dashboard Features

## 1. Overall Analysis

* Total Bookings
* Successful Bookings
* Cancelled Bookings
* Booking Trends
* Ride Distribution

## 2. Cancellation Analysis

* Customer Cancellation Reasons
* Driver Cancellation Reasons
* Cancellation Percentage
* Cancellation Comparison

## 3. Vehicle Type Analysis

* Vehicle-wise Revenue
* Vehicle-wise Booking Count
* Popular Vehicle Types

## 4. Revenue Analysis

* Total Revenue
* Revenue by Vehicle Type
* Revenue Trends Over Time

## 5. Ratings Analysis

* Customer Ratings
* Driver Ratings
* Ride Experience Insights

---

# Tools & Technologies Used

* Power BI
* DAX (Data Analysis Expressions)
* Data Modeling
* Data Cleaning
* Interactive Visualizations

---

# Key KPIs Used

* Total Bookings
* Successful Bookings
* Cancelled Bookings
* Cancellation Rate
* Revenue
* Average Ratings
* CTAT
* VTAT

---

# Dataset Information

The dataset contains:

* Booking ID
* Booking Status
* Customer ID
* Vehicle Type
* Pickup & Drop Locations
* Ride Date
* Revenue
* Ratings
* Cancellation Reasons

---

# Important DAX Measures

## Cancelled Bookings

```DAX
CanceledBookings =
CALCULATE(
    COUNTROWS(ncr_ride_bookings),
    ncr_ride_bookings[Booking Status] IN {
        "Cancelled by Driver",
        "Cancelled by Customer"
    }
)
```

## Total Bookings

```DAX
TotalBookings =
COUNTROWS(ncr_ride_bookings)
```

## Cancellation Percentage

```DAX
CanceledPercentage =
DIVIDE(
    [CanceledBookings],
    [TotalBookings],
    0
)
```

---

# Objectives of the Project

* Analyze ride booking patterns
* Identify cancellation trends
* Monitor operational performance
* Improve business decision-making
* Build an interactive BI solution

---

# Insights Generated

* Percentage of cancelled rides
* Major cancellation reasons
* Most used vehicle category
* Revenue contribution by vehicle type
* Customer booking behavior trends

---

# Future Improvements

* Real-time data integration
* Predictive analytics
* AI-based ride demand forecasting
* Advanced customer segmentation

---

# Developed By

Aisha Ghous

Data Analytics & Power BI Project
