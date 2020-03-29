# Lab-10 Map Description (Map created for course MAP 672, University of Kentucky, Winter session 2020)

## Identifying resources for neural tube defect prevention and treatment in Bangladesh

This description accompanies [this map](https://jfobrycki.github.io/bangladesh-healthfacilities/) that you can view on GitHub

### The map shows three important variables that may help prevent and treat neural tube defects in Bangladesh.

1. The percent of healthcare facilities that offer antenatal care everyday
2. The percent of healthcare facilities that offer folic acid tablets
3. The percent of healthcare facilities that have laboratory capabilities for ultrasounds ahd sonograms

### In considering ways to help prevent neural tube defects, these three types of data are important because:

* Mothers need access to antenatal care.
* Folic acid supplements help prevent neural tube defects.
* Ultrasounds and sonograms can identify potential neural tube defects.

### Key points from the mapped values

Aross these three variables, many divisions have high percentages of healthcare facilities that offer antenatal care and folic acid tablets, but the estimated access to ultrasounds and sonograms is lower. Access to antenatal care and folic acid supplements are both beneficial for maternal and fetal health. Lower access to imaging technology limits neural tube defect detection and could reduce the ability of healthcare providers to determine if the antenatal care and folic acid supplements are improving fetal health and development.

## Mapping steps

Data for this map was collected from two sources

1. [GADM](https://gadm.org/data.html) - for accessing a [Bangladesh shapefile](https://biogeo.ucdavis.edu/data/gadm3.6/shp/gadm36_BGD_shp.zip), specifically the administrative division layer (<i>level 1</i>) 
2. [Bangladesh Health Facility Survey 2014](https://dghs.gov.bd/images/docs/Other_Publication/Bangladesh%20Health%20Facility%20Servey%202014.pdf) - from the [Bangladesh Directorate General of Health Services](https://dghs.gov.bd/index.php/en/)

<ol>
Within the Bangladesh Health Facility survey, three tables were used:
<ol>
<li><i>Table 3.7.2 Laboratory diagnostic capacity</i> - specifically the row "Ultra-sonogram" listed by division</li>
<li><i>Table 6.1 Availability of antenatal care services</i> - specifically the column "Percentage of facilities
offering ANC where ANC services are offered on indicated days: Provides everyday" listed by division </li>
<li><i>Table 6.4 Availability of medicines for routine antenatal care</i> - specifically the column "Folic acid tablets" listed by division</li>
</ol>
</ol>

Data from the survey were transcribed into a csv file, with divisions listed by rows.

![Example table](images/TableExample.png)  

[QGIS](https://qgis.org/en/site/) was used to view the GADM file for Bangladesh, specifically the administrative level 1 layer that shows the divisions in Bangladesh. This csv file was added to QGIS.

A table join was performed using the division column to merge this new data to the division shapefiles. This picture below shows the merge was successful and the data could be visualized.

![Example map](images/MapExample.png)  

Next the dataset was exported as a GeoJSON file with a reduced number of columns from the original GADM file and the coordinate precision was set to 4. The selected CRS was EPSG:4326 - WGS84.

This GeoJSON file was exported and saved. The map was created using Leaflet.
