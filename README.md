# Improving NYC Bus Reliability: Analyzing Delays and Breakdowns

# Table of Contents
- [**Project Background**](#project-background)
- [**Data Structure & Initial Checks**](#data-structure--initial-checks)
- [**Executive Summary**](#executive-summary)
- [**Insights Deep Dive**](#insights-deep-dive)
  - [**Key Factors Behind Bus Service Disruptions**](#key-factors-behind-bus-service-disruptions)
  - [**Variations in Delay Times Across Bus Companies and Boroughs**](#variations-in-delay-times-across-bus-companies-and-boroughs)
  - [**Identifying High-Risk Bus Companies and Boroughs**](#identifying-high-risk-bus-companies-and-boroughs)
  - [**Patterns in Breakdown and Delay Frequency by Day of the Week**](#patterns-in-breakdown-and-delay-frequency-by-day-of-the-week)
- [**Recommendations**](#recommendations)
- [**Assumptions and Caveats**](#assumptions-and-caveats)

---

# Project Background
Frequent bus breakdowns and delays continue to disrupt daily commutes in New York City, creating challenges for transit operations and passenger experience. In this case study, I take on the role of a data analyst for the New York Division of Transportation, investigating inefficiencies in scheduling, maintenance, and transit reliability to help fleet managers and transit teams improve service performance.

**Insights and recommendations are provided on the following key areas:**
- Key Factors Behind Bus Service Disruptions
- Variations in Delay Times Across Bus Companies and Boroughs
- Identifying High-Risk Bus Companies and Boroughs
- Patterns in Breakdown and Delay Frequency by Day of the Week

The Excel workbook, which includes data cleaning and exploratory analysis, is available for review [here.](https://drive.google.com/file/d/16v4zOHwhJbtPXHAlBFplFogHmOhqQgi5/view?usp=sharing)

---

# Data Structure & Initial Checks
The dataset consists of a single table with 282,190 records of bus breakdowns and delays from 2019 to 2023. The data is categorized into the following key areas:
- **Incident Details** – Type of incident, reason, borough, and bus company.
- **Operational Data** – Schools affected, route number, student impact, and school year.
- **Response Tracking** – Date and time of incidents, duration of delays, and whether schools or parents were notified.

## Data Cleaning Steps
To ensure data integrity, the following cleaning steps were taken:
- Used the `TEXT()` function to extract the day of the week from `Occurred_On` to identify weekday trends in breakdowns and delays.
- Extracted the year from `Occurred_On` using the `YEAR()` function.
- Split `How_Long_Delayed` into `Short_Delay_Time_Estimated` and `Long_Delay_Time_Estimated` using the `TEXT-TO-COLUMNS` feature based on predefined thresholds.
- Standardized bus company names by identifying variations and manually correcting inconsistencies.

---

# Executive Summary
Bus breakdowns and delays in NYC and surrounding areas are primarily caused by mechanical failures (57%) and traffic congestion (66.8%). Pride Transportation, Little Richie Bus Service, and Logan Bus Company have the highest breakdown and delay rates, with Pride Transportation alone responsible for over 40% of breakdowns among the top five companies in 2023. Manhattan sees the longest delays, while Queens experienced a 61% rise in breakdowns, pointing to possible maintenance and operational challenges. Improving preventative maintenance, adjusting schedules, and implementing dedicated bus lanes could enhance service reliability.

---

# Insights Deep Dive
## Key Factors Behind Bus Service Disruptions
### Top Causes of Bus Breakdowns
- Mechanical issues are the leading cause of bus breakdowns, with 10,399 incidents related to "Mechanical Problem" and another 2,970 incidents due to "Won’t Start." Flat Tire accounts for 2,499 cases, making it the third most common issue.
- Together, these three reasons contribute to nearly 87% of all recorded breakdowns, highlighting maintenance as a key factor in fleet reliability.
  <img src="Visualizations/Common_Breakdowns.png" alt="Common Breakdowns" width="950">

### Top Causes of Delays
- Heavy traffic is the overwhelming cause of bus delays, accounting for 176,196 incidents (66.8%). The "Other" category is the second most common reason, with 49,135 cases (18.6%), suggesting that many delays do not fit neatly into predefined categories.
- Mechanical issues cause both delays (5.2%) and breakdowns, reinforcing the need for better fleet maintenance.

---

## Variations in Delay Times Across Bus Companies and Boroughs
### Delays by Bus Company
- Selby Transportation has the longest delays, with short delays averaging 60 minutes and long delays reaching 88 minutes.
- Little Linda Bus Co. and Pride Transportation also experience extended delays, with long wait times exceeding 70 minutes.
- The remaining companies in the top 10 report long delays between 60 and 67 minutes, indicating ongoing operational challenges.

### Delays by Borough
- Manhattan experiences the longest delays, with short delays averaging 37 minutes and long delays reaching 53 minutes.
- Rockland County and Queens also experience long delays exceeding 50 minutes, suggesting a trend in urban congestion.
- Connecticut reports the shortest delays, with long delays averaging only 26 minutes

---

## Identifying High-Risk Bus Companies and Boroughs
### Bus Companies with Frequent Breakdowns and Long Delays
- Pride Transportation, Little Richie Bus Service, Logan Bus Company, and Lorinda Enterprises rank in the top 10 for both delays and frequent breakdowns, with Pride, Little Richie, and Logan also among the top five for total breakdowns.
- Over time, Pride Transportation has seen a steady rise in breakdowns, reaching 1,033 in 2023 and accounting for over 40% of the total breakdowns among the top five companies.
- Little Richie Bus Service and Logan Bus Company experienced a decline in breakdowns in 2021 and 2022, possibly due to reduced service during and immediately after the pandemic. However, breakdowns increased again in 2023, suggesting potential maintenance or operational challenges.

### Boroughs with Frequent Breakdowns and Long Delays
- Queens and Manhattan rank among the top boroughs for both delays and breakdowns, with Queens reporting the highest number of breakdowns overall and the third-highest delay times.
- Manhattan ranks fourth for breakdowns but has the longest average delay times at 53 minutes.
- Based on the available dataset, Queens saw a 61% increase in reported breakdowns in 2023 compared to 2022. This increase suggests that fleet maintenance issues or operational inefficiencies may be driving both breakdowns and delays.
- Meanwhile, Manhattan has seen a more gradual and stable trend in breakdowns, with numbers remaining relatively steady over time. 
- Since breakdowns are less frequent in Manhattan, the primary cause of delays is likely due to traffic congestion and route inefficiencies rather than mechanical failures.

---

## Patterns in Breakdown and Delay Frequency by Day of the Week
### Breakdown Trends by Day
- Bus breakdowns are most frequent on Monday (4,146 incidents) and steadily decline throughout the week, reaching 3,318 incidents on Friday. 
- Since school buses remain inactive over the weekend, these issues may be due to factors such as cold starts, battery drainage, or unresolved mechanical problems from Friday, possibly leading to higher failure rates at the start of the week.

### Delay Trends by Day
- Delays follow a similar pattern, with Monday experiencing the highest number of delays (54,667 incidents). While the cause is not explicitly recorded in the dataset, potential explanations include fleet conditions after a two-day break or heavier traffic congestion at the start of the week.
- A mid-week increase on Wednesday and Thursday suggests possible traffic congestion patterns or operational inefficiencies affecting service reliability.
- By Friday, delays drop sharply (49,512 incidents), possibly due to lighter traffic, fewer after-school programs, or early school dismissals reducing demand.

---

# Recommendations
Based on the insights and findings above, I would recommend the following:

### Enhancing Preventative Maintenance to Reduce Breakdowns
- Since 87% of breakdowns result from mechanical issues, strengthening preventative maintenance could significantly reduce service disruptions.
- Implement a monthly or quarterly servicing schedule to prevent mechanical failures.
### Managing Traffic and Optimizing Routes to Reduce Delays
- Consider exploring dedicated bus lanes in Manhattan, Rockland County, and Queens to reduce delays.
- Refine delay categorization to better understand the nearly 19% of cases classified as "Other" delays, which may reveal additional areas for improvement.
### Addressing Performance Issues Among High-Risk Bus Companies
- Conduct annual audits of bus companies that rank high in both breakdowns and delays to assess maintenance practices and operational efficiency.
- Require corrective action plans for companies with frequent failures, outlining steps to improve fleet reliability.
### Improving Service Reliability in High-Risk Boroughs
- Investigate fleet maintenance and staffing challenges in Queens, which saw a 61% increase in breakdowns in 2023.
- Assess congestion and routing issues in Manhattan, which has the longest average delay times (53 minutes).
### Reducing Breakdown and Delay Trends Throughout the Week
- Implement weekend fleet inspections to catch maintenance issues before buses return to service on Monday.
- Adjust Monday schedules by deploying extra buses or tweaking departure times on high-delay routes. 
- Look into mid-week congestion patterns (Wednesday and Thursday) to see if route changes or better timing could help reduce delays.

---

# Assumptions and Caveats
- Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:
- This analysis is based on the available dataset of 282,190 records. Factors such as real-time traffic conditions and maintenance logs were not included.
- Since company names were manually reviewed and adjusted for consistency, minor discrepancies may remain due to data entry variations.
- The division of short and long delay times was based on a set threshold for analysis purposes. While this helps categorize delays, actual transit experiences may vary.
- The borough-level analysis assumes that delays and breakdowns are primarily influenced by local conditions such as traffic congestion, fleet maintenance, and infrastructure. Broader citywide issues, such as extreme weather or transit strikes, were not accounted for separately.
- While data patterns indicate possible links between breakdowns, congestion, and delays, additional validation is needed to establish causation.
- The decrease in breakdowns in 2020 and 2021 is likely due to lower bus usage during the pandemic. This assumption is based on industry trends but was not validated with ridership data.
