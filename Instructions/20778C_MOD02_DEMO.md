# Module 2: Introducing Power BI

- [Module 2: Introducing Power BI](#module-2-introducing-power-bi)
  - [Lesson 1: Power BI](#lesson-1-power-bi)
    - [Demo 1: Creating a Report with Power BI Desktop](#demo-1-creating-a-report-with-power-bi-desktop)
  - [Lesson 2: The Power BI Service](#lesson-2-the-power-bi-service)
    - [Demo 1: Creating an App](#demo-1-creating-an-app)


## Lesson 1: Power BI

### Demo 1: Creating a Report with Power BI Desktop

1. Ensure the **MT17B-WS2016-NAT**, **20778B-MIA-DC** and **20778B-MIA-SQL** virtual machines are running, log on to **20778B-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. In the **D:\\Demofiles\\Mod02** folder, run **Setup.cmd** as Administrator.

3. In the **User Account Control** dialog box, click **Yes**.

4. If prompted to continue this operation, type **Y**, and then press Enter.

5. When the script completes, press any key to close the window.

6. Start **Microsoft SQL Server Management Studio 18**, and connect to the **MIA-SQL** database engine instance using Windows authentication.

7. Open the **Demo.ssmssln** solution in the **D:\\Demofiles\\Mod02\\Demo** folder.

8. In Solution Explorer, expand **Queries**, and then open the **1 - Power BI.sql** script file.

9. On the Taskbar, click **Power BI Desktop**.

10. In the **Welcome to** **Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

11. In the **Sign in** dialog box, enter your account credentials, and then click **Sign in**.

12. In the **Sign in to your account** dialog box, enter your password credentials, and then click **Sign in**.

13. In the **Power BI Desktop** window, click **Get data**.

14. In the **Get Data** dialog box, click **Azure SQL database**, and then click **Connect**.

15. In the **SQL Server database** window, in the **Server** box, type the URL of the Azure server ***\<Server Name\>*.database.windows.net** (where ***\<Server Name\>*** is the name of the server you created), and in the **Database (optional)** box, type **AdventureWorksLT**.

16. Expand **Advanced options**.

17. In SQL Server Management Studio, copy the **1 - Power BI.sql** query to the clipboard.

18. In the Power BI Desktop, in the **SQL statement (optional, requires database)** box, paste the query, and then click **OK**.

19. In the **SQL Server database** window, click **Database**.

20. In the **User name** box, type **Student**.

21. In the **Password** box, type **Pa55w.rd**, and then click **Connect**.

22. In the data preview window, click **Load**.

23. If the **Connection Settings** window appears, leave **Import** selected, and then click **OK**.

24. In the **VISUALIZATIONS** pane, click **Stacked column chart**.

25. In the **FIELDS** pane, under **Query1**, select the **ProductName** and **TotalSales** check boxes. The chart will auto populate. Expand the chart control to horizontally show the full names of the products.

26. In the **VISUALIZATIONS** pane, click **Format**.

27. Expand **Title**, and change the **Title text** value to **Top 10 Selling Products**.

28. Next to **Alignment**, click the **Center** icon.

29. Toggle **Data labels** to be **On**.

30. Expand the **Data colors** list, and choose another color to change the bars on the chart.

31. On the **File** menu, click **Save As**. Name the report **Adventure Works Sales 2**, and save to the **D:\\Demofiles\\Mod02\\Demo** folder.

32. Leave Power BI Desktop and the report open for the next demonstration.

---

## Lesson 2: The Power BI Service

### Demo 1: Creating an App

1. In Power BI Desktop, on the **Home** tab, click **Publish**.

2. In the **Publish to Power BI** dialog box, click **My workspace**, and then click **Select**.

3. The report will be published to the Power BI portal.

4. In the **Publishing to Power BI** dialog box, when the window displays **Success**, click **Open 'Adventure Works Sales 2.pbix' in Power BI** to view the report online.

5. In Internet Explorer, click **SIGN IN**, enter your email address and password, click **Sign in**, and wait for the report to open.

6. When the report is visible, click **Pin Live Page**.

7. In the **Pin to dashboard** dialog box, click **New dashboard**.

8. In the **Dashboard name** box, type **Adventure Works Sales 2**, and then click **Pin live**.

9. Expand **My Workspace**, the dashboard will appear under the **Dashboards** list.

10. Expand **Workspaces**, and then click **Create app workspace**.

11. In the **Workspace** **name** box, type **Adventure Works Sales 2**.

12. In the **Description** box, type **Top 10 selling products**, and then click **Save**.

13. In the **Welcome to the Adventure Works Sales workspace** pane, under **Create new content**, in the **Files** section, click **Get**.

14. Click **Local File**.

15. In the **Choose File to Upload** dialog box, navigate to **D:\\Demofiles\\Mod02\\Demo**, click **Adventure Works Sales 2.pbix**, and then click **Open**.

16. In the left-hand pane, expand **Workspaces**, and then click **Adventure Works Sales 2**.

17. On the toolbar, click **Publish app**.

18. In the **Description** box, type **My top 10 sales app**.

19. Under **App theme color**, click an alternative color, and then click **Publish app**.

20. In the **Adventure Works Sales 2** dialog box, click **Publish**.

21. When the app is successfully published, click **Go to app** and confirm that the app loads.

22. In the left-hand pane, click **Go back**, and then click **Apps**, and confirm that the **Adventure Works Sales 2** app appears in the **Apps** pane.

23. Close Internet Explorer.

24. In the **Publishing to Power BI** dialog box, click **Got it**, and then close Power BI Desktop.

25. Close SQL Server Management Studio, without saving any changes.
