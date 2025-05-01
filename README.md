# Elevate_Labs-Internship-Day-7
Task 7: Basic Sales Summary using SQLite and Python
Objective
This task was given as part of a **Data Analyst Internship**. The goal was to:
- Create a small SQLite database
- Write SQL queries inside Python to get basic sales insights
- Display the output using `print()` and a simple bar chart with `matplotlib`



Tools Used
- Python
- SQLite (via `sqlite3`)
- Pandas
- Matplotlib



Files in This Repository
- `sales_data.db` — The SQLite database file
- `sales_summary.py` — Main Python script for querying and visualizing data
- `sales_chart.png` — Bar chart showing revenue by product
- `README.md` — This file



What I Did
1. Created a `sales` table in `sales_data.db` with fields: `product`, `quantity`, and `price`
2. Inserted sample data for a few products
3. Ran the following SQL query using Python:

   ```sql
   SELECT product, 
          SUM(quantity) AS total_qty,
          SUM(quantity * price) AS revenue
   FROM sales
   GROUP BY product;
