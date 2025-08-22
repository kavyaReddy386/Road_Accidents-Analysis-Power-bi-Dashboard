**Overview**

This Power BI dashboard provides an interactive and visual representation of road accident data. It helps analyze accident trends, causes, locations, and impact factors to support data-driven decision-making for road safety improvements.

**Objectives**

Identify high-risk locations and accident hotspots.

Analyze accident trends by time (year, month, day, hour).

Evaluate severity distribution (fatal, serious, slight).

Determine contributing factors like weather, road surface, vehicle type.

Provide insights for reducing accidents and improving road safety policies.

**Key Features**

Interactive Filters:

Date Range

Location (City, State, Region)

Vehicle Type

Weather Conditions

**Visuals & Metrics:**

**KPIs:** Total Accidents, Fatal Accidents, Casualties

**Trend Analysis:** Accidents over time

**Geospatial Map:** Accident density by region

**Severity Analysis:** Pie/Donut chart showing accident severity

**Top Causes**: Bar chart showing leading causes of accidents

**Data Sources**

**Dataset Name**: Road Accident Statistics

**Format:** CSV/Excel/Database (mention exact source)

**Columns:**

Accident Date & Time

Location (City, State, GPS Coordinates)

Weather Condition

Road Surface Condition

Vehicle Type

Accident Severity

Casualties

Technical Details

**Tool Used:** Power BI Desktop

**Data Model**

**Fact Table:** DATA

Dimension Tables: Calender

**DAX Measures:**

Total Accidents = COUNTROWS(Accidents)

Fatal Accidents = CALCULATE(COUNTROWS(Accidents), Accidents[Severity]="Fatal")

Casualties = SUM(Accidents[Number_of_Casualties])

Calender = CALENDER(MIN(Data[Accident DATE]),MAX( Data[Accident Date] ))

Year = YEAR(Calender[Date])  

Month =FORMAT(Calender[Date],”mmm”)

**Insights & Benefits**

Identify accident-prone zones for targeted interventions.

Understand seasonal and time-based accident patterns.

Correlate accident severity with weather and road conditions.

Assist government agencies and traffic authorities in reducing accidents.
