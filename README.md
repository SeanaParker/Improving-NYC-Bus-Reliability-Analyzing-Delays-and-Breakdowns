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

- **Key Factors Behind Bus Service Disruptions**
- **Variations in Delay Times Across Bus Companies and Boroughs**
- **Identifying High-Risk Bus Companies and Boroughs**
- **Patterns in Breakdown and Delay Frequency by Day of the Week**

The Excel workbook, which includes data cleaning and exploratory analysis, is available for review **[here](#)**.

---

# Data Structure & Initial Checks

The dataset consists of a single table with **282,190 records** of bus breakdowns and delays from 2019 to 2023. The data is categorized into the following key areas:

- **Incident Details** – Type of incident, reason, borough, and bus company.
- **Operational Data** – Schools affected, route number, student impact, and school year.
- **Response Tracking** – Date and time of incidents, duration of delays, and whether schools or parents were notified.

## Data Cleaning Steps

To ensure data integrity, the following cleaning steps were taken:

- Used the `TEXT()` function to extract the day of the week from `Occurred_On` to identify weekday trends in breakdowns and delays.
- Extracted the year from `Occurred_On` using the `YEAR()` function.
- Split `How_Long_Delayed` into `Short_Delay_Time_Estimated` and `Long_Delay_Time_Estimated` using the **TEXT-TO-COLUMNS** feature based on predefined thresholds.
- Standardized bus company names by identifying variations and manually correcting inconsistencies.

---

# Executive Summary

Bus breakdowns and delays in NYC and surrounding areas are primarily caused by:

- **Mechanical failures (57%)**
- **Traffic congestion (66.8%)**

Pride Transportation, Little Richie Bus Service, and Logan Bus Company have the highest breakdown and delay rates, with **Pride Transportation alone responsible for over 40% of breakdowns** among the top five companies in 2023. Manhattan sees the longest delays, while Queens experienced a **61% rise in breakdowns**, pointing to possible maintenance and operational challenges.

**Key recommendations:**
- Improving **preventative maintenance**
- Adjusting **bus schedules**
- Implementing **dedicated bus lanes** to enhance service reliability

---

# Insights Deep Dive

## Key Factors Behind Bus Service Disruptions

### Top Causes of Bus Breakdowns

- **Mechanical issues**: 10,399 incidents related to "Mechanical Problem"
- **Won’t Start**: 2,970 incidents
- **Flat Tire**: 2,499 incidents

Together, these three reasons contribute to **nearly 87% of all recorded breakdowns**.

### Top Causes of Delays

- **Heavy traffic**: 176,196 incidents (**66.8%**)
- **"Other" category**: 49,135 cases (**18.6%**), indicating unclear categorization
- **Mechanical issues**: Cause both breakdowns (**5.2%**) and delays

---

## Variations in Delay Times Across Bus Companies and Boroughs

### Delays by Bus Company

- **Selby Transportation**: Longest delays (60 min short delays, 88 min long delays)
- **Little Linda Bus Co. & Pride Transportation**: Long delays **>70 minutes**
- Other top 10 companies: Long delays between **60-67 minutes**

### Delays by Borough

- **Manhattan**: Longest delays (37 min short, 53 min long)
- **Rockland County & Queens**: Long delays exceeding **50 minutes**
- **Connecticut**: Shortest long delays (26 minutes)

---

## Identifying High-Risk Bus Companies and Boroughs

### High Breakdown & Delay Companies

- **Pride Transportation, Little Richie Bus Service, Logan Bus Company, Lorinda Enterprises**
- **Pride Transportation**: 1,033 breakdowns in **2023**, over **40% of top 5 breakdowns**
- **Little Richie & Logan Bus Company**: Decline during 2020-21 (pandemic) but increased again in 2023

### High Breakdown & Delay Boroughs

- **Queens & Manhattan** rank highest for both **delays & breakdowns**
- **Queens**: Highest breakdowns overall, **third-highest delay times**
- **Manhattan**: **Longest average delay time** (53 min)

---

## Patterns in Breakdown and Delay Frequency by Day of the Week

### Breakdown Trends

- **Monday**: Highest breakdowns (**4,146 incidents**)
- **Friday**: Lowest breakdowns (**3,318 incidents**)
- Possible causes: Cold starts, battery drainage, unresolved Friday issues

### Delay Trends

- **Monday**: Highest delays (**54,667 incidents**)
- **Wednesday & Thursday**: Mid-week increase, likely due to congestion patterns
- **Friday**: Sharp decline (**49,512 incidents**)

---

# Recommendations

### Enhancing Preventative Maintenance to Reduce Breakdowns

- Since **87% of breakdowns** result from mechanical issues, **preventative maintenance** is crucial.
- Implement **monthly/quarterly servicing** to prevent failures.

### Managing Traffic and Optimizing Routes to Reduce Delays

- Explore **dedicated bus lanes** in Manhattan, Rockland County, and Queens.
- Refine **delay categorization** to analyze the **19% "Other"** cases.

### Addressing Performance Issues Among High-Risk Bus Companies

- Conduct **annual audits** of high-risk bus companies.
- Require **corrective action plans** for companies with excessive breakdowns.

### Improving Service Reliability in High-Risk Boroughs

- Investigate **fleet maintenance issues in Queens** (61% increase in breakdowns).
- Assess **congestion & routing issues in Manhattan** (longest delay times).

### Reducing Breakdown and Delay Trends Throughout the Week

- Implement **weekend fleet inspections** to prevent Monday failures.
- Adjust **Monday schedules** (deploy extra buses, tweak departure times).
- Investigate **mid-week congestion patterns** for optimization.

---

# Assumptions and Caveats

- Analysis is based on **282,190 records**, excluding real-time traffic and maintenance logs.
- **Manual standardization** of company names may still contain minor inconsistencies.
- **Short vs. long delays** were categorized by predefined thresholds.
- Borough analysis assumes local conditions (traffic, maintenance, infrastructure) as primary factors.
- **Breakdown-decongestion causation** needs further validation.
- **Pandemic-related drop in 2020-2021 breakdowns** is assumed but not validated with ridership data.
```

This formatting will work well in a GitHub README and make your report **structured, readable, and easy to navigate**. 🚀
