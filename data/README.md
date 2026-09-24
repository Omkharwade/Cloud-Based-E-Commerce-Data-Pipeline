# E-Commerce Dataset

This project uses five e-commerce datasets representing common transactional and master data.

## Datasets

| Dataset | Records | Description |
|---|---:|---|
| Customers | 10,000 | Customer details and registration information |
| Products | 2,000 | Product details, categories, and prices |
| Orders | 100,100 | Customer orders and order-level transaction information |
| Order Items | 200,000 | Products and quantities associated with orders |
| Payments | 100,000 | Payment transaction and payment status information |

## Data Quality Scenarios

The source data intentionally contains realistic data-quality issues to demonstrate data engineering validation and quarantine handling.

Examples include:

- Missing customer IDs
- Missing order dates
- Duplicate order IDs
- Invalid order statuses
- Non-positive order amounts
- Missing product IDs
- Zero quantities
- Invalid payment statuses

These issues are detected during the Silver-layer transformation and invalid records are moved to quarantine tables.

## Data Processing

```text
Raw CSV Data
     ↓
Bronze Layer
     ↓
Data Quality Validation
     ↓
Silver Layer
     ↓
Gold Layer
     ↓
Power BI
