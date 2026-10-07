# DAX Measures Practice

Two Power BI files focused on writing and testing **DAX measures** on chocolate sales / shipment data.

## Files

| File | Tables | Pages | Focus |
|------|--------|-------|-------|
| `DAX.pbix` | calendar, locations, people, products, sales | 6 | Core measures, % calculations, targets |
| `DAX2.pbix` | calendar, locations, people, products, shipments | 6 | Team filters, target comparison, APS/APB |

## Data Model (both files)
Star schema: **sales/shipments** (fact) + products, people, locations, calendar.

## Key Measures Developed

### Aggregations
- Total Amount, Total Boxes, Shipment Count
- Count of Products

### Ratios & Rates
- Amount Per Shipment (APS)
- Amount Per Boxes (APB)
- Boxes Per Shipment
- Bar Shipment %

### Filtered / Segmented
- Americas Shipments / Bar Shipments
- Barr Amount, Barr Amount %
- Low Box Shipment Count
- Total Amount (My Team v1 / v2)

### Targets
- APS Target Achieved?
- Target Comparison (v1, v3)
- Sales Target

## Skills Practised
- `SUM`, `COUNT`, `DISTINCTCOUNT`
- `CALCULATE` with filter arguments
- Percentage of total patterns
- Boolean / status measures (target achieved?)
- Team-based filter context
- Iterating measure versions (v1, v2, v3)

## How to Open
Open `DAX.pbix` or `DAX2.pbix` in Power BI Desktop. Inspect measures under the fact table in the Fields pane.
