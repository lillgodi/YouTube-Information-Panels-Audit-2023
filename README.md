# Data Description
This webpage contains details about the data accompanying WebSci 2024 paper titled YouTube and Conspiracy Theories: Auditing Search Page Level 
Information Panels. The data was collected from a Qualtrics survey distributed using Amazon Mechanical Turk. The survey data is used to conduct 
an audit collected over four months in 14 different locations to investigate the extent, coverage, and consistency of YouTube's information panels. 
Our experiments collect 309 survey responses and 620 queries used in the audit. Demographic questions were also collected. Here 
you will find 5 files across two parts: raw survey data, grouping queries, and audit data.\

*To load the json file into a Pandas DataFrame, use the attribute `orient='split`.

**1. Raw data**  

filename: [YT IP survey_October 11, 2022_08.46.csv](YT%20IP%20survey_October%2011%2C%202022_08.46.csv)  
This file contains all data collected from 309 responses to our survey. Below are the column names relevant to this study:

- Queries used in audit
  - Q4: queries_1
  - Q4: queries_2
  - Q4: queries_3
- Demographics
  - Q1: news freq_1
  - Q7: age
  - Q8: gender
  - Q9: politics
  - Q10: education
 
filename: [allQueries.csv](allQueries.csv)  
This file contains all unique queries collected from the survey that were then used as input data for the audit
of YouTube using selenium.

**2. Grouping queries**  

filename: *[tops_df.json](tops_df.json)  
This file contains each unique query, the handpicked topic and Wikipedia category that the query was grouped into, 
and the number of times the query was repeated in the original data. 

**3. Audit data**

For the audit data below, each row represents one search engine results page (SERP). The column values are the date 
collected, the location of the virtual machine on Google Cloud, the query inputted, the text of the IP, the URL of 
the IP (if no IP, the value is None), the Wikipedia category and handpicked topic associated with the query, and 
isContext, isFactCheck, isNews which indicate the IP type on the SERP.

filename: *[final_df.json](final_df.json)  
Data between December 2021 and April 2022.

filename: *[oct_df.json](oct_df.json)  
Follow-up data from October 2023.

