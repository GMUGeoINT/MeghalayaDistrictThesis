# MeghalayaDistrictThesis
Embedded Finalized Visualization Tool: https://gmugeoint.github.io/MeghalayaDistrictThesis/

India’s state of Meghalaya pursued its 12th, and final, Five Year Plan for state-wide economic development from 2012 – 2017 before following the central government’s directive for all Indian government bodies to cease formalized economic planning. The state set proposed metric goals for the plan’s completion, but there is no apparent public retrospective which analyzes how close the state came to achieving them. Since all goals were set at the state level, there is also a significant gap in understanding how each of Meghalaya’s 11 districts contributed to meeting metric goals. Furthermore, none of this already public data has been aggregated in a way which permits simple accessibility or analysis, especially at the district level. This thesis focuses on using geospatial data visualization, geography-driven analytics, and creating publicly available datasets. It explores an analysis of district and state level metric actuals against goals and their trends over the course of the 12th Five Year Plan. It demonstrates the creation process of a publicly available visualization tool and its associated dataset that includes the first correctly updated district-level map of Meghalaya.

<iframe width="800" height="600" src="https://app.powerbi.com/view?r=eyJrIjoiN2IxY2YyODItZjg3NC00MDNhLTljNzItNDk2NjZkNGYyNzIyIiwidCI6IjBiODMyOGNiLTZmYWMtNGIzMi04MjEzLTU0YTcxMjBmOTYxMyIsImMiOjF9" frameborder="0" allowFullScreen="true"></iframe>

FOLDER GUIDE:
original_data_files:
12YearPlanTargets.pdf: contains Meghalaya's state-level metric targets as found in column 8 for the 12th 5 Year Plan. Table produced by the Meghalaya Central Planning Department and available freely on their website.

District Level Statistics 2018.pdf: contains Meghalaya's district-level metric actuals over the course of multiple years for some of the main metrics identified in the 12th 5 Year Plan goals. 2018 Report produced by the Meghalaya Central Planning Department, Directorate of Economics & Statistics made available freely on their website.

gadm36_IND_shp.zip: contains the original district-level shapefile for the whole country, but is noticeably incorrect for Meghalaya and includes only 10 districts rather than 11 districts. It omits "East Jaintia Hills" and has it merged with "West Jaintia Hills" as a single, incorrect district.

transformed_data:
District Level Statistics 2018.xlsx: contains transposition of the original PDF report's tables into a .xlsx format that is still unusable and required further transformation. Taken from Meghalaya's district-level metric actuals over the course of multiple years for some of the main metrics identified in the 12th 5 Year Plan goals. Original 2018 Report produced by the Meghalaya Central Planning Department, Directorate of Economics & Statistics made available freely on their website. 

Master_Thesis_Table_v2 with goals.xlsx: a merged, properly formatted file which blends together the transposed District Level Statistics 2018.xlsx file information merged with the 12YearPlanTargets.pdf goals for the state. Utilized as the data foundation for the statistical portion of the PowerBI data visualization tool.

MeghalayaDistrictsBackup.qgz: thanks to the editing capabilities in QGIS, contains the correct Meghalaya map which shows all 11 districts. Based on the "gadm36_IND_shp.zip" that was then edited to include "East Jaintia Hills" by separating it from "West Jaintia Hills"

Meghalayan_Districts_2020.geojson: contains the geojson file of the correct Meghalaya map which shows all 11 districts. Based on the "MeghalayaDistrictsBackup.qgz" file which was then saved as a regular geojson file.

viz_files:
Meghalayan12thYearPlan.pbix: contains the final product that merges together the finalized "Master_Thesis_Table_v2 with goals.xlsx" file for the statistical information and the "Meghalayan_Districts_2020.geojson" file which, after being transformed twice, then needed to be uploaded into Mapbox online to be correctly ported into Power BI.
