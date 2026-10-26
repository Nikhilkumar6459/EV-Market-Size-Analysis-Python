# Electric Vehicle Market Size Analysis

## Project Overview
This project uses Python to analyze Electric Vehicle (EV) population data and explore market patterns across vehicle manufacturers, models, geographic locations, electric ranges, and vehicle types.

The analysis uses an EV population dataset containing **177,866 vehicle records and 17 fields**. It demonstrates an end-to-end data analysis workflow, including data cleaning, exploratory data analysis (EDA), statistical analysis, data visualization, geospatial clustering, and basic forecasting with model validation.

## Objectives
- Analyze EV distribution by model year, state, county, and city.
- Identify popular EV manufacturers and vehicle models.
- Compare Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs).
- Examine electric range and base MSRP distributions.
- Explore the relationship between electric range and MSRP.
- Identify geographic clusters using vehicle location coordinates.
- Build and evaluate a basic trend-projection model.
- Develop data-driven recommendations while documenting dataset limitations.

## Tools and Technologies
- **Python**
- **Jupyter Notebook**
- **Pandas** – data manipulation and cleaning
- **NumPy** – numerical operations
- **Matplotlib** – data visualization
- **Scikit-learn** – linear regression, model evaluation, and K-means clustering

## Project Workflow
1. **Data preparation:** Clean text fields, convert numeric columns, inspect missing values, and check duplicate records.
2. **Exploratory analysis:** Summarize vehicle counts by geography, model year, manufacturer, model, and EV type.
3. **Statistical analysis:** Calculate descriptive statistics for positive electric-range and MSRP values and examine their correlation.
4. **Visualization:** Create charts to compare model-year patterns, leading counties, popular makes and models, EV types, and electric-range distributions.
5. **Geospatial analysis:** Parse vehicle coordinates and apply K-means clustering to explore geographic hotspots.
6. **Forecasting and validation:** Fit a simple linear regression model to model-year record counts and evaluate its performance on held-out observations.
7. **Recommendations:** Identify insights and data limitations relevant to further EV market analysis.

## Key Findings
- **Dataset size:** 177,866 vehicle records were analyzed, with no exact duplicate rows removed.
- **Geographic concentration:** Washington State is the most represented state in the dataset.
- **Leading county:** King County has 92,740 records.
- **Leading city:** Seattle has 29,447 records.
- **Leading manufacturer:** Tesla has 79,659 records.
- **Leading model:** Tesla Model Y is the most represented model, with 35,989 records.
- **Electric range:** Among positive electric-range values, the mean is 121.8 miles and the median is 84 miles.
- **Base MSRP:** Among positive MSRP values, the mean is $57,078 and the median is $59,900.
- **Range and MSRP relationship:** The Pearson correlation is 0.406 for records with positive values in both fields, indicating a moderate positive association in this subset.

## Forecasting and Geospatial Analysis
A simple linear regression model was evaluated using held-out observations. It achieved an MAE of 20,903.5, an RMSE of 24,507.0, and an R² of -0.397. The negative R² indicates weak predictive performance, so the projections should be treated as illustrative rather than reliable forecasts.

K-means clustering was also applied to a reproducible sample of up to 10,000 vehicle coordinates, using five clusters to explore geographic patterns.

## Business Recommendations
- Use geographic vehicle counts to identify areas for deeper EV infrastructure analysis.
- Normalize vehicle counts by population and consider charging availability before comparing adoption rates.
- Analyze manufacturer, model, and EV-type distributions to understand the composition of the dataset.
- Treat zero or potentially unavailable range and MSRP values carefully.
- Use time-stamped registration data, population figures, and actual sales or revenue data for more reliable market sizing and forecasting.

## Limitations
- The dataset is a vehicle-population snapshot, not a complete measure of EV sales or market revenue.
- The data is heavily focused on Washington State, so the findings should not be generalized to the entire US EV market.
- Model year is not the same as registration year.
- Geographic record counts are not population-adjusted adoption rates.
- MSRP values may be missing, zero, or outdated.
- The forecasting model performed poorly on the held-out data.

## Project Files
- `Python_Project_EV_Market_Size_Analysis_Nikhilkumar_Ghatage.ipynb` – Jupyter Notebook containing the analysis and code.
- `Python_Project_EV_Market_Size_Analysis_Report_Nikhilkumar_Ghatage.pdf` – project report summarizing the methodology, findings, visualizations, and recommendations.
- `Electric_Vehicle_Population_Data_Excel_sheet.xlsx` – source dataset, if included in the repository.

## How to Run
1. Clone or download this repository.
2. Install the required Python libraries:
   ```bash
   pip install pandas numpy matplotlib scikit-learn openpyxl jupyter
   ```
3. Ensure the source Excel dataset is available at the file path expected by the notebook.
4. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
5. Open the EV market analysis notebook and run the cells in sequence.

## Conclusion
This project demonstrates practical Python skills in data cleaning, exploratory analysis, statistical interpretation, visualization, geospatial clustering, and model evaluation. It provides descriptive insights into the EV population represented in the dataset while highlighting why reliable market sizing requires more comprehensive, time-based registration, population, sales, and revenue data.

**Author:** Nikhilkumar Ghatage
