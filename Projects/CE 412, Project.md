# TOC
>[!SUMMARY] Table of Contents
<%*
    let headers = await tp.file.content
        .split('\n') // split file into lines
        .filter(t => t.match(/^[#]+\s+/gi)) // only get headers
        .map(h => {
            let header_level = h.split(' ')[0].match(/#/g).length;
             // get header text without special characters like '[' and ']'
            let header_text = h.substring(h.indexOf(' ') + 1).replace(/[\[\]]+/g, '');
            let header_link = `[[${tp.file.title}#${header_text}|${header_text}]]`

            // prepend block-quote (>), indentation and bullet-point (-)
            return `>${'    '.repeat(header_level - 1) + '- ' + header_link}`;
        })
        .join('\n')
%><% headers %>
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
![[Pasted image 20240608154029.png]]<sup> 1st Floor Plan </sup>
![[Pasted image 20240608154036.png]]<sup> 2nd to Roof </sup>
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
### Maximum Lateral displacement for Earthquake Load
- Table 6.2.21:
	- From Etabs we get $\delta_{ex}$
		- $\delta_{x}=\frac{C_{d}*\delta_{ex}}{I}$
		- $here, C_{d}=4.5$
	- Allowable Story Drift Limit (Δ): $0.02H = 0.02*96*12 = 23.04 inch$
	- Display 
		- Story Response Plot 
			- Display Type: Maximum Story disp 
			- ex1 ~ ey3 (Maximum)
## Irregularities
### Plan Irregularity
#### Torsional Irregularity
- For every EQ loads(if more than 1.2 and Less than 1.4; $\frac{\Delta max}{\Delta avg}$)
- Show Table
	- Analysis
		- Results
			- Displacements
				- Max/AVG
				- Need Ratio

|   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|
|**Story**|**Load Case/Combo**|**Direction**|**Maximum**<br><br>**in**|**Average**<br><br>**in**|**Ratio**|**Status**|
|OHWT|ex1|X|1.639932|1.639133|1|Ok|
|ROOF|ex1|X|1.471134|1.443967|1.019|Ok|
|4F|ex1|X|1.062319|1.01511|1.047|Ok|
|3F|ex1|X|0.810166|0.764124|1.06|Ok|
|2F|ex1|X|0.543065|0.505835|1.074|Ok|
|1F|ex1|X|0.285614|0.263527|1.084|Ok|
|GF|ex1|X|0.076615|0.076615|1|Ok|
|OHWT|ex2|X|1.650166|1.633962|1.01|Ok|
|ROOF|ex2|X|1.461037|1.439645|1.015|Ok|
|4F|ex2|X|1.018662|1.010027|1.009|Ok|
|3F|ex2|X|0.774519|0.759458|1.02|Ok|
|2F|ex2|X|0.517861|0.502244|1.031|Ok|
|1F|ex2|X|0.271966|0.261484|1.04|Ok|
|GF|ex2|X|0.076659|0.076659|1|Ok|
|OHWT|ex3|X|1.658909|1.644303|1.009|Ok|
|ROOF|ex3|X|1.524015|1.44829|1.052|Ok|
|4F|ex3|X|1.105976|1.020193|1.084|Ok|
|3F|ex3|X|0.845813|0.76879|1.1|Ok|
|2F|ex3|X|0.56827|0.509426|1.116|Ok|
|1F|ex3|X|0.299262|0.26557|1.127|Ok|
|GF|ex3|X|0.076572|0.076572|1|Ok|
|OHWT|ey1|Y|1.770168|1.766487|1.002|Ok|
|ROOF|ey1|Y|1.534578|1.511054|1.016|Ok|
|4F|ey1|Y|1.005211|0.977367|1.028|Ok|
|3F|ey1|Y|0.719548|0.693068|1.038|Ok|
|2F|ey1|Y|0.442131|0.419771|1.053|Ok|
|1F|ey1|Y|0.203659|0.188419|1.081|Ok|
|GF|ey1|Y|0.044831|0.044534|1.007|Ok|
|OHWT|ey2|Y|1.817164|1.76475|1.03|Ok|
|ROOF|ey2|Y|1.762311|1.509169|1.168|Ok|
|4F|ey2|Y|1.1674|0.975335|1.197|Ok|
|3F|ey2|Y|0.841344|0.691171|1.217|Not Ok|
|2F|ey2|Y|0.519117|0.418221|1.241|Not Ok|
|1F|ey2|Y|0.238378|0.187434|1.272|Not Ok|
|GF|ey2|Y|0.042507|0.041796|1.017|Ok|
|OHWT|ey3|Y|1.685291|1.625108|1.037|Ok|
|ROOF|ey3|Y|1.707173|1.401247|1.218|Not Ok|
|4F|ey3|Y|1.173454|0.920467|1.275|Not Ok|
|3F|ey3|Y|0.864556|0.657226|1.315|Not Ok|
|2F|ey3|Y|0.549077|0.400628|1.371|Not Ok|
|1F|ey3|Y|0.263854|0.181024|1.458|Not Ok|
|GF|ey3|Y|0.046928|0.045607|1.029|Ok|
#### Re-entering Corners
- Building is irregular in terms of re-entrant corners if A/L>0.
	- Building is irregular in terms of re-entrant corners if A/L
	- No re-entering corners available for the building

#### Diaphragm Discontinuity
- Diaphragm discontinuity exists if opening area > 1/2 Total Floor Area
- There is no opening except stair and lift in the plan of the building.
- In terms of diaphragm discontinuity, the building is regular
#### Out of Plane Offsets
- There is no out of plane offset irregularity in the building
#### Non-parallel System
- All the shear walls are parallel and symmetric with centroidal orthogonal directions.
### Vertical Irregularity
#### Stiffness Irregularity-Soft Story
- Ex1 and Ey1
- Show Table
	- Analysis
		- Results
			- Structural Results
				- Story Stiffness
					

|            |               |                 |                 |           |            |             |            |
| ---------- | ------------- | --------------- | --------------- | --------- | ---------- | ----------- | ---------- |
| **Story**  | **Load Case** | **Stiffness X** | **Stiffness Y** | **Ke/Ka** | **Status** | **Ke/Kavg** | **Status** |
| **kip/ft** | **kip/ft**    |                 |                 |           |            |             |            |
| OHWT       | ex1           | 1856.286        | 0               | -         |            | -           |            |
| ROOF       | ex1           | 9372.541        | 0               | 5.049082  | Ok         | -           |            |
| 5F         | ex1           | 14412.12        | 0               | 1.537696  | Ok         | -           |            |
| 4F         | ex1           | 18497.77        | 0               | 1.283487  | Ok         | 2.164246    | Ok         |
| 3F         | ex1           | 21975.44        | 0               | 1.188005  | Ok         | 1.55919     | Ok         |
| 2F         | ex1           | 27468.85        | 0               | 1.249979  | Ok         | 1.501431    | Ok         |
| 1F         | ex1           | 36960.5         | 0               | 1.345542  | Ok         | 1.632001    | Ok         |
| GF         | ex1           | 98987.27        | 0               | 2.678191  | Ok         | 3.436867    | Ok         |
| OHWT       | ey1           | 0               | 1538.275        | -         |            | -           |            |
| ROOF       | ey1           | 0               | 7837.794        | 5.095184  | Ok         | -           |            |
| 5F         | ey1           | 0               | 11856.72        | 1.512763  | Ok         | -           |            |
| 4F         | ey1           | 0               | 16444.38        | 1.386925  | Ok         | 2.323441    | Ok         |
| 3F         | ey1           | 0               | 21022.65        | 1.27841   | Ok         | 1.745155    | Ok         |
| 2F         | ey1           | 0               | 29074.21        | 1.382994  | Ok         | 1.768369    | Ok         |
| 1F         | ey1           | 0               | 47509.68        | 1.634083  | Ok         | 2.141965    | Ok         |
| GF         | ey1           | 0               | 147040.1        | 3.094951  | Ok         | 4.519374    | Ok         |

#### Mass Irregularity
- Mass irregularity exists if mass of a story &gt; 200% mass of adjacent stories 
- As per occupancy (Residential building), there is no mass irregularity
- Show Table
	- Model
		- Structural Data
			- Mass Summary
				- Mass Summary by Story
					
| Story | UX lb-s²/ft | UY lb-s²/ft | UZ lb-s²/ft |
| ----- | ----------- | ----------- | ----------- |
| Tank  |             |             |             |
| Roof  |             |             |             |
| 7F    |             |             |             |
| 6F    |             |             |             |
| 5F    |             |             |             |
| 4F    |             |             |             |
| 3F    |             |             |             |
| 2F    |             |             |             |
| 1F    |             |             |             |
| GF    |             |             |             |
| Base  |             |             |             |
####  Vertical Geometric Irregularity
- Irregularity exists if the dimension of the lateral force resisting system at any story is more than 130% of that for any adjacent story.
- There is no Vertical Geometric Irregularity in the building
#### Vertical In-Plane Discontinuity in Vertical Elements Resisting Lateral Force
- Irregularity exists if the offset is greater than the width (d) or there exists a reduction in stiffness of the story below.
- There is no Vertical In-Plane Discontinuity in Vertical Elements Resisting Lateral Force in the building
#### Discontinuity in Capacity-Weak Story
- Story Force
- Ex1 Ey1
- Bottom
- Show Table
	- Analysis
		- Results
			- Structural Results
				- Story Forces
					
|   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|
|**Story**|**Load Case/Combo**|**VX Kip**|**VY kip**|**V present/V top**||**Status (>0.8)**|
|OHWT|ex1|-33.057||-|||
|ROOF|ex1|-160.226||4.846961||Ok|
|5F|ex1|-286.239||1.78647||Ok|
|4F|ex1|-388.006||1.355532||Ok|
|3F|ex1|-466.219||1.201577||Ok|
|2F|ex1|-521.731||1.119069||Ok|
|1F|ex1|-555.953||1.065593||Ok|
|GF|ex1|-571.187||1.027402||Ok|
|OHWT|ey1|0|-33.057||-||
|ROOF|ey1|0|-160.226||4.846961|Ok|
|5F|ey1|0|-286.239||1.78647|Ok|
|4F|ey1|0|-388.006||1.355532|Ok|
|3F|ey1|0|-466.219||1.201577|Ok|
|2F|ey1|0|-521.731||1.119069|Ok|
|1F|ey1|0|-555.953||1.065593|Ok|
|GF|ey1|0|-571.187||1.027402|Ok|
## Summary Table
|           |                       |                                      |            |
| --------- | --------------------- | ------------------------------------ | ---------- |
| **SI No** | **Category**          | **Item Name**                        | **Yes/No** |
| 1         | Plan Irregularity     | Torsional Irregularity               | Yes        |
| 2         |                       | Re-entrant Corners                   | No         |
| 3         |                       | Diaphragm Discontinuity              | No         |
| 4         |                       | Non-parallel System                  | No         |
| 5         |                       | Out-of-Plane Offsets                 | No         |
| 6         | Vertical Irregularity | Stiffness Irregularity-Soft Story    | No         |
| 7         |                       | Mass Irregularity                    | No         |
| 8         |                       | Vertical Geometric Irregularity      | No         |
| 9         |                       | Vertical In-Plane Discontinuity      | No         |
| 10        |                       | Discontinuity in Capacity-Weak Story | No         |
# Adequacy of Structural Memebers
## Column
![[Pasted image 20240608154913.png]] 
<sup> longi rebar </sup>
![[Pasted image 20240608154957.png]] <sup> cross section of column </sup>
![[Pasted image 20240608155018.png]] 
<sup> Long section of Column </sup>
## Beam
![[Pasted image 20240608155053.png]]
<sup> longi rebar </sup>
![[Pasted image 20240608155114.png]] 
<sup> longi section of beam </sup>
![[Pasted image 20240608155143.png]]
<sup> section AA and CC of beam </sup>
![[Pasted image 20240608155212.png]]
<sup> section BB of beam </sup>
## Shear Wall

![[Pasted image 20240608155240.png]]
<sup> longi rebar of SW </sup>
![[Pasted image 20240608155309.png]]
<sup> cross section of SW </sup>
## Slab
![[Pasted image 20240608155333.png]]
<sup> Slab reinforcement req </sup>
![[Pasted image 20240608155359.png]] 
<sup> Slab reinforcement detailing </sup>
## Foundation 
![[Pasted image 20240608155455.png]]
<sup> column Load </sup>
![[Pasted image 20240608155508.png]]
<sup> Detailing of Footing (square)</sup>
# Conclusion
- Structural Inadequacies: Significant structural deficiencies were identified in the building:
	- Beams: Multiple beams failed to meet structural requirements.
	- Columns: Several columns exhibited insufficient strength based on the beam-column ratio, indicating a potential violation of the "strong column-weak beam" principle.
	- Slabs: All slabs required further evaluation for structural adequacy.
- Torsional Irregularity: The building displayed torsional irregularity, a structural weakness that can affect performance under lateral loads like wind or earthquakes.
## Recommendations
- Further modification in the Beam column section is needed
- Multiple separate designs of structural elements are needed for a more economical design