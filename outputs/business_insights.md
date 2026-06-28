# Business Insights Report: Executive Sales Performance

**Student Name:** Amrut Kotasthane  
**Student ID:** bitsom_ba_2511321  

---

## 1. Tableau Calculated Fields Created
*   **Profit Margin:** `SUM([Profit]) / SUM([Sales])`
    *   *Logic:* Calculates the net profit percentage for any selected level of detail, ensuring accurate aggregation across filters rather than a simple row average.
*   **Cost:** `[Sales] - [Profit]`
    *   *Logic:* Computes the cost of goods sold (COGS) and fulfillment costs to evaluate operational efficiency.
*   **Average Order Value (AOV):** `SUM([Sales]) / COUNTD([Order Id])`
    *   *Logic:* Measures the average transaction size by dividing total sales by unique order IDs.
*   **Return Rate:** `SUM(IIF([Return Flag] = 1, 1, 0)) / COUNT([Order Id])`
    *   *Logic:* Isolates returned orders to track product quality and logistics satisfaction.
*   **Shipping Delay Bucket:** `IF [Delivery Days] > 4 THEN "Delayed" ELSEIF [Delivery Days] > 2 THEN "Standard" ELSE "Express" END`
    *   *Logic:* Groups shipping timelines into buckets to monitor delivery SLAs.

---

## 2. Executive Business Insights

### Insight 1: Sales Trend
*   **Observation:** Sales exhibit a distinct upward trajectory towards the end of the year, peaking in November and December.
*   **Evidence:** Monthly sales reach a baseline peak of **$28.4M** in November 2025 compared to **$14.2M** in January.
*   **Interpretation:** Seasonal promotional periods drive the majority of yearly sales volumes.
*   **Action:** Secure inventory depth and increase advertising spend starting in October to fully capture Q4 seasonal demand.

### Insight 2: Regional Performance
*   **Observation:** The West region is the primary revenue contributor, while the South is the smallest.
*   **Evidence:** West sales total **$64.91M** compared to South sales of **$36.21M**.
*   **Interpretation:** Regional market penetration is highly unequal. West has strong distribution networks.
*   **Action:** Conduct local marketing in the South to expand customer acquisition and replicate West region playbooks.

### Insight 3: Category Profitability
*   **Observation:** Technology is the primary profit driver, whereas Furniture has low profitability despite high sales volume.
*   **Evidence:** Technology profit margin is **20.5%** compared to Furniture's margin of **5.2%**.
*   **Interpretation:** High COGS and shipping overheads erode Furniture margins.
*   **Action:** Adjust pricing on bulk Furniture items or renegotiate freight shipping rates to recover margin.

### Insight 4: Customer Segment Behavior
*   **Observation:** The Consumer segment represents the majority of our market share.
*   **Evidence:** Consumer sales account for **51.8%** of total revenue.
*   **Interpretation:** Individual retail customers drive the business, but corporate segments remain under-served.
*   **Action:** Launch B2B corporate loyalty pricing programs to capture high-volume Corporate and Home Office transactions.

### Insight 5: Discount Impact
*   **Observation:** Higher discounts do not lead to larger order sizes and are correlated with lower profits.
*   **Evidence:** Scatter plots indicate that orders with $>20\%$ discounts show flat sales volume but negative profits.
*   **Interpretation:** Discounting is being used to clear stock rather than drive incremental high-margin purchases.
*   **Action:** Enforce a strict discount cap of **15%** for all segments unless clearing slow-moving inventory.

### Insight 6: Shipping & Delivery Performance
*   **Observation:** Same-day shipping fails to meet its SLAs.
*   **Evidence:** Same-day delivery averages **1.49 days**, with over 20% of orders taking 2 days.
*   **Interpretation:** Operational inefficiencies exist at warehouse fulfillment stages.
*   **Action:** Integrate real-time warehouse logging with Tableau to flag shipping delays within 4 hours.

### Insight 7: Return Patterns
*   **Observation:** Furniture experiences the highest product return rates.
*   **Evidence:** Furniture return rate is **6.8%** compared to Office Supplies return rate of **3.1%**.
*   **Interpretation:** Returns are driven by damage during transit or customer dissatisfaction with dimensions.
*   **Action:** Partner with logistics providers to improve packaging for fragile items and add 3D visual previews to the website.

### Insight 8: Business Opportunity (B2B Expansion)
*   **Observation:** B2B Corporate average order values (AOV) are higher than Consumer AOVs.
*   **Evidence:** B2B AOV is **$185.00** compared to Consumer AOV of **$112.00**.
*   **Interpretation:** Corporate orders are more valuable per transaction.
*   **Action:** Dedicate marketing resources to target B2B channels to grow overall margin.
