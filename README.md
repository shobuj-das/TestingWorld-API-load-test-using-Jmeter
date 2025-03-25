# API Performance Testing with Apache JMeter

## Overview
This project demonstrates the process of API performance testing using Apache JMeter. The goal is to evaluate the API's reliability, scalability, and performance under varying workloads and to identify potential bottlenecks.

## What is Performance Testing?
Performance testing is a critical process in software development that evaluates the speed, scalability, and stability of an application under different workloads. It ensures that the application meets performance benchmarks and can handle expected user traffic effectively.

### Why is Performance Testing Needed?
- **Ensures Reliability**: Identifies bottlenecks, crashes, and bugs that could affect the application's reliability.
- **Validates Scalability**: Confirms the application's ability to handle an increasing number of users or requests without performance degradation.
- **Improves User Experience**: Optimizes response times and ensures smooth functionality to enhance user satisfaction.
- **Prepares for Real-World Conditions**: Simulates peak loads and stress scenarios to evaluate performance under extreme conditions.
- **Cost Efficiency**: Detecting and resolving performance issues early reduces operational costs and prevents system downtime.

## API Documentation
[Click here](https://thetestingworldapi.com/swagger/ui/index#/)

## Apache JMeter Install and Run
- Download Apache JMeter: [Click Here](https://jmeter.apache.org/download_jmeter.cgi)
- Install JMeter
- Run the jmeter.bat file from bin folder

## Tools Used
- **Apache JMeter**: For performance testing.
- **.jtl files**: For logging test results.
- **Graphical Reports**: For result visualization.

## Test Scenarios
- Simulating 500, 800, 1000 and 1500 concurrent users accessing the API.
- Stress testing to identify the breaking point.
- Monitoring response times for GET and POST requests.
- Evaluating throughput and error rates under different workloads.

## How to Run the Tests
1. Clone this repository:
   ```bash
   https://github.com/shobuj-das/TestingWorld-API-load-test-using-Jmeter.git
   ```
2. Open the `.jmx` file in JMeter.
3. Configure API endpoints, request parameters, and user counts as needed.
4. Run the test plan.
5. View results in the JMeter Dashboard or export `.jtl` files for analysis.

## Terminal Commands for Run and Report
- Command for Run the test plan
```bash
jmeter -n -t /location/test_plan.jmx  -l /location/report/test_plan.jtl
```
- Command for Report Generate
```bash
 jmeter -g /report/test_plan.jtl -o report.html
```
Terminal must be opened from bin folder.

## Results and Analysis
concurrent user: 1000.

loop count: 1

Ramp-up period (second): 10
### Key Findings
- **Average Response Time**: 3424 ms.
- **Error Rate**: Less than 2%.
- **Peak Throughput**: 73 requests/second.
- **Breaking Point**: Observed when concurrent users exceeded 1500.

![image](https://github.com/user-attachments/assets/ac262780-3e3e-4cd4-a8ef-a39c951a6131)
![image](https://github.com/user-attachments/assets/3470a79d-fcb6-418d-9963-f24ed2bb9937)



## Conclusion
The API performed well under moderate load conditions but experienced increased response times and occasional failures during stress testing. Optimizing database queries and load balancing are recommended for improved scalability.


