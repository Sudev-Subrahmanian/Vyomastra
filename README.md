# NOCTIS-I

### Narrow-beam Optical Communication for Tactical Interlink with Submarines

NOCTIS-I is a conceptual 6U CubeSat mission designed to investigate the feasibility of satellite-to-submarine communication using blue-green laser technology. The mission exploits the optical transmission window of seawater at **532 nm** to establish a one-way communication link between a Low Earth Orbit (LEO) satellite and a submerged receiver. The project was developed as part of a spacecraft systems engineering study at IIST S-SPACE.

## Mission Objective

Traditional submarine communication methods suffer from limited bandwidth, low data rates, and operational constraints. NOCTIS-I proposes the use of a spaceborne blue-green laser transmitter to deliver optical signals through the atmosphere and seawater to a submerged submarine receiver.

The mission aims to:

* Demonstrate the feasibility of satellite-to-submarine optical communication.
* Utilize the low-attenuation blue-green optical window of seawater.
* Study atmospheric losses, beam divergence, and underwater attenuation.
* Establish performance estimates for future operational systems.

---

## Mission Architecture

Communication flow:

Ground Station → S-Band Uplink → CubeSat → Laser Modulation → 532 nm DPSS Laser → Atmosphere → Ocean Surface → Water Column → Submarine Optical Receiver

The spacecraft acts as an optical relay platform, receiving commands from the ground and transmitting information to a submarine through a highly directional laser beam.


# My Contributions

## Payload Subsystem
### Orbit Selection
Did GMAT simulations to obtain the following orbit parameters: 
The payload requirements drove the orbital design:
* Low Earth Orbit at approximately 500 km altitude.
* Inclination of approximately 25° to maximize passes over the Indian Ocean.
* Nadir-pointing geometry to reduce atmospheric and water-path attenuation.
* Approximately 15 orbits per day with communication opportunities during selected passes.

### Laser Transmitter
Selected payload:
**532 nm Diode Pumped Solid-State (DPSS) Nd:YAG Laser**
Key specifications:

| Parameter            | Value    |
| -------------------- | -------- |
| Wavelength           | 532 nm   |
| Optical Output Power | 200 mW   |
| Beam Divergence      | 0.9 mrad |
| Supply Voltage       | 12 V     |
| Electrical Power     | 24 W     |

The wavelength was chosen because it lies within the blue-green transmission window of seawater, where optical attenuation is minimized.

### Optical Link Budget

A preliminary optical link budget was developed to determine feasibility.

Loss mechanisms considered:

* Atmospheric attenuation (MODTRAN analysis)
* Optical system losses
* Beam spreading losses
* Water attenuation through a 30 m column
* Receiver sensitivity constraints

Results:

| Parameter               | Value    |
| ----------------------- | -------- |
| Atmospheric Loss        | 2.5 dB   |
| Optical Loss            | 1.5 dB   |
| Geometric Loss          | 41.02 dB |
| Water Attenuation       | 19.9 dB  |
| Total Link Loss         | 64.82 dB |
| Required Optical Power  | 0.17 W   |
| Available Optical Power | 0.20 W   |

The analysis showed that the selected laser module operates close to the required power threshold, suggesting first-order feasibility of the communication concept.

### Receiver Concept

The submarine receiver employs:

* Photomultiplier Tubes (PMTs)
* Photon-counting electronics
* Optical filtering
* Pulse discrimination circuitry

To increase collection efficiency, a large optical collector using a parabolic or Cassegrain configuration was assumed, providing an effective collection radius of approximately 2 m.


## Power Subsystem

I contributed to subsystem-level power budgeting and payload power integration.

### Power Requirements
Since the optical payload is the dominant power consumer onboard, I participated extensively in spacecraft power-system sizing.

The power subsystem was designed around:

Deployable high-efficiency solar panels
Lithium-polymer battery storage
Eclipse survival capability
Payload peak-power support
Solar Array Sizing

Solar generation calculations were performed using:

Quad-junction GaAs solar cells
Beginning-of-life efficiency ≈ 31.8%
Solar irradiance ≈ 1360 W/m²

The spacecraft requires approximately 15 W of generated power during sunlit operation to simultaneously:

Power spacecraft subsystems
Recharge eclipse energy losses
Support payload operation
Battery Sizing

Using GMAT-derived eclipse durations (~36 min), energy storage requirements were estimated.

Key calculations:

Eclipse energy requirement ≈ 5.66 Wh per orbit
Minimum battery capacity ≈ 56.6 Wh
Battery selected: Optimus-80 Lithium Polymer Space Battery

The sizing considered conservative depth-of-discharge limits to improve battery lifetime and mission reliability.

Energy Budget

Two operational cases were analysed:

Nominal orbit (safe mode only)
Orbit with laser communication

The analysis showed total orbital energy consumption of approximately:

14.03 Wh (safe orbit)
14.06 Wh (communication orbit)

These values were used to determine charging requirements and solar-array sizing.

## Tools Used

* GMAT
* STK
* MODTRAN
* Orbital Mechanics Analysis
* Optical Link Budget Calculations
* CubeSat System Design Methodology

---

## Key Results

* Demonstrated a conceptual satellite-to-submarine optical communication architecture.
* Established a 532 nm blue-green laser payload design.
* Achieved an estimated communication data rate of 10 Mbps.
* Performed atmospheric and underwater attenuation analysis.
* Developed a preliminary optical link budget showing mission feasibility.
* Integrated payload requirements with spacecraft power constraints.

---

## Authors

NOCTIS-I Team
Indian Institute of Space Science and Technology (IIST)

**Sudev Subrahmanian A. R.**

* Payload Subsystem
* Power Subsystem
