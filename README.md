# ETL_project

In this project i downloaded data from https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases as CSV files. the data include number of confirmed case of COVID-19 and the number of death in each country. 

I trannsfer the death data to tables (deaths_us and deaths_global ) in PstgreSQL database .
the first challenge was to create view (death_all) to union global and us data and create another view to have data group by country
( death_all_groupbycountry ) .

next step is to merge confirmed case data ( readed from CSV file ) and number death data (from sql database) .
The result was a new dataframe include the whole data.

the second challenge was to sort data in datafrme by column . 
After doing that now i had soretd data by country name and columns.(X columns are number of comfirmed case and y columns are number of death)

As data are adding by column daily for these kind of data, it is better to use Mongodb instead of PostgreSQL as database.