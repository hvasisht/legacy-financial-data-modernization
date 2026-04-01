# Legacy Financial Data Modernization

## Project Overview
End-to-end ETL project migrating a 10-table legacy 
financial database into 5 modern structured tables 
using SQL and Snowflake.

## Architecture
10 Legacy Tables → 5 Modern Tables

| Legacy | Modern |
|--------|--------|
| EMPLOYEES + DEPARTMENTS | DIM_EMPLOYEE |
| CUSTOMERS + COMPLIANCE | DIM_CUSTOMER |
| ACCOUNTS | FACT_ACCOUNT |
| TRANSACTIONS | FACT_TRANSACTION |
| LOANS + INVESTMENTS | FACT_FINANCIAL_PRODUCT |

## Tools Used
- Snowflake (Cloud Data Warehouse)
- SQL (Transformation & Validation)
- Excel (Data Mapping Document)

## Project Steps
1. Data Profiling — SQL queries to find all issues
2. Data Mapping — Excel document showing field translations
3. Error Logging — Captured 16 data quality issues
4. ETL Transformation — SQL to clean and migrate data
5. Data Validation — Row counts, null checks, reconciliation

## Data Quality Issues Found & Fixed
- NULL values in names, dates, balances
- Inconsistent codes (SAV/SAVING/Sav → Savings)
- Negative balances → set to 0
- Mixed country formats (US/USA/U.S.A → US)
- Mixed date formats (DD/MM/YYYY → YYYY-MM-DD)

## Files
- legacy_financial_data.xlsx — 10 legacy tables
- data_mapping_document.xlsx — mapping + gap analysis
- modern_transformation.sql — full ETL SQL script
- 10 CSV files — individual legacy tables
