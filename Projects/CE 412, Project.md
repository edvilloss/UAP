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
- Modulus of Elasticity (brick chip) = $45000\sqrt(f'_c) = 2623928.353 psi = 377845.6828 kip/ft^2$
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
- Parking Live Load (LL75) = 75 psf
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
## Boundary Conditions (Support Conditions)
Column base supports have been considered as fixed supports in 3D model of super structure Spring supports have been considered for shallow foundation.
## Design Method and Load Combinations
### Unfactored load combinations
- D: (SW + FF + FPW)
- L: (LL42 + LL63 + RPW + LL100 + LL75 + OHWT + Lift)
- Seismic Weight: (SW + FF + FPW) + 0.25(LL42 + LL63 + RPW + LL 75) + 0.5(LL100 + OHWT + Lift)
- D + 0.5L + 0.7W
### Factored Load Combinations
- As per BNBC 2020 (75 combos or 99 combos)
## Bearing Capacity of Shallow Foundation/Pile capacity
Bearing capacity of soil considered for this building is 4 ksf.
## 3D view and Typical Plan of Building
1. Grid and Story data
	1. X grid 
	2. Y grid
	3. Story with base + OHWT
2. Definition of Material properties
	1. Concrete compressive strength (f’c, E)
	2. Steel reinforcement yield strength (fy, fu, fye, fue)
3. Definition of frame members
	1. Definition of column (cross section, material, confinement type, rebar strength, clear cover 1.5" and 4" etc)
		1. Short column 
		2. Regular column
	2. Definition of Beams (cross section, rebar strength, cover to rebar center 2.5" and 3")
		1. Define separate members for various use case (FPW load, parapet wall)
		2. Define roof beam as separate so that selection process for load application is easier
1. Definition of 2D elements (area objects)
	1. Definition of slabs (Type of member: shell, membrane or plate; material strength, thickness)
		1. Parking Slab (75psf_LL; no_RPW)
		2. Floor Slab (42psf_LL; 25psf_RPW; 25psf_FF)
		3. Stair landing (100psf_LL; no_RPW)
		4. Stairs (100psf_LL; 56psf_FF; no_RPW)
		5. Roof (63psf_LL; 40psf_FF; no_RPW)
		6. Cantilever (no_RPW; 25psf_FF; 42psf_LL)
	2. Definition of walls (type of member: shell, membrane or plate; material strength, thickness)
		1. Define pier label
		2. Assign different pier label to different walls
2. Draw the structural geometry (column, shear wall, beam and slab)
3. Definition of dead and live loads
	1. Dead loads:
		1. SW (dead)\_dead\_self weight multiplier-1; M1
		2. FF\_super dead\_self weight multiplier-0 (25psf); Landing (56 psf); M1
		3. FPW_ super dead_self weight multiplier-0; (437.5 lb/ft) except roof all beam; parapet 200 lb/ft; M1
	2. Live Loads
		1. RPW_live; all slab except roof + staircase + stare shape; M0.25
		2. LL42_live; 43 all slab, 63 roof; M0.25
		3. LL100\_live; 100 staircase ; M0.5
		4. LL63\_live; 63 roof M0.25
		5. LL75_live; 75 parking M0.25
		6. OHWT\_livel; outer frame 500 lb/ft; 312psf; M1
		- Lift\_live; Calculated value; M1
4. Definition and assignment of diaphragm (area diaphragm)
	1. Select per floor and assign
5. Definition of Wind loads (as per BNBC: ASCE 7-05)
	1. Wx1; 0 degree; case 1
	2. wx2; 0 degree; case 2
	3. wx3; 0 degree; case 3
	4. wx4; 0 degree; case 4
	5. wy1; 90 degree; case 1
	6. wy2; 90 degree; case 2
	7. wy3; 90 degree; case 3
	8. wy4; 90 degree; case 4
6. Definition of Mass source (Seismic dead loads)
	1. SW 1
	2. 42_LL 0.25
	3. 63_LL 0.25
	4. 75_LL 0.5
	5. 100_LL 0.5
	6. Lift 1
	7. OHWT 1
	8. RPW 0.25
	9. FPW 1
7. Definition of earthquake loads (as per ASCE 7-05)
	1. ex1; x dir
	2. ex2; x + eccentricity
	3. ex3; x - eccentricity
	4. ey1; y dir
	5. ey2; x + eccentricity
	6. ey3; x - eccentricity
8. Assignment of gravity loads (except self-weight) 
	1. FF, RPW, LL42, LL63, LL100, OHWT, Lift as area load
	2. FPW as line load
9. Manual and auto mesh of slabs and walls
	1. For manual meshing, no more than 4 nodes on a shell element  
10. Assignment of section modifier for columns, beams, slabs, walls
	1. Service load modifier for Check
		1. Column
			1. I22 0.98
			2. I33 0.98
		2. Beam
			1. I22 0.49
			2. I33 0.49
		3. Slab 
			1. m11 0.35
			2. m22 0.35
			3. m12 0.35
			4. f11 0.35
			5. f22 0.35
			6. f12 0.35
		4. Shear Wall
			1. m11 0.14
			2. m22 0.14
			3. m12 0.14
			4. f11 0.49
			5. f22 0.49
	2. Factored load modifier for Design		
		1. Column
			1. I22 0.7
			2. I33 0.7
		2. Beam
			1. I22 0.35
			2. I33 0.35
		3. Slab 
			1. m11 0.25
			2. m22 0.25
			3. m12 0.25
			4. f11 0.25
			5. f22 0.25
			6. f12 0.25
		4. Shear Wall
			1. m11 0.1
			2. m22 0.1
			3. m12 0.1
			4. f11 0.35
			5. f22 0.35
11. Definition of load combinations
	1. Unfactored load combinations
		1. D: (SW + FF + FPW)
		2. L: (LL42 + LL63 + RPW + LL100 + OHWT + Lift)
		3. D + L: (SW + FF + FPW + LL42 + LL63 + RPW + LL100 + OHWT + Lift)
		4. Seismic weight: (SW + FF + FPW) + 0.25(LL42 + LL63 + RPW) + 0.5(LL100 + OHWT + Lift)
		5. D + 0.5L + 0.7W
	2. Factored load combinations:
		1. As per BNBC 2020 (75 combos or 99 combos): see lecture notes
			1. Default for Slab, beam, column, wall provided with ETABS
12. Check model automatically in ETABS as well as recheck manually
13. Run analysis and check for any warning (check analysis run log)
14. Check analysis results and compare with approximate manual calculation
15. Check for serviceability and other criteria as per BNBC 2020
16. Check for building irregularities (Plan and vertical)
17. Design concrete frames (Columns and Beams)
	1. Set Design preferences 
		1. ACI 318-08 
		2. Seismic category 
		3. SDS
	2. Design
		1. Concrete frame design
			1. Start Design
	3. Display 
		1. Longi rebar
		2. Rebar parentage
		3. Shear rebar
		4. Column beam capacity ration > 1.2
		5. All failure
	4. Provide rebar while defining section properties
		1. Check
			1. Display
				1. () means check
				2. P-M ration if >1; failed
18. Design concrete shear walls
	1. Shear wall design
		1. Preference
			1. ACI 318-14
			2. SDS
		2. Assign pier section
			1. Uniform
				1. To be designed
		3. Display pier longi (vertical)
			1. pacing
		4. Display reinforcing ration
			1. Cross area * ratio
		5. Display shear reinforcement (Horizontal)
			1. Spacing
		6. Display boundary zone
	2. Table 
		1. Design
			1. Pier table
				1. Export excel
19. Design concrete slabs
	1. Add/Edit design strips
		1. Select story
		2. Include middle strip
		3. $X \rightarrow A$
		4. $Y \rightarrow B$
	2. Show strips 
		1. View option
			1. General
				1. Strip A
				2. Strip B
	3. Design
		1. Concrete Slab Design
			1. Reference
			2. Defining Load combinations
			3. Select story for design
			4. Start design
			5. Display flexural design
				1. Non; for see the rebar requirements(As) per strip 
				2. Select rebars; for providing
			6. Display Punching check
				1. N/C, not calculated
				2. D/C ration, demand capacity
					1. If > 1 than punching
20. Design foundation (shallow foundation: footing or mat)
	1. Manual calculation from Fy reaction on support
21. Export design outputs from ETABS (as .xlsx and .docx)
![[Pasted image 20240608152907.png]] <sup> 3d view </sup>
![[Pasted image 20240608153002.png]]<sup> Parking Floor plan </sup>
![[Pasted image 20240608153025.png]]<sup> 1st Floor Plan </sup>
![[Pasted image 20240608153059.png]]<sup> 2nd to Roof </sup>
## Selection of Analysis type
Structural analysis has been performed by Finite Element Analysis.
# ANALYSIS AND SOFTWARE DESIGN FEATURES
- MS Excel: Spread sheets
- ETABS 16: Extended 3D Analysis of Building System
## Serviceability Criteria
### Vertical Deflection Limits (D+L and L)
- Table 6.1.2: Deflection Limits
	- $D+L: \frac{L}{240}inch$
	- $L: \frac{L}{360}inch$
- ETABS
	- From Loads
		- Show Deformation
			- Load Combination
				- UZ
###  Maximum Lateral displacement for Wind Load
- The overall sway (horizontal deflection) at the top level shall not exceed (1/500)\*H 
	- Where, H = total height of the building above ground (Section 1.5.6.2)
	- D+0.5L+0.7W: $\frac{H}{500}=(\frac{80+10}{500})*12=2.16 inch$
	- 80+10: story height + OHWT
	- Display
		- Story Response Plot
			- Display Type: Maximum Story disp
			- D+0.5L+0.7Wx1 ~ D+0.5L+0.7Wy4 (Maximum)
### Story drift for Wind Load
- Section 1.5.6.1
- Drift ≤ 0.004 for Tn>0.7 
- Display 
	- Story Response Plot 
		- Display Type: Maximum Story drift 
		- wx1 ~ wy4 (Maximum)