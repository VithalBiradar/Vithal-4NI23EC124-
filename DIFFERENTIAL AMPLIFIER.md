# AIM :
Design and Analyze the MOS differential amplifier circuitfor the following specifications
## Components Required
N-MOSFET(nmos4),Resistor(1.833k,0.416k),Power Supply(DC:2.5V, 1.3V),Current source(1.2,mA),Signal generator
## Theory :
A differential amplifier is an electronic circuit that amplifies the difference between two input signals while rejecting any signals that are common to both inputs (common-mode signals). It is a fundamental building block in analog circuits, commonly used in instrumentation, operational amplifiers (op-amps), and signal processing applications.

## Basic Circuit Configuration :
A basic differential amplifier consists of :

1.Two inputs V1 and V2

2.Two Resistors to set gain

3.Power supply

4.An operational amplifer
Two different modes of differentail amplifier :
Common mode :
Common modes siganl : (V1 + V2)/2

2.Diferential mode :
The difference between two inputs : V1 - V2

# Working principle :

The output voltage is proportional to the difference between the two input voltages.

If both the inputs receive the same siganl (common-mode signal), the ideal differential amplifier suppresses it.

The gain of the amplifier depends on the circuit configuration and reisistor values.

Vout = Ad (V1-V2)

Here Ad is differential gain

# Procedure :

1.Open the LTspice software, merge the library file for getting accurate values of NMOS.

2.Select the components which are needed to us like for circuit 1 we need 1.833k & 0.4166k resistor,2 CMOSN, three voltage sources(1.3v,2.5v),ground from the components list.

3.Place them all components in necessory way which is helpfull, connect all the components as in given circuit .

4.Link the specification of list of properties of mosfet like threshold voltage, temperature etc.

5.Lets do the DC Analysis first by opting a simulation, we get .op so after placing it we will get the values of it, thet will displayed.

6.After that lets take Transient analysis of 5m cycle so in input and output waveforms in 5 complete cycle, so here we get and seperate and combined waveforms of input and output.

7.For AC analysis, we should do some changes like converting DC SOURCE to sinosoidal waveform (1.3,50m,1T),after that select the AC simulation from the given options of simulation after giving values of (Decade,20,0.1,1T). So we will get a output after placing node to output waveform
# Circuit 1
![1 1st](https://github.com/user-attachments/assets/0d41fe3d-f04b-4132-8939-f6d07be944f3)
# Dc analysis
![2 dc ouptu](https://github.com/user-attachments/assets/40b661a0-8654-46fd-9413-8aa98d7051cb)
Id1 = 0.6mA

Id2 = 0.6mA

Vocm = 1.4 V

vocm1 = 1.4 V
# Transient Analysis :
Input and Output combined waveforms :
![transient1](https://github.com/user-attachments/assets/6c58f6f7-872c-49ee-97b7-cb93177171f6)
Gain = Vout / Vin

 = (1.35 - 1.25) / (1.65 - 1.15)

 = 0.2 
Gain in dB = 20 * log (0.2)

       = -13.97 dB
 # AC Analysis :
 ![ac analysis 1st](https://github.com/user-attachments/assets/702492f6-4d92-49b3-9ce8-d9e82547e90f)
# Circuit 2 
![2 dc out](https://github.com/user-attachments/assets/7c267307-f6a2-4357-b77c-343c0164e133)
# DC Analysis :
![2nd dc](https://github.com/user-attachments/assets/a01855a0-de89-44af-9bf3-a3a8cc70af06)
Id1 = 0.6mA

Id2 = 0.6mA

Vocm = 1.4 V

vocm1 = 1.4 V
# Transient Analysis :
input output combined waveform
![2nd transient](https://github.com/user-attachments/assets/6b786922-52f5-46d9-b94e-c9cad0c89e73)
Gain = Vout / Vin

 = (1.35 - 1.25) / (1.65 - 1.15)

 = 0.2 
Gain in dB = 20 * log (0.2)

       = -13.97 dB
# AC Analysis  
![2nd ac](https://github.com/user-attachments/assets/f75f568f-cf0e-45fd-8d94-7349ce514b02)
# Circuit 3 :
![3 dc](https://github.com/user-attachments/assets/68a4b5b5-6886-4b93-8c80-5847a0e38090)
dc analysis
![ci3 dc out](https://github.com/user-attachments/assets/bbd94904-d67e-48cd-9cba-bc05a0d42a9e)
Id1 = 0.6mA

Id2 = 0.6mA

Vocm = 1.4 V

vocm1 = 1.4 V
Transient Anaysis :
input wave form






       




