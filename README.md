# QueryHoner

Developing a complicated query requires looking at the data it produces, testing your assumptions about that data, and comparing the data to the source of truth. When, in that process, you find something was amiss about your query, you must iterate on that query and then start the process of validation. This notebook accelerates that process.

## How to structure your query

One of the features of the QueryHoner is that it can iteratively run you query over a longer time period until you have enough data to perform your tests. To enable this feature, your query must include `:days`, which the query will iteratively replace with larger numbers. For example:

```sql
select
    transaction.id,
    transaction.amount,
    transaction.category
from
    transaction
where
    transaction.day > sysdate - :days
```

## My Conda environment

anaconda                  5.0.1   
cx_oracle                 6.0b2           
ipykernel                 4.6.1   
ipython                   6.1.0   
jupyter                   1.0.0   
matplotlib                2.1.0   
notebook                  5.0.0   
numpy                     1.13.3 
pandas                    0.20.3
python                    3.6.3  
scipy                     0.19.1  
seaborn                   0.8.0   
sqlalchemy                1.1.13  
statsmodels               0.8.0 

## Author

Nate Matthews
natezmatthews@gmail.com