
# EV-Queue
Advanced Wait Time Predictions for EV Charging Stations in Optimal Paths

**Client:**

1. Who benefits from exploring this question or building this model/system? Who is this work for specifically?

    - EV companies in the process of creating their own EV charging stations, as well as public and private companies creating EV charging networks for consumers.

**Question/Need:**

2. What is the question behind your analysis? What data science opportunity and potential application do you see? What is the purpose of the EDA you will do and the data science model you will propose?

    - The question at hand is how to reduce wait times and range anxiety for EV users in order to facilitate the adoption of EV's in the general market. Generating predicted wait times per EV charging station and using that data in Optimal Path planning will help EV users make better choices about where to stop for charging along their planned routes, as well as address congestion at individual EV charging stations by redirecting EVs to stations with less
    predicted and actual wait times at anticipated time of arrival. I propose a time series model based on past usage data in order to predict future wait times at individual stations.

**Impact:**


3. What impact are you trying to achieve? In other words, what will your work do for your client

    - I am hoping to help EV companies and EV charging station companies develop better software to facilitate the adoption of EVs amongst the general public.

4. What is your impact hypothesis?

    - By providing predicted wait time data to EVs as they create Optimal Paths based on user input, the amount of travel time and range anxiety for EV users will be reduced, as there will be fewer unknown factors at the time of arrival
    at an EV charging station.


**Data Description:**

5. What dataset(s) do you plan to use, and how will you obtain the data?

    - I will use the [Palo Alto Electric Vehicle Charging Station Usage dataset (July 2011 - Dec 2017)](https://data.cityofpaloalto.org/dataviews/244892/electric-vehicle-charging-station-usage-july-2011-dec-2017/)



6. What is an individual sample/unit of analysis in this project?

    - A single unit of analysis is a single EV charging transaction at a single EV charging station in Palo Alto. Each row of data includes time spent charging, time spent parked, energy received, energy saved, time of arrival, time of departure, transaction ending event, MAC Address of the station, port type, port number, plug type, station address, event id, and zip code of the EV user.


7. What characteristics/features do you expect to work with?

    - I expect to work with the total duration of the transaction, charging time, parked time, energy received, port type, port number, plug type, user zip code, and transaction event ending type.

**Solution Path:**

8. What is your data science solution path?

    - The solution is to use either an ARIMA model or SARIMAX model to predict wait times at individual stations based on station usage. The pattern of usage at individual statons will determine the exact time series model that will best
 predict the data.

 9. What other solution paths might be viable?

    - EV stations can provide actual wait times as EV users arrive based on the actual time customers have been waiting at the station.




**Criteria for Success:**

10. What does success look like? How specifically will you measure your results in order to determine whether your work is successful?

  - Predicted wait times can be compared to actual wait times at individual stations, and residuals for individual models can be compared. The smaller the difference between the predicted vs actual wait time, the more successful the model is. In general, the adoption of wait time data in Optimal Path modeling is the goal. Success can be measured as companies' willingness to consider wait times at EV charging stations when creating Optimal Path software for EVs.

**Assumptions and Risks:**


11. Given what you’ve said about your desired impact and the solution(s) you will use to achieve it, what are some assumptions you’re making?

    - I am assuming that wait times can be predicted based on the data I have available to me, and that wait time data will be useful for Optimal Path creation for EVs.

12. What are the risks to the approach you’ve identified?

    - I am focusing on creating wait times per station instead of wait times per network, the solution that was identified by the researchers of the article I am basing my work on. In so doing, I am taking a risk in assuming that individual EV charging stations will benefit in projecting and predicting their own wait times over having a centralized network.

**Tools::**

13. How do you intend to meet the tools requirement of the project?

    - I will be using Excel spreadsheets and Tableu to create initial projections of station usage based on the data.

14. Are you planning in advance to need or use additional tools beyond those required?

    - If time allows, I would like to learn d3 in order to animate my graphs and presentations, as well as apply a time series model to my data in order to create a prediction of wait times for individual stations in my dataset.

**MVP Goal:**

15. What would a minimum viable product (MVP) look like for this project?

  - My MVP will be a spreadsheet of the dataset I have identified, as well as initual Tableu visualizations that may be helpful for analysis.
