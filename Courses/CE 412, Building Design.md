# Materials and Building Geometry, Gravity Load calculations (DL and LL)

## Material Properties
- Compressive strength, $f'_{c}=\left( 3+\frac{x}{40} \right) ksi$
	- 3.4 ksi
- Yield Strength of Steel reinforcement, $f_{y}=\left( 60+\frac{x}{6} \right) ksi$
	- 62.67 ksi
## Building Geometry
- Grid spacing, $S=\left( 15+\frac{x}{15} \right)ft$
	- 16.067'
- Initial column dimensions: Edge and corner columns (12"X15")~(17.5"X14.5" with 4" clear cover); Center Columns (12"X18")~ (20.5"X14.5" with 4" clear cover)
- Initial beam (12"X15" 2.5" cover)~ Grade Beam (3" cover)
- Slab thickness 5" and Stair slab 6"
- Shear wall thickness 10"
- Shear wall dimension:$S*\left( \frac{S}{2} \right)$
	- $16.067*\left( \frac{16.067}{2} \right)$
- Staircase dimension (minimum):$S*\left( \frac{S}{2} \right)$
	- $16.067*\left( \frac{16.067}{2} \right)$
- OHWT dimension: Size of staircase (Height = 5 ft)
- Story: No-8, height-10ft
- Short column (Foundation to GB): height = 6 ft; cross section increases by 2” in both direction
- Clear cover for short column and GB: 3” and for column and FB: 1.5”
![[Pasted image 20240601132931.png]]
![[Pasted image 20240601132953.png]]
## Gravity Loads
### Dead Loads
- Self-weight of the structural members (Concrete)=150 pcf
	- Assign as dead: SW
- Fixed Partition Wall (FPW): 120 ppcs (on each beam)
	- Assign as FPW:
		- for 10” BW with 8.75 ft height = 875 plf
		- for 5” BW with 8.75 ft height = 437.5 plf
		- for 5” thick and 4 ft height parapet wall = 200 plf
- Floor and Roof Finish (FF): 120 pcf
	- Assign as FF:
		- For tiles with 2 to 3 inches thickness: 20 to 30 psf: use 25 psf
		- For lime terrace with 4 inches thickness: 40 psf: use 25 psf)
### Live Loads
- Floor Live load (LL42): 42 psf
- Staircase Live Load (LL100): 100 psf
- Roof Live Load (LL63): 63 psf
- Random Partition Wall (RPW): 25 psf
- OHWT (H = 5ft): 312 psf
- Lift Load: LT
	- Lift weight: $2*(SW of lift + Passenger Weight)+=4* passenger Weight$ (Note: weight per person: 75 kg) $=4*20*75$ (20 passenger limit)
	- Calculation of lift load 
$$
	- Size-of-liftcore = \frac{S}{2}+\frac{S}{2}
$$
$$
- Passenger-weight: 75 kg
$$
$$
- No-of-passenger: 20
$$
$$
-Unit -load-on-lift-machine-room: \frac{4*PassengerWeight}{Sizeofeach lift core}
$$
$$
=\frac{4*20*75}{\frac{16.067}{2}+\frac{16.067}{2}}=92.9kg /sft *2.205=204.96 psf
$$
- Gardening Load: 120 pcf (minimum as per BNBC: 105 psf):not recommended
# Earthquake Load Calculation as per BNBC 2020
## Base Shear Parameters
- Soil site Class (BNBC 2020_Table: 6.2.13)
	- Site Class according to T6.2.13 = ==SC==
- Seismic Zone Coefficient, Z
	- According to BNBC 2020, T6.2.14, ==Z = 0.28==
	- ==Zone 3==
- Importance Factor, I
	- Occupancy Category (T6.1.1) for Residential Building = II; I = 1.0 (T6.2.17)
- Determination of Seismic Design Category (SDC)
	- According to BNBC 2020, T6.2.18, ==SDC = C==
- Determination of Response Reduction Factor, R
	- According to BNBC 2020, T6.2.19, 
	- R = ==5 (Concrete IMRF)==
	- $C_{d}=4.5$
	- $\Omega_{0}=3$
- Soil Factor (S) and other related parameters (TB, TC, TD)
	- According to BNBC 2020, T6.2.16
		- ==$S = 1.15$==
		- ==$T_B= 0.20$==
		- ==$T_C= 0.6$==
		- ==$T_D = 2.0$==
