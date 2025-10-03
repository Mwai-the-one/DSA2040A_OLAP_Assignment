🍪 Mini OLAP System with SQLite and Pandas
Overview

This project demonstrates how to build a mini OLAP system in Python using SQLite and Pandas inside Jupyter Notebook. It is designed as a learning project to explore how OLAP systems work, particularly the differences between:

ROLAP (Relational OLAP) – working directly with SQL queries on relational data

MOLAP (Multidimensional OLAP) – working with pivot tables and in-memory analytics in Pandas

HOLAP (Hybrid OLAP) – combining relational queries with in-memory summaries

The project also includes demonstrations of the core OLAP operations:

Slice → Fixing one dimension, such as looking only at shipments in January

Dice → Applying multiple filters, such as January shipments to California

Roll-Up → Aggregating data from detailed levels to summaries, such as sales by state

Drill-Down → Going from summary data to more detailed levels, such as sales by state broken down into city

The dataset is simulated and represents a small cookie shop with Customers, Orders, and Shipments.

Project Structure

The repository contains:

README.md (this file)

Jupyter Notebook with the full OLAP demo

SQLite database file, created automatically when the notebook runs

Source data for customers, orders, and shipments

Setup Instructions

Clone the repository from GitHub to your computer.

Install Python libraries including Pandas, SQLite, Matplotlib, Seaborn, and Jupyter Notebook.

Open the Jupyter Notebook and run the cells step by step.

Workflow

Step 1. Connect to SQLite
A connection to the SQLite database is established.

Step 2. Load Data
Three datasets are created as Pandas DataFrames:

Customers (customer details such as name, phone, city, state)

Orders (order details including date, amount, and cookie type)

Shipments (shipment details including shipment date, delivery date, and shipping method)

Step 3. Save to SQLite
The DataFrames are saved into the SQLite database as tables called Customers, Orders, and Shipment.

Step 4. OLAP with SQL (ROLAP)
SQL queries are written to:

Calculate monthly sales totals

Identify the states with the highest number of shipments

Find the buying months of Alice and Bob

Step 5. OLAP with Pandas (MOLAP)
Pivot tables and visualizations are created in Pandas to:

Show cookie sales per month

Plot bar charts for revenue by state

Draw heatmaps to compare cookie sales across months

Step 6. HOLAP (Hybrid OLAP)
Hybrid OLAP is demonstrated by:

Fetching detailed data from SQLite with SQL queries

Building aggregated summaries in Pandas for faster in-memory analysis

Step 7. OLAP Operations

Slice: Total shipments in January

Dice: Total shipments in January to California

Roll-Up: Sales summarized by state

Drill-Down: Sales detailed by state and city

Sample Outputs

Some of the outputs include:

Bar chart showing total sales per state

Heatmap showing monthly cookie sales by type

Pivot table summarizing orders per cookie type across months

Learning Outcomes

By following this project, you will learn:

How to connect Pandas with SQLite.

How to implement ROLAP, MOLAP, and HOLAP.

How to write SQL queries for OLAP-style analysis.

How to use Pandas pivot tables for multidimensional analysis.

How to apply the four OLAP operations: Slice, Dice, Roll-Up, and Drill-Down.

How to visualize OLAP results using Matplotlib and Seaborn.

Recommended Learning Resources

YouTube: OLAP Operations Explained

YouTube: SQLite with Python (Corey Schafer)

YouTube: Pivot Tables with Pandas

Contribution

This repository is intended as a teaching and demonstration project. You are welcome to fork the project, improve the SQL queries, or extend it with more OLAP features.

License

This project is open source
