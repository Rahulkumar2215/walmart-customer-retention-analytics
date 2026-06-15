# Walmart Customer Retention Analytics — Power BI

An interactive Customer Retention dashboard built in Power BI for Walmart. It consolidates customer demographics, transactions, store/channel data, loyalty program data, and churn labels to analyse why customers churn and identify loyal vs. at-risk customers across regions, channels, and loyalty tiers.

## Tools Used

- Power BI Desktop (data modelling, DAX, report building)
- Power Query (data cleaning and transformation)
- Microsoft Excel (source data)

## Datasets

| Table | Key Columns |
|-------|-------------|
| `Customer_Demographics` | Customer_ID, Age, Gender, Region, Income_Level, Membership_Since, Preferred_Channel |
| `Customer_Transactions` | Transaction_ID, Customer_ID, Store_ID, Product_Category, Transaction_Date, Amount, Promotion_Applied |
| `Store_Locations` | Store_ID, Store_Type, Region, Opening_Year |
| `Loyalty_Program` | Customer_ID, Loyalty_Tier, Points_Earned, Points_Redeemed |
| `Churn_Labelled_Customers` | Customer_ID, Last_Purchase_Date, Churn_Flag, Churn_Reason |

## Data Model

`Customer_Demographics` is the central table:

- `Customer_Demographics` → `Customer_Transactions`, `Loyalty_Program`, `Churn_Labelled_Customers` (One-to-Many / One-to-One)
- `Customer_Transactions` → `Store_Locations` (Many-to-One)

## Report Pages

1. **KPIs** — headline retention metrics
2. **Loyalty and Promotion** — promo impact and loyalty engagement
3. **Store / Channel Insights** — store-type and channel performance
4. **Segmentation** — churned, repeat, and high-value customers
5. **Recommendations** — final takeaways

Slicers: Preferred_Channel, Income_Level, Loyalty_Tier, Region.

## Key Findings

- 300 total customers, 149 churned, 151 active — overall churn rate of **49.67%**
- **By region:** West churns highest (60.00%), South lowest (40.85%)
- **By channel:** Online churns more (53.55%) than Store (45.52%)
- **By loyalty tier:** Elite churns highest (54.67%), Basic lowest (40.58%)
- 49% of transactions used a promotion, but promo vs. non-promo spend is nearly flat (~516 each) — almost no uplift
- Loyalty redemption rate of **82.31%**
- Total revenue ~516K, split closely between Online (~259.85K) and Store (~256.42K)
- Average CLV of 486.19; annual CLV of ₹319
- Segments: 149 churned, 119 loyal mid-value, 32 high-value

## Recommendations

- Prioritise the South region and Plus members for retention
- Online underperforms in the East; offline stores underperform in the West
- Promo users churned the most — revise the promotion strategy and make promo codes easier to apply

## Video Walkthrough

https://www.loom.com/share/9a510d476d474e8999221c438ff28876
