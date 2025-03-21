# Snowflake Column Masking Request Portal 🔒
A Streamlit application for submitting and managing requests to apply masking policies to sensitive data columns in Snowflake.

# Overview
The Snowflake Column Masking Request Portal provides a user-friendly interface for data users to request masking policies for sensitive data columns in Snowflake tables. This application streamlines the process of identifying and documenting columns that require data protection, facilitating compliance with data privacy requirements.

# Features

  Database Navigation: Browse through databases, schemas, and tables in your Snowflake account
  Column Selection: Easily select columns that need masking policies applied
  Request Generation: Automatically generate structured masking requests with unique identifiers
  Request Submission: Submit requests directly to a metadata table for tracking
  Email Notifications: Send automated email notifications to the database team when new requests are submitted
  Export Capability: Download request details as CSV files for record-keeping

# How It Works

1. Users select a database, schema, and table from dropdown menus
2. The application displays all columns in the selected table with their data types
3. Users check the columns that require masking
4. The application generates a unique request ID and prepares the submission
5. Once submitted, the request is stored in a metadata table and an email notification is sent

# Requirements

-> Snowflake account with appropriate access permissions
-> Streamlit in Snowflake enabled for your account
-> A metadata table for storing requests (see Setup section)
* Email integration configured in Snowflake (for notifications)

