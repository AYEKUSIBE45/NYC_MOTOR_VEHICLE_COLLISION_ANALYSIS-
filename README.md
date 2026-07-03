# NYC COLLISION ANALYSIS

## Project objective
to analyze motor vehicle collision data reported by the New York City Police Department (NYPD) from January to August 2020 to identify accident trends, temporal patterns, high-risk locations, and the leading contributing factors to road traffic collisions. The analysis aims to generate data-driven insights that can support informed decision-making, improve traffic management, and enhance road safety strategies.

## Data set used
https://docs.google.com/spreadsheets/d/1huf7nbHNZdzr4N6QUvURxeWU-G27KSYU3Kl3v_heXgw/edit#gid=1166525029

## Question 
1.Compare the % of total accidents by month. Do you notice any seasonal patterns?
2. Break down accident frequency by day of week and hour of day. Based on this data, when do accidents occur most frequently? 
 3. On which particular street were the most accidents reported? What does that represent as a % of all reported accidents? 
 4. What was the most common contributing factor for the accidents reported in this sample (based on Vehicle 1)? What about fatal accidents specifically? 
 
## Dashboard interaction
https://drive.google.com/file/d/1l_LdDLa6C_mMh2qQFWwH3OlRIMu9KgdQ/view?usp=sharing

## Process
•	Trimmed leading/trailing whitespace on all text columns and normalized empty strings to true nulls.
•	Dropped 176 rows that were exact duplicates of another row on every field except Collision ID, keeping the first occurrence.
•	Recalculated Persons Injured and Persons Killed as the sum of the Pedestrian, Cyclist and Motorist breakdown columns, treating the granular fields as the source of truth. This simultaneously fixed the 1 missing value and all 4,806 mismatched rows.
•	Recorded the 7,197 missing values as "Unknown / Bridge-Tunnel" rather than guessing a single borough, since these rows cluster on multi-borough infrastructure (bridges, tunnels, expressways) with no reliable single-borough answer.
•	Recorded as "Not at Intersection", preserving the fact that these are valid mid-block collisions rather than data errors.
•	Recoded missing Street Name as "Not Reported"; merged missing Contributing Factor into the existing "Unspecified" category to avoid two parallel "unknown" buckets.

## Dashboard screenshot 1

<img width="944" height="528" alt="NYC COLLISION DASHBOARD 1" src="https://github.com/user-attachments/assets/f134dcd1-0b13-4726-9e99-345d883ee680" />


## Dashboard screenshot 2

<img width="942" height="534" alt="NYC COLLISION DASHBOARD 2" src="https://github.com/user-attachments/assets/92b5da84-4b8d-4959-b46e-542e6d8fbea9" />

## Report
https://drive.google.com/file/d/1l_LdDLa6C_mMh2qQFWwH3OlRIMu9KgdQ/view?usp=sharing
