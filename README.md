# NYC_Subway_System_EDA

## Project-01: Exploratory Data Analysis (EDA) of MTA Turnstile Data:
This repo contains Project-01 data and solution at Istanbul Data Science Academy following Metis curriculum. Project-01 is about Exploratory Data Analysis (EDA) of Metropolitan Transportation Authority (MTA) Turnstile Data between November and May 2021 contains **5,242,282 rows and 11 columns** or 6-month worth of data.

**Exploratory Data Analysis (EDA):**

Exploratory Data Analysis (EDA) is an approach to analysing data set to summarise their main characteristic, often with visual methods. (Wikipedia)

**Objective and Goal:**

Let's name our street artist Arthur. He is looking to make the most of his time by maximizing his profits thanks to his talented work. He wants be at the right place at the right time. 

* Finding the overall busiest stations.
* Finding day with highest traffic per station.
* Finding time period of day with highest traffic per station.

**About MTA:**

The Metropolitan Transportation Authority is North America's largest transportation network, serving a population of 15.3 million people across a 5,000-square-mile travel area surrounding New York City through Long Island, southeastern New York State, and Connecticut.

The MTA network comprises the nation’s largest bus fleet and more subway and commuter rail cars than all other U.S. transit systems combined. The MTA's operating agencies are MTA New York City Transit, MTA Bus, Long Island Rail Road, Metro-North Railroad, and MTA Bridges and Tunnels.

Turnstile data is derived from the physical device at a Control Area (Station) used to collect fares for 
entry into the system. These fares are collected via swipes from a plastic media name MetroCard. The 
collected data is then transmitted to a mainframe application called Automated Fare Collection system 
(AFC).

**Data Collection Methodology:**

The audit register data is extracted from a central database weekly on **Saturdays** for posting. The actual register data is generated at the turnstile device **every 4 hours** at which time the device uploads the data to a central database.

The data is broken down to Daily and Hourly periods. The data is **10 digits long and will roll-over to zero (0) on over-flow**. 

Other factors that may impact the data are:

* Hardware failure where the hard drive needs to be replaced, and initialized.
* Data corruption from faulty devices, or heavy banging on the turnstile

**MTA Turnstile Data:**

Data obtained from http://web.mta.info/developers/turnstile.html.


**Field Descriptions:**

**C/A:**	Control Area (A002)

**UNIT:**	Remote Unit for a station (R051)

**SCP:**	Subunit Channel Position represents an specific address for a device (02-00-00)

**STATION:**	Represents the station name the device is located at

**LINENAME:**	Represents all train lines that can be boarded at this station

**DIVISION:**	Represents the Line originally the station belonged to BMT, IRT, or IND

**DATE:**	Represents the date (MM-DD-YY)

**TIME:**	Represents the time (hh:mm:ss) for a scheduled audit event. The four hour intervals will differ from other stations due to the need for staggering to prevent flooding the system with audit readings all at once. Systemwide, stations have been set to begin audit transmittal between 00 to 03 hours, then every 4 hours after the first audit of the day.

**DESC:**	Represent the "REGULAR" scheduled audit event (Normally occurs every 4 hours)

**ENTRIES:**	The cumulative entry register value for a device.It is a 10 digit number representing the number of entries on the specific device since its inception. Other forms 
of initialization may occur upon roll-over of the counter, erasing the memory device containing the register data, and replacing the processing device of the turnstile.

**EXITS:**	The cumulative exit register value for a device

**Findings:**

![name](https://github.com/METIS-DATA-SCIENCE-PROJECTS/NYC_Subway_System_EDA/blob/main/bar_days.png)
![name](https://github.com/METIS-DATA-SCIENCE-PROJECTS/NYC_Subway_System_EDA/blob/main/output.png)
![name](https://github.com/METIS-DATA-SCIENCE-PROJECTS/NYC_Subway_System_EDA/blob/main/station_day_heatmap.png)
