# Shark Attack Case Study

## Introduction

The objective of this analysis is to detect the main triggers for shark attacks in order to prevent them in the future.

### Current Database

For this analysis, we have two databases:
- The first one contains a wide range of criteria for each attack since 1845, including date, type, activity, species, age and sex of the victim, and injuries.
- The second one provides coordinates of the attacks.

After analyzing the size and structure of the databases, we observe that the first dataset mainly consists of categorical data.

### Process

To achieve our goal, the following steps will be taken:
- Remove unnecessary cells to focus on the most important criteria.
- Format the necessary cells to extract relevant information.
- Generate initial charts for each criterion to identify trends.
- Evaluate correlations and develop an algorithm to predict future attacks.

## Removal of Unnecessary Cells and Handling of Empty Cells

To focus on preventable factors and indicators of injury, we have selected the following criteria for analysis:
- Location: This includes the columns "Country" and "Area".
- Date: This includes the column "Date".
- Level of Injury: This includes the columns "Injury" and "Fatal (Y/N)".
- Activity: This includes the column "Activity".

Additionally, we removed other columns that introduced unnecessary noise. "Location" was removed because it contained highly specific and diverse locations, making it challenging to identify patterns. We decided to focus solely on "Country" and "Area". "Year" was also removed as we already had the information in the "Date" column, aiming for a more consistent dataset.

Regarding empty cells, we observed that approximately 20,000 out of 25,723 cells were empty in each column. To reduce this noise, we removed rows with empty cells in all columns, resulting in a final dataset of 6,302 rows.

## Cleaning of Necessary Cells

Given that our data is mainly categorical, we performed further cleaning and categorization of the remaining cells. The process involved the following steps:
- "Fatal (Y/N)" was categorized as "Y" or "N", and unclear information was left empty.
- "Injury" was categorized into different levels of severity (INJURY NO DETAILS, FATAL INJURY, OTHER, NO INJURY, SEVERE INJURY, MINOR INJURY). Empty cells corresponding to "Y" in the "Fatal (Y/N)" column were converted to "FATAL INJURY".
- "Activity" was categorized based on activity types (Swimming, Surfing, Fishing, OTHER, Diving, Boarding, Boating, Canoeing/Kayaking, Floating, Playing).
- "Date" was simplified to focus only on the month.
- "Country" and "Area" were further categorized, with "Area" being removed eventually. Countries were categorized based on the number of attacks, resulting in a limited number of values (USA, AUSTRALIA, AVERAGE_COUNTRY, SOUTH AFRICA, LOW_COUNTRY, NEW ZEALAND, PAPUA NEW GUINEA, BAHAMAS, BRAZIL).

After this categorization, a small number of empty cells remained. These cells were removed, leaving us with a clean and categorized dataset.

## Identifying Trends

To identify trends, we generated charts for each criterion, focusing on fatal injuries:
- Country: Australia had the highest number of fatal injuries.
- Activity: Swimming was associated with the most fatal injuries.
- Month: January had the highest number of fatal injuries.

## Conclusion

In conclusion, this analysis provided insights into the main triggers for shark attacks. Australia was found to have the highest number of fatal injuries, while swimming was the most risky activity

. January stood out as the month with the highest occurrence of fatal injuries.

Further analysis and complementary steps could include:
- Assessing the correlation between different criteria to gain a deeper understanding of the factors influencing shark attacks.
- Analyzing the geographical distribution of attacks and identifying high-risk areas.
- Incorporating additional external datasets, such as environmental or oceanographic data, to investigate the relationship between environmental factors and shark attacks.
- Developing predictive models to forecast the occurrence and severity of future shark attacks based on historical data and relevant factors.

  
