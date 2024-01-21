# Cyclistic Chicago

### Description 

Cyclistic’s customers include both casual riders and annual members. Annual members are much more profitable and Cyclistic wants to maximize conversion to annual members to help secure the highest possible long-term growth for the business.
Determine how casual riders and annual members use Cyclistic bikes differently. Use these insights to provide recommendations on how to tailor Cyclistic’s marketing strategy to maximize annual member conversion.

### Problem Statement

How should Cyclistic refine its marketing strategy to maximize Annual Member conversion?

### Task

Determine how casual riders and annual members use Cyclistic bikes differently. Use these insights to provide recommendations on how to tailor Cyclistic’s marketing strategy to maximize annual member conversion.

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

---

### Repository/Project Files

- [Jupyter Notebook]((Jupyter)_Cyclistic_1QTR.ipynb)
- [Presentation Slides]((pdf)_Cyclistic_Slides_Chris%20Aguirre.pdf)
- [Bike Trips Spider Map Interactive Dashboard](https://public.tableau.com/app/profile/chrisaguirre/viz/CyclisticChicagoSpiderMap/Sheet1)
- [Bike Trip Start/End Station Trip Volumes Interactive Dashboard](https://public.tableau.com/app/profile/chrisaguirre/viz/CyclisticChicago_17019761911550/EndStationTripVolumes3QFY23)
- [Jupyter Notebook for Spider Map](DF1%20for%20Spider%20Map_Cyclistic.ipynb)
