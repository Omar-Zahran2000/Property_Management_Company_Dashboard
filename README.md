# Property Management Company Dashboard (Mock Project)

## Project Overview
This Power BI project simulates a portfolio-level reporting suite for a U.S.-based property management company. It brings together unit inventory, leasing, rent health, and delinquency into a set of interactive, drillable dashboards. The goal is to demonstrate the end‑to‑end analytics and product thinking I apply at work while keeping client data private.

## Objectives
- Integrate Excel/CSV mock data into a clean semantic model
- Define and track portfolio KPIs: occupancy, rent paid vs. due, delinquency, lease activity, unit mix
- Design role‑ready dashboards for executives and operations
- Enable fast exploration with slicers, field parameters, navigation buttons, and custom tooltips
- Provide auto‑generated narrative (“Report Summary”) and Q&A for ad‑hoc questions

## Data Sources
Mocked flat files representing:
- Units (type, beds/baths, location, size)
- Leases (start/end, status, duration)
- Monthly rent (billed vs. collected, partial/late status)
- Tenants (basic profile and payment behavior)

## Tools & Techniques

| Tool / Feature              | Purpose                                                                 |
|----------------------------|-------------------------------------------------------------------------|
| **Power BI Desktop**       | Data modeling, relationships, formatting, UX                           |
| **Power Query**            | Data shaping, type casting, column derivations                         |
| **DAX**                    | KPI measures (Occupancy %, Active Lease %, Avg Lease Duration, etc.)   |
| **Field Parameters**       | Toggle the Exec line chart (e.g., Rent Paid vs. Rent Due)              |
| **Custom Tooltips**        | On‑hover detail cards and sparkline/area charts                        |
| **Q&A Visual**             | “Ask a question” tile for natural‑language exploration                  |
| **Slicers & Cross‑filter** | Location, Unit Group, Unit Type; visual interactions across the page   |
| **Buttons & Nav**          | Page navigation and “More Info” actions                                |
| **Report Summary**         | Dynamic narrative driven by measures                                    |

---

## Dashboards & Pages

### 1) Executive Summary
High‑level portfolio health with KPI cards, a trend line, and composition visuals.

- **KPIs:** Total Rent Paid, Total Rent Due, Total Units, Occupancy, Occupancy Rate
- **Trend:** *Total Rent Paid by Date* with **field parameter** to toggle to *Rent Due* (and optional rolling trend)
- **Composition:** Rent collected by Unit Group, Occupied Units donut
- **Slicers:** Location, Unit Group, Unit Type (left panel)
- **Usage:** Start here to gauge overall performance; filter by region or unit mix to compare markets

![Exec Summary](images/Exec%20Summary.JPG)

**Filtered view example (North selected):**

![Exec Summary Filtered by location](images/Exec%20Summary%20Filtered%20by%20location.JPG)

---

### 2) Leasing Activity & Occupancy
Operational view of occupancy, leasing velocity, and expirations.

- **KPIs:** Occupancy Rate, **Active Lease %**, **Avg. Lease Duration (months)**
- **Breakdown:** Units by Type stacked bar (Occupied vs. Vacant)
- **Seasonality:** *Leases Started per Month* column chart
- **Action Panel:** *Leases Expiring* counters for the next 7/30/60/90 days
- **Detail Table:** Lease roster with status coloring for quick triage

![Leasing Activity & Occupancy](images/Leasing%20Activity%20%26%20Occupancy.JPG)

---

### 3) Rent Health & Delinquency
Portfolio cash‑flow health and late‑payment analysis with narrative.

- **Top visual:** *Rent Due vs. Paid by Month* columns
- **Status:** Delinquency Status donut and **Late Payment Buckets** (1–10 days, 11–30 days, On Time)
- **Narrative:** **Report Summary** auto‑text explains whether *Late* exceeds *On Time* and highlights bucket totals
- **Tables:** Tenant‑level payment history with Days Late and status color coding
- **Actions:** *More Info* buttons navigate to deeper analyses

![Rent Health & Delinquency](images/Rent%20Health%20%26%20Delinquency.JPG)

**Custom tooltip example – Partial Payments trend shown on hover (area chart):**

![Rent Health & Delinquency - Partial Payments by Date](images/Rent%20Health%20%26%20Delinquency%20-%20Partial%20Payments%20by%20Date.JPG)

---

### 4) Unit Portfolio Performance
Granular unit‑mix and pricing intelligence with smart exploration.

- **Highlights:** *Most Occupied Unit Type*, *Avg. Monthly Rent across Units*, *Average Rent per SqFt*
- **Revenue Mix:** *Rent by Unit Type* bar chart
- **Vacancy Watch:** Gauge shows current vacancy vs. threshold
- **Inventory Map:** Treemap of **Number of Units by Location** with cross‑filter to the right‑side unit table
- **Q&A:** *Ask a question about your data* tile to quickly surface ad‑hoc insights
- **Detail:** Right‑hand unit table with conditional formatting on *Avg Monthly Rent* and lease count

![Unit Portfolio Performance](images/Unit%20Portfolio%20Performance.JPG)

---

## Key Insights (from screenshots)
- **Occupancy ~77–78%** across the portfolio; opportunity to lift utilization by targeting vacancies by unit type and location
- **Rent Paid vs. Due** trends track closely, but delinquencies persist; *Report Summary* shows **Late** > **On Time** in the selected period, indicating systemic risk to cash flow
- **North and West** carry the largest lease counts in the Exec Summary example; targeted marketing in **East/South** could balance exposure
- **Unit Type impact:** *3BR 2BA* is the most occupied type, while smaller units show higher churn—helpful for pricing and concessions strategy
- **Partial Payments** trend is elevated relative to target (tooltip), suggesting process interventions (reminders, payment plans)
- **Expiring Leases** counters (7/30/60/90 days) provide proactive workload planning for the leasing team

---

## How This Helps a Property Management Company
- **Portfolio visibility:** Executives get a single‑page snapshot of financials, occupancy, and mix
- **Collections focus:** Managers can pinpoint the tenants and segments driving late/partial payments
- **Leasing operations:** Expiration counters and monthly starts inform staffing and renewal campaigns
- **Revenue optimization:** Unit mix and location comparisons surface underpriced segments and high‑demand types
- **Self‑service:** Slicers, Q&A, and “More Info” buttons reduce manual ad‑hoc reporting

---

## Interaction & UX Features
- **Field Parameters** – toggle the main line chart between *Rent Paid* and *Rent Due* in Exec Summary
- **Custom Tooltips** – on‑hover popups include micro‑charts (e.g., Partial Payments trend) for context without leaving the page
- **Report Summary** – dynamic narrative converts measures into plain‑English commentary
- **Filters/Slicers** – Location, Unit Group, Unit Type enable quick cohort analysis
- **Navigation Buttons** – consistent bottom‑left icons for page switching and deep dives
- **Cross‑filtering** – clicking bars/treemap slices filters related visuals and the detail tables

---

## Alignment with My Work at RTCS
- **Automated BI Dashboards** – This mock reproduces how I build Power BI solutions that integrate multiple sources and cut manual reporting
- **KPI Definition with Leadership** – Cards, gauges, and the Report Summary demonstrate codified KPIs for portfolio health
- **Process Design** – Expiration counters and delinquency buckets translate analytics into operational workflows
- **Strategy Bridge** – Insights connect to pricing, marketing, and collections actions that lift NOI and reduce risk


