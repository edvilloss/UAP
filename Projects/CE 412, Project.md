# Introduction
## General
Under this project a 6 storied residential building will be constructed located Sirajganj. It is a reinforced concrete (RC) frame structure. The floor slabs will be constructed as beam supported slab. The original topography of the site was probably generally level ground. Based on the soil test report the foundation has been designed as shallow foundation. An Architectural Design Drawing (Auto CAD soft copy), Sub-soil Investigation Report (PDF soft copy), Project Information Sheet (doc. file) slabs found to be adequate in consideration of thickness and reinforcement are provided. So, we need to be submitted ETABS File (Soft copy of edb file), Project report (Soft copy of doc file), Sample drawing (Soft copy of hand sketch). The analysis and design of this building has been conducted according to Bangladesh Nation Building Code (BNBC) 2017.
## Project Information

|   |   |   |   |
|---|---|---|---|
|**Project Information Sheet**|   |   |   |
|**SL NO**|**Item Name**|**Item Description**|   |
|1|Client|Name:|------|
|Information|Address:|-----|
||Profession:||
||Contact No:||
||E-mail:||
|2|Project Location|Plot Area|3250 sft|
|Plot Number|---|
|Thana/Upazila:||
|District:|Sirajganj|
|Division:|Rajshahi|
|Google Earth Location||
|3|Site Information|Adjacent (Utility Service Lines, Buildings, Walls of others property etc)|**North (Front) side**: Open ground,|
|**East  side**: 6-storied animation building (under construction).|
|**South side:** Boundary wall,|
|**West side:** Open ground area|
|Adjacent Road||
|Road level (±0)|0.0 Level|
|Earth Ground Level (EGL)|(-) 1'-0"|
|Plinth Level|(+) 2 '-6"|
|**SL No**|**Item Name**|**Item Description**|   |
|4|Building Information|Occupancy Type:|Residential|
|No. of Story:|6|
|Story Height, Building Height Restriction (RAJUK or any other Authorities)|10'|
|No. of Unit Per Floor, Mezzanine Floor|Two units, No mazzanine floor|
|Structure Type|Office Building|
|Structural System|------|
|Building Foot Print Area|3256 sft|
|Floor Area|19,402 sft|
|No. of Basements|N/A|
|Parking Facilities|8 nos.|
|Ground Floor Facilities|Car parking|
|Roof Facilities|Over head water tank|
|Lift Requirement & Measurement|8 persons lift,Size: 5'-6"X6'-2"|
|UGWT Requirement & Location|From Grid 2-2 to Grid 3-3 southside area, Size: 13'-1"X24'-10"|
|Septic Tank Requirement & Location|N/A|
|OHWT Requirement & Location|Top of stair & lift core area, Size: 17'-6"X24'-1"|
|Ramp Requirement & Location|(±) 0.00 level to (+) 2'-6"|
|Type of  Coarse Aggregate (Brick/Stone)|Brick chips|
# Structural Design Criteria
## Codes, Standards and References
Structural analysis and design of this building have been reviewed according to Bangladesh National Building Code (BNBC) 2020.
ACI318-08 ACI 318M-08: Building code requirement for Reinforced concrete,2008.
ASCE 7-05 ASCE/SEI 7-05: 05: Minimum Design Loads for Buildings and Other Structures
- Structural Analysis has been considered according to BNBC 2020.
- Loading Criteria are considered according to BNBC 2020.
- Material Specifications and properties have been considered according to BNBC 2020.
- Structural Design of RCC has been considered according to BNBC2020.
## Structural Geometry Considerations
Structural geometry (Shape, size, story height and number of stories) have been considered as per architectural design and further requirement also checked.
- Grid
	- X axis 
	- Y axis
	- Story
## Material Specifications
### Concrete
The following concrete grades f'c (28 days cylinder strength) are adopted in design
- Directional Type: Isotropic
- Weight per unit volume 0.15 kip/ft^3
- Modulus of Elasticity (brick chip) = 4$5000\sqrt(f'_c) = 2623928.353 psi = 377845.6828 kip/ft^2$
- Poison's ration 0.2
- Concrete compressive strength, fc' = 3400 psi = 489.6 kip/ft^2
### Rebar
The Following steel grades fy are adopted in design:
Material type: Rebar
- Weight per unit volume: $0.49 kip/ft^3$
- Modulus of Elasticity $4176000 kip/ft^2$
- Minimum Yield Strength, fy: $9024.48 kip/ft^2$
- Minimum Tensile Strength, fu: $11280.6 kip/ft^2$
- Expected Yield Strength, fye: $9926.93 kip/ft^2$
- Expected Tensile Strength, fue: 1$2408.66 kip/ft^2$
## Loading Criteria (detailed calculations)
The building has been analyzed for possible load actions such as Gravity and Lateral Loads.
### Gravity Loads
Gravity loads, such as dead and live loads applied at the floors or roofs of the building according to the provision of BNBC 2020 are as follows
#### Dead loads
- Self-Weight of Concrete = 150 pcf
- Floor finish (FF) on floors = 25 psf;
	- Stairs = 56 psf; 
	- Roof = 40 psf
- Fixed Partition wall (RPW) = 10" beam * 8.75' Height * 120 pcf brick with morter = 875 plf;
	- 5" beam 437.5 plf; 
	- parapet wall = 200 plf
#### Live loads
- Floor Live Load (LL42) = 42 psf
- Staircase Live Load (LL100) = 100 psf
- Roof Live Load (LL63) = 63 psf
- Random Partition Wall (RPW) = 25 psf
- OHWT 5' = 312 psf; Edge = 500 plf
- Lift load = $\frac{4*8*75}{5.5*6.167}*2.206 \approx 170 psf$
### Lateral Loads
Lateral Loads, such as Wind Load and Seismic Load applied at the building in accordance with the provision of Chapter 2, Part 6 of BNBC 2020 is as follows:
#### Wind Load consideration parameters
- Basic Wind Speed = 114 mph
- Structural Importance Factor I = 1
- Exposure Category = A
- Topographic Factor, kzt = 1
- Gust Effect Factor, G = 0.85
- Wind Directionality Factor, kd = 0.85
- Damping Ratio = 5%
- Wind Pressure Coefficients,
	- Cpe = 0.8
	- Cpl = -0.28 (x dir)
	- Cpl = -0.5 (y dir)
#### Earthquake Load consideration parameters
- Soil Site Class = SD
- Seismic Zone Coefficient, Z = 0.28
- Zone = 3
- Importance factor, I = 1
- Seismic Design Category, SDC = D
- Dual System Intermediate Moment Resisting Concrete Frame with Shear Wall
	- Response Reduction Factor, R = 6.5
	- System Overstrength Factor, ![](file:///C:/Users/santo/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png) = 2.5 
	- Deflection Amplification Factor, C_d = 5
- Spectral Response Acceleration Parameters,
	- S_s = 0.7
	- S_1 = 0.28
- Site Coefficients,
	- F_a = 1.35
	- F_v = 2.7
- Building Period, T = 0.78 sec
- Long Period Transition Period, TL = TD = 2
