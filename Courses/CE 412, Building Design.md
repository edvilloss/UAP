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
- Floor 