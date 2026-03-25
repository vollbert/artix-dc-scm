## To Do

# DDR3
- [x] Route the DDR3 memory
- [ ] Do the Delay Matching for DDR3 memory
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
