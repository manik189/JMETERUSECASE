# manish.tiwari
Planit
1. You are given a requirement which states 
"The system should scale to 2000 users". 
What other questions would you need to ask in order to get enough information to create a workload model. 

I will ask following question:
1.	Apart from maximum 2000 Users, other test objective identification like response time, throughput, resource utilization
2.	Insight of application understanding on below scenarios
•	Type of user using this application
•	Business scenarios of every user
•	Predicted current and expected peak load of all scenarios
•	How long peak load will continue
3.	Key scenarios identification 
•	Frequently accessed scenarios
•	Business critical scenarios
•	Resource intensive scenarios
•	Stakeholder concerning scenarios
4.	Navigation path of key scenarios
5.	Test data required for simulation of scenarios 
6.	To understand if application built for mobile devices or not 
7.	Load distribution across identified scenarios
•	If it is existing application, then asks for production server logs to identify user trends
•	Inputs of business team if it is brand new application for anticipated user behaviour 
•	User base across different region


2. How could the requirement above be expanded so that it is more descriptive and testable? Please provide an example of similar requirement which is more descriptive and testable. 
 
     Sample example of business banking application:
     Objective of application:
     Response time:
1.	After user click page should display within 1 second
2.	Any post request should not be more than 3 seconds
3.	Any integration with other downstream application should response within 5 seconds
4.	Complex data calculation on server should response within 8 seconds
Resource Utilization:
1.	Average memory and CPU utilization of DB and APP server should be lesser than 70%
2.	Maximum utilization should not be more than 90% 
Throughput:
Application should have capacity of handling 500 transactions /sec
Maximum User load:
Maximum 1000 user login to system at any point of time

User pattern:
•	Banker work in 9 to 5 shift and all user login to application between 9 to 10 AM.
•	If user login and opening legal entity page, then if user is not doing any activities, then UI will send 
•	Request to server to keep session alive and there is no timeout.
•	If user login and not open any legal entity, then session will expire after 10 minutes, and user need to login again.
•	500 user login with banker access 50 user login with admin access 350 user login with support staff
Access and 100      

     
Use cases
•	Bankers are required to create 500 New Legal entity and work on exiting 4500 existing legal entity per day
•	Support staff need to work on calculation scenarios of risk template which is associated with legal entity and expected number of operations is 4000
•	Credit managers need to approve 300 legal entities daily for business lending application
•	Admin users need to provide role and user mapping 

User spike in day:
         At the time of calculation, it is integrating with API calls and seeing sudden spike of TPS which is going 
         20 and on average it is less than 1 throughout day
  
Banker location:
•	40% bankers are working from home and 60% of bankers are working from LAN
•	Users are distributed between Sydney and Melbourne 

 
3.	As well as creating a script in a tool to do the performance testing, what other factors would need to be considered for a performance testing engagement? 

•	Performance objectives
•	Project scope in terms of duration, engagement, and scope of items to be delivered 
•	Application architecture details such as app server, dB server and integrations
•	Environment details where test to perform whether like prod and if it is shared or isolated
•	Infrastructure setup: Tool licensing (open source or paid), APM tool integration,
•	Tool infrastructure capability to induce load
•	Performance test approach: - round of testing and type of testing
•	Well defined entry and exit criteria
•	Defect management
•	Roles and responsibility 
•	Test data strategy
•	Assumption and risks
