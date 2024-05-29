#Theory #steps #concepts 

# TOC
>[!SUMMARY] Table of Contents
>- [[CE 531, GIS#GIS Introduction|GIS Introduction]]
>    - [[CE 531, GIS#First Known GIS Application |First Known GIS Application ]]
>    - [[CE 531, GIS#GIS For Civil Engineers|GIS For Civil Engineers]]
>    - [[CE 531, GIS#GIS - Definition|GIS - Definition]]
>- [[CE 531, GIS#Types of GIS data|Types of GIS data]]
>    - [[CE 531, GIS#Broader Categories|Broader Categories]]
>    - [[CE 531, GIS#Topology|Topology]]
>    - [[CE 531, GIS#Topology Errors|Topology Errors]]
>- [[CE 531, GIS#Projection System|Projection System]]
>    - [[CE 531, GIS#Importance of PCS|Importance of PCS]]
>    - [[CE 531, GIS#GCS vs PCS|GCS vs PCS]]
>    - [[CE 531, GIS#Most Common PCS|Most Common PCS]]
>- [[CE 531, GIS#Spatial Analysis(https://gisgeography.com/spatial-analysis/)|Spatial Analysis(https://gisgeography.com/spatial-analysis/)]]
>- [[CE 531, GIS#GIS Software and formats|GIS Software and formats]]
>    - [[CE 531, GIS#GIS Software|GIS Software]]
>    - [[CE 531, GIS#GIS Data file formats|GIS Data file formats]]
>- [[CE 531, GIS#Remote Sensing(https://gisgeography.com/remote-sensing-earth-observation-guide/)|Remote Sensing(https://gisgeography.com/remote-sensing-earth-observation-guide/)]]
>    - [[CE 531, GIS#How it works|How it works]]
>        - [[CE 531, GIS#Parts|Parts]]
>        - [[CE 531, GIS# Data Storage| Data Storage]]
>        - [[CE 531, GIS#Land Cover Types |Land Cover Types ]]
>        - [[CE 531, GIS#Data Resolution|Data Resolution]]
>    - [[CE 531, GIS#Identifying Landcover Types|Identifying Landcover Types]]
>    - [[CE 531, GIS#Reading a Satellite Image How to Interpret a Satellite Image: Five Tips and Strategies (nasa.gov)(https://earthobservatory.nasa.gov/features/ColorImage)|Reading a Satellite Image How to Interpret a Satellite Image: Five Tips and Strategies (nasa.gov)(https://earthobservatory.nasa.gov/features/ColorImage)]]
>- [[CE 531, GIS#NDVI(https://opensourceoptions.com/remote-sensing-with-qgis-calculate-ndvi/) |NDVI(https://opensourceoptions.com/remote-sensing-with-qgis-calculate-ndvi/) ]]
>- [[CE 531, GIS#RS in Civil Engineering|RS in Civil Engineering]]
>    - [[CE 531, GIS#DEM download|DEM download]]
>- [[CE 531, GIS#Flood Simulation with GIS|Flood Simulation with GIS]]
>- [[CE 531, GIS#GPS|GPS]]
>    - [[CE 531, GIS#GPS Types|GPS Types]]
>    - [[CE 531, GIS#GPS Applications|GPS Applications]]
>    - [[CE 531, GIS#RS and GPS Integration with GIS|RS and GPS Integration with GIS]]
>    - [[CE 531, GIS#GPS receiver types|GPS receiver types]]
>        - [[CE 531, GIS#Considerations|Considerations]]
>        - [[CE 531, GIS#Using Data from GPS Receivers|Using Data from GPS Receivers]]
>- [[CE 531, GIS#Zero Dark Thirty (2011)|Zero Dark Thirty (2011)]]
>    - [[CE 531, GIS#Failure Reason|Failure Reason]]
>- [[CE 531, GIS#Applications of GIS|Applications of GIS]]
>- [[CE 531, GIS#Concepts|Concepts]]
>    - [[CE 531, GIS#Land Acquisitions|Land Acquisitions]]
>    - [[CE 531, GIS#NDVI|NDVI]]
>    - [[CE 531, GIS#Steps involved in finding Osama Bin Laden|Steps involved in finding Osama Bin Laden]]
>    - [[CE 531, GIS#Mobile Connection to field to do survey|Mobile Connection to field to do survey]]
>    - [[CE 531, GIS#Flood forecasting|Flood forecasting]]
>    - [[CE 531, GIS#GIS with transportation|GIS with transportation]]
>    - [[CE 531, GIS#GIS with water|GIS with water]]
>    - [[CE 531, GIS#GIS with Environment|GIS with Environment]]
# GIS Introduction
## First Known GIS Application 
- 1854
- Cholera broke out in Soho, London
- People dying on the street
- John Snow - a doctor. 
- Struggling to cope.
- 550 died in 2 week
- No Public sanitation
- No sewers
- River full of waste 
- People believed cholera spreading through the air (Bad Air)
- John Snow counted cholera deaths 
- Mapped them along with water pumps
- Map revealed the actual cause 
- Most deaths around the Broad Street water pump
- Relation between cholera and water is thus [reviled](https://www.youtube.com/watch?v=lNjrAXGRda4&pp=ygUgc29obyBsb25kb24gZHIgaG9uIHNobm93IGhhcnZhcmQ%3D)
- 616 died in total
- John became the father of epidemiology
- GIS is used
## GIS For Civil Engineers
- Civil engineering projects have a physical dimension and occupy space
- Interacts with everything else around it, such as roads, buildings, crop field, rivers, and people's homes.
- while Implementing a project, we must know how it is going to interact with its surrounding objects
	- Minimize adverse impacts
	- Identify the most efficient way of design, construction, management, and monitoring

## GIS - Definition
- A database containing geographic data
	- Descriptions of phenomena for which location is relevant
	- Software tools for managing, analyzing, and visualizing those data
- GIS will have locational information, such as x,y coordinates or Latitude, Longitude
- GIS database includes the following locational information:
	- Points (x,y) – minimum requirement. Example: Water wells.
	- Lines – Points (x,y) and group of points making a line. Example: Road network
	- Area – Points (x,y), group of points making a line, group of lines making an area. Example: district boundaries



# Types of GIS data
## Broader Categories
- Two Categories
	- Spatially referenced data
		- represented by vector and raster forms (including imagery) Location data
	- Attribute data
		- represented in tabular format
	- Spatial referenced – Vector and Raster
		- Raster –Grids (scanned image, photograph, satellite image, represented with a grid pattern, continuous surface)
		- Vector –Points, lines, polygons (data represented with x,y coordinates, Property lines, Transportation)![[Pasted image 20240527005837.png]] ![[Pasted image 20240527005847.png]]![[Pasted image 20240527005852.png]]
		- Network (Lines and links, Turn prohibitions, Node-related delays)
## Topology
- Connect points, Lined and Polys
- The spatial relationships between connecting or adjacent vector features points, polylines, and polygons 
- Set of mathematical rules that connect the features together 
## Topology Errors
![[Pasted image 20240527010013.png]]
![[Pasted image 20240527010017.png]]
- Undershoots (vector lines that should connect to each other don’t quite touch.)
- Overshoots (a line ends beyond the line it should connect to.)
- Slivers (vertices of two polygons do not match up on their borders)
# Projection System
Projection system is the way to ==convert an area== on the earth’s (almost spherical) surface to a paper (flat surface). 
Distortions
- Area
- Shape
- Distance
- Direction
Three basic ways to transfer a curved surface to a plane
- Cylindrical 
- Conic
- Planer
- And many combinations of these
Projection systems model the earth with the following
- Undulation of the earth’s surface – Geoid
- Shape of the earth – Ellipsoid
- Modeling the undulations with a mathematical model – Datum
![[Pasted image 20240527010512.png]]
![[Pasted image 20240527010517.png]]
## Importance of PCS
- The earth has a Geographic Coordinate System (GCS) – Latitude/Longitude (Lat/Lon)
- In GIS, A GCS point is converted to PCS point (x,y coordinates)
- For measurement of distance, direction, shape and area
- Correct relationship between two different maps is important
- The same place can have different coordinate values for different GCS Datum
- PCS - A reference system for identifying locations and measuring features on a flat (map) surface
	- Consists of lines that intersect at right angles, forming a grid
	- PCS components
		- an origin
		- an x-axis
		- a y-axis, and
		- a linear unit of measure
	![[Pasted image 20240527010910.png]]
## GCS vs PCS
| GCS                                                  | PCS                                       |
| ---------------------------------------------------- | ----------------------------------------- |
| consists of: Datum (which includes the<br>ellipsoid  | consists of: Geographic Coordinate System |
| Prime Meridian (almost always<br>Greenwich, England) | Projection Method                         |
| Units (always degrees)                               | Projection Parameters                     |
|                                                      | Units                                     |
|                                                      |                                           |
## Most Common PCS
- Universal Transverse Mercator (UTM)
	- Preserves angles and shapes
	- Bangladesh lies between 87 degrees and 93 degrees East, split between
		- Zone 45: 84 to 90 E
		- Zone 46: 90 to 96E
- Two special grids
	- Bangladesh Transverse Mercator (BTM)
	- Bangladesh Universal Transverse Mercator (BUTM)
Geographic coordinate limits 20.5o to 26.5o N latitude, 88o to 93o E
- Lambert Conformal Conic
	- Used by LGED, RHD
	- Preserves direction
- [Cassini ](https://epsg.io/?q=Bangladesh%20kind:PROJCRS&page=3)(also called Cassini-Soldner) Projection System
	- Used for Mouza Maps and cadastral survey
	- Used by DLRS
	- Preserves area and size for small plots
# [Spatial Analysis](https://gisgeography.com/spatial-analysis/)
- Buffer analysis
	- Generates a polygon around features at a set distance. ![[Pasted image 20240527012123.png]]
- Clip tool
	- Cuts out an input layer to a defined feature boundary.![[Pasted image 20240527012130.png]]
- Merge tool
	- Combines data from multiple sources, then adds them into a new data set.![[Pasted image 20240527012141.png]]
- Dissolve tool
	- Unifies adjacent boundaries based on common attribute values![[Pasted image 20240527012148.png]]
- Intersect tool
	- Performs a geometric overlap with all overlapping features becoming part of the output feature class.![[Pasted image 20240527012155.png]]
- Union tool
	- Combines input data layers into a single composite layer, preserving the boundaries and attributes from all input features. ![[Pasted image 20240527012231.png]]
- Erase tool
	- Removes the area that is overlapping with the erasing features.![[Pasted image 20240527012517.png]]
- Append tool
	- Adds data from one or more sources and puts it into an existing target data set![[Pasted image 20240527013307.png]]
- Spatial join
	- Inserts the columns from one feature table to another based on location or proximity.![[Pasted image 20240527013441.png]]
- Relational join ![[Pasted image 20240527013506.png]]
# GIS Software and formats
## GIS Software
- Open-Source GIS 
	-  QGIS
		- Free and open-source cross-platform desktop GIS application
		- Supports viewing, editing, printing, and analysis of geospatial data
		- Cross-platform compatibility – Windows, Linux, Mac OS, Android
	- GRASS – by US Army Corps of Engineers. Used by Academia, environment consultants, and government agencies (NASA, NOAA, USDA, and USGS). Good in image processing.
	- TerrSet (formerly IDRISI) – GIS and remote sensing software. Good for image processing.
	- Whitebox GAT – good for image processing
- Proprietary
	- ArcGiS: proprietary by ESRI
		- High prices for the products
	- MapInfo – by Precisely
	- Geomedia – by Hexagon Geospatial
	- Global Mapper – by Blue Marble
	- SuperGIS – by Supergeo Technologies
	- AutoCAD Map 3D – by Autodesk
	- SuperMap – by SuperMap Software – Chinese
		- Large and powerful software
		- Many advanced features – more than ArcGIS or QGIS
## GIS Data file formats
- ESRI Shapefile
	- Most common geospatial file type
	- Industry standard
	- All commercial and open source accept shapefile as a GIS format
	- Needs minimum three files to make up a shapefile
		- SHP is the feature geometry.
		- SHX is the shape index position.
		- DBF is the attribute data.
- Geographic JavaScript Object Notation (GeoJSON)
	- Mostly for web-based mapping
	- Stores coordinates as text in JavaScript Object Notation (JSON) form.
- Google Keyhole Markup Language (KML/KMZ)
	- This GIS format is XML-based and is primarily used for Google Earth
- [OpenStreetMap](https://www.openstreetmap.org/) OSM XML
	- OSM files are the native file for OpenStreetMap
- Topologically Integrated Geographic Encoding and Referencing (TIGER)
	- Used by the United States Census Bureau
	- Can merge census data sources with the TIGER files
	- Available without cost – public domain
- ERDAS Imagine
	- Commonly used for raster data to store satellite data
	- Proprietary
- GeoTIFF
	- Public domain metadata standard
	- Allows georeferencing information to be embedded within a TIFF file
- GeoPackage
	- GeoPackage (GPKG) – emerging standard
	- Open, non-proprietary, platform-independent and standards-based data format
	- Defined by the [[Open Geospatial Consortium (OGC)]]
	- Can contain anything from vectors, tiles, raster, and layer attributes
	- Easy to share because it’s all contained in a single file.
# [Remote Sensing](https://gisgeography.com/remote-sensing-earth-observation-guide/)
Science of obtaining the physical properties of an area without being there Technology for obtaining information about a target through the analysis of data acquired from a distance.
## How it works
- A sensor takes photographs from a distance
- Electromagnetic signals from objects hits the sensor
- These signals create electronic signals
- Electronic signals are translated into image files
### Parts
- targets - objects or phenomena in an area;
- data acquisition - through specific instruments (sensors); and
	- Passive remote sensing
		- Passive sensors gather radiation emitted or reflected by objects or surrounding areas
		- Reflected sunlight is the most common source of radiation measured by passive sensors.
		- Examples: film photography, infrared
	- Active remote sensing
		- Active sensors emit energy to scan objects and areas, whereupon a sensor detects and measures the radiation reflected or backscattered from the target.
		- RADAR – Radio Detection and Ranging
		- LiDAR – Light Detection and Ranging
	- • aircrafts, • satellites, • balloons, • rockets, • space shuttles
	- ![[Pasted image 20240527113015.png]]
	- 
- data analysis and presentation in the form of an image – with software.
###  Data Storage
A rectangle is divided into rows and columns forming cells or grid points. One number for each cell (or grid point) ![[Pasted image 20240527113226.png]]
### Land Cover Types 
When the sun ray passes through a prism, it is dispersed into seven different colours. It shows that the white light of the sun has many colours. When it hits a coloured object, say red, the reflects only the red colour, and absorbs the others. Then we know that the object’s colour is red.
**Electro Magnetic Waves** : Light is a small part of the electromagnetic spectrum. Electronic sensors can detect signals over a wide range of wavelength. The unique way a given land cover reflects and absorbs light is known as its spectral signature.
### Data Resolution
- Spatial
	- The size of a pixel that is recorded in a raster image
	- Square areas ranging from 1 to 1,000 metres (3.3 to 3,280.8 ft)
- Spectral
	- Number of frequency bands
	- Example: NASA Landsat images have 7 bands
	- Includes several in the infrared spectrum, ranging from a spectral resolution of 0.7 to 2.1 μm.
- Radiometric
	- Number of different intensities of radiation
	- Typically, from 8 to 14 bits (256 levels of the grayscale and up to 16,384 intensities or “shades” of colour)
- Temporal resolutions – how often the image of one area is taken?
	- Frequency of flyovers by the satellite or plane
	- Relevant in time-series studies or those requiring an averaged or mosaic image, as in deforesting monitoring
	- Cloud cover over a given area or object makes it necessary to repeat the collection of said location
## Identifying Landcover Types
- First, decide on what land cover categories we like to use.
- For flood maps, there may be only two categories — dry land and wetland
- A standard global land cover map may have ==seventeen== categories
	- closed shrublands, savannas, evergreen needle leaf forests, urban areas, and ice/snow.
- The only requirement for any land cover category is a **distinct spectral signature** that a satellite can record.
- Blue, 450–515..520 nm
	- Atmosphere and deep water imaging can reach depths up to 150 feet (50 m) in clear water
- Green, 515..520–590..600 nm,
	- vegetation and deep water structures, up to 90 feet (30 m) in clear water.
- Red, 600..630–680..690 nm
	- man-made objects in water up to 30 feet (9 m) deep, soil, and vegetation
- Near infrared (NIR), 750–900 nm
	- vegetation
- Mid-infrared (MIR), 1550–1750 nm
	- vegetation, soil moisture content, and some forest fires
- Far-infrared (FIR), 2080–2350 nm
	- soil, moisture, geological features, silicates, clays, and fires
- Thermal infrared, 10400-12500 nm,
	- emitted instead of reflected radiation to image geological structures, thermal differences in water currents, fires, and for night studies.
- Radar and related technologies
	- terrain and for detecting various objects
- For different purposes, different combinations of spectral bands can be used. Often, bands are artificially combined to identify a particular object or data on the Earth surface. A combination of Red-Near Infrared [(NIR)](https://gisgeography.com/ndvi-normalized-difference-vegetation-index/) gives a good indication of vegetation strength (Normalized Difference Vegetation Index pr NDVI)
	- $\frac{NIR-R}{NIR+R}$ - Ranges from -1 to +1
	- Higher value indicated good vegetation
- There are other indices, such as NDWI (Water Index) and NDSI (Snow Index). [The Index Stack (NDVI, NDWI, NDSI): Description And Features (eos.com)](https://eos.com/make-an-analysis/index-stack/)
## Reading a Satellite Image [How to Interpret a Satellite Image: Five Tips and Strategies (nasa.gov)](https://earthobservatory.nasa.gov/features/ColorImage)

To unlock the rich information in a satellite image, you need to:
- Look for a scale
- Look for patterns, shapes, and textures
	- Bodies of water:
		- rivers, lakes, and oceans
		- simplest features to identify because they tend to have unique shapes and they show up on maps
	- Farms usually have geometric shapes
		- circles or rectangles—that stand out against the more random patterns seen in nature
		- clearing is often square or has a series of herring-bone lines that form along roads
	- A straight line
		- human-made, such as a road, a canal, or some boundary made visible by land use
	- Mountains look like wrinkles or bumps
	- Islands create turbulence that results in swirling vortices or wakes in the cloud
	- Grasslands tend to be pale green, while forests are very dark green
	- Densely built areas are typically silver or gray.
	- Some cities have a more brown or red tone depending on rooftop materials
- Define the colors (including shadows
- Find north
- Consider your prior knowledge
# [NDVI](https://opensourceoptions.com/remote-sensing-with-qgis-calculate-ndvi/) 
#steps
- Download Raster Image ==Landsat 8 or 9==
- Need ==Band 4 and 5==
	- Band 4 = Redband
	- Band 5 = NearInfraRedbad
- Use Raster Calculator
	- Formula = $\frac{NIR-R}{NIR+R}$
	- or $\frac{B_{5}-B_{4}}{B_{5}+B_{4}}$
- Clip the image on particular shapefile if required
- Change the color intro vegetation color (not mandatory)
# RS in Civil Engineering
- Digital elevation modes (DEM)
	- A 3D representation of a terrain
	- Filters out and excludes terrain vector features
		- streams, breaklines, and ridges
		- all ground objects,
			- built (power lines, buildings, and towers)
			- natural (trees and other types of vegetation).
- Digital terrain modes (DTM)
	- A 3D, bare-earth representation of a terrain or surface topography
		- Includes features like rivers, ridges, and breaklines
		- Excludes natural or man-made objects such as:
			- vegetation
			- buildings
- Digital surface modes (DSM)
	- A 3D representation of the heights of the Earth's surface
		- Including natural or man-made objects located on it
	- Represents the mean sea level elevations of the reflective surfaces
		- vegetation, buildings, and other features elevated above the bare earth
![[Drawing1-Model.png]]
## DEM download
#steps 
- [5 Free Global DEM Data Sources - Digital Elevation Models - GIS Geography](https://gisgeography.com/free-global-dem-data-sources/)
- Space Shuttle Radar Topography Mission (SRTM) DEM (30 m pixel size, and 16 m vertical accuracy
	- From USGS Earth Explorer (https://earthexplorer.usgs.gov/)
- ASTER Global Digital Elevation Model (30 m pixel size)
	-  Through NASA Earthdata (https://search.earthdata.nasa.gov/search)
	- USGS Earth Explorer (https://earthexplorer.usgs.gov/)
- JAXA’s Global ALOS 3D World
	- 30-meter resolution digital surface model (DSM) captured by the Japan Space Agency (https://www.eorc.jaxa.jp/ALOS/en/dataset/aw3d30/aw3d30\_e.htm)
- 3D visualization
	- [Developing a 3D Model using QGIS (youtube.com)](https://www.youtube.com/watch?v=WmobNBnN1lc)
	- ![[NoteGPT_MindMap_1716797206674.png| 600]]
# Flood Simulation with GIS
[[Flood map generation (HECRAS).canvas|Flood map generation (HECRAS)]]
![[Pasted image 20240527151518.png]]
# GPS
- GPS – Global Positioning System
- Gives the location and time information anywhere in the world
- A system of earth-orbiting satellites
	- Provides a precise location on the earth’s surface in latitude/longitude coordinates
- Space Segments
	- GPS satellites fly in around the earth at an altitude of approximately 20,000 km
	- Period of 12 hours
	- At least 6 satellites are always within line of sight from any location
	- Satellites are powered by solar cells
- Control Segments – Ensures proper functioning of the whole system
	- Consists of Control Station, Monitor Station, Ground Antenna
	- Control station maintains optimum GPS constellation
	- Monitor station checks the exact altitude, position, speed of orbiting satellites
	- Ground antennas communicate with GPS satellite
- User Segments
	- GPS receiver is composed of an antenna, receiver processor, and highly stable clock
	- At least 4 GPS satellites are required for calculating the exact position
	- Mobile phones are common GPS receivers
## GPS Types
4 types
- GPS – American – First launch in 1978
	- Currently 31 earth orbiting satellites
	- Accuracy 500-30 cm
- GLONASS – Russian – Launched in 1982
	- GLObal NAvigation Satellite System
	- Consists of 24 satellites
- Galileo – by European Space Agency (ESA) – first launched in 2005
	- 30 active satellites
	- 30 active satellites
- BeiDou – Chinese Navigation Satellite System – launched 2000
	- 55 satellites
	- Accuracy 3.6 – 10 cm
## GPS Applications
- Geodetic Control Survey
```
**Geodetic surveying** is the survey in which the curvature of the earth is taken into account and higher degree of accuracy in **linear** and **angular** observations is achieved. The geodetic **surveys** extend over large areas and lines connecting any two points on the surface of the earth are treated as arcs. For calculating their projected distances on the plans or maps, the correction for the earth’s curvature is applied to the measured distances. The angles between the **curved lines** are treated as spherical angles. A knowledge of spherical trigonometry is necessary for making measurements for the **geodetic surveys**.
```
- Cadastral Survey
```
Cadastral surveying is **the sub-field of cadastre and surveying that specialises in the establishment and re-establishment of real property boundaries.** It involves the physical delineation of property boundaries and determination of dimensions, areas and certain rights associated with properties
```
- Photogrammetry, Remote Sensing and Surveying
	- Environmental modelling, Disaster mitigation, mobile mapping
	- GPS receivers provide very accurate data and are widely used in surveying
- Navigation
	- Determining the ground position of an object and helps in the navigation to any location
## RS and GPS Integration with GIS
- GPS, RS, and GIS are three closely related technologies
- GPS – collects location data and feeds into RS and GIS
- RS – Interprets satellite imagery and feeds the output into GIS
- GIS – Carries out all spatial analysis with data from GPS and RS.
- Without location data, GIS is meaningless
- RS provides detailed data to GIS which is otherwise not available
## GPS receiver types
3 types
- Recreation Grade
	- accuracy approx. 3-5m, cost $100-500
	- Mobile phone GPS
		- - accuracy is not essential but just a feel of the location is adequate
		- If there is no network coverage in the project area, we can still get the location if we download the project area map through a WiFi connection or where there is good coverage
		- Route planning for a site visit
		- Tracking the route after the visit
		- Geotagging of the photographs taken during the visit
		Limitations 
		- Data not easily downloadable (app needed)
		- Accuracy is not dependable
- Map Grade
	- accuracy 0.5-2m, cost $1,000-3,000
	- Sometimes need a data processing software
	- Tracking a route with reasonable accuracy
	- Hand-held GPS (map grade)
		- Reconnaissance survey
		- Route planning
		- Data can be downloaded for integration with GIS
		- Simple user interface
		- Used for non-critical applications
- Survey Grade
	- accuracy 1mm, cost starts from $10,000
	- Multiple devices are used simultaneously
	- Require post processing software and GPS data administration services to attain the “verifiable” accuracy levels
	- Accurate survey works
		- Need a professional surveyor and specialized software
		- Expensive, needs a lot of planning and expertise
		- But essential for some projects, such as land acquisition, alignment fixation, siting of structures, etc.
### Considerations
- Accuracy requirement
- Price
- Ease of use
- Data downloading facility
- Post Processing needs
### Using Data from GPS Receivers
- Usually a series of x,y points in ASCII format
- Downloaded onto a computer
- Can be uploaded into any GIS software and plotted on a map
- Compared with established and visible map features
	- Map verification
	- Ground truthing
	- Map rectification
- Mobile devices can also be used as GPS receivers
	- Suitable if location accuracy is not critical
	- Several software available
		- Open-source: QField and Mergin Maps (both work with QGIS) – free for small projects; larger projects need a subscription
		- Commercial: Collector (ESRI), Fulcrum, GIS Cloud
# Zero Dark Thirty (2011)

- The story of the greatest manhunt in history
- CIA announced $25 million for information leading to a wanted person’s capture
- CIA sought help from
	- National Security Agency for codebreaking and communications monitoring
	- National Geospatial Intelligence Agency for maps and surveillance photographs, and
	- National Reconnaissance Office for satellite imagery
Geography Department at UCLA: How GIS and biogeography can help find a wanted person. 
Biogeography: A science that predict how plants and animals distribute themselves over space and time
- two theories
	- Distance-decay theory
		- As one goes further away from a precise location, there is an exponential decline in the turnover of species and a lower probability of finding the same composition of species
		- Bin Laden should be ==closest to the point== where he was last reported
		- Within a region that has a ==similar physical environment and cultural composition== (that is, similar religious and political beliefs)
	- Island biogeography theory
		- Large and close islands will have higher immigration rates and support more species with lower extinction rates than small isolated islands
		- He is in a ==larger town== rather than a smaller and more isolated town where the extinction rate would be higher
- Bin Laden
	- Last seen in ==Jalalabad== on November 13, 2001
	- Last heard from a transmission from ==Tora Bora== on November 28, 2001
- Three spatial scale analyses (global, regional, local) were examined
	- Global scale
		- Distance-decay probability maps from the last known location ![[Pasted image 20240527182945.png]]
		- Using the distance-decay model to his last known location
		- A three-dimensional model of the Tora Bora landscape ![[Pasted image 20240527183926.png]]
	- Regional scale
		- Identified cities with the highest probability of occurrence ![[Pasted image 20240527183105.png]]
		- 26 city islands within a 20-km radius
		- City islands larger than 100 m x 100 m were digitized
		- QuickBird imagery in ArcGIS 9.0 to quantify area and isolation metrics
		- City-islands identified
			- Area of continuous man-made structures
			- Distance in kilometers to all other city-islands was used as an isolation metric
		- ==Kurram== had the highest probability of hosting the person (98%)
		- 86.6% probability that he is within one of the seven FATAs
		- Parachinar - Largest city (red dot)
		- Nightlight imagery also shows that Parachinar is the closest city to his last known location
		- The brightest city by nightlight intensity in Kurram ![[Pasted image 20240527183410.png]]
	- Local scale
		- Studied city structures having suitable size and features  ![[Pasted image 20240527183608.png]] ![[Pasted image 20240527183617.png]] ![[Pasted image 20240527183623.png]] 
		- In Parachinar – three structures meet Bin Laden’s lifestyle requirement criteria
			- He was tall, so high walls
			- Trees to cover the yard
			- Three bedrooms for many people
			- Electricity for a dialysis machine (the person was known to need it)
		- Three buildings
			- Structures A, B, and C are the best fortified and some of the largest residential homes or structures in the city of Parachinar
			- Structures A and C are residential homes, while structure B appears to be a prison
- Imagery source:
	- Landsat ETM+, Shuttle Radar Topography Mission, QuickBird, and Defense Meteorological Satellite Program- Operational Linescan System imagery
	- Georectified into the same geographic coordinate system (WGS84
	- Resampled to same pixel size
## Failure Reason
- Bin Laden was later found in another city in Pakistan
	- 500km away from Parachinar
- They forgot one significant factor
	- Bin Laden’s close relationship with the Pakistan Army
	- The hosting city was only 50km away from Islamabad
	- It has a strong presence of the Pakistan Army
	- He relied more on the Army than the Taleban
- GIS is a powerful tool
	- But must be used ==with all relevant data==
	- Analysis must be ==realistic==
- Bottom line
	- GIS can help in analyzing complex problems spread over a large area
	- But, we must have a ==bigger picture== of the problem to get the best outcome from GIS
# Applications of GIS
- [1000 GIS Applications & Uses - How GIS Is Changing the World - GIS Geography](https://gisgeography.com/gis-applications-uses/)
- Agriculture
	- precision farming
		- Data from the Sky – Satellites and Drones
		- Data online – Real-time mapping
		- Modeling – Mashing data sets
		- Agri-tech:
			- The modern-day farmer needs to understand – soils, weeds, nutrients, weather, insects, disease, machinery, and climate
- Transport and supply chain problems
	- What’s the shortest route to the market?
	- Where should I build a hospital to best serve a community?
	- How can I optimize a vehicle delivery fleet?
		- Point-to-point analysis
		- Finding Coverage
		- Optimize Fleet
		- Select Optimal Site
		- Origin-Destination – OD Cost Matrix
- Inundation forecasting 
	- Uses hydrodynamic models and ArcGIS to prepare flood forecast models
	- Displays in maps for easy understanding
- 3D volumetric modeling
	- Avoiding Dangerous Airspace ![[Pasted image 20240527184831.png]]
	- Finding locations that hide military vehicles from view
	- Mining, geology, and engineering
- Infrastructure planning and management
	- Transport networks, large construction sites
- Urban planning and municipal services (waste collection)
- Utility services planning and management
- Integration of GIS with BIM – indoor mapping for large public buildings
	- Airports, Hospitals, Universities, etc
- Asset management
- Landuse planning and land management
- Watershed delineation, water resources planning and management
- Epidemiological studies
- Disease spread pattern study
- Disease demographic study
- Identification of vulnerable groups
- Finding optimum location for rural health centres
# Concepts
#concepts 
## Land Acquisitions
- Data: Mouza map (Cassini); epsg.io
- Steps
	- Acquire Mouza map 
	- Project Road onto the map
	- Buffer Road
	- Repeat the process [[Model Builder GIS.canvas|Model Builder GIS]] ![[Pasted image 20240527212339.png]]
	![[Pasted image 20240527213126.png]]
## NDVI
- Data Source: Landsat Image from USGS or NASA
- Formula 
	- $\frac{NIR-R}{NIR+R}$
	- or $\frac{B_{5}-B_{4}}{B_{5}+B_{4}}$ for Landsat band 4 and band 5
- Software: Qgis
- As it is a time series analysis, I should go for model building
	- ~~Define Input and Output Folders:~~
		- ~~Use a "**Parameter**" algorithm twice.~~
		- ~~Name the first one "Landsat\_Folder" and set its type to "String". This will store the location of your downloaded Landsat images.~~
		- ~~Name the second one "Output\_Folder" and set its type to "String". This will store the final NDVI time series maps with basemaps.~~
	- ~~Download Landsat 8 Images:~~
		- ~~From USGS~~
		- ~~Insert them into "Landsat\_Folder"~~
	- ~~Looping through Years:~~
		- ~~Use an "**Iterator**" algorithm.~~
		- ~~Set the "iterable" to a list containing the years you want to analyze~~
	- ~~Build the NDVI Processing Chain (Inside the Loop):~~
		- ~~Use a "**Raster Calculator**" algorithm~~
			- ~~Set "Input layer 1" to a combination of the "Landsat_Folder" parameter and the current year from the loop (e.g., os.path.join("(Landsat_Folder)", f"landsat_{{**CURRENT**}}.tif")). This dynamically builds the path based on the loop iteration.~~
			- ~~Set "Input layer 2" similar to layer 1, selecting the NIR band (modify band numbers if needed).~~
			- ~~Formula $\frac{B_{5}-B_{4}}{B_{5}+B_{4}}$~~
			- ~~utput layer: Name it "NDVI_{{**CURRENT**}}.tif" (replace with year dynamically using double curly braces).~~
	- ~~Clip to Desired Area~~
		- ~~Use a "**Clip Raster**" algorithm.~~
			- ~~Input layer: The NDVI layer from the "Raster Calculator" (use the output port).~~
			- ~~Clip layer: Your desired area shapefile~~
			- ~~Output layer: Name it "NDVI_Clipped_{{**CURRENT**}}.tif" (dynamic year).~~
	- ~~Generate Map with Basemap~~
	- ~~Save Output Map (Optional - Inside the Loop):~~
		- ~~Use a "**Save Raster**" algorithm (if using "Composite Bands")~~
	- ~~Model Execution:~~
		- ~~Run the model. This will iterate through the years, calculate NDVI for each year, clip to your area of interest, and optionally generate a map series with a basemap. The final outputs will be saved based on your defined folder paths.~~ 
- Benefits of this Model Builder Approach:
	- Avoids repetitive manual steps for each year.
	- Dynamically builds file paths based on loop iterations.
[[Model Builder GIS.canvas|Model Builder GIS]]
![[Pasted image 20240527203931.png]]

## Steps involved in finding Osama Bin Laden
- Used Biogeography theory and GIS
- Global
	- Distance Decay Theory 
	- 3 dimensional model to get actually closed cities
	- Near Tora Bora
- Regional
	- Island biogeography theory
	- Larger cities are identified
	- Larger cities with light pollution (from night image) are identified
	- (Kurram)
- Local
	- Structures that matches the need of Bin Laded is searched in Paranichar
	- 3 Structures found 
	- 2 of them are residential
	- 1 is a prison
- If failed for one reason
	- Broader picture was not used in GIS analysis
		- good relation between Bin Laden and Pakistani army was not used as an information while doing GIS analysis
## Mobile Connection to field to do survey
- Open source: Margin maps or Qfield
- In Qfiled forms are created as attribute table with the help of a plugin
- Margin maps do not require forms to be created inside Qgis, It can be easily created withing the mobile application.
- Utilize Margin Maps for Field Data Collection
	- Use Margin Maps on your mobile device for data collection in the field. It allows you to capture geospatial information, photos, and notes.
- Export Data from Margin Maps:
	- Margin Maps likely offers options to export your collected data. This could be in formats like CSV, KML, or Shapefile.
- Import Data into QGIS:
	- In QGIS, go to the Layer menu and choose "Add Layer" ->; "Add Vector Layer."
	- Browse to your exported Margin Maps data file and select it.
	- Now you have your field data loaded into QGIS for further analysis and map creation.
- Additional Options in QGIS:
	- Since you now have geospatial data, you can use QGIS's extensive functionalities to:
		- Visualize your data on a basemap.
		- Perform spatial analysis.
		- Create thematic maps.
		- Design a professional map layout using the composer tool.
- Resources:
	- [See how Mergin Maps works | Mergin Maps demo (youtube.com)](https://www.youtube.com/watch?v=dy-B1BW9lA0)

## Flood forecasting
- Data Acquisition and Preparation:
	- **Elevation Data:** Use Digital Elevation Models (DEMs) to understand terrain and potential flow paths.
	- **Historical Flood Data:** Utilize historical flood maps, inundation zones, and river gauge data to identify flood-prone areas.
	- **Precipitation Data:** Integrate real-time and predicted precipitation data from weather stations or radar.
	- **Land Cover Data:** Land cover maps (forests, urban areas) influence runoff and infiltration, impacting flood risk.
- Floodplain Delineation:
	- Use DEMs and spatial analysis tools to identify areas at risk of flooding based on elevation and potential water flow paths.
- Hydraulic Modeling (Optional):
	- Integrate specialized hydraulic models with GIS to simulate flood wave propagation and water level changes in rivers and streams. This requires additional expertise and data
- Flood Inundation Mapping:
	- Combine flood-prone areas, historical data, and real-time precipitation data to create inundation maps that predict the extent of potential flooding.
- Scenario Modeling:
	- Use GIS to model different flood scenarios based on varying precipitation intensities and durations. This helps assess flood risk under different conditions.
- Vulnerability and Risk Assessment:
	- Overlay flood inundation maps with infrastructure, population, and land-use data to identify vulnerable areas and assess potential damage.
- Floodplain Management and Early Warning Systems:
	- Use GIS to create flood hazard maps and evacuation plans for at-risk communities.
	- Integrate real-time monitoring data with GIS for early warning systems that alert people to potential floods.
[[Model Builder GIS.canvas|Model Builder GIS]] ![[Pasted image 20240527215740.png]]
## GIS with transportation
- Route Planning and Optimization (emergency):
	- **Finding the most efficient routes:**
		- distance
		- travel time
		- Traffic congestion,
		- road restrictions
		- turn limitations
- Traffic Analysis and Management
	- **Traffic flow analysis**
	- Real-time traffic monitoring
	- Accident analysis
- Public Transportation Planning
	- Identifying optimal bus stop locations
	- Assessing transit needs
- Infrastructure Management
	- Road maintenance planning
	- Infrastructure asset management
- ==Steps==
	- ==Define your project goals and objectives==
	- ==Collect relevant spatial data==
		- ==road networks==
		- ==traffic data==
		- ==public transportation routes==
		- ==accident locations==
		- ==population data==
	- ==Clean and prepare the data==
		- ==Ensure data accuracy, consistency, and compatibility with your GIS software.==
	- ==Perform spatial analysis==
	- ==Visualize your results==
## GIS with water
- Data Collection and Inventory
	- Spatial Data
		- Surface water bodies (lakes, rivers, streams)
		- Groundwater wells and aquifers
		- Water infrastructure (pipes, canals, treatment plants)
		- Land cover (forests, agriculture, urban areas) - impacting water flow
		- Elevation data (influences drainage patterns)
	- Attribute Data
		- Water quality parameters
		- Well depth and pumping rates
		- Infrastructure capacity and maintenance records
		- Land use data
- ==Water Resource Assessment==
	- ==Mapping and Analysis==
		- ==Visualize the spatial distribution of water resources.==
		- ==Identify areas with water scarcity or potential for new water sources==
		- ==Analyze water flow patterns and drainage networks.==
		- ==Model the impact of climate change on water resources.==
	- Spatial Queries
		- Where are the areas with the highest water demand?
		- What are the potential impacts of a new development on water resources?
		- Which areas are most vulnerable to drought or flooding?
- Water Management Planning
	- Scenario Modeling
- Water Monitoring and Regulation
- ==Public Outreach and Education==
	- ==Interactive Maps==
## GIS with Environment
- Pollution Source Identification and Monitoring:
	- Import point data representing potential pollution sources (e.g., factories, waste facilities).
	- Overlay this data with water quality data (e.g., river samples) as point or polygon layers.
	- Use spatial join to identify facilities near polluted locations.
	- Analyze proximity and upstream/downstream relationships using vector analysis tools.
	- Generate maps to visualize potential pollution sources and areas of concern.
- Environmental Impact Assessment (EIA) for Projects
	- Import project area boundaries as a polygon layer.
	- Overlay with sensitive environmental features (e.g., protected areas, wetlands) from environmental databases or government websites.
	- Use buffer zones around sensitive features to define areas with development restrictions.
	- Analyze land cover data (e.g., forest cover) to assess potential habitat disruption.
	- Generate maps to communicate project footprint and potential environmental impacts.
- Sustainable Land Management and Resource Planning:
	- Import soil quality data as a raster layer
	- Overlay with land cover data (e.g., agricultural land, forests).
	- Use zonal statistics to identify areas with high-quality soil suitable for specific agricultural uses.
	- Analyze land suitability based on soil characteristics and slope information.
	- Generate maps to guide sustainable land use practices and resource conservation.