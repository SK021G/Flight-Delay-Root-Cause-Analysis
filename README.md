# Root Cause Analysis of US Flight Delays

## 1. Business Problem
An airline consortium is facing significant challenges with operational efficiency, leading to frequent flight delays. These delays negatively impact customer satisfaction, increase operational costs (e.g., crew overtime, passenger compensation), and damage brand reputation. This project performs a root cause analysis on a large flight dataset to identify the primary drivers of delays and provide targeted recommendations for operational improvements.

---

## 2. Analysis and Key Findings
An exploratory data analysis was conducted on a sample of **250,000 flight records** from 2015. The analysis utilized both descriptive statistics and **Random Forest Feature Importance** techniques to diagnose the root causes of delays.

#### Finding 1: Performance Varies Significantly by Airline
There is a wide variance in on-time performance across different carriers. Certain budget carriers exhibit a delay rate nearly double the industry average, indicating internal operational inefficiencies specific to their business models.

![Delay Rate by Airline](images/delay_rate_by_airline.png)

#### Finding 2: The Primary Root Cause is Systemic
Descriptive analysis of delay reasons points to a primary bottleneck: **Late Aircraft Arrival**. This single category accounts for over **40%** of all delay minutes, indicating a powerful "snowball effect" where one late incoming flight impacts subsequent departures.

#### Finding 3: Time of Day is the Strongest Predictor
To quantify the drivers of delay, a **Random Forest Classifier** was trained to predict delay status. The model's feature importance analysis identified **Scheduled Departure (Time of Day)** as the #1 predictor of delays, outweighing even the airline itself.

![Feature Importance](images/Feature_importance.png)

*Insight:* This confirms the "snowball effect" hypothesis—flights scheduled later in the day inherit delays from previous legs, making 5:00 PM departures significantly riskier than 6:00 AM departures.

---

## 3. Actionable Recommendations

Based on the findings, the following data-driven recommendations are proposed:

1.  **Focus on Turnaround Efficiency:** Since late arrivals are the main problem, the highest priority should be to optimize aircraft turnaround processes (gate operations, cleaning, refueling, boarding). A 10% improvement in turnaround time could break the chain of cascading delays.

2.  **Implement Strategic Schedule Buffers:** Review flight schedules for afternoon peak hours. Introduce slightly longer, data-informed buffers for flights scheduled after 2:00 PM to absorb accumulated delays from earlier in the day.

3.  **Conduct an Airline-Specific Deep Dive:** Pinpoint the worst-performing airlines and conduct a focused analysis on their operations at busiest hubs to identify specific bottlenecks unique to their network.

---
