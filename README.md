# Experiment - 1 
Analysis of cs amplifier
## Aim:
analyse the Dc analysis, transienr and AC analysis of a CS amplifier circuit and extract the variuos parameters 
associated using LT spice.
## Components are required:
Resistor(1K),voltage supply(1.8v,0.9v) Mosfet(nmos4,pmos4),and connecting wirees.
## Theory:
Mosfet plays a very important role in the electronics.
why we mostly prefer Mosfet as transistor means due to its compact design,low power consumpation,simple 
in the geometry and  adjustable in the size in the VLSI techanolgy.

Mosfet has a four terminals(drain,source,gate,body),And Mosfet has three different configuration can be connected 
through common drain,common gate and common souce the most prefered configuration of the Mosfet is the common source
and common drain because of the amplification in this configuration Mosfet act as a good amplifier.
The Mosfet in the saturation region acts as a good amplifier and the operation condition most be satify these
condition where Vgs>Vth,Vgd<Vth and Vds>=Vov for an N channel mosfet.In the common source configuration there is a 180 degree phase shift between the input and output.
There is very high input impedence that is nearly equal to Ig=0 idealy infinite.
The drain current
Id=1/2kn*Vov*Vov;Vov=Vgs-Vt and Kn=UnCoxW/L
This is the eqation foe the drain current in the saturation region.
# dc analysis
DC Analysis (Direct Current Analysis) is a method used to determine the steady-state behavior of an electrical circuit when powered by constant (DC) voltage or current sources
Finding Node Voltages (using Kirchhoff’s Voltage Law - KVL)
Calculating Branch Currents (using Kirchhoff’s Current Law - KCL)
Determining the Operating Region of Active Components (like MOSFETs, BJTs, and Diodes)
It helps in understanding how a circuit behaves under constant (non-time-varying) conditions, which is useful for biasing and setting up initial conditions before applying AC signals.
# transient analysis
This to done to analyse the response of the circuit to time varying signals.

This is helpful to determine the signl noise, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
# AC analysis
This is nothing but the small signal analysis of the circuit.This is done to determine the Gain of the amplifier circuit .
This also helps to analyze the Frequency Reponse of the amplifier circuit. the gain is given by Av = -gm Rd

# Procedure
* Connect the drain of the NMOS transistor (M1) to the 1kΩ resistor (R1).
   * Connect the other end of R1 to the V1 (1.8V DC power supply).
   * Connect the source of M1 to ground.
   * Connect the gate of M1 to a variable DC voltage source (V2).
   * Set up a multimeter or oscilloscope to measure the drain voltage (V_D).
   *DC Analysis: Set up the circuit as per the circuit diagram with proper connections ensuring valid circuit for further analysis. Apply the DC voltage of Vdd=1.8V and Vgs = 0.9 V . Go to simulate option in the tab and edit simulation command, click on DC analysis and press ok.(.op) Click on Run in the tab menu to get the DC operating point ,Vout and Id.

