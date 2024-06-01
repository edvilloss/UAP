A ==four-story== steel-framed office building comprised of three bays @ ==33 ft== in the East-West direction and two bays @ ==35 ft== in the North-South direction. The floor-to-floor height for the top three (3) floors is ==10 ft==, and for ground floor it is ==16 ft==. Based on the discussion the ==same column size== will be used for the whole height of the building. A ==6-inch-thick RCC slab== will be used in all floor system. A ==25 psf superimposed dead load== considering electrical/mechanical and floor finish need to be accounted for the design. An additional permanent ==partition load of 12 psf== is also specified. Assume ==W12X45 section is used as beam== for the whole building. The ==live load== should be taken from ==BNBC 2020== for the said occupancy type. Loads are to be combined using ==LRFD load combinations==.
1. Design Column C of the structure using the lightest section. Use W14 of A572 Grade 60 steel section for the column.
2. Propose an alternative structural arrangement for the building so that a section of lower weight compared with that of found in Question (a) can be used for Column C. Confirm and justify your alternative structural arrangement by redesigning Column C.
![[Pasted image 20240601212556.png | Section 1 - 3 ]]
![[Pasted image 20240601212649.png]]
![[Pasted image 20240601212704.png]]
![[Pasted image 20240601220543.png]]

## Answer 1
Column C
- Dead Loads
	- 6" thick slab (slab area 33'X17.5')
		- $\frac{33*17.5*6}{12}\cdot(150/1000)*4=173.25k$
	- 25 psf (electrical/mechanical and floor finish)
		- $\frac{25*33*17.5}{1000}*4=57.75k$
	- 12 psf (permanent partition load)
		- $\frac{12*33*17.5}{1000}*4=27.72k$
	- Beam W12X45
		- 45 lb/ft
		- $\frac{45*(33+17.5)}{1000}*4=9.09k$
- Live Loads
	- Office buildings (Table 6.2.3; BNBC 2020)
		- File and computer rooms shall be designed for heavier loads based on anticipated occupancy
			- Lobbies and first-floor corridors = $4.8 kN/m^2$ 