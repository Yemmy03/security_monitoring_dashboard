# Security_Monitoring_Dashboard
**“What gets measured gets managed,” Peter Drucker**

This lab simulates a live dashboard environment for Switch Pay, a fictional fintech company, using a custom-built Splunk lab. By generating purposefully deficient API logs, transaction logs, and firewall logs, this project shows complexity of real-world fintech infrastructure and exposes issues like misconfigurations, improper request handling, and network misbehavior.

### Data Sources
```
i) API Logs (api_log.csv): Captured all incoming API requests including endpoint, method, status code, and originating IP.

ii) Transaction Logs (transaction_log.csv): Captured transaction ID, user ID, status, currency, and processing location.

iii) Firewall Logs (firewall_log.csv): Logged IP traffic, access attempts, and blocked events across the network infrastructure.
```
### **Project Disclaimer: Synthetic Log Data**

*Please note that all data used in this project; API logs, transaction logs, and firewall logs were synthetically generated using a custom Python script. This was intentionally done to simulate realistic fintech system activity and maintain full control over data structure, volume, and behavior patterns. No real user or financial data was used at any point in this project.*

*All names, locations, user identities, and transactional data presented in this project are entirely fictional and are used solely for illustrative and educational purposes. Any resemblance to actual persons, organizations, or events is purely coincidental.*

All csv_logs generated randomly by python and ingested on Splunk can be found here: [CLICK HERE](https://drive.google.com/drive/folders/1dsgkorkwOqa9uuZMRxjkG1n9F_J2yMVR?usp=sharing)

### Objective
```
To implement a Splunk-based operational monitoring dashboard that exposes hidden vulnerabilities and inefficiencies across Switch Pay’s API, transaction, and firewall systems in order to improve system and infrastructural efficiency.
```
### Dashboard Focus
```
Below are the core areas on which I built this live dashboard:

i) API Endpoint Health: Tracks high-failure endpoints, unauthorized access attempts, and irregular status codes.

ii) Transaction Stability: Flags repeated failures, processing delays, or unsupported currency entries.

iii) Firewall Behavior: Flags unusual inbound traffic, port scans, and repeated IP blocks. 
```
### Process:
```
i) Data Engineering: Generated synthetic but realistic log data using Python, covering APIs, user transactions, and firewall activity.

ii) Threat Simulation: Logs were seeded with misconfigurations, missing fields, bad status codes, and malformed events to mimic common vulnerabilities.

iii) Splunk Integration: The data was thereafter ingested and structured into field/ indexes, and several dashboards were built to visualize these inefficiencies.

iv) Executive Reporting: A formal report was prepared for presentation to C-level stakeholders.
```
### Dashboard Solution
i. API Endpoint Failure Rate

Compared failure rates across API endpoints to identify unstable or error-prone services.
<img width="1847" height="718" alt="image" src="https://github.com/user-attachments/assets/cc2f0859-4ee5-497b-85c5-9f3762a5d5cf" />


ii. API Latency Trends in March

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.
<img width="1854" height="721" alt="image (1)" src="https://github.com/user-attachments/assets/8f66b4f5-529d-481f-b6ca-e6553d264516" />


iii. API Latency Trends in April

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.
<img width="1852" height="718" alt="image (2)" src="https://github.com/user-attachments/assets/95e162de-93c9-4bd5-9bf6-567ba68e2ef5" />


iv. API Latency Trends in May

Tracked how long it took the API to respond in order to detect slowdowns and performance reduction.

<img width="1856" height="719" alt="image (3)" src="https://github.com/user-attachments/assets/4f624487-dd11-4874-bb42-96439f949239" />


v. Transaction Status Breakdown

Summarized transactions by status (e.g., success, failed, pending) to assess company's operational health.

<img width="1845" height="713" alt="image (5)" src="https://github.com/user-attachments/assets/229f78d1-be5e-4ca5-8a4f-607d954da7a0" />



vi. Number of Firewall Blocks in March

Visualized number of firewall blocks to understand threat patterns.

<img width="1851" height="722" alt="image (6)" src="https://github.com/user-attachments/assets/5462c806-6843-4cd2-852f-72a0447fb2b7" />



vii. Number of Firewall Blocks in April

Visualized number of firewall blocks to understand threat patterns.

<img width="1848" height="714" alt="image (8)" src="https://github.com/user-attachments/assets/2fd74a1c-256d-4005-895a-72dd6d80a066" />


viii. Number of Firewall Blocks in May

Visualized number of firewall blocks to understand threat patterns.

<img width="1857" height="723" alt="image (10)" src="https://github.com/user-attachments/assets/f3727dcb-2f66-488e-aa9e-75907948b659" />


ix. Top Failing Transactions by Method over the last 3 months

Identified payment methods or channels most associated with failed transactions to pinpoint where the recurrent issues come from.

<img width="1858" height="726" alt="image (11)" src="https://github.com/user-attachments/assets/0ace4a9e-1e3a-462a-8d1d-cef8c78f8742" />


x. Top Blocked IPs over the last 3 months

Identified the most frequently blocked IP addresses, and exposed potential misconfigured or compromised internal sources.

<img width="1819" height="598" alt="image (12)" src="https://github.com/user-attachments/assets/0f647edf-c0bb-414e-bdbd-e4eaef349a73" />