- Building Period, T
	- According to BNBC 2020, T6.2.20
		- ==$C_t = 0.0466$==
		- ==$m = 0.9 (MRF)$==
		- ==$h_n = \frac{86ft}{3.28} = 26.22 m$==
		- ==$T = C_t (h_n)^m = 0.88 sec.$==
- Determination of Damping correction factor, η
	- For 5% damping, η = 1
- Calculation of Normalized acceleration response spectrum, $C_s$
	- According to Equation 6.2.35c
		- $C_s = 2.5 S η \left( \frac{T_c}{T} \right) =2.5*1.35*1*\left( \frac{0.8}{0.88} \right)=3.068$
- Determination of Seismic Dead Loads (Mass Source), W
	- W = 100% DL + 25% LL (≤63psf) + 50% LL ( &gt;63psf)
	- W = ==300psf== x Total Floor Area = 7695000 lb = 7695kip
		- Total Base Share / Total Floor Area $\approx 300$
		- $Total Area = (16.067*5)*(16.067*3)*8-(16.067*2)*16.067*4=28912.63ft^2$
		- $Total base Share (D+L)=8424804lb$
		- M=291.39 psf
- Determination of Seismic Base Shear, V
	- $V=\frac{2}{3}*\left( \frac{ZIC_{S}}{T} \right)W=\frac{2}{3}*\left( \frac{0.28*1*3.068}{7} \right)*W=0.08181W$
## Alternative Method to calculate Seismic Base Shear (ASCE 7_ETABS)
- Calculation of Spectral Response Acceleration Parameter Ss and S1
	- From table 6.C.1
		- $S_{s}=0.7$
		- $S_{1}=0.28$
- Calculation of Site Coefficient Fa and Fv
	- From table 6.C.2
		- $F_{a}=1.15$
	- From table 6.C.3
		- $F_{v}=1.725$
- Calculation of TL
	- Long Period Transition Period, TL = TD = 2.0
- Calculation of Spectral Response Acceleration Parameter SDS and SD1
	- $S_{D1}=\left( \frac{2}{3} \right)*F_{y}*S_{1}=$
	- $S_{D1}=\left( \frac{2}{3} \right)*F_{a}*S_{s}=$
# Wind Load Calculation as per BNBC 2020
- Basic Wind Speed:
	- Location of the Project: Sirajganj
	- From Table 6.2.8: V = 50.6m/s = ==114mph==
- Structural Importance Factor, I
	- From Table 6.1.1: Occupancy Category II (for residential Building)
	- From Table 6.2.9: I = 1.0
- Velocity Pressure Exposure Coefficient, Kz
	- Exposure Category ==A==/B/C
		- B for Etabs
	- From Table 6.2.11:
		- For 15 ft ≤ z ≤ z_g: $K_z = 2.01 \left( \frac{z}{Z_g} \right)^\left( \frac{2}{\alpha} \right)$
		- For z &lt; 15 ft: $K_z = 2.01 \left( \frac{15}{Z_g} \right)^\left( \frac{2}{\alpha } \right)$
	- From table 6.2.10:
		- $\alpha = 9.5$
		- $z_g = 900 ft$

| Story height (z), ft | K_z   |
| -------------------- | ----- |
| 10                   | 0.849 |
| 20                   | 0.901 |
| 30                   | 0.982 |
| 40                   | 1.04  |
| 50                   | 1.09  |
| 60                   | 1.13  |
| 70                   | 1.17  |
| 80                   | 1.207 |
- Topographic Factor, Kzt
	- For Flat Terrain, Kzt = 1.0
- Gust Effect Factor, G or Gf
	- Fundamental Period of the building, T = 0.88 sec ≤ 1.0 (Rigid Building)
	- G = 0.85
- Wind Directionality Factor, Kd
	- From table 6.2.12: for main wind force resisting system, Kd = 0.85
- External Pressure Coefficient, Cpe
	- From figure 6.2.6:
		- In x-direction
		- ![[Pasted image 20240602052828.png]]
			- L = 16.067*5=80.335  ft
			- B = 16.067*3=48.201  ft
			- L/B = 1.67
			- For windward wall, Cpe = 0.8
			- For leeward wall, Cpe = -0.366
		- In y-direction
		- ![[Pasted image 20240602052951.png]]
			- L = 48.201 ft
			- B = 80.335 ft
			- L/B = 0.6
			- For windward wall, Cpe = 0.8
			- For leeward wall, Cpe = -0.5
