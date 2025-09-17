![Dashboard](https://github.com/user-attachments/assets/c2135f1e-9ac8-46c2-89db-ae7a0b17d56b)

## Business Problems
<p>
We want to build a visual dashboard that reports on <b>internet sales</b> for a hypothetical company. Thus, there is an interest in knowing which <b>products</b> are being sold the most, to to which <b>clients</b> (or where is the clientele), and we want to have this data presented over <b>time</b>. Additionaly, as any company depends on profit, we want to compare those sales to the <b>budget</b> value.
</p>

## Process (WIP)
<p>
This project is based on Microsoft's sample database "AdventureWorks". We start by bringing the database to SQL Server in order to select the exact tables we need for the project. 
</p>
<p>
This will be simulation of a sales dashboard, therefore, our main variables of interest will be budget, customers, products and, obviously, sales. The SQL scripts used to make this selection will be in the repository.
</p>
<p>
 First, we make sure the data is in the right type.
</p>
After that, we make sure the schema is correct.
<p>
The Fact tables are used by the dimension tables due to having only numbers, keys, thus avoiding the redundancy of storing multiple copies of the same text (????)
Finally, the dashboard itself. We'll go step by step.
</p>
<p>
Side by side with the title, I've set the filters related to time. On the left side of the dashboard, I've set the filters realted to other variables, such as city and product.
Between these, I've set the main KPI of the dashboard, which tracks the monthly sales as related to budget. (...)  
</p>
