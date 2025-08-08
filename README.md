# ds_Avneesh_Dayal
## Objective
This project analyzes how **trader performance** (profitability, risk, trade volume, and leverage) aligns or diverges from **Bitcoin market sentiment** (Fear vs Greed).  

## Data Sources
1. **Historical Trader Data (Hyperliquid)**  
   - Columns: Account, Coin, Execution Price, Size Tokens/USD, Side, Timestamp, Start Position, Direction, Closed PnL, Leverage, etc.
   - Covers 200k+ trades across multiple symbols.

2. **Fear/Greed Index Data**  
   - Columns: Timestamp, Value, Classification, Date.
   - Classification mapped to two categories:
     - **Fear**: Fear + Extreme Fear
     - **Greed**: Greed + Extreme Greed

## Methodology

### **1. Data Cleaning & Preparation**
- Converted timestamps to proper datetime objects.
- Extracted trade dates for merging.
- Normalized sentiment categories to `Fear` or `Greed`.

### **2. Merging Datasets**
- Joined trade data with daily sentiment values on the `date` field.

### **3. Feature Engineering**
- `is_win`: Boolean flag for profitable trades.
- `pnl_per_usd`: Profit normalized by trade size.
- Standardized trade sides (BUY → Long, SELL → Short).

### **4. Aggregation & Metrics**
- Grouped by sentiment to calculate:
  - Avg & median PnL
  - Win rate
  - Avg trade size
  - Trade count
- Grouped by sentiment & trade side to analyze directional performance.
