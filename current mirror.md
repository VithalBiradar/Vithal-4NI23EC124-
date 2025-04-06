# Design and analyze current mirror circuit as active load in cs amplifier circuit
Before starting with the experiment we need to know what is necessity of replacing the resistive load with current mirror circuit as active load. So let us perform the experiment with resistive load and analyze the circuit and then perform experiment on the current mirror circuit as active load.

The following experiment analyzes a Common-Source (CS) amplifier with a resistive load using LTspice simulation. The objective is to study its voltage gain, frequency response, output resistace, and power consumption. The results help in understanding the limitations of a resistive load and serve as a foundation for exploring active load alternatives.
# Theory
A current mirror circuit is a commonly used configuration in analog electronics, typically employed to replicate a reference current in a load or another part of the circuit. It works by mirroring (or copying) the current flowing through one active device, such as a transistor, and using it to generate the same current in a different device, often in a different location. Basic Operation: A current mirror usually consists of two or more transistors (typically bipolar junction transistors, BJTs, or MOSFETs) that are connected in such a way that the current through one transistor is mirrored by the current through the other transistor(s).
A current mirror is an electronic circuit that replicates a reference current at its output, ensuring a stable and predictable current source. It typically consists of two or more matched transistors, where one transistor sets the reference current and the others mirror it. Current mirrors are widely used in analog circuits for biasing, amplification, and signal processing, offering high accuracy and stability. Variants like the Wilson and cascode current mirrors enhance performance by improving output resistance and reducing errors. Common in integrated circuits, current mirrors play a crucial role in maintaining consistent current flow in amplifiers, voltage regulators, and differential pairs.
# Part A
## Q.Design and analyze current mirror circuit as active load in amplifier circuit , which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and P <= 1mW. Perform DC and AC analysis for mirror ratio 1:1, 1:2. Vary length from 180nm , 500nm , 1µm.

We know that,
Itotal = P/Vdd = 1mW/1.8V = 0.555 mA
Iref = Id = Itotal/2 = 0.555mA/2 = 0.277 mA
To find Vin , Av = -gm * Rout = -gm *(ro1||r02) .
ro1=1/lambda1*(Id1) ; ro2 = 1/lambda2*(Id2) ; Here Id1 = Id2 = Id.
Thus Av= -gm * {(1)/Id*(lambda1 + lambda2)} ; here gm = 2Id/Vov
and thus substituting in equation we get Av = 2/Vov(lambda1+lambda2) ;
Vov = 0.073V and thus Vgs = 0.073 + 0.496 == 0.569V.
As Source is grounded , Vs = 0v and thus Vg = Vgs = 0.569V.
In General, 1:1 using ratio , then Iref = 0.277mA. For 1:2 using ration, then Iref = Itotal/3 = 0.183mA.
### CIRCUIT 1: 1:1 using 180nm
#### A. DC Analysis:
![image](https://github.com/user-attachments/assets/06d80f5d-60a6-4699-ba5b-56daf7f175bf)
![image](https://github.com/user-attachments/assets/28d57d0e-f718-4d79-99f2-906e9ebd2293)
#### B. Transient Analysis :
![image](https://github.com/user-attachments/assets/64278fa6-b936-4ef6-962c-a60dace7137c)
![image](https://github.com/user-attachments/assets/0a18c8ed-ebf8-430f-958f-ec43f7966a3a)
#### C. Frequency Response :
![image](https://github.com/user-attachments/assets/e0299c62-8639-4544-a5c9-a910892f6db6)
![image](https://github.com/user-attachments/assets/30d5098e-ebba-4ece-a5c2-6a7cb8e93296)
Bandwidth is 207.218Mhz.(30dB-3dB= 27dB)
## (W,L) for CMOSP is 10u,180nm and for CMOSN is 31.23u,180n.
#### CIRCUIT 2: 1:2 using 180nm
A. DC Analysis:
![image](https://github.com/user-attachments/assets/fbd321ff-db94-4f90-8a81-105a9b456e88)
![image](https://github.com/user-attachments/assets/8b43e534-3197-41fe-89a1-b622a4f1c4ed)




















