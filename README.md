# DigitalLearningImpactofCovid
An analysis of the impact of Covid-19 on digital learning in United States.

View the Full version with plots on [Kaggle](https://www.kaggle.com/thesoulreaper/the-impact-of-covid-19-on-digital-learning/notebook)

# Problem Statement
The COVID-19 Pandemic has disrupted learning for more than 56 million students in the United States. In the Spring of 2020, most states and local governments across the U.S. closed educational institutions to stop the spread of the virus. In response, schools and teachers have attempted to reach students remotely through distance learning tools and digital platforms. Until today, concerns of the exacaberting digital divide and long-term learning loss among America’s most vulnerable learners continue to grow.

## Understanding the Impact
We have three basic sets of files.

1. The engagement data are based on LearnPlatform’s Student Chrome Extension. The extension collects page load events of over 10K education technology products in our product library, including websites, apps, web apps, software programs, extensions, ebooks, hardwares, and services used in educational institutions. The engagement data have been aggregated at school district level, and each file represents data from one school district.
2. The product file includes information about the characteristics of the top 372 products with most users in 2020.
3. The district file includes information about the characteristics of school districts, including data from National Center for Education Statistics (NCES), The Federal Communications Commission (FCC), and Edunomics Lab.

Before moving on any further, I should add a few notes:

1. In the districts data, we have rows which have null values in the state column. I have droppped such rows as they won't be able to provide any information about the scenario.
2. Also, the county_connections ratio does not provide any information as it has lots of null values as well as highly skewed observation i.e only 1 observtion is [1, 2] and rest others [0.18, 1]. Hence, I have decided to drop the column.
3. We have the engagement data for 236 districts however for most of the districts the data is not complete. I have decided to include only those districts that have data for the whole year. Also, the engagement data contains data for products which are not included in the products file. We'll be omitting those from our analysis as well.
4. I have used Median to aggregate the numerical data as the data is highly skewed. Also, I have used Log to display numerical values to represent the data much more visually appealing.
