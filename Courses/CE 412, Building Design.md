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
	- According to BNBC 2020, T6.2.19, R = ==5 (Concrete IMRF)==
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
- Determination of Seismic Base Shear, V
	- $V=\frac{2}{3}*\left( \frac{ZIC_{S}}{T} \right)W=\frac{2}{3}*\left( \frac{0.28*1*3.068}{7} \right)*W=0.08181W$
## Alternative Method to calculate Seismic Base Shear (ASCE 7_ETABS)
- Calculation of Spectral Response Acceleration Parameter Ss and S1
	- From table 6.C.1
		- $S_{s}=0.7$
		- $S_{1}=0.28$
- 