# Excel-Parental-Leave-Analysis

## Introduction

Insights regarding parental leave pique the interest of three distinct groups: the Government, job seekers, and employees and employers.

According to ILO standards, there is a requirement for a minimum maternity leave period of 14 weeks, with a recommendation to extend it to at least 18 weeks. This extension is suggested to give the mother sufficient time for rest and recovery after childbirth.https://www.ilo.org/wcmsp5/groups/public/---dgreports/---gender/documents/publication/wcms_838655.pdf

The benchmark used in this analysis sets a minimum standard of 14 weeks for maternity leave. Companies will be assessed against this benchmark to determine if they meet the requirement or fall below the recommended duration

## Purpose of the Analysis

The purpose of this analysis is to demonstrate my proficiency in data analytics using Excel. I will utilize **Pivot Tables** and **Pivot Charts** to analyze the data and find answers to the following questions:
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
* I downloaded the data from the [Maven Analytics website] (https://mavenanalytics.io/). Maven Analytics utilized this publicly available data to create exercises and scenarios for educational purposes 
* The data source contains two files in CSV format: one contains a sheet of information about the directory and the other data for analysis. I merged both in a file for practical use.
* There are 1601 observations and 6 variables or fields. The variables are described as follows:

| Variable | Description | Missing Values <br>( in this case denoted by N/A) |
|----------|-------------|:----------------:|
| Company | Company name | 0 |
|Industry | Company Industry & sub-industry (Industry: Sub-industry)| 3 |
| Paid Maternity Leave | Paid weeks off from work for mothers after the birth of their child | 0 |
| Unpaid Maternity Leave| Unpaid weeks off from work for mothers after the birth of their child | 107 |
| Paid Paternity Leave | Paid weeks off from work for fathers after the birth of their child | 1312 |
| Unpaid Paternity Leave | Unpaid weeks off from work for fathers after the birth of their child | 1537 |

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
|Meet ILO Standard?   | Yes if the company offers 14 or more weeks of maternity Leave <br> No, if the company offers less than 14 weeks of maternity Leave  |

## Data Visualization
In the Excel file, I have included a visualization located in the sheet named 'Chart.' For more details and insights, I encourage viewers of my portfolio to explore this specific sheet. 

## Key Findings and Recommendations

* Approximately 49% (789) of the companies meet the ILO recommendations for parental leave, indicating that there is still room for improvement in this area.
* Among the industry groups with more than 50 companies, Financial Services and Banks stand out as the industry with the highest percentage of companies meeting the ILO Standards, reaching an impressive 70%. However, the Industry for Health Care Equipment & Services faces a challenge, as it has the highest percentage of companies (63%) that do not comply with the ILO Standards.
* When considering paternity leave, the average duration of paid paternity leave is 7 weeks, while the average duration of unpaid paternity leave is 8 weeks. On the other hand, for maternity leave, the average duration of paid maternity leave is 11 weeks, and the average duration of unpaid maternity leave is 7 weeks. 
* A concerning finding is that when focusing solely on paid maternity leave, a significant 77% of the companies do not meet the ILO standards. This highlights the need for stronger, more comprehensive policies to support working mothers during this critical time.

Addressing the disparities identified in parental leave policies is crucial for creating an inclusive and supportive work environment. Aspiring to meet and exceed the ILO Standards will not only benefit employees and their families but also contribute to the long-term success and growth of businesses. By embracing progressive parental leave policies, companies can attract and retain talent, foster positive company culture, and make a meaningful impact on their workforce's well-being and productivity.

**Recommendations for Governments:**

* Work with companies in the Health Care & Equipment and Services industry to identify challenges and devise strategies to improve compliance with the ILO Standards
* Highlight the success of Financial Services and Banks in meeting the ILO Standards and share their best practices with other industries. Encourage companies to adopt similar policies and showcase the benefits of supporting parental leave.
* Continue to conduct research and collect data on parental leave policies and their impact on employees and companies. Use the data to support evidence-based decision-making and policy changes.

**Recommendations for the Companies:**

* Conduct employee surveys to gather feedback on parental leave policies and work-family balance. Use the insights from these surveys to identify areas of improvement and address any concerns.
* Implement flexible return-to-work options, such as phased return or remote work arrangements, to facilitate a smooth transition for employees returning from parental leave.
* Track and measure the impact of parental leave policies on employee satisfaction, retention, and productivity. Use these metrics to evaluate the effectiveness of the policies and make data-driven improvements.

**Recommendation for further studies:**
* Conduct a cross-country analysis to compare parental leave policies and practices in different countries. This study can shed light on the impact of cultural, economic, and legislative factors on parental leave provisions.
* Investigate the long-term effects of parental leave on employee retention, career progression, and overall job satisfaction. Understanding the extended impacts of parental leave policies can provide valuable insights for employers and policymakers.

## Ressources

* I used the Report of Luka Mihailo Jović as inspiration https://mavenanalytics.io/project/4525
* Dataset was downloaded from Maven Analytics https://www.mavenanalytics.io/data-playground?accessType=open
  
## Grateful for Your Review

Dear reviewers and visitors,

I want to express my heartfelt gratitude to all those who have taken the time to review my project. As this is my first endeavor to showcase my data analytics skills, your interest and feedback mean a lot to me.
I created this project with the aim of learning and improving my abilities as a data analyst. It has been a rewarding experience for me to analyze and present insights on parental leave policies using Excel. However, I acknowledge that there might be areas for improvement, and I welcome any constructive feedback you may have.

Warm regards,

Janet
