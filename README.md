# 🛒 BlinkIT Sales Analysis Dashboard – Power BI Project

An interactive Power BI dashboard analyzing sales performance, customer ratings, and product trends for **BlinkIT**, India’s last-minute grocery delivery app.  
The report provides **key business insights** to help stakeholders make data-driven decisions.

---

## 📊 Objective

To create a one-page interactive dashboard that:
- Tracks **Total Sales, Average Sales, Average Ratings, and Items Sold**.
- Identifies **top-performing categories, outlets, and years**.
- Compares **sales trends** by item type, fat content, outlet size, and location.
- Enables **dynamic filtering** through slicers and KPIs.

---

## 🧠 Data Modeling

The data model follows a **star schema**:

### **Fact Table**
- `BlinkIT Grocery Data` – Sales amount, ratings, item count, outlet info.

### **Dimension Tables**
- **DimItem** – Item type, fat content.  
- **DimOutlet** – Size, location tier, establishment year, outlet type.  
- **DimDate** – Date table for time-based analysis.

---

## 🛠 Steps Followed

1. **Data Import:** Loaded CSV file into Power BI Desktop.  
2. **Data Profiling:** Checked column quality, distribution, and profiles in Power Query.  
3. **Data Cleaning & Transformation:** Ensured data accuracy and consistency.  
4. **KPI Creation:** Built measures for Total Sales, Average Sales, Average Rating, and Number of Items.
5. **Matrix for Slicer Control:** Created a dynamic slicer using a DAX table.
6. **DAX Measures:**
   ```DAX
   Total Sales = SUM('BlinkIT Grocery Data'[Sales])
   Avg Sales   = AVERAGE('BlinkIT Grocery Data'[Sales])
   Avg Rating  = AVERAGE('BlinkIT Grocery Data'[Rating])
   No of Items = COUNTROWS('BlinkIT Grocery Data')
