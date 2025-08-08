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

