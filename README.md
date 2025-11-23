# 🚖 OLA Ride Analytics Dashboard – Power BI

This repository contains a complete analytics dashboard built in **Power BI** to analyze OLA ride operations.  
The dashboard provides structured insights into ride performance, customer patterns, revenue trends, time-slot behavior, cancellations, and vehicle-wise contributions.

---

## 📊 Project Objective
The goal of this project is to convert raw OLA ride data into clean, interactive, and decision-oriented business insights using Power BI.  
The dashboard is designed to help understand:
- Ride demand patterns  
- Revenue performance  
- Rider & driver behavior  
- Operational inefficiencies such as cancellations and incomplete rides  

---

## 🧩 Dataset Overview
The dataset includes:
- Date & Time  
- Booking ID  
- Booking Status  
- Customer ID  
- Vehicle Type  
- Pickup & Drop Locations  
- Cancelled & Incomplete Ride Reasons  
- Ride Distance  
- Booking Value  
- Payment Method  
- Rider & Driver Ratings  

---

## 🛠️ Tools & Skills Used
- **Power BI**
- **DAX (Data Analysis Expressions)**
- **Power Query (ETL)**
- **Data Modeling**
- **Data Cleaning**
- **KPI Metrics Design**
- **Interactive Visualization**

---

## 📁 Project Files
- `OLA_Dashboard.pbix` – Power BI dashboard file  
- `Dataset.csv` – Raw data (if you want to upload)  
- `README.md` – Project documentation  

---

## 📌 Dashboard Features

### **1. Overview Page**
- Completed, Cancelled & Incomplete Ride KPIs  
- Peak and low-demand hours  
- Time-slot classification using DAX  
- Rides by Booking Status  

### **2. Location Analysis**
- Top pickup & drop locations  
- Heatmap-style insights  
- Ride distance patterns  

### **3. Rider Analytics**
- New vs Returning vs Regular riders  
- Customer ratings  
- Cancellation behavior  

### **4. Revenue Analysis**
- Total revenue  
- Vehicle-wise revenue split  
- Payment method trends  

### **5. Vehicle Insights**
- Ride distribution by vehicle type  
- Vehicle performance & contribution  
- Revenue per km / per ride (if calculated)

---

## 🧮 Key DAX Measures Used
Some important DAX calculations include:

```DAX
Total Rides = COUNT(Uber[Booking ID])

Completed Rides = CALCULATE(COUNT(Uber[Booking ID]), Uber[Booking Status] = "Completed")

Cancelled Rides = CALCULATE(COUNT(Uber[Booking ID]), Uber[Booking Status] = "Cancelled")

Total Revenue = SUM(Uber[Booking Value])

Average Rating = AVERAGE(Uber[Customer Rating])
