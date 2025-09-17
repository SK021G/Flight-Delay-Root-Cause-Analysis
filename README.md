# Root Cause Analysis of US Flight Delays

## 1. Business Problem
An airline consortium is facing significant challenges with operational efficiency, leading to frequent flight delays. These delays negatively impact customer satisfaction, increase operational costs (e.g., crew overtime, passenger compensation), and damage brand reputation. This project aims to perform a root cause analysis on a large flight dataset to identify the primary drivers of delays and provide targeted recommendations for operational improvements.

---

## 2. Analysis and Key Findings
An exploratory data analysis was conducted on a sample of 200,000 flight records from 2015. The analysis identified several key factors contributing to an overall significant delay rate of nearly 18%.

#### Finding 1: Performance Varies Significantly by Airline
There is a wide variance in on-time performance across different carriers. Certain airlines exhibit a delay rate nearly double the industry average, indicating internal operational inefficiencies.

![Delay Rate by Airline](images/delay_rate_by_airline.png)

#### Finding 2: The Primary Root Cause is Systemic
The analysis of delay reasons for all delayed flights clearly points to a primary bottleneck in the system. **Late Aircraft Arrival** is the single largest contributor, responsible for over 40% of all delay minutes. This indicates a powerful "snowball effect" where one late flight impacts the subsequent departures of that same aircraft.

---
## 3. Actionable Recommendations

Based on the findings, the following data-driven recommendations are proposed to address the root causes of flight delays:

1.  **Focus on Turnaround Efficiency:** Since late arrivals are the main problem, the highest priority should be to optimize aircraft turnaround processes (gate operations, cleaning, refueling, boarding). A 10% improvement in turnaround time could significantly reduce downstream delays.

2.  **Conduct an Airline-Specific Deep Dive:** Pinpoint the worst-performing airlines and conduct a focused analysis on their operations at their busiest hubs to identify specific bottlenecks unique to their network.

3.  **Implement Strategic Schedule Buffers:** Review flight schedules on peak delay days (e.g., Mondays, Thursdays). Introduce slightly longer, data-informed buffers between flights to absorb minor initial delays and prevent the cascading "late aircraft arrival" effect.

---

## 4. How to Use This Project
1. Clone this repository to your local machine.
2. Install the required Python libraries: `pip install -r requirements.txt`
3. Open and run the `Flight_Delay_Analysis.ipynb` file in a Jupyter environment to see the full analysis.
