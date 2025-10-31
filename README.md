# Mangrove-Extent-Mapping
Created a single unified polygon geometry of ALL mangroves in Bangladesh that can be used for consistent analysis across all your projects.
1. Loaded Global Mangrove Forests Distribution dataset
2. Extracted mangrove pixels within Bangladesh boundaries
3. Converted raster pixels to vector polygons using reduceToVectors()
4. Filtered out small/noise polygons (count > 10)
5. Merged all individual polygons into one unified geometry using dissolve()
6. Exported as reusable Earth Engine Asset for all future analyses
