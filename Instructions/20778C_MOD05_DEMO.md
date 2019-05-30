# Module 5: Modeling Data

- [Module 5: Modeling Data](#module-5-modeling-data)
  - [Lab: Modeling Data](#lab-modeling-data)
    - [Lesson 1: Relationships](#lesson-1-relationships)
      - [Demo 1: Working with Relationships in Power BI](#demo-1-working-with-relationships-in-power-bi)
    - [Lesson 2: DAX Queries](#lesson-2-dax-queries)
      - [Demo 1: Using Row and Filter Context in DAX Formulas](#demo-1-using-row-and-filter-context-in-dax-formulas)
    - [Lesson 3: Calculations and Measures](#lesson-3-calculations-and-measures)
      - [Demo 1: Creating Calculated Columns and Measures with DAX](#demo-1-creating-calculated-columns-and-measures-with-dax)


## Lab: Modeling Data

### Lesson 1: Relationships

#### Demo 1: Working with Relationships in Power BI

1. Ensure the **MT17B-WS2016-NAT**, **20778B-MIA-DC** and **20778B-MIA-SQL** virtual machines are running, log on to **20778B-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. In the **D:\\Demofiles\\Mod05** folder, run **Setup.cmd** as Administrator.

3. In the **User Account Control** dialog box, click **Yes**.

4. If prompted to continue this operation, type **Y**, and then press Enter.

5. When the script completes, press any key to close the window.

6. On the Taskbar, click **Power BI Desktop**.

7. In the **Welcome to** **Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

8. In the **Sign in** dialog box, enter your account credentials, and then click **Sign in**.

9. In the **Power BI Desktop** window, click **Get data**.

10. In the **Get Data** dialog box, click **Excel**, and then click **Connect**.

11. In the **Open** dialog box, navigate to **D:\\Demofiles\\Mod05\\Demo**, click **Adventure Works Sales Data.xlsx**, and then click **Open**.

12. In the **Navigator** dialog box, select the **DimCurrency**, **DimCustomer**, **DimDate**, **DimProduct**, **DimPromotion**, **DimSalesTerritory**, and **FactInternetSales** check boxes, and then click **Load**.

13. In the views pane on the left-hand side, click **Model**.

14. Point out that Power BI has created the relationships automatically. The layout represents a star schema.

15. Maximize the tables in the relationship diagram to display all columns.

16. Point out that Power BI has not created a relationship to **DimDate** from **FactInternetSales**.

17. On the **Home** tab, click **Manage Relationships**.

18. In the **Manage relationships** dialog box, click **New**.

19. In the **Create relationship** dialog box, in the top table list, click **FactInternetSales**. When the table preview appears below, click the **OrderDateKey** column.

20. In the bottom table list, click **DimDate**. When the table preview appears below, click the **DateKey** column.

21. Check that the **Cardinality** is set to **Many to one (*:1)**, the **Cross filter direction** is **Single**, and **Make this relationship active** is selected, and then click **OK**.

22. In the **Manage relationships** dialog box, click **Close**.

23. In the diagram, in the **FactInternetSales** table, click the **DueDateKey** column. Drag the **DueDateKey** column to the **DateKey** column in the **DimDate** table. Point out the dotted line to show that the relationship is inactive. This is because there is more than one related column in the two tables.

24. In the diagram, in the **FactInternetSales** table, click the **ShipDateKey** column. Drag the **ShipDateKey** column to the **DateKey** column of the **DimDate** table. Point out the dotted line to show that the relationship is inactive.

25. Point out that the relationships from **FactInternetSales** to **DimCurrency**, **DimProduct**, **DimPromotion**, and **DimSalesTerritory**, have a cross filter direction of **Single**, indicated by the single arrow icon. These are lookup tables, so should be Single.

26. On the **Home** tab, click **Manage Relationships**.

27. In the **Manage relationships** dialog box, double-click the **FactInternetSales (CurrencyKey)** relationship.

28. In the **Edit relationship** dialog box, in the **Cross filter direction** list, ensure **Single** is selected, and then click **OK**.

29. In the **Manage relationships** dialog box, double-click the **FactInternetSales (ProductKey)** relationship.

30. In the **Edit relationships** dialog box, in the **Cross filter direction** list, ensure **Single** is selected, and then click **OK**.

31. In the **Manage relationships** dialog box, double-click the **FactInternetSales (PromotionKey)** relationship.

32. In the **Edit relationships** dialog box, in the **Cross filter direction** list, ensure **Single** is selected, and then click **OK**.

33. In the **Manage relationships** dialog box, double-click the **FactInternetSales (SalesTerritoryKey)** relationship.

34. In the **Edit relationships** dialog box, in the **Cross filter direction** list, ensure **Single** is selected, and then click **OK**.

35. In the **Manage relationships** dialog box, click **Close**.

36. Click the relationship line between **FactInternetSales** and **DimCustomer**. Point out that this is a one to one relationship because the FactInternetSales table only contains an extract. Normally this would be many to one. This must be changed so it is ready for the remainder of the data to be loaded later.

37. Right-click the relationship line between **FactInternetSales** and **DimCustomer**, and then click **Delete**.

38. In the **Delete Relationship** dialog box, click **Delete**.

39. On the **Home** tab, click **Manage Relationships**.

40. In the **Manage relationships** dialog box, click **New**.

41. In the **Create relationship** dialog box, in the top table list, click **FactInternetSales** and in the data preview, click the **CustomerKey** column.

42. In the bottom table list, click **DimCustomer**, and in the data preview, click **CustomerKey**.

43. In the **Cardinality** list, click **Many to one (*:1)**, and then click **OK**.

44. In the **Manage relationships** dialog box, click **Close**.

45. In the diagram, point out that the relationship icon next to **FactInternetSales** is now a star icon.

46. On the **File** menu, click **Save**, and save the file to the **D:\\Demofiles\\Mod05\\Demo** folder as **Adventure Works Sales 5.pbix**.

47. Leave Power BI Desktop open for the next demonstration.

---

### Lesson 2: DAX Queries

#### Demo 1: Using Row and Filter Context in DAX Formulas

1. In Power BI Desktop, in the Views list on the left side of the window, click **Report**.

2. In the **FIELDS** pane, right-click **FactInternetSales**, and then click **New measure**.

3. In the formula bar, highlight **Measure =**, type the following script, and then press Enter:
    ```
    TotalSales = SUM(FactInternetSales[SalesAmount])
    ```

4. In the **FIELDS** pane, right-click **FactInternetSales**, and then click **New column**.

5. In the formula bar, highlight **Column =**, type the following script:
    ```
    European Sales = CALCULATE(FactInternetSales[TotalSales], DimSalesTerritory[SalesTerritoryGroup] = "Europe")
    ```

6. Point out that the **TotalSales** measure has been used in the formula, and then press Enter.

7. In the **FIELDS** pane, select the **European Sales** check box to add it to the report.

8. In the **VISUALIZATIONS** pane, click **Gauge**, and then click **Format**.

9. Expand **Gauge axis**, in the **Max** box, type **1000000**, and in the **Target** box, type **1000000**.

10. Leave Power BI open for the next demonstration.

---

### Lesson 3: Calculations and Measures

#### Demo 1: Creating Calculated Columns and Measures with DAX

1. In Power BI Desktop, in the view pane, click **Data** to open the data view.

2. In the **FIELDS** pane, click **DimCustomer** to select the table, and preview the data.

3. Right-click **DimCustomer**, and click **New column**.

4. In the formula bar, highlight **Column =**, type the following script, and then press Enter:
    ```
    FullName = [FirstName] & " " & [LastName]
    ```

5. If the new column is not visible, scroll to the right of the table. Note the new **FullName** column in the table.

6. In the **FIELDS** pane, point out the icon next to the new column, which indicates that this has been created using a DAX formula.

7. In the **FIELDS** pane, right-click **DimCustomer**, and then click **New column**.

8. In the formula bar, highlight **Column =**, type the following script, and then press Enter:
    ```
    MaleFemale = IF([Gender] = "M", "Male", "Female")
    ```

9. Note the new column at the end of the table.

10. On the **Modeling** tab, in the **Calculations** group, click **New Column**.

11. In the formula bar, highlight **Column =**, type the following script, and then press Enter:
    ```
    Relationship = IF([MaritalStatus] = "M", "Married", "Single")
    ```

12. Note the new column at the end of the table.

13. On the **Modeling** tab, in the **Calculations** group, click **New Table**.

14. In the formula bar, highlight **Table =**, type the following script, and then press Enter:
    ```
    DimCountry = DATATABLE ("Country", STRING, "Code", STRING,{{"United States", "US"},{"United Kingdom", "UK"},{"France", "FR"},{"Germany", "DE"},{"Spain", "ES"}})
    ```

15. In the **FIELDS** pane, note the new table.

16. On the **Modeling** tab, in the **Calculations** group, click **New Measure**.

17. In the formula bar, highlight **Measure =**, type the following script, and then press Enter:
    ```
    MostRecentOrder = MAX(FactInternetSales[OrderDateKey])
    ```

18. In the **FIELDS** pane, note the icon next to the measure, to indicate that this is a calculated field.

19. In the **FIELDS** pane, click the **MostRecentOrder** field.

20. On the **Modeling** tab, in the **Properties** group, click **Home Table: DimCountry**, and click **FactInternetSales**. This moves the measure so that it resides in the **FactInternetSales** table.

21. In the **FIELDS** pane, note that the **MostRecentOrder** measure now appears under **FactInternetSales**.

22. Close Power BI Desktop, saving any changes.
