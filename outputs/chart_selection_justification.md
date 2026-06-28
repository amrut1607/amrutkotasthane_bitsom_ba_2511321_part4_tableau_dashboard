# Chart Selection Justification Report

**Student Name:** Amrut Kotasthane  
**Student ID:** bitsom_ba_2511321  

---

## 1. Line Chart for Monthly Trends
*   **Question Answered:** How are sales and profits changing over time?
*   **Why Appropriate:** Line charts are the industry standard for continuous temporal data, making it easy to identify trend directions and seasonal spikes.
*   **Marks Card Fields:** 
    *   *Columns:* `Order Date` (Truncated to Month/Year)
    *   *Rows:* `SUM(Sales)`, `SUM(Profit)`
    *   *Color:* Measure Names (Green for Sales, Red for Profit)
*   **Design Principle:** Maintained a clean visual hierarchy by keeping gridlines soft and labeling peak months directly.
*   **Mistake Avoided:** Avoided using a 3D bar chart, which distorts values and makes time comparison difficult.

---

## 2. Grouped Bar Chart for Product Categories
*   **Question Answered:** Which categories drive sales vs. net profit?
*   **Why Appropriate:** Grouped bars allow direct comparison of two metrics across discrete categories.
*   **Marks Card Fields:**
    *   *Columns:* `Category`
    *   *Rows:* `SUM(Sales)`, `SUM(Profit)` (Measure Values)
    *   *Color:* Measure Names
*   **Design Principle:** Sorted categories descending by sales to establish a logical reading flow.
*   **Mistake Avoided:** Avoided using a stacked bar chart, which hides the true difference in category profit margins.

---

## 3. Scatter Plot for Discount vs. Profit
*   **Question Answered:** How does discounting affect order profitability?
*   **Why Appropriate:** Scatter plots display the correlation between two continuous variables.
*   **Marks Card Fields:**
    *   *Columns:* `Discount`
    *   *Rows:* `Profit`
    *   *Detail:* `Order Id`
    *   *Color:* `Category`
*   **Design Principle:** Applied transparency to scatter points to prevent overlapping clutter.
*   **Mistake Avoided:** Avoided using a simple average line, which hides individual order outliers.
