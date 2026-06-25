# Comprehensive Sales Analysis & Dashboarding Case Study: Wide World Importers

##  Project Overview
This project focuses on building an interactive retail performance dashboard using Power BI Desktop for **Wide World Importers**. The objective was to transform transactional sales data into structured visual insights, enabling stakeholders to track product quantity distributions, identify temporal business shifts, and evaluate employee sales performance.

---

## Data Architecture & Dimensions
The analytics environment utilises a star schema database design consisting of fact and dimension tables:
* **`FactSale`**: Contains transactional records including metrics like `Quantity`, `Profit`, and tax calculations.
* **`DimEmployee`**: Contains organisational staff details, mapping transactions to individual salespeople.
* **`DimDate`**: Provides temporal attributes (`Calendar Year`) for time-series aggregation.

---

##  Development Process & Methodology

### Phase 1: Product Distribution & Trend Analysis
1.  **Baseline Visual Layer**: Initialised a Column Chart visual to track the fundamental metric `Quantity of Items Sold` broken down over four years (2013–2016).
2.  **Granular Feature Engineering**: Progressively updated the chart properties from the `FactSale` data pane to compare storage types side-by-side by adding the following factual metrics:
    * `Total Dry Items`
    * `Total Chiller Items`

### Phase 2: Employee Performance & Matrix Layout
1.  **Tabular Reporting**: Implemented a blank **Table Visualisation** at the footer of the canvas to create a granular tabular breakdown.
2.  **Contextual Mapping**: Populated rows by mapping the categorical dimension `Employee` from the `DimEmployee` table.
3.  **Data Consolidation**: Added underlying fact fields (`Quantity`, `Total Including Tax`, and `Profit`) to create a unified, cross-filterable ledger of performance metrics per staff member.
4.  **UI/UX Optimisation**: Integrated a clean descriptive header ("Sales Data") via an Inserted Text Box visual and synchronised the page canvas tab title to ensure production-grade report hygiene.

---

##  Analytical Observations & Insights

### 1. Supply Chain & Inventory Shift (2013–2016)
* **The 2016 Operational Pivot**: Data analysis shows that between **2013 and 2015**, Wide World Importers exclusively distributed dry products, with `Total Chiller Items` registering at absolute zero. 
* **Inference**: A significant business pivot occurred in **2016**, marking the company's entry into cold-chain logistics and the distribution of chilled items.

### 2. High-Performer Deep Dive (FY2016)
By applying temporal cross-filtering (isolating the fiscal year **2016** on the primary column chart), individual employee performance was isolated:
* **Top Performer Focus**: Sales Representative **Sophia Hinton** demonstrated exceptional performance in the newly diversified market, generating **$309,004.06** in `Total Including Tax` revenue across 13,507 individual item sales.

---

##  How to Interact with the Report
1. Download the `Power_BI_Project.pbix` file from this repository.
2. Open the file using **Power BI Desktop**.
3. Use the Column Chart to click on specific **Calendar Years** to experience the dynamic cross-filtering behaviour across the employee summary table.
