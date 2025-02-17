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
# AC analysis
This to done to analyse the response of the circuit to time varying signals.

This is helpful to determine the signl noise, DC shift between the input and the output. This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.

# Procedure
* Connect the drain of the NMOS transistor (M1) to the 1kΩ resistor (R1).
   * Connect the other end of R1 to the V1 (1.8V DC power supply).
   * Connect the source of M1 to ground.
   * Connect the gate of M1 to a variable DC voltage source (V2).
   * Set up a multimeter or oscilloscope to measure the drain voltage (V_D).
   *DC Analysis: Set up the circuit as per the circuit diagram with proper connections ensuring valid circuit for further analysis. Apply the DC voltage of Vdd=1.8V and Vgs = 0.9 V . Go to simulate option in the tab and edit simulation command, click on DC analysis and press ok.(.op) Click on Run in the tab menu to get the DC operating point ,Vout and Id.

![image](https://github.com/user-attachments/assets/38f4d9fc-75c2-4ca5-9cbc-2d768321fdad)
# calculation
CALCULATION:
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

# Inference:
Current is directly Propotional to the Width of the Mosfet and the current changes with the change in width.

Mosfet saturation ensures the mosfet works as an amplifier and produces the desired negative gain as per the equation Av=-gm*Rd.

Q point stability is attained in saturation region thus helping in attaining linear amplification .

The Mosfet gain is increased in mid band frequency range (small signal analysis).

The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.
This is essential in high speed applications.

6.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.
Also helps in understanding the frequency response and small signal behaviour of the circuit.

Circuit 2:











