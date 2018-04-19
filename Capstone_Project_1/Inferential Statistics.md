# Statistics Report

The data for this project, which is obtained 
from [H1B](https://www.foreignlaborcert.doleta.gov/pdf/PerformanceData/2017/H-1B_Disclosure_Data_FY17.xlsx) 
applications contains only three numerical variables after data wrangling. But of those three variables only two of them have a
useful value. Those variables are 'prevailing_wage' and 'employer_wage'. The variable 'prevailing_wage' is determined 
directly by the US Department of Labor from its [wage library](http://www.flcdatacenter.com/OesWizardStart.aspx). 
The variable 'employer_wage' is what an employer proposes as salary for whom the application is filed.

In the present project,the purpose is to determine the salary a job applicant may expect to propose for salary negociation, so
the variable 'employer_wage' becomes the target for the model we are going to develop. Of course one of the possible independent 
variables to use then would be 'prevailing_wage'. For that purpose, the graph below shows a scatter plot of employer proposed 
wage against the prevailing wage.

![](./Figures)