- Internal Pressure Coefficient, Cpi
	- Not Required
- Calculation of Velocity Pressure, q$_z$ (eqn. 6.2.17)
	- $q_z = 0.00256 I K_z K_{zt} K_d V^2 (lb/ft2)$
	- $=0.00256*1.0*K_z*1.0*0.85*1142 = 28.28 K_z$
- Calculation of Design Wind Pressure, Pz
	- In x-direction
		- $P_z = q_z G C_{p-ww} + q_h G C_{p-lw}$
		- $=28.28 K_z* 0.85*0.8 + 28.28  K_h*0.85*0.366$
		- $= 19.23 K_z + 8.8 K_h$
	- In y-direction
		-  $P_z = q_z G C_{p-ww} + q_h G C_{p-lw}$
		- $=28.28 K_z* 0.85*0.8 + 28.28  K_h*0.85*0.5$
		- $= 19.23 K_z + 12.02 K_h$


| Story Height (z), ft | Kz         | qz<br><br>(lb/ft2) | Pz (x-dir.)<br><br>(lb/ft2) | Pz (y-dir.)<br><br>(lb/ft2) |
| -------------------- | ---------- | ------------------ | --------------------------- | --------------------------- |
| 10                   | 0.849      | 24.009             | 23.8                        | 26.53                       |
| 20                   | 0.901      | 25.48              | 25.26                       | 28.156                      |
| 30                   | 0.982      | 27.77              | 27.525                      | 30.687                      |
| 40                   | 1.04       | 29.41              | 29.151                      | 32.5                        |
| 50                   | 1.09       | 30.825             | 30.552                      | 34.062                      |
| 60                   | 1.13       | 31.956             | 31.673                      | 35.312                      |
| 70                   | 1.17       | 33.087             | 32.795                      | 36.562                      |
| 80                   | 1.207 = Kh | 34.133             | 33.832                      | 37.718                      |
# Mathematical Modeling of the super structure utilizing FEA software ETABS (v16.2.1)
## Given Data
- Material Strength (f’c &amp; fy)
- Building Geometry (Grid, story) and Location and orientation of columns, beams, shear walls and slab extents as well as their dimensions.
- Gravity loads: DL & LL (as per occupancy)
- Lateral loads: Wind and Earthquake loads
## Steps to model (Define, Draw, Assign) the super structure via ETABS v16.2.1
1. Grid and Story data
2. Definition of Material properties
	- Concrete compressive strength (f’c, E)
	- Steel reinforcement yield strength (fy, fu)
3. Definition of frame members
	- Definition of column (cross section, material, confinement type, rebar strength, clear cover etc)
	- Definition of Beams (cross section, rebar strength, cover to rebar center)
4. Definition of 2D elements (area objects)
	-  Definition of slabs (Type of member: shell, membrane or plate; material strength, thickness)
	- Definition of walls (type of member: shell, membrane or plate; material strength, thickness)
5. Draw the structural geometry (column, shear wall, beam and slab)
6. Definition of dead and live loads
	- Dead loads:
		- SW (dead)\_dead\_self weight multiplier-1
		- FF\_super dead\_self weight multiplier-0
		- FPW_ super dead_self weight multiplier-0
	- Live Loads
		- RPW_live
		- LL42_live
		- LL100\_live
		- LL63\_live
		- OHWT\_live
		- Lift\_live
7. Definition and assignment of diaphragm (area diaphragm)
8. Definition of Wind loads (as per BNBC: ASCE 7-05)
9. Definition of Mass source (Seismic dead loads)
10. Definition of earthquake loads (as per ASCE 7-05)
11. Assignment of gravity loads (except self-weight)
	- FF, RPW, LL42, LL63, LL100, OHWT, Lift as area load
	- FPW as line load
12. Manual and auto mesh of slabs and walls
13. Assignment of section modifier for columns, beams, slabs, walls
	- ![[Pasted image 20240602055352.png]]
	- ![[Pasted image 20240602055357.png]]
	- ![[Pasted image 20240602055403.png]]
	- ![[Pasted image 20240602055410.png]]