![image](https://github.com/user-attachments/assets/38f4d9fc-75c2-4ca5-9cbc-2d768321fdad)
# calculation
Power = 50uW
Loop Equation: Vdd=Vds+Id*Rd
P=I*V (Id=27.08uA , Vdd=1.8V)
clearly Vds=Vout; Vds>=Vgs-Vth
Rd (upon calculation) =10.33Kohm
Widhth=0.3um(Vary width to get the current)
Vds=1.772V
gain=-20dB(from AC analysis)
Q point is (1.772V,27.08uA)

# Result
![image](https://github.com/user-attachments/assets/2df09210-0a66-4708-be89-7ffc049790be)
Id=27.08uA
vout=1.772v
width=1.08um
DC Operating point : (1.772,27.08uA) is obtained for 1.08um Width and 180nm Length.
# transient analysis
![image](https://github.com/user-attachments/assets/efdcb483-43cb-4f48-b903-8659b34b1a95)
Vout=1.772v
There is 180 degree phase shift between input and output or the DC level shift
# Ac analysis
![image](https://github.com/user-attachments/assets/3cf65998-4b65-46bb-8cca-79b2e141505a)
#inference
1.Current is directly Propotional to the Width of the Mosfet and the current varies with the change in width.
2.Mosfet saturation ensures the mosfet works as an amplifier and produces the desired negative gain as per the equation Av=-gm*Rd.
3.Q point stability is attained in saturation region thus helping in attaining linear amplification .
4.The Mosfet gain is increased in mid band frequency range (small signal analysis).
5.The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.
6.This is essential in high speed applications.
7.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.
Also helps in understanding the frequency response and small signal behaviour of the circuit.

Circuit 2:
# Theory
This is done ensure the mosfet operates in saturation and to calculate the DC operationg point of the transistor. This prevents signal noise .
This helps in the determination of the biasing resistors.
This helps in getting a correct operating point despite the fluctuation in the other parameters.

# dc analysis
DC Analysis (Direct Current Analysis) is a method used to determine the steady-state behavior of an electrical circuit when powered by constant (DC) voltage or current sources
Finding Node Voltages (using Kirchhoff’s Voltage Law - KVL)
Calculating Branch Currents (using Kirchhoff’s Current Law - KCL)
Determining the Operating Region of Active Components (like MOSFETs, BJTs, and Diodes)
It helps in understanding how a circuit behaves under constant (non-time-varying) conditions, which is useful for biasing and setting up initial conditions before applying AC signals.
# transient analysis
This to done to analyse the response of the circuit to time varying signals.

This is helpful to determine the signl noise, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
# AC analysis
This is nothing but the small signal analysis of the circuit.This is done to determine the Gain of the amplifier circuit .
This also helps to analyze the Frequency Reponse of the amplifier circuit. the gain is given by Av = -gm Rd

# Procedure: 
1. Open LTspice and Create a New Schematicand Launch LTspice.Create a new schematic by selecting File → New Schematic.
2. Place Components Voltage Sources (V1 & V2) and Select Voltage and place two sources.Set V1 as a DC source with 1.8V.Set V2 as an AC + sine source: SINE(0.7 50m 1K) AC 1.
Transistors (PMOS & NMOS),Add PMOS and NMOS transistors from the component library.Connect them in a CMOS inverter configuration:M2 (PMOS): Source to V1 (1.8V), Drain to Vout.
M1 (NMOS): Drain to Vout, Source to Ground.Gate of both transistors connected to V2.
3. Define the MOSFET Models
AC Analysis:.ac dec 20 0.1 1T.This performs an AC sweep from 0.1Hz to 1THz in 20 points per decade.
Transient Analysis:.tran 3m,Runs a transient simulation for 3ms.
4.Observe how the circuit responds in time domain (transient).Check the gain and phase shift (AC analysis).
# CIRCUIT DIAGRAM
![image](https://github.com/user-attachments/assets/68bca057-c33b-4e5e-9352-1b6f6b9bf32b)
# calculation

# result
![image](https://github.com/user-attachments/assets/e41dae36-1f96-4bfd-80f8-890a1efd3fb3)
DC Operating Point =( 0.9V ,27uA)
# Transient Analysis:
![image](https://github.com/user-attachments/assets/cbf45a5d-6779-48bd-8aaf-270ce9af4cc1)
There is 180 degree phase shift between input and output and a DC level phase shift observed.
Vout=0.9V and the width =1.08um.
# AC Analysis:
![image](https://github.com/user-attachments/assets/d3d5cf60-603f-4086-9882-9f11252055d0)

# Inference:
1.The Current Id is dependent on width and hence it changes when the width changes whereas the remaining parameters remain constany.
2.DC Analysis ensures proper biasing and hence the mosfet operates in saturation and Q point stability is attained.
3.The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.
This is essential in high speed applications.
4.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.
Also helps in understanding the frequency response and small signal behaviour of the circuit.
5.Together all the analysis helps in designing and opyimising an amplifier.




















