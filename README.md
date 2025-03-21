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

+ Snowflake account with appropriate access permissions
+ Streamlit in Snowflake enabled for your account
+ A metadata table for storing requests (see Setup section)
+ Email integration configured in Snowflake (for notifications)

# Setup
# 1. Run the Setup SQL Script
Before using the application, you need to set up the required database objects and permissions. A SQL setup script (setup.sql) is provided in this repository that creates:

+ A metadata table to store masking requests
+ Email notification integration
+Required permissions for the application

Review and modify the script as needed for your environment before executing it in Snowflake.

# 2. Configure Permissions
Ensure the user running the application has the necessary privileges to:

+ Access the databases, schemas, and tables they need to view
+ Insert records into the metadata table
+ Use the email notification integration

# 3. Deploy the Application
Deploy this application through Streamlit in Snowflake:

1. Navigate to Snowsight
2. Go to Streamlit
3. Create a new Streamlit app
4. Copy the code from this repository into your new app
5. Save and run the application

# Usage

1. Log in to Snowflake and navigate to the Streamlit app
2. Select the database, schema, and table containing sensitive columns
3. Check the boxes next to columns that need masking
4. Click "Generate Masking Request"
5. Review the request details
6. Click "Submit" to send the request to the database team

# Security Considerations

+ This application operates with the permissions of the logged-in user
+ Make sure users have appropriate access to the tables they need to view
+ The metadata table should have appropriate access controls
+ Email notifications contain basic information about the request (not sensitive data)

# Customization
You can customize this application by:

+ Modifying the metadata table structure to capture additional information
+ Changing the email template for notifications
+ Adding approval workflows
+ Implementing additional validation logic

# Troubleshooting

+ If you encounter connection issues, ensure you're running the app within Snowflake Streamlit
+ For email notification failures, verify that the email integration is properly configured
+ If requests aren't being saved, check permissions on the metadata table
