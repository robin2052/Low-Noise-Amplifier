In receiver applications, the first amplifier in the signal chain has a dominant effect on the noise performance of the overallsystem. This amplifier should exhibit as low a noise figure as 
possible while providing an acceptably high power gain. Thedesign procedure for this low-noise amplifier (LNA) should therefore account for both gain and noise performance.

In this article, we’ll learn about how to design a unilateral LNA based on these requirements. We’ll start off by exploring how the noise parameters of a two-port network are specified in RF applications, then work through the process of 
designing a unilateral amplifier that achieves both a specific gain and a specific level of noise. Finally, we’ll test our design using the RFdesign software .


<img width="1595" height="661" alt="image" src="https://github.com/user-attachments/assets/aff18aa9-3c6e-4ce0-b002-5cea74351a72" />


# why NF has a minimum, where NFmin comes from, and why you cannot reduce NF below that limit, no matter what matching network you design?

🔵 1. Every Transistor Has Internal Noise Sources
Inside a MOSFET/BJT/HEMT, several physical noise mechanisms exist:

For MOSFET:

Channel thermal noise (due to random motion of electrons in the channel)
Gate resistance noise (due to real part of gate metal)
Flicker noise (1/f) (dominant at low freq)
Drain thermal noise

For BJT:

Base resistance thermal noise
Collector shot noise
Base shot noise

These internal noise sources are always present, even with no external components.

You cannot eliminate them — they are consequences of physics
(thermal agitation, carrier movement, quantum/statistical effects).

# Input Matching Can “Rotate” Noise but Cannot Reduce It Below the Intrinsic Limit
<img width="1580" height="463" alt="image" src="https://github.com/user-attachments/assets/8062d2d7-2e21-43c1-8da9-d0a0acb2f408" />

<img width="1552" height="675" alt="image" src="https://github.com/user-attachments/assets/25b8021c-de65-4ac4-b481-9b2642494194" />

<img width="1563" height="615" alt="image" src="https://github.com/user-attachments/assets/53ad513d-8739-47c4-b83c-7f56df31a109" />

<img width="1606" height="674" alt="image" src="https://github.com/user-attachments/assets/82284dd0-4fcd-4987-9a2e-08050845558b" />

<img width="1586" height="619" alt="image" src="https://github.com/user-attachments/assets/927f1973-091e-442b-b8cc-37ae353aa6f3" />

# Deep intuition about the Noise Figure

<img width="1547" height="627" alt="image" src="https://github.com/user-attachments/assets/d5642b58-38f7-4299-9a27-8f23c6a0de83" />

<img width="1519" height="468" alt="image" src="https://github.com/user-attachments/assets/4dd1a22c-dcc8-4f59-939f-b0f0ffae7836" />

# What is Noise Resistance Rn?

<img width="1515" height="732" alt="image" src="https://github.com/user-attachments/assets/d2786167-0ec4-418e-814e-2af446a1e31b" />
<img width="1111" height="215" alt="image" src="https://github.com/user-attachments/assets/f3513f00-2757-4ea3-b218-b0ca38a4bcf1" />












