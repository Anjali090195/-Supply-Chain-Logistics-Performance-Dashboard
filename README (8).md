
# Project Title

**🚚 Supply Chain & Logistics Performance Dashboard**

**📊 Project Overview**

A 3-page interactive Power BI dashboard analyzing supply chain, logistics, inventory, and operational performance.
An Overview page with page navigation buttons enables seamless movement across all dashboard pages.

**🛠 Tools & Technologies**

Power BI

DAX (Data Analysis Expressions)

Page Navigation (Buttons)

Data Modeling & Visualization


**📄 Dashboard Structure & DAX Measures**

**🔹 Overview Page**

Used Page Navigation feature to navigate to:

Business Performance Overview

Inventory & Logistics Performance

Operational Performance & Quality Insights


**🔹 Page 1: Business Performance Overview**

**DAX Measures Used:**

Total Revenue =
SUM(supplychain[Revenue generated])

Total Units Sold =
SUM(Supplychain[No: of products Sold])

Total Lead Time =
AVERAGE(Supplychain[Lead Time]+AVERAGE(supplychain[Manufacturing lead time]+AVERAGE(supplychain[shipping times])

Avg Defect Rate % =
AVERAGE(Supplychain[Defect Rates])

**Focus:**
Revenue performance, sales volume, lead time impact, and defect trends.

**🔹 Page 2: Inventory & Logistics Performance**

**DAX Measures Used:**

Total Stock =
SUM(supplychain[Stock Levels])

Inventory Turnover =
DIVIDE([Total units sold],
    AVERAGE(supplychain[Stock Levels]))


Avg Shipping Time =
AVERAGE(Supplychain[Shipping Time])

Shipping Cost per Unit =
DIVIDE(
    SUM(Supplychain[Shipping Cost]),[Total Units Sold])


**Focus:**
Inventory movement, logistics efficiency, shipping time, and cost analysis.

**🔹 Page 3: Operational Performance & Quality Insights**

**DAX Measures Used:**

Avg Supplier Lead Time =
AVERAGE(Supplychain[Lead Time])

Avg Manufacturing Lead Time =
AVERAGE(Supplychain[Manufacturing Lead Time])

Manufacturing Cost per Unit =
DIVIDE(
    SUM(Supplychain[Manufacturing Cost]),
    SUM(Supplychain[product volumes])
)

Defective Units =
SUMX(Supplychain,Supplychain[Product volumes]*supplychain[Defective Units])

**Focus:**
Supplier efficiency, manufacturing performance, cost control, and quality issues.

**📈 Key Features**

Multi-page dashboard with page navigation

KPI cards built using custom DAX measures

Interactive slicers (location, supplier, SKU, product type, carrier)

Clear separation of business, logistics, and operational insights


**👩‍💻 Author**

Anjali D

Aspiring Data Analyst




