# Pharmacy Database Management System

This repository contains a university project for the database course. It implements a database for a pharmacy, including schema creation, data insertion, and a variety of queries to extract meaningful business insights.

The database is designed to manage inventory, sales, patient records, prescriptions, and employee information.

## Database Technology

The SQL scripts in this project are written for **Oracle Database**.

## Database Schema

<img width="1243" height="552" alt="image" src="https://github.com/user-attachments/assets/04c61357-ff32-4dcc-af62-1dd35deaafd1" />

-   **`PHARMACEUTICAL_FORM`**: Stores different forms of medication (e.g., tablet, syrup, cream).
-   **`PRODUCERS`**: Contains information about drug and product manufacturers.
-   **`ITEMS`**: A master list of all products sold, including drugs, cosmetics, and medical supplies.
-   **`DISEASE`**: A list of diseases for linking recommendations and prescriptions.
-   **`RECOMMENDATIONS`**: Links items to the diseases they can be used to treat.
-   **`PHARMACEUTIST`**: Stores information about the pharmacy's employees.
-   **`PATIENTS`**: Manages patient records, including contact details and purchase history.
-   **`GRN` (Goods Received Note)**: Header table for tracking incoming stock shipments from producers.
-   **`GRN_DETAILED`**: Line items for each `GRN`, detailing specific products received.
-   **`SALES`**: Header table for customer transactions.
-   **`SALES_DETAILED`**: Line items for each sale, detailing products sold.
-   **`PRESCRIPTIONS`**: Manages prescription-specific information linked to a sale.
-   **`PRESCRIPTIONS_DETAILED`**: Details the items included in a prescription.

## Example Queries

The `pharmacy_database.sql` file includes several queries that demonstrate the system's capabilities. These queries answer common business questions, such as:

-   **Financial Reporting**:
    -   What is the total value of goods received from each producer per month?
    -   What are the total payment obligations due by the end of the year?
-   **Inventory Management**:
    -   Which products are set to expire by the end of 2026?
    -   Which items have never been sold?
    -   What is the current inventory count for each item?
    -   Which products have the lowest price?
-   **Sales and Employee Performance**:
    -   What is the total sales value for each patient?
    -   How many sales has each active employee made?
    -   List all sales handled by pharmacists who are no longer active.
-   **Patient and Product Analysis**:
    -   How many products are there for each VAT rate?
    -   Hierarchical query to show patient recommendation chains.
-   **Data Manipulation and Functions**:
    -   Calculate an 8% salary increase for active employees.
    -   Calculate the number of weeks between the current date and payment due dates.
    -   Demonstrate `NULLIF` and `SUBSTR` functions on employee and patient data.
