---
layout: single
title: "Projects"
permalink: /projects/
---
# 🏫 The Real Effects of Debt Relief on Education Outcomes

## 📌 Overview
This project evaluates the long-term impact of capital investments in school infrastructure on student performance and labor market outcomes. I analyze a quasi-natural experiment in Texas, where state programs subsidized school district debt payments, providing exogenous variation in capital spending.

---

## 🎯 Objectives

- Determine whether increased capital investment improves student outcomes.
- Use causal inference techniques to identify long-term effects.
- Quantify educational and economic impacts of state-level debt support.

---

## 🧩 Data Sources

- **Texas Education Agency (TEA)** – Student-level K-12 data (1993–2011)
- **Texas Higher Education Coordinating Board (THECB)** – College outcomes
- **National Center for Education Statistics (NCES)** – School finances
- **Academic Excellence Indicator System (AEIS)** – District demographics and performance
- **U.S. Census (1990 & 2000)** – Socioeconomic controls

> Dataset includes 870 Texas school districts, with longitudinal student and financial records across more than a decade.

---

## 🛠️ Tools & Techniques

- **Languages**: Python, Stata, SQL
- **Libraries**: pandas, numpy, matplotlib, statsmodels
- **Methods**:
  - Two-stage least squares (2SLS)
  - Fixed effects panel regression
  - Difference-in-differences
  - Policy-based instrumental variable design
- **Data Engineering**:
  - Merging and cleaning multi-source administrative data
  - Imputing policy eligibility from funding formulas
  - Standardizing scores and constructing derived metrics

---

## 🧪 Methodology

### Step 1: Instrumental Variable Construction

- **Instrument**: `DTL_High × Post`
- DTL_High: High pre-policy debt-to-property-tax-levy ratio (1987–1991)
- Post: Indicator for post-policy period (1998 onward)
- Motivation: Districts with high pre-existing debt burdens are more likely to benefit from state subsidies

### Step 2: 2SLS Regression

- **First Stage**:  
  Capital spending instrumented using policy interaction  
  `Cap_{i,t} = π(DTL_High × Post) + controls + FE + ε`

- **Second Stage**:  
  Estimate impact of capital on outcomes  
  `Ȳ_{i,t} = β × Ĉap_{i,t} + controls + FE + u`

- **Outcomes Measured**:
  - Standardized test scores (reading & math)
  - Graduation & attendance rates
  - College enrollment & exam participation
  - Early-career income (ages 24–26)

---

## 📊 Key Results

| Outcome | Effect per $1,000 per pupil | Significance |
|--------|-----------------------------|--------------|
| Math test scores | +0.12 SD | ✅ Significant |
| Reading test scores | +0.06 SD | ✅ Significant |
| Graduation rate | +1.9 percentage points | ✅ Significant |
| Attendance rate | +0.12 percentage points | ✅ Significant |
| College enrollment | +0.9 percentage points | Not statistically significant |
| Early-career earnings | +2% (non-college grads) | ✅ Significant (delayed effect) |

---

## 📁 Repository Structure



# Investing in Schools: How Debt Relief Helps Students Succeed through Better Facilities

## Summary
This study examines how capital spending affects educational outcomes in debt-laden school districts. Using a quasi-natural experiment with Texas debt relief programs, I find that state-supported infrastructure investments significantly improve student performance and graduation rates. The results highlight the long-term benefits of financial intervention in school districts with limited debt capacity.

## Problem Statement
How does capital spending in debt-laden school districts impact educational outcomes?

## Data Sources
- Texas Education Agency (TEA): K-12 individual student outcomes and school district finances.
- Texas Higher Education Coordinating Board (THECB): College enrollment data.
- National Center for Education Statistics (NCES): School district income statement information.
- U.S. Census Data – Local economic indicators.

## Methodology

## Key Findings
1. Impact of Debt Relief on Capital Spending
- Debt relief programs increased capital spending by $570 per student (+22% over 3 years).

2. Educational Outcomes
- Test Scores:
A $1,000 increase per pupil in capital spending raised 8th-grade reading scores by 0.06 and math scores by 0.12 standard deviations.
Effects were delayed but long-lasting, with gains materializing 5+ years post-investment.
- Graduation & Attendance:
Graduation rates increased by 1.9 percentage points.
Attendance rates improved by 0.12 percentage points.
- College & Labor Market Outcomes:
Small but positive effects on college entrance exam participation (+1.3 p.p.) and college enrollment (+0.9 p.p.).
Early-career earnings increased by ~2% per year for non-college-educated students

## [Read more](https://thomas-s-lee.github.io/files/JMP.pdf)

