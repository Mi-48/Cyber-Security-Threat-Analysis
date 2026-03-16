Cyber Security Threat Analysis

The following analysis was conducted on cybersecurity attacks worldwide, spanning the period from 2015 to 2025. The analysis was conducted using Power BI reports, which convey various metrics based on total attacks, financial losses, the number of users affected, and the average resolution time of attacks.

The reports answer the following questions:

1. What were the total financial losses each year?
2. What were the total financial losses that occurred in each country?
3. Financial losses based on each attack type.
4. No. of attacks per cyber attack type.
5. Avg. resolution time per attack type.
6. Total users affected by each type of attack.
7. What were the total financial losses incurred by each sector?
8. Total number of users affected in each sector.
9. Total number of attacks occurred in each sector by each type of attack.
10. How many attacks were neutralized using a specific defense mechanism
11. How many attacks occurred per security vulnerability?

Data:

The data comes from kaggle.com (https://www.kaggle.com/datasets/atharvasoundankar/global-cybersecurity-threats-2015-2024/data). The dataset is synthetically generated for educational, research, and analytical use. It is manually structured to reflect realistic cybersecurity incident reporting. This report uses the data for trend and pattern analysis.

Methodology:

The data has been analyzed using Power BI desktop app.The report has been visualized suing various tools such as bar, column and line charts, tables and matrix. Following meaures were made using "DAX" on the data to help extract key insights:

Core DAX measures:
1. Total attacks
- Total Attacks = COUNTROWS('Cyber Attacks')

2. Total financial loses
- Total Financial Loss = SUM('Cyber Attacks'[Financial Loss in Million Dollars])

3. Users affected
- Total Users Affected = SUM('Cyber Attacks'[Number of Affected Users])

4. Users affected per attack
- Users per Attack = DIVIDE([Total Users Affected], [Total Attacks])

5. Financial loses per attack
- Loss per Attack = DIVIDE([Total Financial Loss], [Total Attacks])

6. Country Rank
- Country Rank = RANKX(ALL(Country[Country]),[Total Financial Loss],,DESC)

7. Average resolution time
- Average Resolution Time = AVERAGE('Cyber Attacks'[Incident Resolution Time (in Hours)])

\
1. Summary

Key insights:

- A total of 3000 attacks occurred between 2015 and 2025
- There were $151K (million dollars) total financial losses
- About 2 bn users were affected
- Average resolution time was 36.48 hrs
- 2017 was the year of the greatest financial losses
- The UK incurred most of the financial losses during the entire span

\
2. Attack Analysis

key insights:

- Attack type DDoS casued the most financial loses and affected a mojor number of users
- The greated resolution time was for 'Malware' type.

\
4. Industry Analysis

Key Insights:

- The IT sector incurred the most financial loses
- Most of the users were affected in the IT sector

\
4. Defense and Security Analysis

Key insights: 

- Most of the attacks were tackled using antivirus software
- The largest number of attacks occurred due to zero-day exploitation
