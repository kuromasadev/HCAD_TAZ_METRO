# HCAD_TAZ_METRO
Harris County Appraisal District Parcels within Houston Metro Service Area

### Executive Summary

Collecting and analyzing random samples of parcels to determine at any given selection: 

Data about the parcel itself
- Parcel Count Share between City of Houston vs other municipalities (incl unincorporated)
- spread of state class, land use code and building type

Data about physical access to transit
- Distance to the nearest Transit Center
- Distance to the nearest commuter park and ride 
- Distance to the nearest LRT station

Data about physical barriers to transit 
- bridges within 1 mile radius
- railroad crossings within 1 mile radius
- freeway within 1 mile radius

## Step 1: Extracting Randomized Sample of Parcel Geometries within METRO Service Area
![alt text](REF/image.png)

Independent Randomized Samples, initially set at 5, collected 500 at a time, filtering out records without geometry and skipping repeating. Each record is given a hex code, and the sample set is given an ID to prepare summaries.

Example: 
Collected 394 valid records (attempt 1)
Collected 807 valid records (attempt 2)
Collected 1210 valid records (attempt 3)

Collected 403 valid records (attempt 1)
Collected 802 valid records (attempt 2)
Collected 1220 valid records (attempt 3)

Collected 403 valid records (attempt 1)
Collected 806 valid records (attempt 2)
Collected 1217 valid records (attempt 3)

Collected 422 valid records (attempt 1)
Collected 829 valid records (attempt 2)
Collected 1242 valid records (attempt 3)

Collected 408 valid records (attempt 1)
Collected 804 valid records (attempt 2)
Collected 1198 valid records (attempt 3)

## Step 2: Extracting Collected Account Numbers and Real Property Data
Notable Observations from test 5-set samples

*Data Types between GIS and Real Property does not match*

Currency Conversion Summary:
appr_val: 12174 rows processed | 610 nulls filled | original type was float64
tot_appr_val: 12174 rows processed | 8 nulls filled | original type was object
mkt_val: 12174 rows processed | 610 nulls filled | original type was float64
tot_mkt_val: 12174 rows processed | 8 nulls filled | original type was object

*Important Column Mismatches* 
Column Mismatches Found:
HCAD_NUM vs acct_clean: 8 records do not match (0.07% of total)
state_class_y vs state_class_x: 1162 records do not match (9.54% of total)
appr_val vs tot_appr_val: 14 records do not match (0.11% of total)
mkt_val vs tot_mkt_val: 14 records do not match (0.11% of total)

## Step 3: Calculating Overlay Analysis 

## Step 4: Run a random forest model to determine the current random "snapshot" generalization of the METRO Service Area
