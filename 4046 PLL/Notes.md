# **4046 PLL Circuit**



### **DESIGN**

A. VCO Capacitor => 470pF (471 Value), VCO\_OUT (Pin 3) Direct conn. to Comp\_in (Pin 4)

B. Phase Comparator 1 used

C. Loop Filter

 	1. R3 = 68 k-Ohm (Blue-Grey-Orange-Silver)

 	2. C2 = 470pF (471 Value)

 	3. T1 = R3C2 = 31.96uS

 	4. VCO Free Range (or full VCO range), \[This is also VCO Lock Range, as described in datasheet]

 		fmin,free = 35kHz

 		fmax,free = 50kHz

 		=> 2fL = 15kHz => fL = 7.5kHz

 		=> VCO Center Freq = f0 = 42.5kHz

 

 	4. 2fc ~ (1/pi)\*sqrt((2\*pi\*fL)/T1) = 12.222kHz => fc = 6.111kHz

 	5. Capture Range (fcl, fch)

 		fcl = fo - fc = 36.389 kHz

 		fch = f0 + fc = 48.6 kHz

 



D. PWR => VCC = 5 Vdc



### 

### **Tuning:**

A. Lower Frequency of VCO (Fmin)

 	1. Connect VCO\_IN (PIN 9) to GND

 	2. Adjust R2 Resistor until VCO\_OUT (Pin 4) = 35kHz

 	3. Measurement R2 = 81.4 k-Ohm \[using 100k (104) pot.]





B. Upper Frequency of VCO (Fmax)

 	1. Connect VCO\_IN (PIN 9) to VCC (5V)

 	2. Adjust R1 Resistor until VCO\_OUT (Pin 4) = 50kHz

 	3. Measurement R1 = 140 k-Ohm \[using 1M (105) pot.]





### **Measurements:**

VCO Lock Range,

 	fmin = 35.2 kHz

 	fmax = 50.8 kHz



VCO Capture Range,

 	fmin = 35.2 kHz

 	fmax = 50 kHz

