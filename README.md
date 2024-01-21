# Cyclistic Chicago

### Description 

Cyclistic’s customers include both casual riders and annual members. Annual members are much more profitable and Cyclistic wants to maximize conversion to annual members to help secure the highest possible long-term growth for the business.
Determine how casual riders and annual members use Cyclistic bikes differently. Use these insights to provide recommendations on how to tailor Cyclistic’s marketing strategy to maximize annual member conversion.

### Problem Statement

How should Cyclistic refine its marketing strategy to maximize Annual Member conversion?

### Task

Determine how casual riders and annual members use Cyclistic bikes differently. Use these insights to provide recommendations on how to tailor Cyclistic’s marketing strategy to maximize annual member conversion.

### The Dataset

- Time Period: APR23 - JUN23
- Rows: 1,751,035
- Columns: 13

<table style="border-collapse: collapse; border-spacing: 0; margin: 0; padding: 0;">
  <tr style="margin: 0; padding: 0;">
    <td style="margin: 0; padding: 0; border: none; align: left;">
      <img src="Cyclistic Chicago Dataset Variables.png" alt="Dataset Variables" width="600" height="450" style="width:4000px;margin: 0; padding: 0; display: block;"/>
    </td>
  </tr>
</table>

[Link to Dataset](https://divvy-tripdata.s3.amazonaws.com/index.html)

### Analysis Plan

1. Import necessary libraries/modules
2. Load datasets
3. Perform initial EDA
4. Conduct data cleaning
   - Nulls
   - Duplicates
   - Outliers
   - Whitespace
   - Misspellings
   - Ensure consistent start/end station name and id pairs
5. Conduct data wrangling and feature engineering
   - Fix dtypes
   - Create variables:
     - Split Time and Date into separate variables
     - Trip Duration
     - Avg Start Lat and Avg Start Lng
     - Day of Week
     - Weekend boolean
     - Time of Day category
     - Start and End Station Combo
6. Perform full EDA, noting findings
7. Build Random Forest and XGBoost models and use feature importances to further guide EDA
8. Create Casual Rider and Annual Member customer profiles based on findings
9. Provide final recommendations/next steps

### Customer Profiles

**Members**
- Likely city residents and University of Chicago students
- More likely to take trips to non-tourist destinations
- More likely to have shorter trip durations
- More likely to travel Monday - Friday instead of on weekends
- Most traveled day of the week: Thursday
- Top Start/End station: Kingsbury St & Kinzie St (id: KA1503000043), a major business district
- Top Round Trip station: W Armitage Ave & N Sheffield Ave (id: 20254.0), near subway and bus stations
- Slightly more likely than Casual Riders to take trips earlier in the day
- Trip volumes peak in the evenings during the week and in the afternoons on the weekends
- Make up higher percentage of trips overall in non-Summer months than Summer months
- Less likely to visit more different stations
- More likely to travel more different routes (start/end station combos), except in the early mornings
- Trips per station likely to vary more widely
- Trips per route likely to vary less widely
- Not as likely as Casual Riders to take round trips
- Less likely to take round trips from more different stations
- More likely to use electric bikes than other bike types
- Not likely to use docked bikes
- Less likely than Casual Riders to take longer trips in the late morning/afternoon
- AVG lat/long location about the same as Casual Riders (just east of Goose Island)

**Casual Riders**
- Casual Riders
- Likely tourists
- More likely to take trips to tourist destinations
- More likely to have longer trip durations
- More likely to travel on the weekends
- Most traveled day of the week: Saturday
- Top Start/End station: Streeter Dr & Grand Ave (id: 13022) (also top round trip station), a top tourist destination
- Slightly more likely to take trips later in the day
- Trip volumes peak in the evenings during the week and in the afternoons on the weekends
- More likely to take trips in the Summer months
- More likely to visit more different stations
- Less likely to travel more different routes (start/end station combos), except in the early mornings
- Trips per station likely to vary less widely
- Trips per route likely to vary more widely
- Twice as likely as Members to take round trips
- More likely to take round trips from more different stations
- More likely to use electric bikes than other bike types
- More likely than Members to use docked bikes; docked bike trips have longer duration
- More likely than Members to take longer trips in the late morning/afternoon
- AVG lat/long location about the same as Members (just east of Goose Island)

### Top Recommendations

1. Determine how Annual Membership could be more attractive for tourists and make requisite additions/changes
   - consider discounted membership rates/promotions for frequent trips to top tourist destinations, on weekends, for longer trips, and for trips during the Summer months

2. Direct the majority of marketing communications to tourists and feature top tourist destinations/activities (i.e. the Navy Pier and DuSable Harbor) on the weekends in the Summer months in marketing content
   - it may be helpful to identify and target tourists who visit Chicago more than once per year
  
3. Implement partnerships with nearby tourist spot establishments for top tourist stations and advertise resulting value-added services/offers for customers who become Members

### Additional Data to Improve Recommendations

- Customer demographic and psychographic data for each Member/Casual Rider
- Unique customer IDs for trips (to follow customers from one trip to the next over time)
   - can be used to personalize marketing content for individual customers as well as further distinguish between Members/Casual Riders
- Fill in the remaining missing data for start and end locations
- Figure out why especially electric bikes are potentially causing so many nulls and fix the issue

---

### Repository/Project Files

- [Jupyter Notebook]((Jupyter)_Cyclistic_1QTR.ipynb)
- [Presentation Slides]((pdf)_Cyclistic_Slides_Chris%20Aguirre.pdf)
- [Bike Trips Spider Map Interactive Dashboard](https://public.tableau.com/app/profile/chrisaguirre/viz/CyclisticChicagoSpiderMap/Sheet1)
- [Bike Trip Start/End Station Trip Volumes Interactive Dashboard](https://public.tableau.com/app/profile/chrisaguirre/viz/CyclisticChicago_17019761911550/EndStationTripVolumes3QFY23)
- [Jupyter Notebook for Spider Map](DF1%20for%20Spider%20Map_Cyclistic.ipynb)
