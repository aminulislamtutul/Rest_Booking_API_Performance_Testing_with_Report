### Rest Booking API Performance Testing with Report
This project demonstrates performance testing using JMeter of tests for load testing of the API.
## Feature
- Load Testing
- Tests for GET, POST, PUT, PATCH, DELETE requests
## Technology Used
- JMeter
## Perrequisite
- Java jdk
## Installation
1. Java jdk: [download and install java jdk.](https://www.oracle.com/apac/java/technologies/downloads/)
- To verify the version of Java which version is installed
- Go to cmd and write this command:
```Console
java -version
```
2. JMeter: [download and install JMeter.](https://jmeter.apache.org/download_jmeter.cgi)
- Unzip the folder to your computer.
- Go to the Bin folder inside your JMeter folder and launch the .bat file.
-After clicking the bat file, wait a few seconds JMeter UI will be shown.
```Console
Note: Make sure that you do not close the .exe file, as that will also close JMeter UI.
```
## JMeter from command line
### Why use the command line?
- GUI consumes memory, slowing down the process.
- Integrate with any external process CI and CD.
### How is the process?
1. Go to the JMeter bin folder.
2. Go to the folder address bar, write cmd then enter. You see the command window
3. Run the Command like below:
```Console
jmeter -n -t “location of your test file” -l “location of results file.jtl”
```
- -n == non gui mode
- -t == your test file
- -l == your location result
4. Create html report end of the test. Open cmd line, go to the JMeter bin folder go to cmd.
5. Run the command like below:
```Console
jmeter -g “location of results file.jtl” -o “location of results file.html”
```
### Test Setup
The performance tests were conducted using JMeter with different levels of concurrency. Each test executed a specified number of concurrent requests with a fixed loop count to evaluate the system's response time, throughput, and error rate.
The following tests were performed:
1. 10 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~1
- Total Concurrent API Requests: 70
2. 50 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~7
- Total Concurrent API Requests: 350
3. 100 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~11
- Total Concurrent API Requests: 700
4. 200 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~23
- Total Concurrent API Requests: 1400
5. 300 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~35
- Total Concurrent API Requests: 2100
6. 400 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~46
- Total Concurrent API Requests: 2800
7. 500 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~58
- Total Concurrent API Requests: 3500
8. 600 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~70
- Total Concurrent API Requests: 4200
9. 700 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~81
- Total Concurrent API Requests: 4900
10. 800 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~93
- Total Concurrent API Requests: 5600
11. 900 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~105
- Total Concurrent API Requests: 6300
12. 1000 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~116
- Total Concurrent API Requests: 7000
13. 1200 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~140
- Total Concurrent API Requests: 8400
14. 1500 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~175
- Total Concurrent API Requests: 10500
15. 1700 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~198
- Total Concurrent API Requests: 11900
16. 2000 Concurrent Requests with 1 Loop Count:
- Average Transactions Per Second (TPS) for Total Samples: ~226
- Total Concurrent API Requests: 14000

During the test execution with 2000 concurrent requests, 219 requests experienced connection timeouts, resulting in an error rate of 1.56%.
## Test Result
The performance test results indicate that the BookingAPI on HerokuApp can handle concurrent requests up to approximately 13,000 API calls with an error rate close to zero. The tests demonstrated the system's stability and ability to process a significant number of concurrent requests while maintaining acceptable response times and throughput.

To provide more insights into the test results, reports were generated for each of the concurrent request scenarios:
- [Load Test Plan 10 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%2010%20user%2010Sec/restful_booker_10_concurrent_requests.html)
- [Load Test Plan 50 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%2050%20user%2010Sec/restful_booker_50_concurrent_requests.html)
- [Load Test Plan 100 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20100%20user%2010Sec/restful_booker_100_concurrent_requests.html)
- [Load Test Plan 200 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20200%20user%2010Sec/restful_booker_200_concurrent_requests.html)
- [Load Test Plan 300 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20300%20user%2010Sec/restful_booker_300_concurrent_requests.html)
- [Load Test Plan 400 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20400%20user%2010Sec/restful_booker_400_concurrent_requests.html)
- [Load Test Plan 500 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20500%20user%2010Sec/restful_booker_500_concurrent_requests.html)
- [Load Test Plan 600 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20600%20user%2010Sec)
- [Load Test Plan 700 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20700%20user%2010Sec/restful_booker_700_concurrent_requests.html)
- [Load Test Plan 800 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20800%20user%2010Sec/restful_booker_800_concurrent_requests.html)
- [Load Test Plan 900 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%20900%20user%2010Sec)
- [Load Test Plan 1000 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%201000%20user%2010Sec/restful_booker_1000_concurrent_requests.html)
- [Load Test Plan 1200 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%201200%20user%2010Sec/restful_booker_1200_concurrent_requests.html)
- [Load Test Plan 1500 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%201500%20user%2010Sec/restful_booker_1500_concurrent_requests.html)
- [Load Test Plan 1700 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%201700%20user%2010Sec/restful_booker_1700_concurrent_requests.html)
- [Load Test Plan 2000 user 10sec](https://github.com/aminulislamtutul/Rest_Booking_API_Performance_Testing_with_Report/tree/master/Load%20Test%20Plan%202000%20user%2010Sec/restful_booker_2000_concurrent_requests.html)

Please refer to these reports for a detailed analysis of response times, throughput, and other performance metrics observed during the tests.
## Conclusion
Based on the performance testing results, it can be concluded that the BookingAPI on HerokuApp exhibits robust performance characteristics. The system showcases impressive scalability, handling tens of thousands of concurrent API requests with a negligible error rate.
