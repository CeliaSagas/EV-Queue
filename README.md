![Banner](https://github.com/CeliaSagas/EV-Queue/blob/1c39bc96dd561033cb5c162b8bdbf11fb56555bb/img/EV%20Queue.jpg)

# EV-Queue

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/celiasagas/ev-queue)
![GitHub issues](https://img.shields.io/github/issues-raw/celiasagas/ev-queue)
![GitHub pull requests](https://img.shields.io/github/issues-pr/celiasagas/ev-queue)
![Project Code](https://img.shields.io/github/languages/top/celiasagas/ev-queue)


<!-- Describe your project in brief -->

Electric Vehicles are a growing market that we want to encourage, but the infrastructure to support this burgeoning market just isn't quite there.

That's where EV-Queue comes in: dashboards that offer predicted wait times per station for consumers, so they can see in real time the number of spots available at each station, and self select where they'd like to go to charge their vehicle.

The idea is that by offering the information to the consumer, traffic buildups can be avoided at EV stations, which will greatly reduce range anxiety and frustration, and aid in the adoption of Electric Vehicles.

# Demo-Preview
<!-- Add a demo for your project -->

This project uses Python packages pandas and datetime, Excel, and Tableau.

![Time Series Dashboard](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/salary_hist.png)

There are weekly, monthly, daily, and hourly patterns overall and also for each individual station.


![User Dashboard](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/revenue_bar.png)

The user dashboard offers electric vehicle owners predicted wait times, number of available charging ports, average transactions, and transaction duration per time window for each station.

![Station Owner Dashboard](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/location_bar.png)

The station owner dashboard gives owners the opportunity to track transactions and revenue for each station by time window, and test out variable rate opportunities.


# Table of contents


- [Project Title](#project-title)
- [Demo-Preview](#demo-preview)
- [Table of contents](#table-of-contents)
- [Data](#Data)
- [Usage](#usage)
- [License](#license)
- [Footer](#footer)

# Data

**Data Preparation** :mag:

1.	Generated end date and time for missing data by adding transaction duration to starting time.
2.	Converted total duration timedelta to fractions of an hour
3.  Generated individual plug ID's using Station Address, Station ID, and Plug ID.
3.	Counted individual transactions for each station for each time window, counting 1) transactions that start and end in the same time window 2) transactions that start in a previous time window and end in another time window of the same day, 3) transactions that start on the previous day and end in the next (overnight)
4.	Generated elapsed time per transaction in order to identify average time for the next user to leave per station.
5. Created a variable rate model based on rates offered at PG&E for Electric Vehicle users.
6. Created user, station owner, and time series dashboards on Tableau using Palo Alto data.


# Usage
[(Back to top)](#table-of-contents)

Palo Alto Electric Vehicle Usage Data is available online:

[Electric Vehicle Usage Data](https://data.cityofpaloalto.org/dataviews/257812/ELECT-VEHIC-CHARG-STATI-83602/)


# License
[(Back to top)](#table-of-contents)

This project is designed for free and open use.

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to top)](#table-of-contents)

Here here to the age of Electricity!

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/datacoinfooter.png)
