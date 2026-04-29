📊 Trading Journal (React Dashboard)

A trading analytics dashboard built with React that processes real broker CSV data, converts timezones, groups order fills into trades, and generates performance insights.

🚀 Key Features
  📂 Smart CSV Import (Real Broker Data)
      Supports broker order history CSV
      Filters only “Filled” executions
      Handles semicolon-separated files
      Cleans and normalizes raw data
  🔄 Order → Trade Conversion
      Groups multiple fills into a single trade
        Supports:
          Scaling in
          Scaling out
        Automatically detects:
          Entry time
          Exit time
          Average exit price
          Total PnL
  🌎 Timezone Normalization
      Converts all timestamps from local (NZ) to New York market time
      Ensures accurate session-based analysis
      
📊 Analytics Dashboard
Trade table (cleaned + grouped trades)
  Key statistics:
    Win rate
    Average winner / loser
    RRR (realized)
    Best & worst stock
    Streaks
   Charts:
    Equity curve
    Drawdown
    Performance by day
    Plain-English insights
    
🧱 Tech Stack
  React (Vite)
  JavaScript
  Recharts (data visualization)
  PapaParse (CSV parsing)
  CSS (custom styling)
  
📂 Project Structure
src/
  app/
  components/
    dashboard/
    trades/
  features/
  lib/
  styles/
  
▶️ How to Run
npm install
npm run dev

📄 Supported CSV Format
Supports broker order history CSV, including:
Date/Time;Symbol;Side;Quantity;Price;Event
Only rows with:
Event = Filled are used.
Includes sample CSV

🎯 Purpose
This project was built to:
  Analyze real trading performance using broker data
  Identify strengths and weaknesses
  Improve decision-making using data-driven insights

🚧 Future Improvements (V2)
  Manual trade entry
  Local storage persistence
  Advanced filtering (ticker, setup, time)
  Setup-based analytics
  Trade tagging system

👤 Author
Ralph Viado
