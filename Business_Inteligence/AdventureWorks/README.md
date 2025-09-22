# Internet Sales Dashboard (AdventureWorks) 
![Dashboard](https://github.com/user-attachments/assets/9845983e-87f2-47c7-b746-9666d7ee3d2a)

## Business problem
We want to build an interactive **sales dashboard** for a hypothetical company to answer common business questions, such as:

- Which **products** are selling the most?  
- Who are the **top customers** and where are they located?  
- How are sales evolving **over time**?  
- How do actual sales compare to the **monthly budget**?

The dashboard should enable business users to quickly monitor performance, spot trends and variances, and filter results by time, product and geography.

---

## Data source
This project uses Microsoft's sample database **AdventureWorks** as the source of sales, product and customer data. The dataset is loaded into **SQL Server** and then queried to extract only the tables and fields required for the dashboard.

---

## Process
![SQL](https://github.com/user-attachments/assets/64eac49d-94cd-41d2-a11a-7ae2f77bed51)
<p>
We start by bringing the database to SQL Server in order to select the exact tables we need for the project. 
</p>
<p>
This will be simulation of a sales dashboard, therefore, our main variables of interest will be **budget**, **customers**, **product** and, obviously, **sales**. With simple SQL scripts, such as the one pictured, we are able to selectively produce four .csv files for our purposes: DIM_Calendar, DIM_Customers, DIM_Product and FACT_InternetSales (the budget file was manually created by me for the purposes of this exercise). The SQL scripts will be in the repository.
</p>

![Schema](https://github.com/user-attachments/assets/d39e27e9-c581-44bd-9549-a7ad589ea694)

<p>
After making sure the columns are sorted into the right types of data, we make sure the schema is correct. The arrangement pictured means that the sales and budget tables have items that refer to only *one* date, customer and product, while simultaneously one of these, such as a particular customer, may refer to multiple sales, representing the fact that one person might make multiple purchases throughout time.
</p>

![SQL](https://github.com/user-attachments/assets/64eac49d-94cd-41d2-a11a-7ae2f77bed51)

<p> Finally, the dashboard itself. We'll go step by step. This is a repeat of the first image, the main page of the dashboard, for reference.
</p>
<p>
Side by side with the title, I've set the filters related to time, while beneath the title, on the left side of the dashboard, I've set the filters related to other important variables, such as city and product.
</p>
<p>
Between these, I've set the main KPI of the dashboard, which tracks the monthly sales as related to budget (which is also calculated monthly). It is set to flip from green to red when the budget exceeds the sales and to show the exact percentage of diference  
</p>
<p>
Beneath the KPI, we have a large line graph displaying sales against budget throughout time. The graph can be drilled either up or down, to show the passage of time from years to days (thougn, again, the budget changes only monthly). Additionaly, at the right side we have a bar graph that neatly compares the two variables in a more condensed manner. As it is, it lacks data for any meaningful analysis, but it should work for a quick comparison between years.
</p>
<p>
At the right side with a global map that hightlights the cities with the highest values of total sales, marked by the larger bubbles. It is a convenient way of selecting the most relevant cities that will come handy later. 
</p>
<p>
Finally, we have a simple and direct table with the sales and budget values monthly (as related to the selected year on the bar above the dashboard) 
</p>

![Dashboard](https://github.com/user-attachments/assets/f18ddc27-977c-40b0-ad18-2ea90145155f)

<p>
This is the product page of the dashboard, where the presentation favors information related to the product table. 
</p>
<p>
Aside from the familiar parts, the line graph is replaced by a detailed matrix with all of the specific product (category and sub category) sales values throughout time. Above it, another handy bar chart for quickly copnveying information on the relative values between product categories and their subcategories. I've also added a small line graph, as to retain some information related to budget. 
</p>
<p>
On the right side, the familiar map gain a companion line graph. It defaults to the city with the highest sales (London), but displays the values through time for any city that is selected on the map or on the bar at the left side of the dashboard.
</p>

![Dashboard](https://github.com/user-attachments/assets/e4d5d845-b0c5-4f2b-b498-018d26de5d9d)

<p>
This is the client page of the dashboard, where the presentation favors information related to the client table. 
</p>
<p>
It follows the same format as the product page, with the large matrix at the center displaying each customer within their respective cities, with the values of their total purchases (sales). Additionaly, we have added a graph displaying the 10 clients that buy the most from the hypothetical company. 
</p>
<p>
With these, hopefully all of the questions raised at the start can be answered given the data provided. Thank you for your time reading this!
</p>

---

## Notes & credits
- Data: Microsoft AdventureWorks sample database.  
- Tools: SQL Server, Power BI Desktop, Python (for ad-hoc cleaning if needed).  
- SQL scripts and the Power BI file are included in this repository.
