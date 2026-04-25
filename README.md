# Global Sales Data Warehouse & BI Solution

## Overview
End-to-end data warehousing and business intelligence solution 
built on SQL Server, processing 100,000+ sales records from 
multiple source systems.

## Tech Stack
SQL Server | SSIS | SSAS | Power BI | Visual Studio 2022

## Architecture
- **Data Warehouse**: Star schema with 1 fact table and 4 dimension tables
- **ETL Pipeline**: SSIS packages to extract, transform, and load 
  from multiple source types
- **OLAP Cube**: SSAS cube with drill-down hierarchies
- **Reporting**: Power BI reports published to Power BI Service

## Key Features
- SCD Type 2 on Dim_Product to track historical pricing changes
- Lookup, Derived Column, and Data Conversion transformations 
  for surrogate key resolution
- Three-level product category hierarchy
- Accumulating fact logic to track transaction processing time
- Power BI drill-through and cascading filter functionality

## How to Run
1. Restore the SQL Server database using the provided scripts
2. Open the Visual Studio solution and configure connection strings
3. Run SSIS packages in order: [1.load_dimension.dstx, 2.load_fact.dstx, 3.Update_accumulatingFact.dstx]
4. Connect Power BI file to your local SSAS cube
