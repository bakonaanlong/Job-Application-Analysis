# Job Application Analysis Dashboard README

## 1. Background and Overview

This dashboard provides a comprehensive visual analysis of job market trends based on real-world job application data I scraped from a job application site.

The analysis focuses on **data-centric roles** I applied for (e.g., data analysts, DBA, data engineer) and explores key dimensions including:
- Geographic job density
- Required skills and tools
- Work arrangements (full-time, part-time, contract)
- Compensation structures
- Cloud service adoption
- Educational requirements

The dashboard is split across **two primary views**:
1. **Job Market Landscape** – Focuses on skills, hours, geography, and cloud adoption.
2. **Compensation & Application Insights** – Analyzes salary trends, job types, and income distribution.

**Data Source**: LinkedIn.  
**Tool**: Microsoft Power BI  
**Author**: Bako Naanlong  

---

## 2. Data Structure Overview

The underlying dataset is structured around **job postings** with the following fields:

| Field | Description | Data Type | Example |
|------|-------------|-----------|---------|
| `Job ID` | Unique identifier for each job posting | String | J123456 |
| `Job Title` | Role title | String | Data Analyst |
| `Country` | Location of job | String | United States |
| `Region` | Continent or sub-region | String | North America |
| `Job Type` | Full-time, Part-time, Contract | Categorical | Full-time |
| `Hours/Week` | Average weekly hours | Numeric | 40 |
| `Compensation (USD)` | Annual or monthly salary | Numeric | 85,000 |
| `Income Range` | Binned income level | Categorical | High Income |
| `Cloud Service` | Yes/No flag for cloud requirement | Boolean | Yes |
| `Degree Required` | Yes/No | Boolean | No |
| `Skills Mentioned` | List of tools/skills in posting | Array/String | Excel, SQL, Python |
| `Skill Necessity` | Mentioned vs. not mentioned (proxy for importance) | Categorical | Mentioned |

**Key Derived Metrics**:
- **Skill Distribution by Necessity**: Skills explicitly mentioned are treated as "necessary."
- **Average Compensation by Country/Job Type**: Aggregated mean values.
- **Cloud vs Non-Cloud Services**: Binary classification of job tech stack.

---

## 3. Executive Summary

- **Excel** dominates as the most universally required tool, appearing in nearly **100% of analyzed job postings**.
- **SQL** is the second most critical skill, far ahead of advanced tools like **Python**, **Snowflake**, or **Tableau**.
- **78.26% of jobs** are **non-cloud** focused, indicating a persistent reliance on on-premise or hybrid environments.
- Only **39.13% of roles** explicitly require a **degree**, suggesting a growing trend toward skills-based hiring.
- **Full-time positions** dominate the market (**~85%**), with average weekly hours near **40**.
- **Dubai** offers the **highest average compensation**, significantly above global averages.
- **Average compensation declines sharply** outside top-tier markets (e.g., US, UAE, UK).
- **Cloud-based roles** command **higher average pay** and are more likely to require degrees.

---

## 4. Insights Deep Dive

### 4.1 First Dashboard: Job Market Landscape

#### A. Geographic Job Density
- **Europe** and **North America** show the highest concentration of data-related roles.
- **Asia** has moderate density, led by India and East Asia.
- **Africa** and **South America** have minimal representation, indicating underpenetration of formal data job markets.
- **Australia** stands out as a high-density outlier in Oceania.

#### B. Most Important Skills/Tools
- **Excel** is mentioned in **~95%+** of jobs — the uncontested foundational tool.
- **SQL** follows at **~75%**, confirming its role as the backbone of data manipulation.
- **Cloud Tools** (generic) rank third, but specific platforms trail:
  - **Power BI** > **Python** > **Snowflake** > **Tableau** > **R**
- Skills not mentioned are assumed less critical — a proxy for **market-expected baseline competency**.

#### C. Work Hours and Job Type
- **Full-time roles**: ~40 hours/week
- **Part-time**: ~20–25 hours/week
- **Contract**: ~30–35 hours/week
- Full-time roles dominate volume and consistency in hours.

#### D. Cloud Service Adoption
- **78.26% Non-Cloud** vs **21.74% Cloud**
- Cloud roles work **slightly fewer average hours** (~38 vs ~40), possibly due to automation efficiencies.
- Cloud jobs are **more likely to require degrees** and pay **~20–30% higher** on average.

#### E. Degree Requirement
- **60.87%** of jobs **do not require a degree**
- **39.13%** explicitly list a degree as necessary
- Degree requirement correlates strongly with:
  - Cloud-based roles
  - Higher compensation brackets
  - Full-time corporate positions

---

### 4.2 Second Dashboard: Compensation & Application Insights

#### A. Compensation by Geography
- **Top 5 Highest-Paying Locations**:
  1. **Dubai** (~$110K+ avg)
  2. **United States**
  3. **Switzerland**
  4. **United Kingdom**
  5. **Germany**
- Compensation drops **precipitously** beyond the top 10 countries.
- **India, Brazil, South Africa, Ukraine** cluster at the lower end (<$40K avg).

#### B. Compensation vs. Cloud Adoption
- **Cloud Service jobs**: ~$85K avg
- **Non-Cloud jobs**: ~$65K avg
- **~30% pay premium** for cloud expertise.

#### C. Degree and Compensation
- **Degree Required**: ~$78K avg
- **No Degree Needed**: ~$62K avg
- Degree acts as a **compensation gatekeeper**, especially in mid-to-high income roles.

#### D. Job Type and Income Distribution
- **Full-time roles** dominate **Good and High Income** tiers.
- **Contract roles** skew toward **Mid and High Income**, but with higher variance.
- **Part-time roles** are overwhelmingly **Low to Mid Income**.

#### E. Hours vs. Income
- Higher weekly hours (35–40+) strongly correlate with **High Income** roles.
- Roles under 20 hours/week rarely exceed **Mid Income**.

---

## 5. Recommendations

### For Job Seekers
1. **Master Excel and SQL first** — they are non-negotiable across all markets.
2. **Prioritize cloud certifications** (AWS, Azure, GCP) to access **30%+ higher-paying roles**.
3. **Target high-compensation hubs**: Dubai, US, Switzerland, UK — even remotely.
4. **Leverage skills over degrees** — 60%+ of roles are open to non-graduates with strong portfolios.
5. **Focus on full-time roles** for stability and income growth.

### For Employers & Recruiters
1. **Reduce degree barriers** — tap into a larger, skilled talent pool.
2. **Clearly differentiate cloud vs non-cloud roles** in postings to attract right candidates.
3. **Offer competitive pay in emerging markets** to attract global remote talent.
4. **Highlight tools explicitly** — especially Power BI, Python, Snowflake for advanced roles.


---

**Dashboard File**: `Job_Application_Analysis.pbix`  
**Author**: Bako Naanlong  
 
