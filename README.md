java c
Midterm Practice Questions
OMIS 6230 - Fall 2023
(Please practice in Excel using Analytic Solver for demand forecast and using Solver for optimization problems, which will be tested in the Midterm exam)
1.   Given data on a city’s bikesharing program, you are tasked with creating a demand forecasting model to predict the number of bikes rented during evening rush hour. A sample of the data is provided in the table below. Rigorously discuss the steps you would take to create an effective forecasting model and verify its performance given 782 data points. What exactly does the forecasting model predict; can you quantify the prediction errors? Looking at the data, what types of signals do you think you may observe? Is there any additional data you would collect to create a more precise demand prediction model? Make sure that you defend all your choices.
Day
Season
(Categorical)
Temperature (Celsius)
Humidity (%)
Windspeed (Km/h)
Bikes
Rented During Rush Hour
Bike Rentals (Day Lag)
Bike Rentals (Week Lag)
778
4
25.83
80.75
14.99963
1228
587
1840
779
4
23.165
41.75
21.00115
1496
1228
1772
780
4
22.96
62
8.249375
1773
1496
1741
781
4
23.985
61.25
9.99975
1816
1773
1781
782
4
23.37
94
10.50058
719
1816
587
2.   Suppose that the data in the previous question is from the testing set. The table below presents the demand predictions for four different forecasting models that have been fitted using the training data and then applied to the test set.
Quantitatively and qualitatively discuss which model you believe to be the most effective and why. Do you trust the predictions that each of the models produce? Finally, for each of the four forecasting models, describe the reasoning behind why you believe they achieve the accuracy/performance you observe.
Day
Holt-Winters Predictions
Exponential Smoothing   Predictions
Dynamic Linear Regression
Predictions
Boosted Regression Tree Predictions
778
1512.9
1637.2
1553.9
1758.1
779
1885.5
1635.3
1673.2
1868.3
780
1845.6
1634.7
1652.6
1760.2
781
1698.2
1636.8
1675.3
1827.0
782
1973.9
1634.6
725.1
831.4
Holt-Winters (RMSE)
Exponential
Smoothing (RMSE)
Dynamic Linear
Regression (RMSE)
Boosted Regression Trees (RMSE)
604.4555
463.6225
189.1918
294.1099
Mean = 1406.4
Standard Deviation = 403.6189
3.   A property business and development company is attempting to determine whether to expand their green power
initiative. More specifically, a few years ago they installed eighty 500W solar panels at a single commercial business plaza with the purpose of creating a new revenue stream, i.e., to sell the electricity generated by the solar panels back to the grid. You have been given a historical data set tracking the number of Watts generated per week as well as the  average weather conditions for that week. Your task is to create a demand forecasting model to predict the average weekly number of Watts generated. Perform. a time series analysis using the data set that has been provided (figures are in days); implement at least three prediction models and provide performance metrics for each model. Please summarize your overall approach and discuss which forecasting model you would recommend be implemented in practice; make sure defend your modeling choices. Finally, is there any additional data you would collect to create a more precise demand prediction model?
4.   RocketCell, a major US cellphone manufacturer, is making production plans for the coming year. RocketCell has    worked with its customers to come up with forecasts of monthly requirements (in thousands of phones) as shown in the following table.
Manufacturing is primarily an assembly operation, and capacity is governed by the number of people on the production line. The plant operates for 20 days a month, eight hours each day. One person can assemble a phone every 10 minutes. Workers are paid 20 dollars per hour and a 50 percent premium for overtime. The plant currently employs 1,250 workers. Component costs for each cellphone total 20 dollars. Carrying inventory from one month to   the next incurs a cost of 3 dollars per phone per month. RocketCell currently has a no-layoff policy in place. Overtime is limited to a maximum of 20 hours per month per employee. Assume that RocketCell has a starting inventory of 50,000 units and wants to end the year with the same level of inventory.
(1) Assuming no backlogs, no subcontracting, and no new hires (this setting is referred to the base case). (a)  Define decision variables.
(b) Formulate the mathematical model.
(c)  What is the optimum production plan that minimized the annual cost? What is the annual cost of this schedule?
(d) Is there any value for management to negotiate an increase of allowed overtime per employee per month from 20 hours to 40?
(e)  Reconsider parts (c) and (d) if RocketCell starts with only 1,200 employees. Reconsider parts (c) and (d) if RocketCell starts with 1,300 employees. What happens to the value of additional overtime as the workforce size decreases?
(2) Assume that the plant has 1,250 employees and a no-layoff policy. Overtime is limited to 20 hours per
employee per month. A third party has offered to produce cellphones as needed at a cost of $26 per unit. (a)  Define additional decision variable(s).
(b) How to formulate the mathematical model?
(c)  How should RocketCell use the third party? How does your answer change if the third party offers a price of $25 per unit?
(d)  Should RocketCell use the third party if the per unit cost is $28?
(3) Reconsider the RocketCell data in Exercise 1. Assume that the plant has 1,250 employees and a no-layoff policy. Overtime is limited to at most 20 hours per employee per month. Also assume no subcontracting option. RocketCell has a team of 50 people who are willing to work as seasonal employees. The cost of bringing them on is 800 dollars per employee, and the layoff cost is 1,200 dollars per employee.
(a)  Define the additional decision variable(s).
(b) How to formulate the mathematical model?
(c)  What is the optimal production, hiring, and layoff schedule? What is the annual cost of this schedule?
(d) Relative to having 1,250 permanent and 50 seasonal employees, will RocketCell gain significantly if it carries only 1,100 permanent employees but has 200 seasonal employees?
5.   A real estate broker is responsible for selling homes in a new development. There are two types of floor plans: Model  A and Model B. Model A requires 0.6 acres of land and Model B requires 1.0 acre of land. Twelve acres are available. The broker has orders for three Model A and three Model B homes, and the contractor has requested that no more than 10 Model A homes be sold. The broker also operates a tree nursery and wants to use at least 81 maple trees to landscape the development. Each Model A and Model B home will receive nine maple trees. The broker estimates it will cost $300,000 to sell a Model A home and $400,000 to sell a Model B home. Formulate this problem as an LP to minimize the selling cost.
6.   BubbleTech is a startup that focuses on developing applications for tablets. The company has a staff of 55
programmers and a budget of $250,000 to allocate towards developing new apps. The company is currently evaluating the feasibility of developing six new apps (information in the table).
Formulate the binary program for the situation faced by the BubbleTech considering the following conditions:
a.   Users interested in application 4 will also be interested in application 5, and viceversa. Thus, if either application 4 or application 5 is developed, the other must also be developed.
b.   The programming code for application 2 relies heavily on the code for application 4. For that reason, application 2 will be developed only if application 4 is developed.
c.   Application 3 and 5 are closely related apps. Therefore, if application 3 is developed, application 5 will not be developed, and viceversa.
d.   Given the restricted marketing capabilities of BubbleTech, the company plans to develop at most four of the pote代 写OMIS 6230 – Fall 2023 Midterm Practice Questions
代做程序编程语言ntial apps at this time.
7.   Clifton Distribution has 3 plants and 4 distribution centers. The supply capability of their plants, the demand from their distribution centers, and the distance between each location, are summarized in the table below:
Formulate the LP for Clifton assuming they want to minimize total product-miles.
8.   The city of Moosonee, Ontario is soliciting bids from 4 companies (A, B, C, and D) for 6 potential bus routes that
support the surrounding communities. Each company submits a set of bids which reflect the cost of providing service to a route for a single year. That is, let cij  represent the cost that company i says it will charge to provide service to route j. After all bids are submitted, city council must make two decisions: it must decide whether to open a route, and if so, which company should be assigned to service it. They also have restrictions:
(1)  Only one company can be assigned to a route if it is opened.
(2) Each company can be assigned to at most two bus routes.
(3) At least three bus routes must be opened.
(4) Route 2 and 5 must both be opened or not at all.
(5) Either route 3 must be opened or route 4 must be opened but not both.
(6) If company B is assigned to route 1, it cannot also provide service to route 4.
(7) If company A is assigned to route 3, it must also be assigned to route 5.
(8)  Company D must be assigned to at least one route.
The council’s objective is to minimize the total cost of providing service to all opened routes. Formulate a binary program to determine which routes to open and the optimal assignment of companies to routes.
(Since this question did not provide the cost parameters (i.e., cij), you could practice the mathematical formulation without Excel implementation.)
9.   Sidewalk Labs is developing a smart city, called Quayside, on Toronto’s Waterfront. One initiative that residents can look forward to is more affordable housing options. Specifically, each apartment complex will be constructed in a modular fashion to keep costs low. This means that although the construction process for each apartment building will be similar, the style. of each complex can be adjusted as per the needs of the community. The City of Toronto has identified N=11 separate sites and two design styles: A and B. The cost of constructing each of these apartment complexes consists of a fixed and variable component:
(a)  A fixed cost of An=10000000n is incurred if apartment style. A is chosen to be built at site n.
(b) A fixed cost of Bn=10000000(11−n) is incurred if apartment style. B is chosen to be built at site n.
(c)  If an apartment is built at site n, a cost of $50000 is incurred for each apartment unit in the building.
The City of Toronto and Sidewalk Labs architects have requirements that must be followed:
(1) A minimum of 4 and a maximum of 9 apartment buildings must be constructed.
(2) Buildings designed using style. A must have a minimum of 175 units and a maximum of 245 units.
(3) Buildings designed using style. B must have a minimum of 210 units and a maximum of 305 units.
(4) The total number of units constructed in all apartment buildings must exceed 2,400.
(5) If a building is constructed at site 4, then one must also be constructed at site 7.
(6) If a building of style. A is constructed at site 5, then a building of style. B must be constructed at site 6.
Formulate a MILP to minimize the sum of all construction costs for the City of Toronto and Sidewalk Labs.
10. Toronto City Hall is considering 14 locations on which to open safe injection clinics to combat the cities opioid crisis. The cost of opening a safe injection clinic onsite n = 1, … , 14 consists of two components:
(a)  A fixed cost $1,000,000 is incurred if and only if a safe injection clinic on site n is opened.
(b) If a clinic opens on site n, a cost $100 is incurred for every customer assigned to be served at that clinic.
The city has constraints that must be adhered for their plan to be approved by the provincial government.
(1)   At least 4000 customers must be assigned to all the cities clinics.
(2)   At most 8000 customers must be assigned to all the cities clinics.
(3)   At least 5 of the 14 clinics must be opened.
(4)   At most 14 of the 14 clinics can be opened.
(5)   Any clinic that is opened can be assigned at most 600 customers.
(6)   A clinic cannot be opened simultaneously at sites 7 and 9.
(7)   If a clinic is opened at site 2, then a clinic must be opened at site 11.
(8)   If a clinic is opened at site 8, then a clinic cannot be opened at site 10.
(9)   If a clinic is opened at site 3, then at least one clinic should be opened at site 12 or 14.
(10) If a clinic is opened at site 1, then a clinic must be opened at sites 10 and 13.
Formulate a MILP model to minimize the sum of all costs and help Toronto City Hall determine (i) which sites to open a safe injection clinic at; and (ii) how to assign customers to each open clinic.
11. Farm Boy® is Canadian grocery store based in Ottawa, Ontario that has recently decided to expand to Toronto. There are a total of 15 potential supermarket locations but it remains to determine where they should be opened and their overall size in square meters. For each location n = 1, … , 15, a fixed cost of $2,000,000 is incurred if Farm Boy®    decides to build a supermarket at that site. If a supermarket is built at site n, a variable cost of $2.00 per square meter is incurred. The company has certain requirements:
(1) At least 8 supermarkets must be built and none can exceed 23,000 square meters.
(2) At least 296,000 square meters of supermarket must be built across all stores.
(3)  If a supermarket is built at site 1, one must also be built at sites 7, 12, and 15.
(4)  The number of supermarkets built at sites 3, 5, 7, 9, 11, 13 must exactly equal 4.
(5)  The number of supermarkets built at sites 4, 6, 8, 10, and 14 cannot be less than 2.
(6) If a supermarket is opened at location 4, then one must also be opened at location 10.
(7) A supermarket must be opened at site 3 or 13 but supermarkets cannot be opened at both sites.
(8) The size of all supermarkets built at sites 6-10 must be 1.2 times greater than the size of all supermarkets built at sites 1-5 but must also be less than 3.4 times the size of all supermarkets built at sites 11-15.
Formulate a MILP model to minimize the sum of all costs for Farm Boy’s expansion to Toronto with the restriction that no more than one supermarket can be built at any of the 15 potential locations.
12. As part of a new green initiative, the Canadian government is planning on creating solar panel farms across the
country. The goal is to generate at least 10 million kW of electricity per year. They are considering 20 possible sites   that are already part of crown land. It will cost $3 million to transform. each site into a suitable area for solar farming. The government must then decide how many panels to install per site and has two choices:
(a)  Small Panels: Generate 6000 kW of electricity per year at a cost of $5000 per panel.
(b) Large Panels: Generate 20000 kW of electricity per year at a cost of $25000 per panel.
Each site has capacity for 110 small panels where large panels are three times the size of small panels. However, there are several restrictions that have been negotiated with each of the provincial governments:
(1) Exactly 3 solar panel farms must be built at sites 1-5.
(2) At most 4 solar panel farms can be built at sites 6-10.
(3) At least 2 solar panels farms must be built at sites 11-15.
(4) If a solar panel farm is built at site 16 then none can be built at sites 18-20.
(5) If a solar panel farm is built at site 17 then none can be built at sites 18-20.
(6) At each site n = 1, … ,20, the ratio small panels / large panels must beat least 10%
(7) The number of small panels that are installed, at all sites combined, should exceed 30%.
Formulate and solve a MILP model to determine at which sites to build a solar panel farm and how many small and large panels to install at each of the sites. Why do you think that, at several of the solar panel farms, not all of the capacity is being used?





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
