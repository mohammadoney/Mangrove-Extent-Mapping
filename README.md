# Mangrove-Extent-Mapping

Objective:
The objective of this project is to create a comprehensive and unified spatial dataset representing all mangrove forest areas across Bangladesh. This project aims to map the entire national mangrove coverage by converting raster-based mangrove data into a clean, dissolved vector polygon suitable for area calculation and further geospatial analysis.

Data Acquisition:
Administrative Boundary: The FAO GAUL (2015) dataset provided the national boundary of Bangladesh to clip the global data.
Mangrove Baseline Data: The Global Mangrove Forests Distribution (2000) dataset from Landsat served as the primary source for identifying mangrove pixels worldwide.

Data Processing:
The processing pipeline was designed to create a clean, national-level mangrove map:
Clipping: The global mangrove raster was clipped to the Bangladesh boundary.
Mask Creation: A binary mask was created where pixels classified as mangroves have a value of 1, and all other areas are 0.
Raster to Vector Conversion: The reduceToVectors function was used to convert the mangrove pixels into vector polygons.
Noise Reduction: Small, potentially erroneous polygons were filtered out using a threshold based on pixel count (count > 50).
Geometry Dissolving: All the individual mangrove polygons were merged into a single, unified geometry using the dissolve() method, creating one continuous feature representing the total mangrove forest area.

Data Analysis:
The key analytical output is the total area of mangrove forests in Bangladesh, calculated directly from the final dissolved geometry. The analysis also involved:
Quantifying the number of individual mangrove patches before the merge. 
Visualizing the national distribution of mangroves, highlighting the Sundarbans as the dominant feature.
Creating a clean, ready-to-use asset for future projects that require a precise mangrove boundary.

Potential Usage and Impact:
National Resource Inventory: Provides an authoritative map for government agencies to quantify and monitor national mangrove resources.
Conservation Planning: Essential for creating protected area boundaries and managing forest resources.
Climate Policy and Carbon Accounting: Serves as a baseline for calculating blue carbon stocks and reporting under initiatives like REDD+.
Disaster Risk Reduction: Informs coastal zone management plans by identifying where mangroves provide natural storm surge protection.
Comparative Studies: Allows for comparison with mangrove extents in other countries or with future national-level maps to assess change.