14. Definition of load combinations
	- Unfactored load combinations
		- D: (SW + FF + FPW)
		- L: (LL42 + LL63 + RPW + LL100 + OHWT + Lift)
		- D + L: (SW + FF + FPW + LL42 + LL63 + RPW + LL100 + OHWT + Lift)
		- Seismic weight: (SW + FF + FPW) + 0.25(LL42 + LL63 + RPW) + 0.5(LL100 + OHWT + Lift)
		- D + 0.5L + 0.7W
	- Factored load combinations:
		- As per BNBC 2020 (75 combos or 99 combos): see lecture notes
15. Check model automatically in ETABS as well as recheck manually
16. Run analysis and check for any warning (check analysis run log)
17. Check analysis results and compare with approximate manual calculation
18. Check for serviceability and other criteria as per BNBC 2020
19. Check for building irregularities (Plan and vertical)
20. Design concrete frames (Columns and Beams)
21. Design concrete shear walls
22. Design concrete slabs
23. Design foundation (shallow foundation: footing or mat)
24. Export design outputs from ETABS (as .xlsx and .docx)
# Building Irregularities
## Plan Irregularity
1. Torsional Irregularity
	- For every EQ loads(if more than 1.2 and Less than 1.4; $\frac{\Delta max}{\Delta avg}$)
	- Show Table
		- Analysis
			- Results
				- Displacements
					- Max/AVG
					- Need Ratio
					- Not Ok
					
| Story | Load Case/Combo | Item       | Max Drift | Avg Drift | Ratio |
| ----- | --------------- | ---------- | --------- |:---------:| ----- |
| Roof  | ex1             | Diaph D1 X | 0.002035  | 0.001724  | 1.18  |
| Roof  | ex2             | Diaph D1 X | 0.00188   | 0.001715  | 1.096 |
| Roof  | ex3             | Diaph D1 X | 0.00219   | 0.001733  | 1.264 |
| Roof  | ey1             | Diaph D1 Y | 0.00279   | 0.002787  | 1.001 |
| Roof  | ey2             | Diaph D1 Y | 0.003221  |  0.00281  | 1.146 |
| Roof  | ey3             | Diaph D1 Y | 0.003166  | 0.002763  | 1.146 |
| 7F    | ex1             | Diaph D1 X | 0.002158  | 0.001777  | 1.214 |
| 7F    | ex2             | Diaph D1 X | 0.001921  | 0.001758  | 1.093 |
| 7F    | ex3             | Diaph D1 X | 0.002394  | 0.001796  | 1.333 |
| 7F    | ey1             | Diaph D1 Y | 0.003133  | 0.002932  | 1.068 |
| 7F    | ey2             | Diaph D1 Y | 0.00336   | 0.002957  | 1.136 |
| 7F    | ey3             | Diaph D1 Y | 0.003712  | 0.002908  | 1.276 |
| 6F    | ex1             | Diaph D1 X | 0.00227   | 0.001801  | 1.261 |
| 6F    | ex2             | Diaph D1 X | 0.001952  |  0.00177  | 1.103 |
| 6F    | ex3             | Diaph D1 X | 0.002588  | 0.001832  | 1.413 |
| 6F    | ey1             | Diaph D1 Y | 0.003487  | 0.003054  | 1.142 |
| 6F    | ey2             | Diaph D1 Y | 0.003443  | 0.003078  | 1.119 |
| 6F    | ey3             | Diaph D1 Y | 0.004262  | 0.003031  | 1.406 |
| 5F    | ex1             | Diaph D1 X | 0.002312  | 0.001774  | 1.304 |
| 5F    | ex2             | Diaph D1 X | 0.001934  | 0.001734  | 1.116 |
| 5F    | ex3             | Diaph D1 X | 0.00269   | 0.001814  | 1.483 |
| 5F    | ey1             | Diaph D1 Y | 0.003775  | 0.003099  | 1.218 |
| 5F    | ey2             | Diaph D1 Y | 0.003382  | 0.003119  | 1.084 |
| 5F    | ey3             | Diaph D1 Y | 0.004695  |  0.00308  | 1.524 |
| 4F    | ex1             | Diaph D1 X | 0.002253  | 0.001678  | 1.343 |
| 4F    | ex2             | Diaph D1 X | 0.001846  | 0.001632  | 1.131 |
| 4F    | ex3             | Diaph D1 X | 0.00266   | 0.001724  | 1.543 |
| 4F    | ey1             | Diaph D1 Y | 0.003899  | 0.003009  | 1.296 |
| 4F    | ey2             | Diaph D1 Y | 0.003134  | 0.003021  | 1.037 |
| 4F    | ey3             | Diaph D1 Y | 0.004889  | 0.002996  | 1.632 |
| 3F    | ex1             | Diaph D1 X | 0.00216   |  0.00151  | 1.43  |
| 3F    | ex2             | Diaph D1 X | 0.001721  | 0.001458  | 1.18  |
| 3F    | ex3             | Diaph D1 X | 0.0026    | 0.001562  | 1.664 |
| 3F    | ey1             | Diaph D1 Y | 0.003661  | 0.002742  | 1.335 |
| 3F    | ey2             | Diaph D1 Y | 0.002906  |  0.00275  | 1.057 |
| 3F    | ey3             | Diaph D1 Y | 0.004728  | 0.002733  | 1.73  |
| 2F    | ex1             | Diaph D1 X | 0.001927  | 0.001243  | 1.55  |
| 2F    | ex2             | Diaph D1 X | 0.001487  | 0.001187  | 1.252 |
| 2F    | ex3             | Diaph D1 X | 0.002367  | 0.001299  | 1.822 |
| 2F    | ey1             | Diaph D1 Y | 0.003104  | 0.002226  | 1.394 |
| 2F    | ey2             | Diaph D1 Y | 0.002422  | 0.002232  | 1.085 |
| 2F    | ey3             | Diaph D1 Y | 0.004166  | 0.002221  | 1.875 |
| 1F    | ex1             | Diaph D1 X | 0.001273  | 0.000718  | 1.773 |
| 1F    | ex2             | Diaph D1 X | 0.000928  | 0.000682  | 1.361 |
| 1F    | ex3             | Diaph D1 X | 0.001618  | 0.000755  | 2.145 |
| 1F    | ey1             | Diaph D1 Y | 0.001888  | 0.001196  | 1.578 |
| 1F    | ey2             | Diaph D1 Y | 0.001447  | 0.001234  | 1.173 |
| 1F    | ey3             | Diaph D1 Y | 0.002755  | 0.001194  | 2.307 |
2. Re-entering Corners
	- Building is irregular in terms of re-entrant corners if A/L>0.

