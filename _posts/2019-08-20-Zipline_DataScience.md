---
layout:     post
title:      Zipline Unmmaned Aerial Vehicle Data Exploration & Analysis.
subtitle:   An unstructured, independent exploratory data analysis & visulization assignment using 450+ flight datasets csv files to discern details and find patterns, business insights, engineering risks or anomalies. 
date:       2019-05-23
author:     Jiashu Miao
header-img: 
catalog: true
tags:
    - Python
    - R
    - Tableau
    - Plotly
    - Data Exploration
    - Modelling
    - Fraud Detection
    - Big Data
    - Project 
    
---



# Zipline Data Scientist Take Home Project

## Introduction

Zipline operates the world’s only drone delivery system at national scale to send urgent medicines like blood transfusions and vaccines to those in need – no matter where they live. We’re at the forefront of a logistics revolution**, designing, manufacturing, and operating our own battery powered autonomous aircraft fleet to overcome** the challenges of delivering just-in-time, lifesaving medical supplies around the world.

In this example dataset taken from our distribution center in Muhanga, we serve rural hospitals in the western half of Rwanda, delivering blood transfusions used to treat conditions like malaria anemia and postpartum hemorrhaging.**After an order is placed, an electromechanically actuated launcher accelerates one of our aircraft -** known internally as a ***"Zip"*** — at 5 g's from 0 to 30 m/s (67 mph) in less than a second. From there, the plane autonomously navigates a pre-defined route to the delivery site, drops its package, and returns to the distribution center to recover. If you're looking for more background information on Zipline before diving into the data, you can check out these videos:
- [Zipline - Impact in Rwanda](https://www.youtube.com/watch?v=dfNpQzivkJA) - Brief overview of our operations in Rwanda
- [How Rwanda Built A Drone Delivery Service](https://www.youtube.com/watch?v=jEbRVNxL44c) - In-depth study of the engineering work behind our current drone platform
- [The Super-Fast Logistics of Delivering Blood By Drone](https://www.youtube.com/watch?v=bnoUBfLxZz0) - Outline of our delivery services in Rwanda
- [In Rwanda, His Drones Are Saving Lives](https://www.youtube.com/watch?v=NBdB3G9Qvqs) - Profile of one of our first flight operators
- [Zipline's World Class Drone Safety Features](https://www.youtube.com/watch?v=QTnBm3rXmss) - A short video describing how we develop safe aircraft


**A Zip is made up of three components — a battery, wing, and body. For each flight, a flight operator selects one of each component, "asembling" the Zip immediately prior to flight, as our fulfillment operators prepare the package before it's placed in the assembled Zip.**
## The Dataset

In this directory, you'll find:
- This readme
- A `flight_XXXXX.csv` file for each flight in the dataset. Each file contains the following signals from 5 seconds prior to launch, to 15 seconds after launch, logged at approximately 50Hz:

Name | Units | Description
--- |:---:| -----:
`seconds_since_launch` | seconds | time since launch
`position_ned_m[0]` | meters | position of the zip relative to a fixed reference point in the north direction
`position_ned_m[1]` | meters | position of the zip relative to a fixed reference point in the east direction
`position_ned_m[2]` | meters | position of the zip relative to a fixed reference point in the down direction
`velocity_ned_mps[0]` | meters/second | velocity of the zip, in the north direction
`velocity_ned_mps[1]` | meters/second | velocity of the zip, in the east direction
`velocity_ned_mps[2]` | meters/second | velocity of the zip, in the down direction
`accel_body_mps2[0]` | meters/second^2 | acceleration of the zip, in the body-forward direction
`accel_body_mps2[1]` | meters/second^2 | acceleration of the zip, in the body-right direction
`accel_body_mps2[2]` | meters/second^2 | acceleration of the zip, in the body-down direction
`orientation_rad[0]` | radians | Euler (Tait-Bryan) roll of the zip
`orientation_rad[1]` | radians | Euler (Tait-Bryan) pitch of the zip
`orientation_rad[2]` | radians | Euler (Tait-Bryan) yaw of the zip
`angular_rate_body_radps[0]` | radians/second | Angular velocity of the zip, about the body-forward direction
`angular_rate_body_radps[1]` | radians/second | Angular velocity of the zip, about the body-right direction
`angular_rate_body_radps[2]` | radians/second | Angular velocity of the zip, about the body-down direction
`position_sigma_ned_m[0]` | meters | estimated standard error of position_ned_m[0], i.e. positional uncertainty in the north direction
`position_sigma_ned_m[1]` | meters | estimated standard error of position_ned_m[1], i.e. positional uncertainty in the east direction
`position_sigma_ned_m[2]` | meters | estimated standard error of position_ned_m[2], i.e. positional uncertainty in the down direction

- A `summary_data.csv` file containing the following data for each flight in the dataset:

Name | Units | Description
--- |:---:| -----:
`flight_id` | n/a | unique identifier for the flight
`battery_serial_number` | n/a | serial number of the battery
`body_serial_number` | n/a | serial number of the body
`wing_serial_number` | n/a | serial number of the wing
`commit` | n/a | git commit SHA representing the version of software
`launch_airspeed` | meters/second | airspeed of the plane during launch
`launch_groundspeed` | meters/second | groundspeed of the plane during launch
`launch_timestamp` | n/a | time string `YYYT-MM-DD HH:MM:SS CAT` where CAT, i.e. Central Africa Time, is the timezone
`preflight_voltage` | volts | dc voltage of the battery immediately prior to launch
`air_temperature` | celsius | air temperature during launch
`rel_humidity` | percentage | relative humidity during launch
`static_pressure` | pascals | static air pressure during launch
`wind_direction` | degrees | direction of the wind during launch, with 0 blowing to the north, 90 blowing to the east
`wind_magnitude` | meters/second | magnitude of the wind during launch

## The Project

This is a relatively unstructured, independent exploratory data analysis & visualization assignment. Use your skills to discern details and find patterns in the data, and show us your process in a Jupyter notebook (or similar). Ultimately, we're looking for you to communicate actionable insights — things like corrupted or missing data points, unexplained behaviors, individual outlier launches, diurnal weather patterns, poorly performing parts, etc. — to the engineering & operations team in the form of interpretable figures and tables with a short description of your findings.

## Sample Code 

---------------- 

#### [R code](https://michaelmiaomiao.github.io/webfile/Rzip.html)

![](https://michaelmiaomiao.github.io/webfile/Rzip.png)


----------------



#### [Python code](https://michaelmiaomiao.github.io/webfile/PYzip.pdf)



<object data="https://michaelmiaomiao.github.io/webfile/PYzip.pdf" type="application/pdf" width="800px" height="1200px">
    <embed src="https://michaelmiaomiao.github.io/webfile/PYzip.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="https://michaelmiaomiao.github.io/webfile/PYzip.pdf">Download PDF</a>.</p>
    </embed> 
</object>

-------------------



#### [Tableau](https://michaelmiaomiao.github.io/webfile/Tzip.pdf)



<object data="https://michaelmiaomiao.github.io/webfile/Tzip.pdf" type="application/pdf" width="800px" height="1200px">
    <embed src="https://michaelmiaomiao.github.io/webfile/Tzip.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="https://michaelmiaomiao.github.io/webfile/Tzip.pdf">Download PDF</a>.</p>
    </embed> 
</object>

-------------------

## The findings & conclusions


###  Pleae also check Tableau and Python file for more intersting fingdings.

### Here is some digest from my over-all analysis 


### Conclusion and insights

- This analysis gives me several fidings though need further study for validation:
  - The voltage has missing values
  - There are **fours** flights that their locations are weird when looking at map at launch (upper left corner, need check)
  - specific battery and body series affects the creating of missing voltage, **Avoid from using 577209618523054080 to check error** 
  - The components **are not used equally frequenly** which possibly causes overuse to affects the quality of drone system. 
  - The wing series **15SPJJJ09028064** affects the launch_airspeed and need check.
  - on 2018-09-30, only battery **15SPJJJ10056048** used the whole day and causes largest average error.  
  
### Some possible relation: 
  - the higher the air temperature, the higher the wind, and the lower the static pressue and lower humidity. 
 

 ```distance = -1.7995 * air.temperature -5.4204 * wind.magnitude  -0.0275 * static_pressure + 2.698e+03```
 
 - the unexplained behavior then make sense why `2018-09-23` has low lauch_airspeed but highest distance: the wind is small and it's pretty cold with high humidity and low pressure verfies my fidings.
 
- **So to travel longer distance in same period, beside checking the components to used at best performance, the weather matters too, and it is preferable that to fly at lower temperature with higher humidity, which might counter my common sense.**

- And hence people at Zipline can use weahter to best perform the fast delivery and power-saving drone system.

- Please refer to tableau visualizaed plots and python for more. 




	- *`physics`: rainy/cloudy has lower pressure, and lower wind and colder, but lower pressure makes techinician depressed mood therefore might cause some mistake when choosing and installing the components and monitoring the positions* 
 	- *`history` weather:2018-09-23 weather in Rwanda was cloudy and high humidity.*  
