# NHS-Scotland-Cancer-Waiting-Times-Performance-and-Health-Board-Analysis

# Project Overview

This project analyses cancer waiting-time performance across the NHS Scotland health boards,and identify trends,variation,and areas of underperformance.
The aim is to identify trends in cancer waiting times,assess performance against national standards,compare health boards, analyse variation across cancer types and provide evidence-based insights that could support healthcare service improvement.

The project demonstrates an end-to-end health informatics analytics workflow,viz:

Data acquisition → Data quality → Data preparation → SQL analysis → Python analysis → Power BI modelling → Dashboard → Insights → Recommendations

The analysis focuses on the two principal cancer waiting-time standards:

31-day standard
62-day standard

The underlying statistics are published by Public Health Scotland as accredited official statistics.

# Business / Healthcare Problem #

Cancer patients often experience delays between referral, diagnosis and the start of treatment. Consequently, monitoring these waiting times is essential, as prolonged waits place significant pressure on both patients and healthcare services and may reflect underlying capacity constraints and/or inefficiencies in clinical pathways.

The key analytical question for this project is:

"How does cancer waiting-time performance vary across NHS Scotland, health boards and cancer pathways, and where are the greatest areas of underperformance"?

# Project Objectives

The project aims to provide insight into these business questions:

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

# Dataset

The analysis uses publicly available NHS Scotland cancer waiting-time statistics published by Public Health Scotland.

The dataset contains information relating to cancer waiting-time performance, including measures such as:

• Reporting period
• NHS Board
• Cancer type/pathway
• Number of patients
• Waiting-time measures
• Percentage meeting the relevant standard
  31-day performance
  62-day performance

The precise fields depend on the version of the Public Health Scotland dataset used for the analysis.

# Data source

Public Health Scotland:

https://www.publichealthscotland.scot/

The latest release used for this project should be documented in the data/README.md file so that the analysis remains reproducible.

# Data Governance and Privacy

This project uses publicly available aggregate statistics.

No identifiable patient-level information is used.

The project therefore does not require the storage or publication of:

• Patient names
• NHS numbers
• Addresses
• Dates of birth
• Individual clinical records
• Other directly identifiable patient information

Healthcare analytics must consider confidentiality, information governance and appropriate use of health data.

Where patient-level data is used in future versions, appropriate governance, access controls, lawful processing and disclosure controls would be required.

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


