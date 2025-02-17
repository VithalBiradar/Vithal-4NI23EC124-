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
1.Create a new folder and name it as project file.Save the LT spice file in this folder.

2.Name the mosfet as CMOSN and the length as 180nm and width as 1.08um initially.

4.DC Analysis: Set up the circuit as per the circuit diagram with proper connections ensuring valid circuit for further analysis. Apply the DC voltage of Vdd=1.8V and Vgs = 0.9 V . Go to simulate option in the tab and edit simulation command, click on DC analysis and press ok.(.op) Click on Run in the tab menu to get the DC operating point ,Vout and Id.
![image](https://github.com/user-attachments/assets/38f4d9fc-75c2-4ca5-9cbc-2d768321fdad)







