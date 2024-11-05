# Spatial_Indexing_in-Python
![image](https://github.com/user-attachments/assets/5acf2577-4071-40d5-9a73-35d1a14eef0e)

This code performs a spatial analysis to identify roads within a 100-meter buffer around specific points and visualizes the results on a map.

# Here’s a breakdown of each part:

* Buffer Creation:

buffer_gdf is a GeoDataFrame containing circular buffer zones, each with a 100-meter radius around each point in points_reproject. This helps isolate a defined spatial area around each point of interest.

The Coordinate Reference System (CRS) of buffer_gdf matches points_reproject to ensure all spatial data aligns correctly.

* Spatial Join:

select_road uses a spatial join to find all roads in the roads_reproject layer that intersect with the 100-meter buffer zones around the points. This is achieved using predicate='intersects', which selects only the roads that touch or cross into any of the buffer zones.

* Plotting:

The buffer_gdf is plotted in blue, with a semi-transparent fill and a black edge to clearly define the buffer areas.

The select_road layer, representing roads intersecting with buffer zones, is plotted in red.

points_reproject, the original points, are displayed in green as small markers.

This layered plot visually highlights the proximity of roads to the points of interest within the buffer zones.

* Display:

plt.show() renders the combined plot, allowing for a clear visualization of which roads fall within the designated 100-meter range around each point.

This analysis helps to examine the spatial relationship between the points and nearby road segments, which could be useful for proximity studies, urban planning, or transportation analysis.