| Story | Global X |        |         |            | Global Y |        |         |           |
| ----- | -------- | ------ | ------- | ---------- | -------- | ------ | ------- | --------- |
|       | **A**    | **L**  | **A/L** | **Status** | **A**    | **L**  | **A/L** | **Satus** |
| GF    | 0        | 80.335 | 0       | ok         | 0        | 48.201 | 0       | ok        |
| 1F    | 0        | 80.335 | 0       | ok         | 0        | 48.201 | 0       | ok        |
| 2F    | 0        | 80.335 | 0       | ok         | 0        | 48.201 | 0       | ok        |
| 3F    | 0        | 80.335 | 0       | ok         | 0        | 48.201 | 0       | ok        |
| 4F    | 0        | 80.335 | 0       | ok         | 0        | 48.201 | 0       | ok        |
| 5F    | 16.067   | 80.335 | 0.2     | ok         | 32.134   | 48.201 | 0.67    | Not ok    |
| 6F    | 16.067   | 80.335 | 0.2     | ok         | 32.134   | 48.201 | 0.67    | Not ok    |
| Roof  | 16.067   | 80.335 | 0.2     | ok         | 32.134   | 48.201 | 0.67    | Not ok    |
3. Diaphragm Discontinuity
	- Diaphragm discontinuity exists if opening area > 1/2 Total Floor Area
	- There is no opening except stair and lift in the plan of the building.
	- In terms of diaphragm discontinuity, the building is regular
4. Out of Plane Offsets
	- There is no out of plane offset irregularity in the building
5. Non-parallel System
	- All the shear walls are parallel and symmetric with centroidal orthogonal directions.
## Vertical Irregularity
1. Stiffness Irregularity-Soft Story
	- Ex1 and Ey1
	- Show Table
		- Analysis
			- Results
				- Structural Results
					- Story Stiffness
					
