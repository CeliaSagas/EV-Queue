![Header](https://github.com/CeliaSagas/EV-Queue/blob/66e64a81f41efb59c3fc9e36ea6a7e398dc73a96/img/EV%20Queue.jpg)




# EV-Queue
Optimizing Electric Vehicle Charging Stations for Increased Use

**Design**

This project is inspired by an experimental project in [Electric Vehicle Route Planning Design](https://arxiv.org/abs/2102.06503) published by Schoenberg & Dressler published on [arXiv.org](https://arxiv.org/). The researchers proposed an adaptive charging and routing strategy by employing a central charging station database that helps estimate wait times at charging stations ahead of the anticipated arrival of EV users. For this project, publicly shared [Electric Vehicle Charging Station Data](https://data.cityofpaloalto.org/dataviews/257812/ELECT-VEHIC-CHARG-STATI-83602/) was collected on 8 publicly owned Electric Vehicle Stations comprised of 59 individual plugs for Electric Vehicle charging over the course of 1 year and used to generate predicted wait times and variable rates of charge.

**Data**

The dataset contains 47,735 individual transactions with 39 features for each, 12 of which are categorical. A few feature highlights include the Start Time and End Time of a transaction, the amount kWh used, the unique station and plug identifier, and the total fee paid by the user.  Three dimensions (Station Address, Station Name, and Port Number) were combined to create unique identifiers for each charging plug at each station, and an in-depth analysis of 10 numerical features was conducted in order to create predicted wait times and apply variable rates.


**Algorithms**

**Feature Engineering**

The following transformations were performed on the data in order to support further analysis:

  1. Combined Station Address, Station Name, and Port Number to create unique ID per individual plug at each station.
  2. Converted Time Delta into fractions of an hour
  3. Derived kWh Fee and Parking Fee from Total Fee paid by user
  4. Determined a variable rate following structure set up by PG&E
  5. Created ‘Week Day’ and ‘Month’ categories from Start Date of transaction
  6. Created two hour time windows from start date of transactions
  7. Derived number of transactions initiated and number of cars still parked at the station for each station and time window


**Proposed Model**

The proposed model for this data is a SARIMA Time Series predictive model, as this data shows time series patterns on Week, Month, Day, and Time Window dimensions.

**Tools**

  - Timedelta and Pandas for initial data cleaning
  - Excel for data manipulation and feature engineering
  - Tableau for interactive visualizations

**Communication**

In addition to slides and visuals presented at the Metis Business Fundamentals final presentation, this project will be published on GitHub, Medium, Linkedin, and my personal website.


**Dashboards**

[User Dashboard - Predicted Wait Times](https://public.tableau.com/app/profile/celia.sagastume/viz/PaloAltoElectricVehicleChargingStations-UserDashboard/UserDashboard)

[Station Dashboard - Revenue](https://public.tableau.com/app/profile/celia.sagastume/viz/PaloAltoElectricVehicleChargingStations-StationDashboard/StationDashboard)

[Time Series Dashboard - Data Pattern Visualization](https://public.tableau.com/app/profile/celia.sagastume/viz/PaloAltoElectricVehicleChargingStations-TimeSeriesDashboard/EVChargingStations-TimeSeries)

**Excel Workbooks**

[Palo Alto Data for 2019 per Station](https://github.com/CeliaSagas/EV-Queue/blob/main/data/Palo_Alto_2019.xlsm)

[Palo Alto Final Sheets for Tableau](https://github.com/CeliaSagas/EV-Queue/blob/main/data/Palo_Alto_Final.xlsx)
