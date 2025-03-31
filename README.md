

Description of the data and file structure


Data Overview

This dataset includes results from an analysis assessing the impact of removing specific road segments (links) on the global efficiency of the road network in Apulia, Italy. The analysis focuses on bridges (excluding pedestrian bridges) and other road links, considering their hierarchical classification in OpenStreetMap (OSM) and their impact on network efficiency. Additionally, the dataset includes seismic risk scores (MPS) for each road segment to evaluate the potential disruption from seismic events.

The data is divided into two main parts:

Efficiency Results for All Bridges: This file contains the results of the efficiency analysis for all bridges in the study area, before and after their removal.

Updated Road Data with Results: This file includes road data with the calculated global efficiency impact due to the removal of each road segment, including the MPS seismic risk score.

Part 1: Efficiency Results for All Bridges

This dataset focuses on the bridges within the road network and calculates the impact of removing each bridge on the overall global efficiency of the road network.

Columns:

OSM ID: Unique identifier for the road segment in OpenStreetMap (OSM).

Highway Type: The type of road segment (e.g., motorway, primary, secondary, tertiary, track) based on the OSM highway tagging system.

Buffer Distance (km): The radius around the bridge or road link, in kilometers, within which the impact on global efficiency is measured.

Original Global Efficiency: The global efficiency of the network before the removal of the bridge or road link.

New Global Efficiency: The global efficiency of the network after the removal of the bridge or road link.

Change in Efficiency: The difference in global efficiency due to the removal of the bridge or road link.

Part 2: Updated Road Data with Results

This dataset includes road segments that were analyzed for their impact on the global efficiency of the road network, with each road segment assigned an MPS score, which is a proxy for the INGV seismic risk score. The results show how the removal of each road segment affects network efficiency and seismic risk.

Columns:

Road Type: The type of road segment (e.g., motorway, track, unclassified, tertiary).

Start Latitude (start_lat): Latitude of the starting point of the road segment.

Start Longitude (start_lon): Longitude of the starting point of the road segment.

End Latitude (end_lat): Latitude of the ending point of the road segment.

End Longitude (end_lon): Longitude of the ending point of the road segment.

Start Geometry (start_geom): The geometry (Point) representing the start of the road segment (in WKT format).

End Geometry (end_geom): The geometry (Point) representing the end of the road segment (in WKT format).

Original Efficiency (original_efficiency): The global efficiency of the road network before the removal of the road segment.

New Efficiency (new_efficiency): The global efficiency of the road network after the removal of the road segment.

Change in Efficiency (change_in_efficiency_y): The change in global efficiency due to the removal of the road segment.

Percentage Change (percentage_change): The percentage change in global efficiency after the removal of the road segment.

Midpoint Latitude (lat_media): The latitude of the midpoint of the road segment.

Midpoint Longitude (long_media): The longitude of the midpoint of the road segment.


Dataset Description

Road Network Data Source:

OpenStreetMap (OSM): Road data is extracted from OpenStreetMap (OSM) in GeoJSON format, providing detailed information about road segments and their classifications (motorway, primary, secondary, etc.).

Bridges: All bridges, excluding pedestrian bridges, are retained and considered in the analysis. Bridges play a significant role in determining network resilience and connectivity.

Additional Data:

ISTAT Data: For the inner city of Foggia Province, data from ISTAT was used. This region is characterized by low population density and limited access to services, as defined in Italy's Partnership Agreement 2014-2020.

Data Applications

This dataset provides valuable insights into:

Network Resilience: The impact of removing individual road segments (particularly bridges) on the global efficiency of the road network. This helps to understand the vulnerability of the network and the consequences of potential disruptions.

Seismic Risk Assessment: The inclusion of MPS scores allows for evaluating the potential disruption in the road network due to seismic activity, offering a comprehensive view of both infrastructure resilience and environmental risks.

Urban Planning: The dataset can inform urban and infrastructure planning by identifying key road segments (especially bridges) whose removal could significantly impact network efficiency. This can guide decision-making on road maintenance, upgrades, and disaster preparedness.

Requirements for Analysis

To work with the dataset effectively, it is recommended to use tools and libraries capable of handling spatial data and performing network analysis. These include, but are not limited to:

QGIS or ArcGIS for spatial data visualization and analysis.

Python (with libraries such as Pandas, Geopandas, NetworkX, and NumPy) for advanced data processing and network modeling.

R for spatial data analysis and network resilience assessment.

Code/software

To work with the dataset effectively, the following libraries are recommended for spatial data processing, visualization, and network analysis:

GeoPandas: For handling and analyzing geospatial data in Python.

Latest Version: geo pandas==0.12.2

Folium: For interactive map visualization, which is useful for plotting geographic data.

Latest Version: folium==0.14.0

Geopy: For geocoding and geospatial queries, useful for distance calculations and address lookups.

Latest Version: geopy==2.3.0

Pandas: For data manipulation and analysis, especially for working with tabular data.

Latest Version: pandas==2.0.0

NetworkX: For the analysis of complex networks, such as calculating global efficiency and resilience of road networks.

Latest Version: networkx==3.1

Access information

Other publicly accessible locations of the data:



Data was derived from the following sources:



