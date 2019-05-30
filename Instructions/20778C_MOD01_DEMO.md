# Module 1: Introduction to Self-Service BI Solutions

- [Module 1: Introduction to Self-Service BI Solutions](#module-1-introduction-to-self-service-bi-solutions)
  - [Lesson 2: Introduction to Data Analysis](#lesson-2-introduction-to-data-analysis)
    - [Demo 1: Importing Data with Power BI Desktop](#demo-1-importing-data-with-power-bi-desktop)
  - [Lesson 3: Introduction to Data Visualization](#lesson-3-introduction-to-data-visualization)
    - [Demo 1: Visualizing Data with Power BI Desktop](#demo-1-visualizing-data-with-power-bi-desktop)
  - [Lesson 6: Microsoft Tools for Self-Service BI](#lesson-6-microsoft-tools-for-self-service-bi)
    - [Demo 1: Publishing a Report to the Power BI Service](#demo-1-publishing-a-report-to-the-power-bi-service)


## Lesson 2: Introduction to Data Analysis

### Demo 1: Importing Data with Power BI Desktop

1. Ensure that the **MT17B-WS2016-NAT**, **20778C-MIA-DC**, and **20778C-MIA-SQL** virtual machines are running, and then log on to **20778C-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. In the **D:\\Demofiles\\Mod01** folder, run **Setup.cmd** as **Administrator**.

3. In the **User Account Control** dialog box, click **Yes**.

4. If prompted to continue this operation, type **Y**, and then press Enter.

5. When the script completes, press any key to close the window.

6. If you do not have a Power BI login, open Internet Explorer, go to **https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-signing-up-for-power-bi-with-a-new-office-365-trial**, and follow the steps to create an account.

7. On the desktop, double-click **Power BI Desktop**.

8. In the **Welcome to Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

9. In the **Sign in** dialog box, enter your credentials, and then click **Sign in**.

10. In the **Sign in to your account** dialog box, enter your credentials, and then click **Sign in**.

11. On the **Power BI Desktop** screen, click **Get data**.

12. In the **Get Data** dialog box, click **SQL Server database**, and then click **Connect**.

13. In the **SQL Server database** dialog box, in the **Server** box, type **MIA-SQL**.

14. In the **Database (optional)** box, type **AdventureWorksDW**, and then click **OK**.

15. In the **SQL Server database** dialog box, leave the default settings unchanged, and then click **Connect**.

16. In the **Encryption Support** dialog box, click **OK**.

17. In the **Navigator** dialog box, select the **FactInternetSales** check box.

18. Click **Select Related Tables**, and then click **Edit**.

19. If the **Connection Settings** dialog box appears, leave **Import** selected, and then click **OK**.

20. In the **Untitled - Power Query Editor** window, in the **Queries** pane, click **FactInternetSales**.

21. Right-click the **CarrierTrackingNumber** column, and click **Remove**.

22. Right-click the **CustomerPONumber** column, and click **Remove**.

23. In the **Queries** pane, click **DimCustomer**.

24. Right-click the **Title** column, and click **Remove**.

25. Right-click the **NameStyle** column, and click **Remove**.

26. Right-click the **Suffix** column, and click **Remove**.

27. Right-click the **MaritalStatus** column, and click **Replace Values**.

28. In the **Replace Values** dialog box, in the **Value To Find** box, type **M**.

29. In the **Replace With** box, type **Married**, and then click **OK**.

30. Right-click the **MaritalStatus** column, and click **Replace Values**.

31. In the **Replace Values** dialog box, in the **Value To Find** box, type **S**.

32. In the **Replace With** box, type **Single**, and then click **OK**.

33. Right-click the **Gender** column, and click **Replace Values**.

34. In the **Replace Values** dialog box, in the **Value To Find** box, type **F**.

35. In the **Replace With** box, type **Female**, and then click **OK**.

36. Right-click the **Gender** column, and click **Replace Values**.

37. In the **Replace Values** dialog box, in the **Value To Find** box, type **M**.

38. In the **Replace With** box, type **Male**, and then click **OK**.

39. On the **Home** menu, click **Close & Apply**.

40. Wait until the data has successfully loaded.

41. In the **FIELDS** pane, expand **FactInternetSales**, and then click **SalesAmount**.

42. On the **Modeling** tab, in the **Formatting** group, click **Format: Currency general**, point to **Currency**, and then click **$ English (United States)**.

43. In the **FIELDS** pane, right-click **DimCustomer**, and then click **New column**.

44. In the formula bar, type **FullName = DimCustomer[FirstName] & " " & DimCustomer[LastName]**, and then press Enter.

45. On the **File** menu, click **Save**. Name the file **Adventure Works Sales**, and save the file to **D:\\Demofiles\\Mod01**.

46. Leave Power BI Desktop open for the next demonstration.

---

## Lesson 3: Introduction to Data Visualization

### Demo 1: Visualizing Data with Power BI Desktop

1. In Power BI Desktop, in the **FIELDS** pane, under **DimCustomer**, select **Gender**, and **MaritalStatus**.

2. Under **FactInternetSales**, select **SalesAmount**.

3. In the **VISUALIZATIONS** pane, click **Clustered column chart**. 

4. Click **Format**, expand **Title**, and then change the **Title text** to **Sales by Gender and Marital Status**.

5. Change **Alignment** to **Center**.

6. In the **FIELDS** pane, expand **DimProduct**, and drag the **Color** field onto the report canvas to create a new table.

7. Under **FactInternetSales**, drag the **OrderQuantity** field onto the new table.

8. In the **VISUALIZATIONS** pane, click **Donut chart**.

9. Click **Format**, and then expand **Title**.

10. Change the **Title text** to **Orders by Color**.

11. Change **Alignment** to **Center**.

12. In the **FIELDS** pane, under **FactInternetSales**, drag the **SalesAmount** field onto the report canvas to create a new column chart.

13. In the **VISUALIZATIONS** pane, click **Fields**.

14. In the **FIELDS** pane, expand **DimDate**, and drag the **EnglishMonthName** to the **Axis** property.

15. Grab the resizer on the column chart to widen the chart so that the month names display clearly.

16. In the **VISUALIZATIONS** pane, click **Format**, and then expand **Title**.

17. Change the **Title text** to **Sales by Month**.

18. Change **Alignment** to **Center**.

19. On the **File** menu, click **Save**.

20. Leave Power BI Desktop open for the next demonstration.

---

## Lesson 6: Microsoft Tools for Self-Service BI

### Demo 1: Publishing a Report to the Power BI Service

1. In Power BI Desktop, on the **Home** tab, click **Publish**.

2. If you are prompted to save your changes, click **Save**.

3. In the **Publish to Power BI** dialog box, ensure that **My workspace** is selected, and then click **Select**.

4. The report will then be published to the Power BI portal. When the window displays **Success**, click **Open 'Adventure Works Sales.pbix' in Power BI** to view the report online. 

5. When the browser opens, if you are prompted to Sign in, click **SIGN IN**, and then enter your Power BI credentials, enter your email address and password, and wait for the report to open.

6. On the **Sales by Gender and Marital Status** column chart, click **Pin visual**.

7. In the **Pin to dashboard** dialog box, click **New dashboard**, type **Adventure Works Sales 1**, and then click **Pin**.

8. On the **Orders by Color** donut chart, click **Pin visual**.

9. In the **Pin to dashboard** dialog box, click **Existing dashboard** , in the list click **Adventure Works Sales 1**, and then click **Pin**.

10. On the **Sales by Month** column chart, click **Pin visual**.

11. In the **Pin to dashboard** dialog box, click **Existing dashboard**, in the list click **Adventure Works Sales 1**, and then click **Pin**.

12. In the left menu, expand **My Workspace**, and then under **Dashboards**, click **Adventure Works Sales 1**.

13. Drag the lower-right corner of the **Sales by Month** column chart, and expand it so it is as wide as the two charts above it.

14. Close Internet Explorer.

15. In the **Publishing to Power BI** dialog box, click **Got it**.

16. Close Power BI Desktop.
