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
	- [ ]  DQ/DM within ±50 of DQS in same byte lane 
	- [ ] DQS/DQS# differential skew < 2 mil 
	- [ ] DQS to CK within ±25 mil (MIG leveling handles the rest) 
	- [ ] Fly-by topology for Addr/Cmd/CK 
	- [ ] Solid GND reference plane, no splits under DDR3 signals 
	- [ ] 50 Ω / 100 Ω impedance control
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
- [ ] Add series termination resistors on transmitter sides for rgmii
- [ ] 

# Things to consider for Second design
- Better stackup with thinner traces (other manufacturer)
- replace 0402 with 0201 resistors and caps to improve routing