# Low-Noise-Amplifier

A low-noise amplifier (LNA) is an electronic component that amplifies a very low-power signal without significantly degrading its signal-to-noise ratio (SNR). Any electronic amplifier will increase the power of both the signal and the noise present at its input, but the amplifier will also introduce some additional noise. LNAs are designed to minimize that additional noise, by choosing special components, operating points, and circuit topologies. Minimizing additional noise must balance with other design goals such as power gain and impedance matching.

LNAs are found in radio communications systems, amateur radio stations, medical instruments and electronic test equipment. A typical LNA may supply a power gain of 100 (20 decibels (dB)) while decreasing the SNR by less than a factor of two (a 3 dB noise figure (NF)). Although LNAs are primarily concerned with weak signals that are just above the noise floor, they must also consider the presence of larger signals that cause intermodulation distortion.

# Design considerations

Low noise amplifiers are the building blocks of communication systems and instruments. The most important LNA specifications or attributes are:[2]

Gain
Noise figure
Linearity
Maximum RF input
A good LNA has a low NF (e.g. 1 dB), enough gain to boost the signal (e.g. 10 dB) and a large enough inter-modulation and compression point (IP3 and P1dB) to do the work required of it. Further specifications are the LNA's operating bandwidth, gain flatness, stability, input and output voltage standing wave ratio (VSWR).

For low noise, a high amplification is required for the amplifier in the first stage. Therefore, junction field-effect transistors (JFETs) and high-electron-mobility transistors (HEMTs) are often used. They are driven in a high-current regime, which is not energy-efficient but reduces the relative amount of shot noise. It also requires input and output impedance matching circuits for narrow-band circuits to enhance the gain (see Gain-bandwidth product)

# Gain
Amplifiers need a device to provide gain. In the 1940s, that device was a vacuum tube, but now it is usually a transistor. The transistor may be one of many varieties of bipolar transistors or field-effect transistors. Other devices producing gain, such as tunnel diodes, may be used.

Broadly speaking, two categories of transistor models are used in LNA design: Small-signal models use quasi-linear models of noise and large-signal models consider non-linear mixing.

The amount of gain applied is often a compromise. On the one hand, high gain makes weak signals strong. On the other hand, high gain means higher-level signals, and such high-level signals with high gain may exceed the amplifier's dynamic range or cause other types of noise such as harmonic distortion or nonlinear mixing.

# Noise figure
The noise figure helps determine the efficiency of a particular LNA. LNA suitability for a particular application is typically based on its noise figure. In general, a low noise figure results in better signal reception.

# Impedance
The circuit topology affects input and output impedance. In general, the source impedance is matched to the input impedance because that will maximize the power transfer from the source to the device. If the source impedance is low, then a common base or common gate circuit topology may be appropriate. For a medium source impedance, a common emitter or common source topology may be used. With a high source resistance, a common collector or common drain topology may be appropriate. An input impedance match may not produce the lowest noise figure.

# Biasing

Another design issue is the noise introduced by biasing networks. In communication circuits, biasing networks play a critical role in establishing stable operating points for active components, but they also introduce noise. The primary types of noise introduced by these networks are thermal noise and flicker noise. Thermal noise arises from resistive elements in the network, which is inevitable as any resistive component generates noise due to the random motion of charge carriers. This type of noise is especially problematic at high frequencies. Flicker noise, also known as 1/f noise, is related to the current flow through devices like transistors and becomes more significant at lower frequencies.[3]

In an LNA, the biasing network must be carefully designed to minimize the impact of noise on the overall performance. Improper biasing can lead to increased noise figures, compromising the signal-to-noise ratio and degrading communication system performance. The design and selection of components within the bias network are therefore crucial to ensuring low-noise operation, particularly in systems that rely on amplifying weak signals.[4]

In practice, the bias point strongly affects an LNA’s noise figure, gain, linearity, and stability. A transistor’s key noise parameters, the minimum noise factor (F_min), the equivalent noise resistance (R_n), and the optimum source match (Γ_opt), all change with current and voltage. Designers therefore sweep the quiescent current and voltage and pick a bias that meets the noise figure target while leaving headroom for linear operation, rather than simply using the highest current available.[5][6]

Common bias schemes include simple self bias, which uses a source or emitter resistor with a gate or base divider, and active bias loops that hold the quiescent current over temperature and process variation. Self bias is passive and tends to stabilize with temperature but slightly reduces available gain. Active bias improves repeatability, at the cost of extra circuitry and possible loop stability checks.[7][8]

Technology specific sequencing also matters. Many depletion mode LNAs need a negative gate bias and a positive drain supply. To prevent overcurrent during power up and power down, the gate bias is applied and removed before the drain supply. Designers often use bias controllers or simple sequencing circuits, sometimes with temperature compensation. By contrast, some LNAs, such as CMOS, usually run from a single positive supply and set current with emitter or source degeneration plus active bias.[9][10][11]

Because S parameters and stability factors change with bias and temperature, LNAs that may see arbitrary source impedances are typically checked for unconditional stability across bias and temperature corners. Only the minimum damping or feedback needed is added so that stability does not unduly raise the noise figure.[12]

# Applications
LNAs are used in communications receivers such as in radio telescopes, cellular telephones, GPS receivers, wireless LANs (WiFi), and satellite communications.

In a satellite communications system, the ground station receiving antenna uses an LNA because the received signal is weak since satellites have limited power and therefore use low-power transmitters. The satellites are also distant and suffer path loss: low Earth orbit satellites might be 120 miles (190 km) away; a geosynchronous satellite is 22,236 miles (35,785 km) away.

The LNA boosts the antenna signal to overcome feed line losses between the antenna and the receiver.

LNAs can enhance the performance of software-defined radio (SDR) receiver systems. SDRs are typically designed to be general purpose and therefore the noise figure is not optimized for any one particular application. With an LNA and appropriate filter, performance is improved over a range of frequencies.


# Design Procedure 

## Step 1: Check Transit Frequency and Nfmin.

When w is Increased the Nfmin  decreases but the Transit Frequency Decreases. So We Have to trade Off between them .
<img width="1565" height="705" alt="image" src="https://github.com/user-attachments/assets/ca10cfd2-5b46-4c11-bbc8-130c92cff18d" />
From My design when i Increase the bias resistance the Nfmin was decreasing and also the max gain goes up to  20 dB. This is not expected as we know that the noise increase with resistor.

## Step 2: Check the stability 
k>1
Mu>1
Del<1

##  Step 3: Check the Nf and Nfmin 

## Step 4: Matching from the gain and noise circle In the input side and The output side will be matched by Normal Lc Matching.

# Design An Amplifier Which Specifications are :
### Gain > 13dB
### Nf <2.3 dB
### I < 7mA
### Frequency of operation 5 Ghz

# Circuit of the Design 

<img width="1302" height="657" alt="image" src="https://github.com/user-attachments/assets/98242d09-7551-4cdc-8715-d96cef1869e0" />

# Result Of the design 
<img width="862" height="759" alt="image" src="https://github.com/user-attachments/assets/68e5cac8-b8db-43f7-9798-74a7783dd07f" />





