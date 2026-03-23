[README.md](https://github.com/user-attachments/files/26183023/README.md)
**BOB OKEYO**

DS-FT 15 HYBRID

<u>PHASE 3 PROJECT</u>

A study of car accidents in the City of Chicago to derive patterns and trends from the data so as to improve on safety on the roads.

**OBJECTIVES**

- Improving road safety standards within the city of Chicago.
- Derive and be aware of patterns from car accidents.
- Learning from data so as to understand and predict the primary     contributory cause of car accidents.


**DATASET**

I use the three datasets below for our objective

- Traffic_Crashes_-_Crashes, 
- Traffic_Crashes_-_Vehicle, 
- Traffic_Crashes_-_People

**DATA PREPARATION**

<u>Check for missing values</u>

- Total missing values: 2806299
- Total missing values: 8033367
- Total missing values: 110031395

<u>Merging the datasets</u>

- Check for common columns on People and Vehicles datasets
- Check for common columns on People-Vehicle and Crashes datasets

- Use the common columns on People and Vehicles to join the two datasets

- Join merged dataset with Crashes using common columns and named the merged dataset as final_merged

+ *CRASH_RECORD_ID*
+ *CRASH_DATE*
+ *VEHICLE_ID*

**DATA CLEANING**

- Checking for missing values
- Check missing values by percentage
- Drop the rows where core crash data is missing (the 161 outliers)
- We use CRASH_HOUR as a proxy for data that should definitely be there
- Dropping rows with missing values per column
- Convert date and time columns to datetime objects

**EXPLORATORY DATA ANALYSIS**

- Visualization of several columns

- *LIGHTING_CONDITION*
- *CRASH-MONTH*
- *CRASH_HOUR*
- *STREET NAME*
- *PRIM_CONTRIBUTORY_CAUSE*
- *CRASH_DAY_OF_WEEK*

**ONE-HOT-ENCODING SOME OF THE CATEGORICAL COLUMNS FOR MODELLING**

- *WEATHER_CONDITION*
- *LIGHTING_CONDITION*
- *DRIVER_ACTION*
- *DRIVER_VISION*
- *PRIM_CONTRIBUTORY_CAUSE*
- *ROADWAY_SURFACE_COND*

- Computing coorelation for encoded columns
- Plot heatmap to study relatioships

**MODELING, FEATURE ENGINEERING AND PERFORMING MULTIPLE CLASSIFICATION**

- Grouping one-hot encoded PRIM_CONTRIBUTORY_COLUMN for modelling 
- Modeling using multiple variables

**PLOTTING A CLASSIFICATION REPORT FOR PRIM CONTRIBUTORY CAUSE**

- Heatmap for Precision, Recall, F1-score
- Bar chart for Support (Class Imbalance)
- Precision vs Recall Comparison

To "plot this" classification report, I have visualized the three critical dimensions of your model's performance: the Metric Heatmap, the Class Imbalance, and the Precision-Recall Conflict.

**1. Classification Report Heatmap**
This heatmap provides a visual "report card." The warmer colors (Green) indicate where the model is succeeding, while the cooler/red colors indicate where it is failing.
Success: Aggressive/Illegal Driving and Unknown/Other show the strongest performance overall.
Failure: Distraction/Impairment and Environment/Vehicle are clearly lagging, showing low precision and F1-scores

**2. Class Support (The Root Cause of Inaccuracy)**
This bar chart "maps" the volume of data behind each category.
The Imbalance: W have roughly 14 times more data for "Aggressive/Illegal Driving" than we do for "Distraction/Impairment."
The Impact: Because the model has so few examples of distracted drivers to learn from, it is defaulting to the more common categories. This is the primary reason the overall accuracy dropped to 48%.

**3. Precision vs. Recall Comparison**
This plot highlights the "logic" of your model.
High Precision / Low Recall (Driver Error, Unknown): For these classes, the model is very conservative. It doesn't guess "Driver Error" often, but when it does, it's usually right (0.59-0.77 precision).
Low Precision / High Recall (Distraction, Environment): For these, the model is "over-guessing." It captures about 43% of the actual incidents, but it's wrong nearly 90% of the time it makes that prediction.\


**OBSERVATIONS**

Based on my findings, here are some interesting analyses:

**Crash Causes**: A breakdown of the PRIM_CONTRIBUTORY_CAUSE and DRIVER_ACTION shoews taht driver actions is the main contributor for car accidents. Drivers failing to yield right-of-way has over 150,000 incidences, followed closely by divers following too closely.

**Temporal Trends:** An analysis by CRASH_HOUR, CRASH_DAY_OF_WEEK, and CRASH_MONTH reaveal an interestign pattern. 

-From the analysis I have noted that the highest accidents are recorded between 2pm - 5pm with over 80,000 cases and 8am - 6pm at over 60,000 cases by the hour. This can be attributed to rush hours in the city. This analysis highlights that the volume of traffic significantly influences the frequency of crashes, with risk increasing dramatically during peak transition times.

-Fridays and Saturdays record the highest number of accidents within a week. 

-The months of May through to October record the highset number of accidents.

**RECOMMENDATIONS AND NEXT STEPS**

From the trend analysis and the predictive model, we can safely predict that car accidents are likely to occur because of the actions and behaviour of the driver.

Whereas weather conditions attribute to a signicant number of car accidents, majority of of the cases are attributed to driver actions.

Therefore, the authorities of the city of Chicago can do the following to avert car accidents.

**1.Installation of CCTV cameras on strategic intersections for recording of incidences and deterring motorists from breaking traffic rules.** 

**2.The city of Chicago authoroties has to enforce and penalize offenders to discourage breaking rules on the road.** 

**3.Speed bumps and speed limits are recommended during rush hours and during rainy and snowy seasons of the year, frequent traffic stops on the weekends for careless driving as some of the cases could be driving under the influence of alcohol.**

**4.Public sensitication on road safety and traffic laws**



