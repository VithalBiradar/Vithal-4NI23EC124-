# Design and analyze current mirror circuit as active load in cs amplifier circuit
Before starting with the experiment we need to know what is necessity of replacing the resistive load with current mirror circuit as active load. So let us perform the experiment with resistive load and analyze the circuit and then perform experiment on the current mirror circuit as active load.

The following experiment analyzes a Common-Source (CS) amplifier with a resistive load using LTspice simulation. The objective is to study its voltage gain, frequency response, output resistace, and power consumption. The results help in understanding the limitations of a resistive load and serve as a foundation for exploring active load alternatives.
# Theory
A current mirror circuit is a commonly used configuration in analog electronics, typically employed to replicate a reference current in a load or another part of the circuit. It works by mirroring (or copying) the current flowing through one active device, such as a transistor, and using it to generate the same current in a different device, often in a different location. Basic Operation: A current mirror usually consists of two or more transistors (typically bipolar junction transistors, BJTs, or MOSFETs) that are connected in such a way that the current through one transistor is mirrored by the current through the other transistor(s).

