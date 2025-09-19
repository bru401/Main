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
This project is based on Microsoft's sample database "AdventureWorks". We start by bringing the database to SQL Server in order to select the exact tables we need for the project. 
</p>
<p>
This will be simulation of a sales dashboard, therefore, our main variables of interest will be **budget**, **customers**, **product** and, obviously, **sales**. The SQL scripts used to make this selection will be in the repository.
</p>
<p>
First, we make sure the data is in the right type. Then, we make sure the schema is correct.
</p>

![Schema](https://github.com/user-attachments/assets/d39e27e9-c581-44bd-9549-a7ad589ea694)

<p>
(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)(WIP)
The Fact tables are used by the dimension tables due to having only numbers, keys, thus avoiding the redundancy of storing multiple copies of the same text (????)
Finally, the dashboard itself. We'll go step by step.
</p>
<p>
Side by side with the title, I've set the filters related to time. On the left side of the dashboard, I've set the filters realted to other variables, such as city and product.
Between these, I've set the main KPI of the dashboard, which tracks the monthly sales as related to budget. (...)  
</p>

![Dashboard](https://github.com/user-attachments/assets/f18ddc27-977c-40b0-ad18-2ea90145155f)

![Dashboard](https://github.com/user-attachments/assets/e4d5d845-b0c5-4f2b-b498-018d26de5d9d)

---

## Notes & credits
- Data: Microsoft AdventureWorks sample database.  
- Tools: SQL Server, Power BI Desktop, Python (for ad-hoc cleaning if needed).  
- SQL scripts and the Power BI file are included in this repository.
