## To Do

# DDR3
- [ ] Find Assembly house in munich
- [x] Route the DDR3 memory
- [ ] impedance matching
	- 50 ohm single ended
		layer 3 and 5 trace thickness 0.175mm from multicb datasheet 
	- 100 Ohm differential 
		- 0.11 / 0.16mm (used calculator tool) 
- [ ] include all tha package delays
- [ ] replace obsolete .. with alternative
- MT41K256M16TW-093:P:  DDR3L 256x16 with speed grade 2133
	- make s skew limits much more relaxed

- [ ] Do the Delay Matching for DDR3 memory
![[Pasted image 20260326165011.png]]
![[Pasted image 20260403101223.png]]
Currently current configuration max dq skew 67ps for pair 1
- [x] check the validation of the pinout
	![[Pasted image 20260325133729.png]]
	![[Pasted image 20260325133813.png]]
- [ ] get the Correct values for the 100 Ohm differential pairs
- [ ] place the capacitors and resistors to the correct locations for the ddr3 chip
    - 4 capacitors were missing in original
	- Capacitors way to far from the power pins
	- Why are a handful of caps footprint 0201 x5R +-20 percent (makes no sense) either all or none for the same class. makes manufacturing harder
- [x] Changed Clock Termination According to UG589 from 
		![[Pasted image 20260325125533.png]]
		to
		![[Pasted image 20260325125712.png]]
		![[Pasted image 20260325125657.png]]
- [ ] 

## Ethernet
- [ ] "RGMII v2.0 is supported at 1.8V in HP I/O or up to 2.5V in HR I/O"  
	- i think i stay with the 3.3V 
	![[Pasted image 20260325150038.png]]	
- [.] Add series termination resistors on transmitter sides for rgmii
- [ ] impedance matching 50 rgmii and 100 ohm differential ethernet 

## USB

## eMMC
- [ ] chip obsolete find alternative to MTFC16GAPALNA-AIT 
	- all micron parts with unclear lifecycle information
	- SFEM016GB2ED1TO-I-5E-111-STD : 16Gb better write speed and active lifecycle

# Things to consider for Second design
- Better stackup with thinner traces (other manufacturer)
- replace 0402 with 0201 resistors and caps to improve routing
- clock with higher than 400mhz ddr but check impedance (i think you need 40 ohm for this)

## Pcie
- Differential Pair 85 Ohm +- 10%

## Qspi
Routing is not optimal.. place flash further to the fpga and maybe only use one flash without ROT Module connector.

## New Caps
- for 4.7uF use 0603: smaller packages have bigger voltage drop at 3.3V
	- Voltage rating doesn't affect the voltage drop therefore use 6.3V rated 
	- [**C0603C475K9PAC**](https://yageogroup.com/products?search=C0603C475K9PAC)  	
	- 

# JTAG Chip not available
- use this instead -> JTAG-HS3 Programming Cable
- https://www.digikey.de/en/products/detail/digilent-inc/410-299/5015666?utm_source=oemsecrets&utm_medium=aggregator&utm_campaign=buynow

# Consolidate BOM
- Reassign all parts in Kicad directly