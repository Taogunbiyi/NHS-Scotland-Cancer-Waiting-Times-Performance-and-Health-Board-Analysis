# NHS-Scotland-Cancer-Waiting-Times-Performance-and-Health-Board-Analysis

# Executive Summary
This portfolio project analyses **40,800 records across 14 fields** from the supplied NHS Scotland cancer waiting-time dataset. The data covers **2012 to Q1 2025**, two cancer waiting-time standards, 19 health-board/reporting categories and 24 cancer-type categories.

The project demonstrates an end-to-end Health Informatics analytics
workflow:

**Healthcare problem → data quality → preparation → SQL → Power BI → insight → recommendation**

The analysis focuses on the **31-day** and **62-day** cancer
waiting-time standards. Public Health Scotland states that the **31-day
standard** measures time from decision to treat to first treatment, while
the **62-day standard** measures time from receipt of referral to treatment.
The standards have been national standards since 1 April 2012.

The project demonstrates how health informatics analysis combines performance percentages with denominator size, waiting-time distributions and longitudinal trends.

The dashboard is designed to help analysts and operational stakeholders
move from headline performance to health-board and cancer-pathway
detail.

**Important:** This portfolio analysis is based on the uploaded dataset and therefore ends at **January--March 2025**. It should not be presented as the latest NHS Scotland position as the Public Health Scotland has subsequently published newer releases.

# Project Overview

This project analyses cancer waiting-time performance across the NHS Scotland health boards,and identify trends,variation,and areas of underperformance.
The aim is to identify trends in cancer waiting times,assess performance against national standards,compare health boards, analyse variation across cancer types and provide evidence-based insights that could support healthcare service improvement.

The analysis focuses on the two principal cancer waiting-time standards: **31-day standard**, and **62-day standard**.

# Business / Healthcare Problem 
Cancer patients often experience delays between referral, diagnosis and the start of treatment. Consequently, monitoring these waiting times is essential, as prolonged waits place significant pressure on both patients and healthcare services and may reflect underlying capacity constraints and/or inefficiencies in clinical pathways. The key analytical question for this project is:

**How does cancer waiting-time performance vary across NHS Scotland, health boards and cancer pathways, and where are the greatest areas of underperformance?**

## Business Questions

The project provided insight into these business questions:
    
1. What is the overall NHS Scotland cancer waiting-time performance?
2. How does 31-day performance compare with 62-day performance?
3. Which health boards meet the 95% standard?
4. Which health boards show persistent underperformance?
5. Which cancer types have the longest waits?
6. How do median and maximum waits differ?
7. How does eligible referral volume change over time?
8. Does performance change materially across quarters?
9. Where should operational teams investigate further?
10. How can the dashboard support continuous performance monitoring?

# Dataset Profile

The analysis used publicly available NHS Scotland cancer waiting-time statistics published by Public Health Scotland.

The portfolio is based on the Exccel dataset containing information relating to cancer waiting-time performance, including measures such as:

  Field                                      Description                                Type   

Target Type                               31 Day or 62 Day standard                     Text
Quarter End                                 Reporting quarter                           Text
Year                                         Reporting year                            Integer
Quarter number                               Reporting quarter                         Integer             
Health Board                              NHS board/reporting category                 Text           
Cancer Type                               Cancer pathway/category                      Text
Number of Eligible referrals            Eligible referrals in the reporting group      Integer 
Number of Eligible referrals            Eligible referrals met Target                  Integer                                                      
Target performance                     Percentage meeting the standard                 Numeric              
Max                                        Maximum waiting time                        Integer
Median                                     Median waiting time                         Numeric
95th percentile                        95th-percentile waiting time where              Numeric
                                                    available    

## Data Coverage
-   Records: 40,800
-   Fields: 14
-   Period: 2012 to January-March 2025
-   Target types: 31 Day and 62 Day
-   Health-board/reporting categories: 19
-   Cancer-type categories: 24

## Data source
Public Health Scotland Cancer Waiting Times:
https://publichealthscotland.scot/healthcare-system/waiting-times/cancer-waiting-times/

## Privacy
The dataset used in this portfolio is aggregate reporting data. Do not add patient-level identifiable information to this repository.

## Missing data
The source contains missing values in Median, 95th percentile, Rate of Referrals and Concatenation. These are retained/documented rather than silently replaced.