| Story | Load Case |     |     | Stiffness Xlb/ft |     |     | Stiffness Y lb/ft |
| ----- | --------- | --- | --- | ---------------- | --- | --- | ----------------- |
| Tank  | ex1       |     |     | 1470955.11       |     |     | 0                 |
| Roof  | ex1       |     |     | 6499876.52       |     |     | 0                 |
| 7F    | ex1       |     |     | 11582439.17      |     |     | 0                 |
| 6F    | ex1       |     |     | 16005368.36      |     |     | 0                 |
| 5F    | ex1       |     |     | 20158677.12      |     |     | 0                 |
| 4F    | ex1       |     |     | 24845677.35      |     |     | 0                 |
| 3F    | ex1       |     |     | 30549239.55      |     |     | 0                 |
| 2F    | ex1       |     |     | 39532567.06      |     |     | 0                 |
| 1F    | ex1       |     |     | 70790638.67      |     |     | 0                 |
| GF    | ex1       |     |     | 132583174.83     |     |     | 0                 |
| Tank  | ey1       |     |     | 0                |     |     | 1037490.19        |
| Roof  | ey1       |     |     | 0                |     |     | 4015718.98        |
| 7F    | ey1       |     |     | 0                |     |     | 7147017.78        |
| 6F    | ey1       |     |     | 0                |     |     | 9519699           |
| 5F    | ey1       |     |     | 0                |     |     | 11536668.71       |
| 4F    | ey1       |     |     | 0                |     |     | 13855758.09       |
| 3F    | ey1       |     |     | 0                |     |     | 16827769.67       |
| 2F    | ey1       |     |     | 0                |     |     | 22075559.86       |
| 1F    | ey1       |     |     | 0                |     |     | 42512505.74       |
| GF    | ey1       |     |     | 0                |     |     | 95282518.33       |
2. Mass Irregularity
	- Mass irregularity exists if mass of a story &gt; 200% mass of adjacent stories 
	- As per occupancy (Residential building), there is no mass irregularity
	- Show Table
		- Model
			- Structural Data
				- Mass Summary
					- Mass Summary by Story
					
| Story | UX lb-s²/ft | UY lb-s²/ft | UZ lb-s²/ft |
| ----- | ----------- | ----------- | ----------- |
| Tank  | 5403.02     | 5403.02     | 0           |
| Roof  | 18260.29    | 18260.29    | 0           |
| 7F    | 23923.03    | 23923.03    | 0           |
| 6F    | 23923.03    | 23923.03    | 0           |
| 5F    | 23923.03    | 23923.03    | 0           |
| 4F    | 26876.43    | 26876.43    | 0           |
| 3F    | 26934.71    | 26934.71    | 0           |
| 2F    | 26934.71    | 26934.71    | 0           |
| 1F    | 27034.57    | 27034.57    | 0           |
| GF    | 13904.43    | 13904.43    | 0           |
| Base  | 859.39      | 859.39      | 0           |
3.  Vertical Geometric Irregularity
	- Irregularity exists if the dimension of the lateral force resisting system at any story is more than 130% of that for any adjacent story.
	- There is no Vertical Geometric Irregularity in the building
4. Vertical In-Plane Discontinuity in Vertical Elements Resisting Lateral Force
	- Irregularity exists if the offset is greater than the width (d) or there exists a reduction in stiffness of the story below.
	- There is no Vertical In-Plane Discontinuity in Vertical Elements Resisting Lateral Force in the building
5. Discontinuity in Capacity-Weak Story
	- Story Force
	- Ex1 Ey1
	- Bottom
	- Show Table
		- Analysis
			- Results
				- Structural Results
					- Story Forces
					
