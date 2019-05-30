# Module 8: The Developer API Development with Power BI

- [Module 8: The Developer API Development with Power BI](#module-8-the-developer-api-development-with-power-bi)
  - [Lesson 1: The Power BI API](#lesson-1-the-power-bi-api)
  - [Lesson 2: Custom Visuals](#lesson-2-custom-visuals)
    - [Demo 1: Importing and Using a Custom Visual](#demo-1-importing-and-using-a-custom-visual)
      - [Import a Custom Visualization](#import-a-custom-visualization)
      - [Use a Custom Visualization](#use-a-custom-visualization)


## Lesson 1: The Power BI API 

### Demo 1: Using the Power BI Embedded Playground

1. Start the **MT17B-WS2016-NAT**, **20778B-MIA-DC**, and **20778B-MIA-SQL** virtual machines, and then log on to **20778B-MIA-SQL** as **Student** with the password **Pa55w.rd**.

2. In Internet Explorer, go to **https://microsoft.github.io/PowerBI-JavaScript/demo/v2-demo/index.html**.

3. Under **Sample Report**, click **Select**.

4. In the **Embed** pane, review the default options.

5. In the **Code** pane, review the code to embed the report, and then click **Run**.

6. In the **Log** pane, review the events listed, and then in the **Embedded view** pane, review the report.

7. In the **Region** section of the report, click **East**, and wait for the report to update showing on the results for the East region.

8. On the right-hand side of the report above **FILTERS**, click the expand arrow.

9. Expand **Month**, and then select **Jan-14**. Note that the report updates to show only data in the East region in January 2014.

10. Review the events list in the **Log** pane again.

11. In the **Interact** pane, expand **Data**, and then click **Export visual data summarized**.

12. In the **Code** pane, click **Run**.

13. Review the data returned to the **Log** pane.

14. In the left-hand menu, click **Sample tool**.

15. Under **Sample Q&A**, click **Select**.

16. In the **Embed** pane, review the default options.

17. In the **Code** pane, review the code to embed the Q&A element, and then click **Run**.

18. In the **Embedded view** pane, review the question and the answer.

19. Change the last variable in the question to **clustered bar chart**, and then review the change to the answer.

20. Close Internet Explorer.

---

## Lesson 2: Custom Visuals

### Demo 1: Importing and Using a Custom Visual

#### Import a Custom Visualization

1. Log on to **20778B-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. In Internet Explorer, go to **https://app.powerbi.com/visuals**.

3. In the **Search Microsoft AppSource** box, type **Aster Plot**, and then press Enter.

4. In the **Aster Plot** visual, click **Get it now**.

5. In the **Sign in to Microsoft AppSource** dialog box, enter the credentials you used to sign up for Power BI service, and then click **Sign in**.

6. If the **One more thing** dialog box appears, click **Continue**.

7. On the **Office Store** page, click **Download for Power BI**.

8. In the message box, click **Save**, and download the visual to a folder on your local machine.

9. On the Taskbar, click **Power BI Desktop**.

10. In the **Welcome to** **Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

11. In the **Sign in** dialog box, enter your account credentials, and then click **Sign in**.

12. In the **Sign in to your account** dialog box, enter your password credentials, and then click **Sign in**.

13. In the **Power BI Desktop** window, click **Open other reports**.

14. In the **Open** dialog box, browse to **D:\\Demofiles\\Mod08\\Demo**, click **Adventure Works Sales.pbix**, and then click **Open**.

15. If the **Introducing Q&A** dialog box appears, click **Got it**.

16. In the **VISUALIZATIONS** pane, click the ellipsis (**...**), and then click **Import from file**.

17. In the **Caution: Import custom visual** dialog box, click **Import**.

18. In the **Open** dialog box, browse to the location where you saved Aster Plot, click **AsterPlot.x.x.x.x.pbiviz**, and then click **Open**.

19. In the **Import custom visual** dialog box, click **OK**.

#### Use a Custom Visualization

1. In the **Report** view, at the bottom of the page, click the **Company Report** tab.

2. Click the **Line Total by Company Name** visual.

3. In the **Visualizations** pane, click the **Aster Plot** icon. Data that was previously displayed using the **Clustered column chart** is now displayed in the **Aster Plot** visualization.

4. Close Power BI Desktop, without saving any changes, and then close Internet Explorer.
