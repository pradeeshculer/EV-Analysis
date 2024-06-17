# EV Analysis Dashboard

### Dashboard Link : https://public.tableau.com/app/profile/pradeesh.reddy/viz/EVAnalysis_17186050959750/Dashboard1?publish=yes

## Overview
This project entails creating an interactive dashboard in Tableau named "EV Analysis." The dashboard visualizes various aspects of electric vehicle (EV) data, including vehicle distribution, ownership, and type. The dataset used in this project was a CSV file containing information about EVs such as VIN, location details, model year, make, model, electric range, and more.

## Dataset
The dataset was a CSV file with the following columns:
- VIN (1-10)
- County
- City
- State
- Postal Code
- Model Year
- Make
- Model
- Electric Vehicle Type
- Clean Alternative Fuel Vehicle (CAFV) Eligibility
- Electric Range
- Base MSRP
- Legislative District
- DOL Vehicle ID
- Vehicle Location
- Electric Utility
- 2020 Census Tract

The dataset was clean and free from errors.

## Steps to Create the Dashboard

### 1. Connect to Data
1. Open Tableau.
2. Click to connect to data.
3. Load the CSV file containing the dataset.

### 2. Create Bar Chart
1. Create a bar chart to display the vehicle year versus the distinct vehicle ID count.

### 3. Create Map Visualization
1. Create a map to show the distribution of vehicle ownership across different locations.

### 4. Create Column Chart for Top 10 Counties
1. Right-click on the `County` field.
2. Click on `Create Set`.
3. Click on `Top > By Field` to filter the top 10 counties based on vehicle ownership.
4. Drag the created county set to the filters.

### 5. Apply Filter to All Worksheets
1. Right-click on the filter.
2. Click `Apply to Worksheets`.
3. Select `All using this data source`.

### 6. Create Make and Model Column Chart
1. Press `Ctrl` and click both `Make` and `Model`.
2. Click `Create Hierarchy` to create a hierarchy of these fields.
3. Drag the hierarchy to the rows.

### 7. Create Parameter for Make and Model
1. Right-click and select `Create Parameter`.
2. Set the data type to `String` and allowable values to `List`.
3. Add the necessary values and create the parameter.
4. Right-click and click on `Show Parameter Control`.
5. Create a calculated field with the expression:
   ```[Make]= [Car Make]```
6. Drag the created parameter to the filter and check `True`.

### 8. Create Donut Chart for Vehicle Type
1. Create a calculated field with the following expression:
   ```0```
2. Click `Apply` and `OK`.
3. Drag `0` into rows to bring up a pie chart.
4. Hold `Ctrl` and drag `0` again into rows to create two pie charts.
5. Right-click on the second `0` in rows and select `Dual Axis`.
6. Change the second `Sum(0)` from pie to circle and decrease the size of the circle.
7. Remove all fields from the second `Sum(0)`.
8. Increase the size of the first pie chart to create the outer ring of the donut chart.

### 9. Create Dashboard
1. Click on the dashboard icon at the bottom.
2. Drag a blank object into the workspace.
3. Bring a horizontal container to the top.
4. Add a text box at the top for titles or descriptions.
5. Select any chart, click on the horizontal container, and select `Distribute Evenly`.

## Usage
- Open the Tableau workbook (`.twb` or `.twbx` file).
- Interact with the various visualizations to explore the data.
- Use the filters and parameters to customize the views.

# Snapshot of Dashboard (Tableau Public)

![Snap of EV Dashboard](https://github.com/pradeeshculer/EV-Analysis/assets/115096109/61f4bb5c-4cf3-475e-a89b-a04930042a7d)

## Conclusion
The EV Analysis Dashboard provides valuable insights into the distribution and characteristics of electric vehicles across different regions. By leveraging Tableau's powerful visualization tools, we can explore trends and patterns in EV ownership, helping stakeholders make informed decisions. This project demonstrates the effectiveness of data visualization in making complex data more accessible and understandable.

