SSA ==four-story== steel-framed office building comprised of three bays @ ==33 ft== in the East-West direction and two bays @ ==35 ft== in the North-South direction. The floor-to-floor height for the top three (3) floors is ==10 ft==, and for ground floor it is ==16 ft==. Based on the discussion the ==same column size== will be used for the whole height of the building. A ==6-inch-thick RCC slab== will be used in all floor system. A ==25 psf superimposed dead load== considering electrical/mechanical and floor finish need to be accounted for the design. An additional permanent ==partition load of 12 psf== is also specified. Assume ==W12X45 section is used as beam== for the whole building. The ==live load== should be taken from ==BNBC 2020== for the said occupancy type. Loads are to be combined using ==LRFD load combinations==.
1. Design Column C of the structure using the lightest section. Use W14 of A572 Grade 60 steel section for the column.
2. Propose an alternative structural arrangement for the building so that a section of lower weight compared with that of found in Question (a) can be used for Column C. Confirm and justify your alternative structural arrangement by redesigning Column C.
![[Pasted image 20240601212556.png | Section 1 - 3 ]]
![[Pasted image 20240601212649.png]]
![[Pasted image 20240601212704.png]]
![[Pasted image 20240601220543.png]]
![[417.png]]
	![[417x.png]]
	![[417y.png]]
	
## Answer 1
### Load on column C
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
- Total Dead Loads = $173.25+57.75+27.72+9.09=267.81k$
- Live Loads
	- Office buildings (Table 6.2.3; BNBC 2020)
		- File and computer rooms shall be designed for heavier loads based on anticipated occupancy
			- Lobbies and first-floor corridors = $4.8 kN/m^2$ 
			- Offices =$2.4 kN /m^2$
			- Corridors above first floor =$3.8kN /m^2$
		- Taking Offices $2.4kN /m^2 *20.885 =50.1lb /ft^2$
			- $\frac{50.1*33*17.5*4}{1000}=115.73k$
- LRFD load 
	- 1.2DL+1.6LL
	- $\phi P= 1.2*(173.25+57.75+27.72+9.09)+1.6*115.73=506.54k$
### $4.71*\sqrt(\frac{E}{F_{y}})$
- $4.71*\sqrt(\frac{E}{F_{y}})=4.71*\sqrt(\frac{29000}{60})=103.55$
### Trial 1
- Assuming Steel Section of  W14x22 for Column
	- $I_x=199 in^4$
	- $r_x=5.54 in$
	- $I_y=7 in^4$
	- $r_y=1.04 in$
- $Beam, I= 348 in^4$
- For Colum Weak Axis (Y),
	- $G_{A}=\sum \frac{\left( \frac{I}{L} \right)_{Col}}{\left( \frac{I}{L} \right)_{Beam}}$
	- $G_{A}=\frac{ \frac{7}{10*12}+\frac{7}{16*12}}{\frac{348}{33*12}+\frac{348}{33*12}}=0.05$
	- $G_{B}=Fixed=0 \approx 1$
	- $k = 1.17$
	- $kL=18.72'$
	- $\frac{kL}{r_{y}}=\frac{18.72*12}{1.04}=216 > 103.55 ( not ok)$
	- $F_{e}=\frac{\pi^2E}{\left( \frac{kL}{r} \right)}$
- From Strong axis (x)
	- $G_{A}=\frac{ \frac{199}{10*12}+\frac{199}{16*12}}{\frac{348}{35*12}}=2.5$
	- $G_{B}=Fixed= 0 \approx 1$
	- $k=1.5$
	- $kL=24'$
### Trial 2
- Assuming Steel Section of  W14x30 for Column
	- $I_x=291 in^4$
	- $r_x=5.73 in$
	- $I_y=19.6 in^4$
	- $r_y=1.49 in$
- $Beam, I= 348 in^4$
- For Colum Weak Axis (Y),
	- $G_{A}=\sum \frac{\left( \frac{I}{L} \right)_{Col}}{\left( \frac{I}{L} \right)_{Beam}}$
	- $G_{A}=\frac{ \frac{19.6}{10*12}+\frac{7}{16*12}}{\frac{348}{33*12}+\frac{348}{33*12}}=0.15$
	- $G_{B}=Fixed=0 \approx 1$
	- $k = 1.18$
	- $kL=18.88'$
	- $\frac{kL}{r_{y}}=\frac{18.88*12}{1.49}=216 > 103.55 ( not ok)$
	- $F_{e}=\frac{\pi^2E}{\left( \frac{kL}{r} \right)}$
- From Strong axis (x)
	- $G_{A}=\frac{ \frac{199}{10*12}+\frac{199}{16*12}}{\frac{348}{35*12}}=2.5$
	- $G_{B}=Fixed= 0 \approx 1$
	- $k=1.5$
	- $kL=24'$


### 1st trial
- 
- Assuming $\frac{KL}{r}=100$
- $r=4.8$ (weak y)
- $r=9.984$ (strong x)
- $F_{e}=\frac{\pi^2*29000}{\left( \frac{kL}{r} \right)^2}=\frac{\pi^2*29000}{(100)^2}=28.62 ksi$
- $F_{cr}=\left( 0.658^\left( \frac{F_{y}}{F_{e}} \right) \right)*F_{y}=\left( 0.658^\left( \frac{60}{28.62} \right) \right)*60=24.5ksi$
- $506.54k=\phi*F_{cr}*A_{g}$
	- $A_{g}=\frac{506.54}{24.5*0.9}=22.97 in^2$
- W14X82
	- $A_{g}=24in^2$
	- $r_{y}=2.48in$
### 2nd trial
- Assuming $\frac{KL}{r}=90$
- $r=2.133$
- $F_{e}=\frac{\pi^2*29000}{\left( \frac{kL}{r} \right)^2}=\frac{\pi^2*29000}{(90)^2}=35.34 ksi$
- $F_{cr}=\left( 0.658^\left( \frac{F_{y}}{F_{e}} \right) \right)*F_{y}=\left( 0.658^\left( \frac{60}{35.3} \right) \right)*60=29.48ksi$
- $506.54k=\phi*F_{cr}*A_{g}$
	- $A_{g}=\frac{506.54}{29.48*0.9}=19.09 in^2$
- W14X68
	- $A_{g}=20in^2$
	- $r_{y}=2.46in$
### 3nd trial
- Assuming $\frac{KL}{r}=80$
- $r=2.4$
- $F_{e}=\frac{\pi^2*29000}{\left( \frac{kL}{r} \right)^2}=\frac{\pi^2*29000}{(80)^2}=44.72 ksi$
- $F_{cr}=\left( 0.658^\left( \frac{F_{y}}{F_{e}} \right) \right)*F_{y}=\left( 0.658^\left( \frac{60}{44.72} \right) \right)*60=34.22ksi$
- $506.54k=\phi*F_{cr}*A_{g}$
	- $A_{g}=\frac{506.54}{34.22*0.9}=16.45 in^2$
- W14X68
	- $A_{g}=17.9in^2$
	- $r_{y}=2.45in$
	- $I_{y}=107 in^4$
	- $I_{x}=640 in^4$
### Check K value
#### Y dir
![[Pasted image 20240602005039.png]]
![[Pasted image 20240602004925.png]]
- Beam,
	- $I_{y}=50in^4$
	- $L=33'$
	- 