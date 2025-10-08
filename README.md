# security_monitoring_dashboard
**“What gets measured gets managed,” Peter Drucker**

In a world where financial platforms run on the speed of APIs and microtransactions, the ability to identify hidden deficiencies in real-time data is no longer a luxury but a necessity.

This lab simulates a live dashboard environment for Switch Pay, a fictional fintech company, using a custom-built Splunk lab. By generating purposefully deficient API logs, transaction logs, and firewall logs, this project shows complexity of real-world fintech infrastructure and exposes issues like misconfigurations, improper request handling, and network misbehavior.

### Data Sources

i) API Logs (api_log.csv): Captured all incoming API requests including endpoint, method, status code, and originating IP.

ii) Transaction Logs (transaction_log.csv): Captured transaction ID, user ID, status, currency, and processing location.

iii) Firewall Logs (firewall_log.csv): Logged IP traffic, access attempts, and blocked events across the network infrastructure.

### **Project Disclaimer: Synthetic Log Data**

*Please note that all data used in this project; API logs, transaction logs, and firewall logs were synthetically generated using a custom Python script. This was intentionally done to simulate realistic fintech system activity and maintain full control over data structure, volume, and behavior patterns. No real user or financial data was used at any point in this project.*

*All names, locations, user identities, and transactional data presented in this project are entirely fictional and are used solely for illustrative and educational purposes. Any resemblance to actual persons, organizations, or events is purely coincidental.*

All csv_logs generated randomly by python and ingested on Splunk can be found here: [CLICK HERE](https://drive.google.com/drive/folders/1dsgkorkwOqa9uuZMRxjkG1n9F_J2yMVR?usp=sharing)

### Objective

To implement a Splunk-based operational monitoring dashboard that exposes hidden vulnerabilities and inefficiencies across Switch Pay’s API, transaction, and firewall systems in order to improve system and infrastructural efficiency.

### Dashboard Focus

Below are the core areas on which I built this live dashboard:

i) API Endpoint Health: Tracks high-failure endpoints, unauthorized access attempts, and irregular status codes.

ii) Transaction Stability: Flags repeated failures, processing delays, or unsupported currency entries.

iii) Firewall Behavior: Flags unusual inbound traffic, port scans, and repeated IP blocks. 

### Process:

i) Data Engineering: I generated synthetic but realistic log data using Python, covering APIs, user transactions, and firewall activity.

ii) Threat Simulation: Logs were seeded with misconfigurations, missing fields, bad status codes, and malformed events to mimic common vulnerabilities.

iii) Splunk Integration: The data was thereafter ingested and structured into field/ indexes, and several dashboards were built to visualize these inefficiencies.

iv) Executive Reporting: A formal report was prepared for presentation to C-level stakeholders.

### Dashboard Solution
![image.png](attachment:359d6eab-005e-4b66-9ddf-1a5efae81efa:image.png)

ii. API Latency Trends in March

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.

![image.png](attachment:7446ea46-afbd-448b-aa77-b66005319e49:image.png)

iii. API Latency Trends in April

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.

![image.png](attachment:8aa30fac-f356-4280-8ccd-94e677fa3bb2:image.png)

iv. API Latency Trends in May

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.

![image.png](attachment:d1c32d13-0b41-4a45-a7a3-f0846e9cce01:image.png)

v. Transaction Status Breakdown

Summarized transactions by status (e.g., success, failed, pending) to assess company's operational health.

![image.png](attachment:bfdbf700-4c93-4f13-bd34-3231db783e2f:image.png)

vi. Number of Firewall Blocks in March

Visualized number of firewall blocks to understand threat patterns.

![image.png](attachment:d584c5a1-ee84-4ce7-be45-43e772bf586e:image.png)

vii. Number of Firewall Blocks in April

Visualized number of firewall blocks to understand threat patterns.

![image.png](attachment:0558acf8-6f5e-43fe-a844-95c10a1dfe28:image.png)

viii. Number of Firewall Blocks in May

Visualized number of firewall blocks to understand threat patterns.

![image.png](attachment:2e570b75-0d09-4c81-aa0c-f741d552acd8:image.png)

ix. Top Failing Transactions by Method over the last 3 months

Identified payment methods or channels most associated with failed transactions to pinpoint where the recurrent issues come from.

![image.png](attachment:fab33733-1801-40d5-ab80-c91c6627de58:image.png)

x. Top Blocked IPs over the last 3 months

Identified the most frequently blocked IP addresses, and exposed potential misconfigured or compromised internal sources.

![image.png](attachment:ddb9ad92-eaa2-466f-934d-a89650c37629:image.png)
i. API Endpoint Failure Rate

Compared failure rates across API endpoints to identify unstable or error-prone services.
