# Excel-Parental-Leave-Analysis

## Introduction

Insights regarding parental leave pique the interest of three distinct groups: the Government, job seekers, and employees and employers.
* The government needs to know how many weeks of parental leave a company offers to ensure that all parents have access to this important benefit, promote gender equality in the workforce, and improve the health and well-being of children.
* A job seeker or employee needs to have insights about the number of parental leave a company gives to make sure that the company is a good fit for their family's needs, to negotiate for better parental leave benefits, and to make an informed decision about whether or not to take parental leave
* Firms need to have insights about the number of weeks of parental leave they offer to attract and retain top talent, comply with government regulations, improve their CSR (Corporate Social Responsibility) profile, and reduce turnover.

According to ILO standards, there is a requirement for a minimum maternity leave period of 14 weeks, with a recommendation to extend it to at least 18 weeks. This extension is suggested to give the mother sufficient time for rest and recovery after childbirth.https://www.ilo.org/wcmsp5/groups/public/---dgreports/---gender/documents/publication/wcms_838655.pdf

The benchmark used in this analysis sets a minimum standard of 14 weeks for maternity leave. Companies will be assessed against this benchmark to determine if they meet the requirement or fall below the recommended duration

## Purpose of the portfolio

The purpose of this portfolio is to demonstrate my proficiency in data analytics using Excel. I will utilize **Pivot Tables** and **Pivot Charts** to analyze the data and find answers to the following questions:
* How many companies meet the ILO standards regarding maternity leave?
* Which industry group offers the highest number of companies that fulfill the ILO standards for maternity leave?
* Which industry group has the highest number of companies that do not meet the ILO standards for maternity leave?
* What is the average duration of paid and unpaid maternity leave among the companies?
* What is the average duration of paid and unpaid paternity leave among the companies?
* Which companies offer the most paid parental leave weeks?
* Are there noticeable differences between industries?
* Which industries offer the highest number of paid and unpaid parental leave weeks?

Through this portfolio, I aim to showcase my ability to manipulate and visualize data effectively, providing valuable insights and conclusions based on the information gathered.

## Data Source and Description

The data used in this analysis is publicly available and falls under the public domain.
* I downloaded the data from the Maven Analytics website. Maven Analytics utilized this publicly available data to create exercises and scenarios for educational purposes https://www.mavenanalytics.io/data-playground?accessType=open
* The data source contains two files in CSV format: one contains a sheet of information about the directory and the other data for analysis. I merged both in a file for practical use.
* There are 1601 observations and 6 variables or fields. The variables are described as follows:

| Variable | Description |
|----------|-------------|
| Company | Company name |
|Industry | Company Industry & sub-industry (Industry: Sub-industry)|
| Paid Maternity Leave | Paid weeks off from work for mothers after the birth of their child |
| Unpaid Maternity Leave| Unpaid weeks off from work for mothers after the birth of their child |
| Paid Paternity Leave | Paid weeks off from work for fathers after the birth of their child |
| Unpaid Paternity Leave | Unpaid weeks off from work for fathers after the birth of their child |

## Data Cleaning and Preparation

* I found one duplicated observation. This was for the company 'Collins Aerospace.' I deleted both rows concerning this company because the information about Paid Maternity Leave and Unpaid Maternity Leave differed between the rows. This means I analyzed 1599 observations instead of 1601.
* I split the field 'Industry' into two: 'Industry' and 'Sub-industry,' to filter the information according to the industry without making distinctions between sub-industries. Some sub-industries were not provided, so I filled the empty cells with 'not specified'.
* I created a field called 'Industry Group.' This new column groups industries that belong to the same category. I obtained the information from the following page https://en.wikipedia.org/wiki/Global_Industry_Classification_Standard. The reason for doing this is that some industries contain only a small number of companies.
* I also created the column 'Total Maternity Leave.' This column represents the sum of Paid Maternity Leave and Unpaid Maternity Leave. To accomplish this, I used an Excel formula that replaces the 'N/A' values in the 'Unpaid Maternity Leave' field with zero to avoid error values.
* I created the field 'Is ILO Standard fulfilled?'. This variable has two values: 'yes' and 'no.' 'Yes' means that the number of offered Maternity Leave is 14 or more, and 'No' indicates that the number of Maternity Leave is less than 14.
* In conclusion, I have included the following three fields:

| Variable | Description|
|----------|----------|
|Industry Group   |Group of Industries with similar characteristics  |
|Total of Maternity Leave  | Sum of Paid Maternity Leave and Unpaid Maternity Leave |
|Meet ILO Standard?   | Yes if the company offers 14 or more weeks of maternity Leave. n/No, if the company offers less than 14 weeks of maternity Leave  |
