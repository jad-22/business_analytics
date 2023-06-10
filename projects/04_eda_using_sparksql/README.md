# 04. World Cup Data Exploration using Spark SQL

### Data Source

Credit to matj42 for the football matches dataset. Data can be found in his github repository ([source link](https://github.com/martj42/international_results))

### Objectives

The idea behind this is to showcase my SQL level, which by no means is advanced but sufficiently capable of handling most data explorations and queries.
We further utilise Spark to explore the potential to integrate SQL queries via spark and data processing and analysis in pandas.

![football_matches_across_years](https://github.com/jad-22/business_analytics/blob/main/projects/04_eda_using_sparksql/04_football_across_years.png)

### Takeaways

Although the dataset used in our case was small, SparkSQL is definitely a useful tool in working with big data, connecting our expertise in SQL with pandas capabilities.
We have also answered some questions that we initially set out with:

1. How many FIFA matches have been held so far?
   * 7.7k qualifier matches beginning 1933
   * 948 world cup matches beginning 1930, no qualifier matches when FIFA first started

2. Which teams qualified, hence participated the most in FIFA?
   * Brazil, Argentina and Mexico are the top 3 most frequently participating teams 
   * With average scores per match 2.37, 2.06 and 1.88 respectively
   
3. Which teams are the top performing teams?
   * In terms of winning matches, Brazil, Germany and Argentina are the top 3 highest performers
   * With total wins of 155, 150 and 129 respectively
   * With average goal difference of 2.45, 2.67 and 1.98 respectively

4. How has international football scene develop over the years?
   * Started of in 1930s with only 38 participating teams
   * Progress was halted in 1940s due to the World War
   * Has quickly grown to 185 participating countries by 2020
