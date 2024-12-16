# Renewable Energy Insights Dashboard – Using Power BI

## Project Overview
The **Renewable Energy Insights Dashboard** provides a detailed and interactive platform for analyzing key renewable energy metrics. It leverages Power BI's capabilities to enable data-driven decision-making by presenting essential Key Performance Indicators (KPIs) and analytical insights.

### Key Features
- **Investments and Incentives**: Tracks funding sources and achieved incentives.
- **Employment Impact**: Highlights renewable energy's contribution to job creation.
- **Storage Efficiency & ROI**: Assesses the performance and returns of energy storage solutions.
- **Pollution Index**: Quantifies the environmental footprint of renewable energy systems.
- **Capacity Analysis**: Examines disparities between minimum and average installed capacities.
- **Dynamic Data View**: Conditionally formatted table emphasizes critical data points.

This dashboard equips stakeholders with actionable insights for advancing renewable energy projects.

## Steps to Create the Dashboard

### 1. Data Preparation
- **Load Data**: Imported raw data into Power BI.
- **Data Cleaning**: Removed errors, duplicates, and null values using Power BI's data transformation tools.
- **Feature Engineering**: Added new calculated columns for detailed analysis.

### 2. Key Calculations
#### a. Energy Return on Investment (EROI)
```DAX
EROI = DIVIDE (energy_dataset_[Energy_Production_MWh], energy_dataset_[Energy_Consumption_MWh])
```

#### b. Type of Renewable Energy
```DAX
Type of Renewable Energy = SWITCH (
    energy_dataset_[Type_of_Renewable_Energy],
    1, "Solar",
    2, "Wind",
    3, "Hydroelectric",
    4, "Geothermal",
    5, "Biomass",
    6, "Tidal",
    7, "Wave"
)
```

#### c. Grid Integration Level
```DAX
Grid Integration Level = SWITCH (
    energy_dataset_[Grid_Integration_Level],
    1, "Fully Integrated",
    2, "Partially Integrated",
    3, "Minimal Integrated",
    4, "Isolated Microgrid"
)
```

#### d. Funding Sources
```DAX
Funding Sources = SWITCH (
    energy_dataset_[Funding_Sources],
    1, "Government",
    2, "Private",
    3, "Public-Private Partnership"
)
```

#### e. Storage Efficiency
```DAX
Storage Efficiency = DIVIDE (energy_dataset_[Storage_Efficiency_Percentage], 100)
```

---

### 3. Dashboard Components
#### a. Title and Slicers
- Added a title and slicers for interactive filtering.

#### b. Cards
- **KPIs Displayed**:
  - Initial Investment
  - Total Jobs Created
  - Average Storage Efficiency
  - Average EROI
  - Average Air Pollution Index
  - Total GHG Emission Reduction

#### c. Charts
- **Bar Chart**: Total Jobs Created by Funding Sources and Renewable Energy.
- **Pie Charts**:
  - Contribution of different renewable energy types to energy production.
  - Financial investments from different funding sources.
- **Waterfall Chart**: Comparison between minimum and average installed capacity by grid integration level.

#### d. Data Table
- Includes columns:
  - Renewable Energy Type
  - Grid Integration Level
  - Air Pollution Reduction Index
  - Storage Efficiency Percentage
  - GHG Emission Reduction (CO2)

---

## Insights Summary
The Renewable Energy Insights Dashboard** provides a comprehensive overview of key metrics, including 3.77T in investments, 38M jobs created, and 378.52M GHG emissions reduced. 
The energy mix shows balanced contributions from Wind, Solar, Biomass, and Hydroelectric sources, while funding is evenly distributed among Public-Private Partnerships, Government, and Private sectors.
With an Average Storage Efficiency of 75.22% and EROI of 3.62.

The dasboard highlights strong performance but also identifies optimisation opporunitites in grid intergration and energy storage, particularly for Tidal energy. 
This tool empowers stakeholders to make data-driven decisions for sustainable energy groeth.
