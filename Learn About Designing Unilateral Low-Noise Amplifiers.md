Source : https://www.allaboutcircuits.com/technical-articles/learn-about-designing-unilateral-low-noise-amplifiers/

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

<img width="1366" height="603" alt="image" src="https://github.com/user-attachments/assets/631d2fc9-5825-4152-ae0c-8e3e95ab73c0" />

<img width="1376" height="766" alt="image" src="https://github.com/user-attachments/assets/2ec9a517-5319-45b3-9625-7e9f911ccca8" />


# Alternative Form of the Noise Factor Equation

<img width="1363" height="621" alt="image" src="https://github.com/user-attachments/assets/7a782e5f-746f-4efa-9224-bcba5746679a" />

<img width="1349" height="244" alt="image" src="https://github.com/user-attachments/assets/53716e3e-7c83-4291-9b32-a8425f1c5da2" />

<img width="970" height="786" alt="image" src="https://github.com/user-attachments/assets/04c4f75d-e08c-4c34-b3f7-8c7a87dc9ac2" />

<img width="829" height="476" alt="image" src="https://github.com/user-attachments/assets/8b209474-934e-4aad-88c5-10a5d170be77" />

<img width="849" height="420" alt="image" src="https://github.com/user-attachments/assets/ea812a60-053a-4e9d-9a7d-c56747a597da" />

<img width="829" height="757" alt="image" src="https://github.com/user-attachments/assets/13bd32e1-1526-4926-afb6-5fcfd85fdaff" />

<img width="1053" height="184" alt="image" src="https://github.com/user-attachments/assets/5267dd0f-1f4a-41c1-9177-ce2e01f4e54d" />

<img width="943" height="547" alt="image" src="https://github.com/user-attachments/assets/0371194f-1220-4c13-b236-20105c8c859e" />

<img width="927" height="531" alt="image" src="https://github.com/user-attachments/assets/ae5e54b3-adcd-40c7-963e-10efa210f7ec" />

<img width="895" height="616" alt="image" src="https://github.com/user-attachments/assets/64a2b3a7-dd15-4dd1-98e3-9752a7ebb634" />

<img width="902" height="799" alt="image" src="https://github.com/user-attachments/assets/1fec1e9b-23fd-42ba-a528-d8c82040a11f" />

<img width="924" height="663" alt="image" src="https://github.com/user-attachments/assets/dd1621f7-a1dd-404d-887d-27b778d9390d" />
