| Story | Load Case/Combo | Location |     | VX lb      | VY lb      |
| ----- | --------------- | -------- | --- | ---------- | ---------- |
| Tank  | ex1             | Bottom   |     | -28639.13  | 0          |
| Tank  | ey1             | Bottom   |     | 0          | -28639.13  |
| Roof  | ex1             | Bottom   |     | -113553.52 | 0          |
| Roof  | ey1             | Bottom   |     | 0          | -113553.52 |
| 7F    | ex1             | Bottom   |     | -209583.07 | 0          |
| 7F    | ey1             | Bottom   |     | 0          | -209583.06 |
| 6F    | ex1             | Bottom   |     | -290771.46 | 0          |
| 6F    | ey1             | Bottom   |     | 5.407E-05  | -290771.46 |
| 5F    | ex1             | Bottom   |     | -357541.32 | 0          |
| 5F    | ey1             | Bottom   |     | 6.121E-05  | -357541.32 |
| 4F    | ex1             | Bottom   |     | -416898.58 | 0          |
| 4F    | ey1             | Bottom   |     | 9.251E-05  | -416898.58 |
| 3F    | ex1             | Bottom   |     | -461334.35 | 0          |
| 3F    | ey1             | Bottom   |     | 9.568E-05  | -461334.34 |
| 2F    | ex1             | Bottom   |     | -491502.65 | 0          |
| 2F    | ey1             | Bottom   |     | 9.822E-05  | -491502.65 |
| 1F    | ex1             | Bottom   |     | -508494.59 | 0          |
| 1F    | ey1             | Bottom   |     | 0.0001059  | -508494.58 |
| GF    | ex1             | Bottom   |     | -511214.62 | 0          |
| GF    | ey1             | Bottom   |     | 0.0001059  | -511214.61 |
# Serviceability Criteria
1. Vertical Deflection Limits (D+L and L)
	- Table 6.1.2: Deflection Limits
		- D+L: $\frac{16.067*2}{240}=0.803inch$
		- L: $\frac{16.067*12}{360}=0.54inch$
	- From Loads
		- Show Deformation
			- Load Combination
				- UZ
					- OK ![[Pasted image 20240602131937.png]]
2. Maximum lateral displacement for Wind Load
	- The overall sway (horizontal deflection) at the top level shall not exceed (1/500)\*H 
	- Where, H = total height of the building above ground (Section 1.5.6.2)
	- D+0.5L+0.7W: $\frac{H}{500}=(\frac{80+10}{500})*12=2.16 inch$
	- 80+10: story height + OHWT
	- Display
		- Story Response Plot
			- Display Type: Maximum Story disp
			- D+0.5L+0.7Wx1 ~ D+0.5L+0.7Wy4 (Maximum)
				- ![[Pasted image 20240602133440.png]](Wx4)
				- OK
3. Story drift for Wind Load (Section 1.5.6.1)
	- Drift ≤ 0.004 for Tn>0.7
	- Display 
		- Story Response Plot 
			- Display Type: Maximum Story drift 
			- wx1 ~ wy4 (Maximum)
			- ![[Pasted image 20240602133849.png]] (Wy4)
			- OK
4. Maximum lateral displacement for Earthquake Load
	- Table 6.2.21:
	- From Etabs we get $\delta_{ex}$
		- $\delta_{x}=\frac{C_{d}*\delta_{ex}}{I}$
		- $here, C_{d}=4.5$
	- Allowable Story Drift Limit (Δ): $0.02H = 0.02*96*12 = 23.04 inch$
	- Display 
		- Story Response Plot 
			- Display Type: Maximum Story disp 
			- ex1 ~ ey3 (Maximum)
			- ![[Pasted image 20240602140001.png]](ey3) $*C_{d}$
			- $4.05*4.5=18.25\leq 23.04$
			- Ok
5. Story drift for Earthquake Load
	- Table 6.2.21: 
	- Allowable Story Drift Limit (Δ): 0.02
	- rom Etabs we get $\delta_{ex}$
		- $\delta_{x}=\frac{C_{d}*\delta_{ex}}{I}$
		- $here, C_{d}=4.5$
	- Display 
		- Story Response Plot 
			- Display Type: Maximum Story drift
			- ex1 ~ ey3 (Maximum)
			- ![[Pasted image 20240602140403.png]] (ey3)
			- $0.0048*4.5=0.021$
			- Not Ok
			- Increase Column dim in y axis
# Additional Requirements
1. Overturning Moment (W and E)
	- Report
		- Project Report
			- 4.2 Auto Wind Loading
				- Wx1
				- ![[Pasted image 20240602142111.png]]
					- $M_{0}=16*9.28+26*9.71+36*10.41+46*10.97+56*11.44+66*11.84+76*12.201+86*19.355=5294.206 k-ft$
					- $M_{R}=\frac{W_{D+L}*(16.067*5)}{2}$
					- $W_{D+L}$
						- Show Table
							- Analysis
								- Results
									- Reactions
										- Base Reactions
											- D+L
												- Fz
												- 8424.804 kip
					- $M_{R}=\frac{8424.804*(16.067*5)}{2}=338403.31 k-ft$
				- Wy1
				- ![[Pasted image 20240602142138.png]]
				- $M_{0}=16*17.8+26*9.71+36*10.41+46*10.97+56*11.44+66*11.84+76*12.201+86*19.355=5294.206 k-ft$