# Data Governance and Privacy
This project uses aggregate healthcare statistics for portfolio and educational purposes.
No identifiable patient-level information is used.
## Patient Privacy
The project does not require the storage or publication of:
• Patient names
• NHS numbers
• Addresses
• Dates of birth
• Individual clinical records
• Other directly identifiable patient information

## Principles demonstrated
-   Confidentiality
-   Data minimisation
-   Purpose limitation
-   Appropriate use
-   Data quality
-   Responsible interpretation
-   Disclosure awareness

## Small-number disclosure
Small denominators require caution. Percentage performance for small NHS boards can move substantially because one or two patients may materially change the result.

## Governance context
A production healthcare analytics environment would require appropriate access controls, lawful processing, information governance approval where applicable, auditability and adherence to organisational policies.

# Analytical Workflow

           PUBLIC HEALTH SCOTLAND DATA
                    │
                    ▼
              DATA QUALITY CHECKS
                    │
                    ▼
               DATA PREPARATION
                    │
                    ▼ 
              DATA MODELLING 
                    │ 
                    ▼ 
                 POWER BI 
                    │ 

      ┌───────────┼───────────┐ 
      ▼            ▼             ▼ 
     KPIs         Trends.     Comparisons

      └───────────┼───────────┘ 
                    ▼ 
               KEY INSIGHTS 
                    │ 
                    ▼ 
               RECOMMENDATIONS
              
# Data Preparation

Before analysis, the dataset was assessed for data-quality issues.

The preparation process included:

• Checking column names and data types
• Standardising NHS Board names
• Checking reporting periods
• Identifying missing values
• Checking duplicate records
• Validating numerical fields
• Checking percentages
• Standardising cancer-type categories
• Creating analytical variables
• Removing or documenting inappropriate records

Data-quality checks were performed before calculating KPIs to reduce the risk of misleading results.

# Data Quality Assessment

The project evaluates:

Data-quality dimension	& Data Assessment;
• Completeness	 - Percentage of missing values
• Validity	 - Values fall within expected ranges
• Consistency	- Categories and names are standardised
• Uniqueness	 - Duplicate records identified
• Accuracy - 	Values checked against source documentation
• Timeliness 	- Reporting period recorded
• Integrity -	Relationships between fields assessed.    

# Key Performance Indicators

The dashboard focuses on healthcare-relevant KPIs.

### 31-Day Performance

Measures the percentage of relevant patients whose treatment started within the 31-day standard.

### 62-Day Performance

Measures the percentage of relevant patients whose treatment started within the 62-day standard.

### Median Waiting Time

The median represents the middle waiting-time value and reduces the influence of extreme observations.

### Maximum Waiting Time

Shows the longest recorded waiting time within the relevant reporting group.

### Target Achievement

Measures whether performance meets the applicable national standard.    

# Power BI Dashboard

The Power BI dashboard is structured into several analytical pages.

## Page 1 — Executive Overview

The executive page provides a high-level summary of NHS Scotland performance. The purpose is to allow a healthcare professional or analyst to have a quick understanding of the overall performance. 

The Key visuals include;
• Total Eligible referrals
• Total Eligible referral met
• 31-day performance (%)
• 62-day performance (%)
• Median waiting time (days)
• Maximum waiting time (days)
• Performance trend
• Target achievements 

## Page 2 — Waiting-Time Trends

This page analyses performance over time,and addressed questions such as; 

• Is performance improving?
• Is performance deteriorating?
• Are there periods of significant change?
• How has median waiting time changed?
• How has target achievement changed?

These were visualised using Line charts,
KPI cards, Trend indicators, and Year/quarter slicers.

## Page 3 — Health Board Performance

This page compares NHS health boards, and 
addressed questions such as; 

• Which boards perform above the national level?
• Which boards perform below the national level?
• Which boards have persistent underperformance?
• Which boards show improvement?

Visualisations used include Health board ranking, Performance comparison, Conditional formatting, Trend by health board, and Target achievement, allowing users to select and investigate individual health board performance over time.

## Page 4 — Cancer Type Analysis

This page compares waiting-time performance by cancer type/pathway.

Questions addressed include;
• Which cancer types have the longest waits?
• Which cancer types perform best against the standards?
• Which pathways show the greatest variation?
• Are some cancer types consistently below target?

## Page 5 — Waiting-Time Distribution

This page examines the distribution of waiting times. Measures examined include:

• Minimum wait
• Maximum wait
• Median wait
• Average wait
• Distribution of waiting times


