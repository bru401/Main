# Internet Sales Dashboard (AdventureWorks) 
![Dashboard](https://github.com/user-attachments/assets/c2135f1e-9ac8-46c2-89db-ae7a0b17d56b)

## Business problem
We want to build an interactive **sales dashboard** for a hypothetical company to answer common business questions, such as:

- Which **products** are selling the most?  
- Who are the **top customers** and where are they located?  
- How are sales evolving **over time**?  
- How do actual sales compare to the **monthly budget**?

The dashboard should enable business users to quickly monitor performance, spot trends and variances, and filter results by time, product and geography.

---

## Business problem
<p>
We want to build a visual dashboard that reports on <b>internet sales</b> for a hypothetical company. Thus, there is an interest in knowing which <b>products</b> are being sold the most, to to which <b>clients</b> (or where is the clientele), and we want to have this data presented over <b>time</b>. Additionaly, as any company depends on profit, we want to compare those sales to the <b>budget</b> value.
</p>

## Process
<p>
This project is based on Microsoft's sample database "AdventureWorks". We start by bringing the database to SQL Server in order to select the exact tables we need for the project. 
</p>

![SQL](https://github.com/user-attachments/assets/64eac49d-94cd-41d2-a11a-7ae2f77bed51)

<p>
This will be simulation of a sales dashboard, therefore, our main variables of interest will be budget, customers, products and, obviously, sales. The SQL scripts used to make this selection will be in the repository.
</p>
<p>
First, we make sure the data is in the right type. Then, we make sure the schema is correct.
</p>

![Schema](https://github.com/user-attachments/assets/d39e27e9-c581-44bd-9549-a7ad589ea694)

<p>
The Fact tables are used by the dimension tables due to having only numbers, keys, thus avoiding the redundancy of storing multiple copies of the same text (????)
Finally, the dashboard itself. We'll go step by step.
</p>
<p>
Side by side with the title, I've set the filters related to time. On the left side of the dashboard, I've set the filters realted to other variables, such as city and product.
Between these, I've set the main KPI of the dashboard, which tracks the monthly sales as related to budget. (...)  
</p>
