# DataQualityAnalysis

##  Title
**Data Quality Analysis**

##  Description
The **DataQualityAnalysis** tool automates spatial and temporal analysis of campaign data to detect anomalies and support targeted interventions. It is part of the **GIST Analytic Toolbox** and generates key outputs such as:

- Submission clustering points  
- Multiple submissions per supervisor  
- Team-level reporting gaps  

These outputs provide **actionable insights** at the LGA, ward, and individual levels, helping to improve **data quality** and **accountability** in health campaigns through geospatial analytics.



---

## Usage
### Using the GIST Analytic Toolbox for Campaign Data Quality Analysis in **ArcGIS Pro**

This tool is compatible with campaign datasets like **e-Tally** and **MST**, or any dataset with geolocation fields.

### Requirements
- Licensed installation of **ArcGIS Pro v3.x**
- The **GIST Analytic Toolbox**
- Input **CSV data file**

---

##  Overview
The data quality component of the GIST Analytic Toolbox uses **geospatial analysis** to assess and improve the quality of campaign data in ArcGIS Pro. It enables:
- Detection of suspicious patterns and anomalies  
- Informed decision-making for campaign managers  
- Better data integrity and field accountability  

---

## Key Outputs
| Output File | Description |
|-------------|-------------|
| `stack_points_table.csv` | Identifies locations with multiple form submissions (stacked submissions) |
| `multiple_submissions_table.csv` | Supervisors who submitted more than one form per day |
| `daily_team_rate.csv` | Number of unique teams submitting forms per day |
| `team_rate.csv` | Unique teams that submitted forms during the campaign |
| `geolocation_quality.csv` | Number of inaccurate GPS submissions per LGA |

---

## Purpose
These outputs help support **targeted corrections**, enabling **more effective health campaigns** through improved data collection and field team oversight.

---

## Syntax
```text
DataQualityAnalysis (
    eTally_CSV_Table,
    Output_Folder,
    Number_of_Campaign_Days,
    Latitude_Field,
    Longitude_Field,
    Geolocation_Precision_Field,
    submission_Date_Field,
    State_Field,
    LGA_Field,
    Ward_Field,
    Team_Code_Field,
    Device_ID_Field,
    supervisor_Name_Field,
    Supervisor_Number_Field,
    Proximity_Distance_Threashold,
    Proximity_Days_Threashold,
    Time_Field_Format,
    eTally_spatial_reference,
    Projection_spatial_reference,
    {geocoordinate_capture_location_field},
    {team_type_field},
    Geolocation_Precision_Threshold,
    Geolocation_Precision_Outlier
)
