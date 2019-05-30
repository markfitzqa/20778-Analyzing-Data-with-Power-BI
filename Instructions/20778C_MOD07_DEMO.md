# Module 7: Direct Connectivity

- [Module 7: Direct Connectivity](#module-7-direct-connectivity)
  - [Lesson 1: Cloud data](#lesson-1-cloud-data)
    - [Demo 1: Using Azure SQL Database as a Power BI data source](#demo-1-using-azure-sql-database-as-a-power-bi-data-source)
      - [Import data from tables in a database in Azure SQL Database](#import-data-from-tables-in-a-database-in-azure-sql-database)
      - [View relationships between the tables](#view-relationships-between-the-tables)


## Lesson 1: Cloud data

### Demo 1: Using Azure SQL Database as a Power BI data source

#### Import data from tables in a database in Azure SQL Database

1. Ensure that the **MT17B-WS2016-NAT**, **20778C-MIA-DC**, and **20778C-MIA-SQL** virtual machines are running, and then log on to **20778C-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. On the Taskbar, click **Power BI Desktop**.

3. In the **Welcome to Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

4. In the **Sign in** dialog box, enter your account credentials, and then click **Sign in**.

5. In the **Sign in to your account** dialog box, enter your password credentials, and then click **Sign in**.

6. In the **Power BI Desktop** window, click **Get data**.

7. In the **Get Data** dialog box, click **Azure SQL database**, and then click **Connect**.

8. In the **SQL Server database** window, in the **Server** box, type the URL of the Azure server **\<*Server Name*\>.database.windows.net** (where \<*Server Name*\> is the name of the server that you created).

9. In the **Database (optional)** box, type **AdventureWorksLT**, and then click **OK**.

10. In the **SQL Server database** dialog box, on the **Database** tab, in the **User name** box, type **Student**.

11. In the **Password** box, type **Pa55w.rd**, and then click **Connect**.

12. In the **Navigator** dialog box, select the **SalesLT.Customer**, **SalesLT.SalesOrderDetail**, and **SalesLT.SalesOrderHeader** check boxes, and then click **Load**.

13. In the **FIELDS** pane, notice that the three tables have been added. When the report is published to the Power BI service, the tables are combined into a single dataset.

#### View relationships between the tables

1. In the menu on the left, click **Model**, and then increase the size of the **SalesLT SalesOrderDetail**, **SalesLT SalesOrderHeader**, and **SalesLT Customer** tables to display all columns.

2. Position the cursor on the relationship arrow between **SalesLT SalesOrderDetail** and **SalesLT SalesOrderHeader**. Notice that the related columns are highlighted.

3. Position the cursor on the relationship arrow between **SalesLT SalesOrderHeader** and **SalesLT Customer**. Point out that the related columns are highlighted.

4. In the menu on the left, click **Report** to return to the report canvas.

5. In the **FIELDS** pane, expand **SalesLT Customer**, and drag the **CompanyName** field onto the canvas to create a table.

6. In the **FIELDS** pane, expand **SalesLT SalesOrderDetail**, and drag the **LineTotal** field to the table on the report.

7. In the **VISUALIZATIONS** pane, click **Stacked column chart**.

8. Drag the right edge of the chart to stretch it across the report and display the customers in full.

9. In the **VISUALIZATIONS** pane, click **Format**, expand **Title**, and then rename the chart **Line Total by Company Name**.

10. In the **FIELDS** pane, in **SalesLT Customer**, drag the **CompanyName** field onto the canvas to create a table below the chart.

11. In the **FIELDS** pane, in **SalesLT SalesOrderDetail**, drag the **OrderQty** field to the table on the report.

12. In the **VISUALIZATIONS** pane, click **Stacked column chart**.

13. Drag the right edge of the chart to stretch it across the report and display the customers in full.

14. In the **VISUALIZATIONS** pane, click **Format**, expand **Title**, and then rename the chart **Order Quantity by Company Name**.

15. Expand **Data colors**, and then select a different color from the **Default color** selector.

16. Click on the canvas.

17. In the **FIELDS** pane, in **SalesLT Customer**, drag the **CompanyName** field onto the **Page level filters** in the **VISUALIZATIONS** pane.

18. Close Power BI desktop without saving your changes.
