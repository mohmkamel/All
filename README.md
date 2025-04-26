Featured Stored Procedure: 
+++++++++++++++++++++Sel_Frst_Col
The Sel_Frst_Col stored procedure is designed to dynamically retrieve the first N columns from a specified table in the database. Below is an overview of its functionality:

Parameters:

@TblName (varchar, max): Name of the target table.
@NumCol (int): Number of columns to retrieve (default: 1).
Procedure Details:

Utilizes system views (sys.columns and sys.tables) to identify the target table and its columns.
Dynamically constructs a query based on the specified number of columns and executes it.
Supports flexible column retrieval for use cases requiring partial table data.
Usage Example:

SQL
EXEC [dbo].[Sel_Frst_Col] @TblName = 'your_table_name', @NumCol = 3;
This procedure is particularly useful for scenarios where you need to programmatically access specific columns from a table without hardcoding column names.
