# bandgap_reference_130nm

## Theory:

### Why we need bandgap reference circuit?

Typical silicon ICs must be stable at the low temperature like -40C to as high as 125C. Unless there is a constant voltage over the temperature range, the IC/circuits will not have proper functionality. For example, when we are thinking about a MOSFET(Metal Oxide Semiconductor Filed Effect Transistor), the source voltage can determine whether the mosfet is in linear or in the saturation region and that can alter the full functionality of the circuits (e.g. opamps etc.)

![](/images/Capture1.PNG)



### How to solve the problem?
-The most simplest way to solve the problem is to use a resistive divider

-Forward biased transistor and resistor is another approach but still shows sensitity towards temperature

-We practice here on a cmos bandgap reference circuit that achieves the requirement of low sensitivity for temperature

### BGR Types

- Self biased current mirror (simplest to start with)
- With Operational Amplifier

### Tools that we will use

We are focusing on opensource tapeout, hence from the PDK to softwares we use are opensource.

PDK: 130nm PDK offered by skywater with collaboration with Google and efbaless

Software: 

-*ngspice* for circuit simulation

-*Magic* for layout editor

##CMOS Bandgap Circuit

### Block Diagram

The overall idea of CMOS bandgap generator can be understood from the figure below. Basically two different temperature dependant voltage reference circuits are created first. These voltage refernces are complementary to each other, meaning if one increases reference voltage with respect to temperature, the other decreases the reference voltage with in similar slope with temperature. Hence substraction of these volatges gives zero resultant increase or decrease with time.  

![](/images/Capture2.PNG)
