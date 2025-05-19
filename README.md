# HCAD_TAZ_METRO
## Reframing Transit Corridor Investment Readiness Through Land-Based Analysis

*Harris County Appraisal District Parcels within Houston Metro Service Area*

![Random Samplings of HCAD Parcels within METRO Service Area](REF/image.png)

Traditionally, transit planning focuses on demographic and ridership indicators to guide corridor investment. While population density and socioeconomic metrics remain important, this approach often overlooks the foundational influence of Texan **land characteristics** on both current and future transit viability. This project proposes a reframed, **land-centered methodology** to assess readiness for transit investment across the METRO Service Area.

### Objective 

To develop a **TAZ (Traffic Analysis Zone) Transit Readiness Index** rooted in the economic and structural characteristics of land—independent of population trends or current ridership—thereby enabling the agency to proactively identify high-opportunity areas for infrastructure and service investment.

### **Data Integration**

This approach merges two core datasets:

1. **Appraisal District Parcel Data (HCAD)** – capturing the physical, categorical, and valuation-based attributes of land across Harris County.
2. **Traffic Analysis Zones (TAZs)** – representing the spatial framework used in transportation modeling, capital planning, and performance tracking.



### **Analytical Model**

A **tree-based Random Forest regression model** was constructed to estimate each parcel’s economic value based on land attributes alone. Key model inputs included:

- **Generalized Land Use Code (LBCS)**
- **State Property Class Description**
- **Parcel Acreage**
- **Year of Improvement Construction**

The model’s output, a predicted **log-transformed appraised value**, serves as a **proxy for land economic intensity**—a structural indicator of how the land *should* perform given its characteristics, irrespective of demographic conditions.

By comparing the **actual appraised value** to the model’s predicted value, we derive a **residual score** that flags potential "underperformance."



### **TAZ Readiness Index**

The proposed final product is a weighted **TAZ Transit Readiness Index**, incorporating a set of factors:

| Component                        | Description                                        | Weight (TBD) |
| -------------------------------- | -------------------------------------------------- | ------------ |
| **Model Residual Score**         | Difference between predicted and actual land value |              |
| **Parcel Redevelopment Profile** | Acreage and improvement age mix                    |              |
| **Infrastructure Access**        | Proximity to arterials, transit, and utilities     |              |
| **Regulatory Alignment**         | Zoning/buildout potential vs. current use          |              |
| **Perception Proxy**             | Crime rates, vacancy patterns, nearby investment   |              |

This index identifies and ranks TAZs as **Ready**, **Emerging**, or **Constrained**, enabling targeted investment in transit-supportive infrastructure and services.
