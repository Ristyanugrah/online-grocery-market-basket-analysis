# Online Grocery Market Basket Analysis: Product Bundling & Cross-Selling

## Project Overview

This project explores online grocery transaction data to identify product combinations that may support cross-selling and product bundling strategies.

Using Python and Pandas, the analysis transforms order-level transaction data into a basket matrix, where each row represents an order and each column represents a product. Boolean values indicate whether a product appears in a particular order.

This structure provides the foundation for Market Basket Analysis, which can be extended with association rule mining to discover frequently purchased product combinations.

## Business Objectives

- Transform transaction data into a basket matrix.
- Explore product co-occurrence patterns across orders.
- Identify potential product combinations for cross-selling.
- Discover bundling opportunities based on purchasing behavior.
- Support data-driven promotional and merchandising strategies.

## Dataset

**Dataset file:** `online_grocery.csv`

The notebook uses the following columns:

- `order_id` — Unique identifier for an order.
- `product_name` — Name of the product purchased.

The dataset contains transaction-level product information. Dataset size, date coverage, and the total number of unique products and orders should be confirmed during the analysis.

## Tools & Technologies

- Python
- Pandas
- Jupyter Notebook / Google Colab
- Association rule mining techniques (planned extension)

## Methodology

### 1. Load Transaction Data

Load the online grocery dataset into a Pandas DataFrame and inspect the transaction records.

### 2. Prepare Transaction Data

Select `order_id` and `product_name`, then remove duplicate order-product combinations to ensure that each product appears only once per order.

### 3. Create the Basket Matrix

Transform the transaction data into a wide-format matrix:

- Rows represent orders.
- Columns represent products.
- `True` indicates that a product appears in an order.
- `False` indicates that a product does not appear in an order.

This format can be used as input for frequent itemset mining and association rule analysis.

## Current Analysis Status

The current notebook implements data preparation and basket matrix construction.

The following analyses are potential next steps and have not yet been demonstrated by the supplied code:

- Frequent itemset discovery.
- Association rule generation.
- Support, confidence, and lift calculation.
- Ranking product combinations for cross-selling and bundling.

## Potential Business Applications

Once frequent product combinations have been identified, the results can help support:

1. **Cross-selling:** Recommend complementary products during shopping or checkout.
2. **Product bundling:** Create bundles from products frequently purchased together.
3. **Promotional campaigns:** Design targeted offers around relevant product combinations.
4. **Merchandising:** Explore product placement and recommendation opportunities.
5. **Customer experience:** Improve product discovery through relevant recommendations.

These are potential applications rather than confirmed findings from the current notebook.

## Limitations

- The current analysis only prepares transaction data and does not yet establish product associations.
- Product names must be consistent to avoid treating the same product as multiple items.
- Duplicate order-product records are removed, so the analysis represents product presence rather than purchase quantity.
- The dataset's size, time period, and completeness have not yet been documented.
- Promotional decisions should be validated against business constraints, product margins, and actual customer behavior.

## Repository Structure

```text
online-grocery-market-basket-analysis/
├── online_grocery_market_basket_analysis.ipynb
├── README.md
└── data/
    └── README.md
```

The dataset can be stored locally or documented in `data/README.md` if it cannot be redistributed.

## How to Run

1. Clone or download this repository.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Place `online_grocery.csv` in the appropriate location.
4. Update the file path if necessary.
5. Run the notebook cells in sequence.
6. Inspect the resulting basket matrix.

## Author

**Risty Anugrah Dwi Septiana**

- GitHub: [Ristyanugrah](https://github.com/Ristyanugrah)
- Data Analytics Portfolio: [data-analytics-portfolio](https://github.com/Ristyanugrah/data-analytics-portfolio)
- Portfolio Website: [risty-portfolio.vercel.app](https://risty-portfolio.vercel.app/)

---

*This project demonstrates transaction data preparation for Market Basket Analysis, with a focus on product bundling and cross-selling opportunities.*
