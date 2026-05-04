## US Car Accidents - Severity Prediction

---

## Context and Motivation

Traffic accidents are one of the most significant public safety challenges in the United States, costing hundreds of billions of dollars every year in economic and societal impact. A large share of these costs is driven by a relatively small number of high-severity accidents.

The **proactive approach** to road safety aims to prevent potentially unsafe conditions before they occur. To implement it effectively, it is essential to be able to **predict the likelihood and severity** of an accident from contextual variables (weather, infrastructure, time, geographic location), without requiring detailed information about the accident itself or the vehicles involved.

The provided dataset contains approximately 7.7 million accident records collected across 49 US states.

---

## Project Objectives

1. **Predictive modeling:** build a model capable of predicting the severity of an accident (`Severity`) from the features available at the time of the event. The candidate may choose whether to predict the full severity index or focus specifically on identifying critical-severity accidents (severity equal to 4).
2. **Key factor identification:** determine which variables most strongly influence accident severity and communicate the findings clearly.

---

## Dataset Schema

The CSV file contains **47 columns**. The full attribute descriptions are listed below:

### Identification and Target

| # | Column | Description |
|---|--------|-------------|
| 1 | `ID` | Unique identifier for the accident record. |
| 2 | `Severity` | **Target variable.** Accident severity on a scale of 1–4: `1` = minimal traffic impact, `4` = significant traffic impact (long delay). |

### Time

| # | Column | Description |
|---|--------|-------------|
| 3 | `Start_Time` | Start date and time of the accident (local timezone). |
| 4 | `End_Time` | Date and time when the traffic impact was cleared (local timezone). |

### Geographic Location

| # | Column | Description |
|---|--------|-------------|
| 5 | `Start_Lat` | GPS latitude of the start point. |
| 6 | `Start_Lng` | GPS longitude of the start point. |
| 7 | `End_Lat` | GPS latitude of the end point. |
| 8 | `End_Lng` | GPS longitude of the end point. |
| 9 | `Distance(mi)` | Length of the road segment affected by the accident (miles). |
| 11 | `Number` | Street number in the address. |
| 12 | `Street` | Street name. |
| 13 | `Side` | Relative side of the street (Right/Left). |
| 14 | `City` | City. |
| 15 | `County` | County. |
| 16 | `State` | State. |
| 17 | `Zipcode` | ZIP code. |
| 18 | `Country` | Country. |
| 19 | `Timezone` | Timezone based on accident location (Eastern, Central, Mountain, Pacific). |
| 20 | `Airport_Code` | Code of the nearest airport-based weather station. |

### Weather Conditions

| # | Column | Description |
|---|--------|-------------|
| 21 | `Weather_Timestamp` | Timestamp of the weather observation associated with the accident. |
| 22 | `Temperature(F)` | Temperature in Fahrenheit. |
| 23 | `Wind_Chill(F)` | Perceived temperature (wind chill) in Fahrenheit. |
| 24 | `Humidity(%)` | Relative humidity (%). |
| 25 | `Pressure(in)` | Air pressure (inches). |
| 26 | `Visibility(mi)` | Visibility in miles. |
| 27 | `Wind_Direction` | Wind direction. |
| 28 | `Wind_Speed(mph)` | Wind speed (mph). |
| 29 | `Precipitation(in)` | Precipitation amount in inches, if any. |
| 30 | `Weather_Condition` | General weather condition (rain, snow, fog, thunderstorm, etc.). |

### Points of Interest (POI) — Road Infrastructure

All of the following columns are boolean and indicate the **presence of a nearby infrastructure element** at the accident location.

| # | Column | Description |
|---|--------|-------------|
| 31 | `Amenity` | Presence of a nearby amenity. |
| 32 | `Bump` | Presence of a speed bump or hump. |
| 33 | `Crossing` | Presence of a pedestrian crossing. |
| 34 | `Give_Way` | Presence of a give-way sign. |
| 35 | `Junction` | Presence of a junction. |
| 36 | `No_Exit` | Presence of a no-exit sign. |
| 37 | `Railway` | Presence of a railway. |
| 38 | `Roundabout` | Presence of a roundabout. |
| 39 | `Station` | Presence of a station (bus, train, etc.). |
| 40 | `Stop` | Presence of a stop sign. |
| 41 | `Traffic_Calming` | Presence of traffic calming measures. |
| 42 | `Traffic_Signal` | Presence of a traffic signal. |
| 43 | `Turning_Loop` | Presence of a turning loop. |

### Light Conditions

| # | Column | Description |
|---|--------|-------------|
| 44 | `Sunrise_Sunset` | Period of day (Day/Night) based on sunrise/sunset. |
| 45 | `Civil_Twilight` | Period of day based on civil twilight. |
| 46 | `Nautical_Twilight` | Period of day based on nautical twilight. |
| 47 | `Astronomical_Twilight` | Period of day based on astronomical twilight. |

### Free Text

| # | Column | Description |
|---|--------|-------------|
| 10 | `Description` | Natural language description of the accident. |

---

## Deliverables

The candidate is free to structure the work as they see fit. At the end of the project, they should be able to answer the following three questions:

1. **What model did you train and what performance do you achieve** in predicting accident severity?
2. **What are the most important factors** influencing accident severity according to your model? Can you explain why?
3. **What operations did you perform on the dataset? What challenges did you encounter** and how did you address them?

**Deliverable:** a public GitHub repository containing the code and at least one document describing the process followed and the results obtained (notebook, report, or any other format deemed appropriate).
The candidate will be asked to present and discuss their work during the interview.

---

## Practical Notes

- The full dataset is very large. If you are not able to load to complete file, you can also work on the reduced version (1M sampled rows).
- Complete freedom in the choice of programming language and algorithmic approaches.
- Perfect results are not expected: what matters is clarity of reasoning, quality of analysis, and the ability to communicate decisions effectively.

---

*Good luck!*
