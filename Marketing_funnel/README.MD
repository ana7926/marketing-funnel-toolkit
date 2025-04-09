# Business Data Analysis Toolkit


## 📑 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Project Purpose & Business Value](#project-purpose--business-value)
- [Marketing Funnels: Detailed Description](#marketing-funnels-detailed-description)
- [Individual Traffic Channel Sheet](#individual-traffic-channel-sheet)
- [Technical Implementation](#technical-implementation)
- [Tools & Skills Applied](#tools--skills-applied)
- [Examples of Use](#examples-of-use)
- [Future Improvements](#future-improvements)
- [Final Thoughts](#final-thoughts)

## Overview
This project is a comprehensive toolkit built in Google Sheets, designed to help businesses analyze and optimize their marketing, financial, and payroll processes. It consists of three main components: **Marketing Funnels**, **Financial Analysis**, and **Salary Widget**. The primary goal of the marketing funnels section is to evaluate the performance of various customer acquisition sources, enabling businesses to identify high-performing channels for increased ad budget allocation and underperforming ones that may need reevaluation or discontinuation to avoid wasting resources.


## Project Structure
The project is divided into three parts:
1. **Marketing Funnels** 
   - Analyze the performance of different marketing channels to optimize ad spend.  
2. **Financial Analysis**  
   - Tools for assessing income, expenses, profitability and other necessary metrics for the good existence of a business.  
3. **Salary Widget**  
   - Calculate employee salaries, including taxes and bonuses. And most importantly, it shows the employee his current KPI performance and what needs to be done to increase his salary.

## Project Purpose & Business Value

This tool helps small businesses:

- 🧭 Track leads and conversions across multiple marketing channels.
- 🕵️‍♀️ Spot the most effective traffic sources and focus your efforts (because who has time for guesswork?).
- 💸 Calculate conversion rates and customer acquisition costs (CAC) to spend smarter, not harder.
- 🔍 Visualize sales funnel performance at every stage — from curious clicks to happy customers.
- 🚦 Detect bottlenecks (yes, we’re looking at you, leaky funnels) and spot areas for improvement.
- 🔮 Forecast future sales with data-driven magic.

By building this tool, I prove that I’m not just a data nerd — I’m a data nerd who understands how numbers translate to growth strategies and financial health for businesses!

## Marketing Funnels: Detailed Description
The **Marketing Funnels** section is designed to track and analyze the performance of various marketing channels, such as Target Instagram, Google Ads, SMM, Cross-Marketing, and Flyers. It provides a clear overview of the customer journey, from initial reach to final membership, helping businesses understand which channels are most effective at converting leads into paying customers. It is compiled from [personal tables for each individual traffic source](https://docs.google.com/spreadsheets/d/18UbCYCmYHT0UhvSi8QXXYHwRIDvc2aSxA5sjXRmFEW4/edit?gid=452872515#gid=452872515).

> ✨ **Quick note:**  
> What you see here is just a sneak peek of the full dashboard.  
> For the complete experience, feel free to explore the full version right here: [Google Sheets Link](https://docs.google.com/spreadsheets/d/18UbCYCmYHT0UhvSi8QXXYHwRIDvc2aSxA5sjXRmFEW4/edit?gid=1096805160#gid=1096805160).  
> *The table is view-only, no download needed. Enjoy the walkthrough!*

### Marketing Funnel & Financial Summary (01.01.2025 — 31.01.2025)

_Below is a sample marketing funnel for a specialist, covering key metrics from **January 1 to January 31, 2025**._

<details open>
<summary><strong>Advertising</strong></summary>

| Parameter | Comparison | Total |
|-----------|------------|-------|
| Ad Expenses (salary included) | 23,739.1 | 25,153.3 |
| Showings | 658,933 | 734,191 |
| Cost per Showing | 0.04 | 0.03 |
| CR to Click | 0.34% | 0.33% |
| Clicks | 2,214 | 2,388 |
| Cost per Click | 10.72 | 10.53 |

</details>

<details>
<summary><strong>Leads & Prepayments</strong></summary>

| Parameter | Comparison | Total |
|-----------|------------|-------|
| CR to Lead | 1.04% | 1.09% |
| Leads | 23 | 26 |
| Cost per Lead | 1,032.28 | 967.43 |
| CR to Prepayment | 26.09% | 30.77% |
| Prepayments | 6 | 8 |
| Cost per Prepayment | 3,956.52 | 3,144.16 |

</details>

<details>
<summary><strong>Sales & Revenue</strong></summary>

| Parameter | Comparison | Total |
|-----------|------------|-------|
| CR Prepayment to Sale | 100% | 100% |
| Memberships | 7 | 8 |
| Cost per Membership | 3,391.3 | 3,144.16 |
| Revenue from Memberships | 21,000 | 24,000 |

</details>

<details>
<summary><strong>Profitability</strong></summary>

| Parameter | Comparison | Total |
|-----------|------------|-------|
| Total Cash Inflow | 23,958.3 | 27,008.3 |
| Total Cash Outflow | 23,739.1 | 25,153.3 |
| Net Profit | 219.2 | 1,855 |

</details>

---

#### 🔍 Notes:
- _***ROMI***, ***Total Cash Inflows***, and ***Customer Acquisition Cost*** are highlighted as key performance indicators._
- 📈 _Period 2 shows significant growth in ***ROMI*** and ***Membership Cash Inflows***._
- _For full analysis and interactive table, [click here](https://docs.google.com/spreadsheets/d/18UbCYCmYHT0UhvSi8QXXYHwRIDvc2aSxA5sjXRmFEW4/edit?gid=1096805160#gid=1096805160)._



## Individual traffic channel sheet


### Purpose 

This sheet captures data for individual traffic sources (e.g., Instagram) and feeds into the consolidated Marketing Funnel. It tracks daily ad performance for detailed analysis.

![Marketing-funnel](/Marketing_funnel/pic/individual_funnel.gif)

---

### How it works
> This setup offers a cost-effective alternative to ERP systems, supporting both manual entry and potential automation via ad platform integrations. 

#### Automatically filled data *(light cells)*:
- _Date, specialist payment, budget with VAT (if applicable), and funnel metrics (leads to memberships)._

#### Data that can be manually filled *(green cells)*:
- _Comments (optional), budget, reach, showings, clicks, and transitions_

### How to Use
1. Enter budget and reach in green cells on the Individual Traffic Channel sheet.  
2. Review automated metrics (e.g., CAC, ROMI) in the Marketing Funnel table.  
3. Use charts to identify trends and bottlenecks.  


![Marketing Funnel Table](/Marketing_funnel/pic/marketing-sales-funnel.gif)

_The consolidated table summarizes performance across all channels for a holistic view._

---


## Technical Implementation

Built entirely in Google Sheets, this toolkit prioritizes accessibility and ease of use. Here’s how it’s structured:

- **Data Structure:** Organized to mirror the customer journey—from awareness to repeat purchases.

- **Formulas & Automation:** Uses IF, ARRAYFORMULA, SUM, COUNTIF, and QUERY to calculate conversion rates, revenue, CAC, and ROI automatically.

  ```excel
  Ad Expenses = SUMIFS(SUMMARY_BUDGET_WITH_VAT;SUMMARY_DATE;"<="&SF_COMPARSION_END;SUMMARY_DATE;">="&SF_COMPARSION_START;SUMMARY_CHANNEL;SF_CHANNEL) + SUMIFS(SUMMARY_SPECIALIST_PAYMENT;SUMMARY_DATE;"<="&SF_COMPARSION_END;SUMMARY_DATE;">="&SF_COMPARSION_START;SUMMARY_CHANNEL;SF_CHANNEL)

  Memberships = SUMIFS(SUMMARY_PREPAYMENT_FOR_FIRST_MEMBERSHIP;SUMMARY_DATE;"<="&SF_COMPARSION_END;SUMMARY_DATE;">="&SF_COMPARSION_START;SUMMARY_CHANNEL;SF_CHANNEL)

  CAC = IFERROR(Ad_Expenses / Memberships, 0) 
  // Calculates Customer Acquisition Cost, returning 0 if no memberships to avoid division errors.
  
  ROMI = IFERROR((Total_Cash_Inflows - Ad Expenses)/Ad Expenses;0)

- **Dynamic Updates:** Metrics adjust in real-time as inputs change, enabling scenario analysis.

- **Visualization:** Charts highlight funnel stages and performance trends.

- **Scalability:** Easily expandable by adding new data—no formula redesign needed.
Data Security

- **Protection:** All automatically populated cells are locked to prevent accidental changes, editable only by the owner.

- **Validation:** Manual input fields (green cells) include data validation to ensure accuracy (e.g., positive numbers for budgets, valid dates). This minimizes errors and maintains data integrity.


## Tools & Skills Applied

- ⚙️ Advanced spreadsheet techniques and formula automation.
- 📊 Data visualization for clear, actionable insights.
- 🧩 Marketing metrics (CTR, CVR, CPA, CAC, CPL).
- 📈 Channel performance analysis.
- 🧠 Business-oriented design tailored to small business needs.
- 🗂️ Structured layout for efficient decision-making.


> ### Examples of Use
> - **Optimize Ad Spend**: Identify which channels (e.g., Target Instagram) have the highest CR Lead to Purchase (e.g., 27.6%) and allocate more budget there.
> - **Identify Underperforming Channels**: Spot channels with low conversion rates (e.g., Flyers with -37.8% CR Lead to Purchase) and consider pausing or revising campaigns.
> - **Track Revenue Growth**: Use the Cash Inflows and P&L Incomes charts to monitor actual vs. planned revenue and adjust strategies accordingly.
> - **Analyze Customer Acquisition Costs**: Compare the cost per lead and cost per acquisition across channels to ensure efficient spending.

### Future Improvements  
-  **API Integration:** Auto-import data from Meta Ads.  
-  **Dashboard:** Build a Tableau/Power BI version.  
-  **Forecasting:** Add predictive modeling (ARIMA/Prophet). 

## Final Thoughts

This toolkit is more than just a spreadsheet. It’s a:

* 🧭 Strategic compass for marketing investments
* 💡 Practical analytics solution for daily decision-making
* 🚀 Scalable system built to support business growth

Whether you’re a business owner looking to optimize your marketing budget, a data professional seeking efficiency, or simply someone who appreciates the power of well-structured data — this tool delivers clarity and control.

Explore it. Analyze it. Use it to guide smarter decisions.

And remember: behind every great business move, there’s a clear, data-backed insight.

💌 If you’d like to discuss this project in more detail, share feedback, or explore collaboration — feel free to reach out or leave a ⭐ on GitHub.

Stay data-driven. Stay focused. And let your numbers work for you. 📊🚀



