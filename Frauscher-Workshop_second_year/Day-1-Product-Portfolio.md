# Frauscher Workshop — Day 1: Product Portfolio and Train Detection Systems

**Date:** 8 October 2026  
**Workshop Domain:** Railway Signalling, Train Detection and Railway Technology  
**Learning Focus:** Frauscher Product Portfolio, EULYNX, Axle Counters, RSR180 Wheel Sensors, FAdC Architecture and System Reliability

---

## 1. Introduction

Frauscher develops railway technology solutions, particularly train detection systems used in railway signalling and train operations. Train detection is essential for determining whether a track section is occupied by a train or clear for other movements.

During Day 1 of the workshop, I studied the Frauscher product portfolio, railway train detection principles, axle counter technology, wheel sensors, system architecture, communication interfaces and the importance of reliability and safety in railway infrastructure.

## 2. Frauscher Product Portfolio

The workshop introduced several product and system categories.

### 2.1 Higher-Level Railway Systems

- **IXL — Interlocking:** Prevents conflicting train movements by controlling signals and points according to defined safety conditions.
- **MDM:** A product/system category mentioned in the workshop's portfolio presentation. The exact expansion should be confirmed from the presentation.
- **SSP:** Another system category included in the portfolio overview. Its exact expansion should be confirmed from the original slide.

### 2.2 Train Detection Systems

The following products were introduced:

- **FAdC — Frauscher Advanced Counter:** An axle-counter-based train detection system.
- **FTVS:** A train detection system/product identified in the Frauscher portfolio. Confirm its full product name from the original presentation.
- **ACS2000:** A train detection product/system identified during the portfolio overview.

Train detection systems provide information about train presence and track occupancy to support railway signalling operations.

### 2.3 Point Control System

**FAdP — Frauscher Advanced Point System**

This product category relates to railway point or switch control. Points guide trains from one track to another, and their position must be correctly controlled and detected for safe train movements.

### 2.4 Frauscher Advanced Data Transmission

**FAdT — Frauscher Advanced Data Transmission**

FAdT concerns data transmission within railway applications. Reliable communication is important for transferring information between field equipment and higher-level railway systems.

---

## 3. EULYNX Platform

### 3.1 What Is EULYNX?

EULYNX is a European railway initiative that promotes standardised interfaces between railway signalling subsystems.

Its purpose is to support interoperability, reduce dependence on proprietary interfaces and make it easier to integrate compatible signalling equipment from different suppliers.

The workshop introduced the following concepts:

- IP-based architectures
- Standard Communication Interfaces (SCIs)
- Interoperability between signalling subsystems
- Standardisation of railway signalling interfaces

### 3.2 Why Is Standardisation Important?

Without standard interfaces, equipment from different manufacturers may require special integration work and proprietary communication arrangements.

Standardised interfaces can make system integration and future upgrades easier, provided the equipment implements compatible specifications.

### 3.3 EULYNX Academy

The EULYNX Academy basic course was noted as a future learning activity.

**Further study:** Understand the purpose of SCIs, interface specifications and interoperability in modern railway signalling.

---

## 4. Railway Train Detection

Train detection determines whether a train is present in a particular railway area.

The result is used by signalling and interlocking systems to help determine whether a route or track section can be safely used.

### 4.1 Track-Based Detection

Track-based systems use equipment associated with the railway track.

Two important examples are:

**A. Track Circuits**

Track circuits use electrical properties of the rails to detect train occupancy. A train's wheelsets and axles affect the electrical circuit, allowing the system to identify an occupied section.

Types introduced during the workshop:

- DC track circuits
- AC track circuits
- AFTC — Audio Frequency Track Circuits

Track circuits can also support broken-rail detection under suitable circuit conditions, although detection is not guaranteed for every rail failure.

**B. Axle Counters**

Axle counters use wheel sensors at defined points along a track.

The system counts axles entering and leaving a section. When the evaluated counts and system conditions establish that the section is clear, the system can report a clear status.

Axle counters do not directly measure the electrical continuity of the rails. Consequently, an axle counter alone cannot reliably detect every broken rail.

### 4.2 Train-Based Detection

The workshop notes also identified:

- GNSS satellite positioning
- Odometry
- CBTC systems

These approaches use train position or movement information rather than relying solely on trackside occupancy detection.

Their suitability depends on the application, system design, safety requirements and operational conditions.

### 4.3 Applications of Train Detection

Train detection technology can support:

- Track vacancy detection
- Railway interlocking
- Switch-point protection
- Level-crossing protection
- Urban and mass-transit railway operations
- Industrial and main-line railways

---

## 5. CBTC Fallback System

**CBTC stands for Communication-Based Train Control.**

CBTC is used in metro and other railway applications to support train movement control using communication and train-position information.

### 5.1 Basic Working Sequence

The sequence discussed in the workshop was:

Train → CBTC → Radio Communication → Zone Controller → Movement Authority

The components have the following roles:

1. **Train:** Reports relevant train-position and movement information.
2. **Radio communication:** Transfers data between the train and the control system.
3. **Zone Controller:** Processes relevant information and supports train movement supervision.
4. **Movement Authority:** Defines the permitted extent of train movement under the applicable control system.

### 5.2 What Is a Fallback System?

A fallback arrangement provides an alternative operating method when the primary CBTC function is unavailable or degraded.

The workshop discussed axle counters as part of the fallback concept.

A trackside train detection system can provide occupancy information to support an alternative signalling arrangement. The actual fallback sequence depends on the railway's approved design, interlocking logic and operating rules.

**Important:** A fallback system is not automatically safe merely because an axle counter is installed. All required conditions, interlocking checks and authorised operating procedures must be satisfied.

---

## 6. Triggering of a System

**Definition:** Triggering is the activation of a system or a specific response when a predefined condition or event occurs.

### Railway Example

When a train wheel passes over a wheel sensor:

1. The wheel changes the sensor's magnetic field.
2. The sensor's electrical response changes.
3. The evaluation equipment detects the response.
4. The event is processed as part of axle counting.
5. The evaluated information contributes to track-section occupancy determination.

The exact detection thresholds and logic depend on the sensor and evaluation system.

---

## 7. RAMS and RAMSS

The workshop notes recorded the term RAMSS.

RAMS is the widely used railway engineering framework covering four main properties:

| Letter | Term | Meaning |
|---|---|---|
| R | Reliability | The system performs its required function without failure for the specified period. |
| A | Availability | The system is operational and ready for use when required. |
| M | Maintainability | The system can be inspected, diagnosed, repaired and restored efficiently. |
| S | Safety | The system avoids unacceptable risks and hazardous failures. |

The additional **Security** in RAMSS refers to protecting equipment and systems against threats such as unauthorised access and cyberattacks.

RAMS and cybersecurity are related but distinct engineering concerns. Security should not be treated as a replacement for functional safety.

### Example

A train detection system should:

- Count axles reliably.
- Remain available during required operations.
- Allow technicians to diagnose faults.
- Enter or maintain a safe state when required by its safety design.
- Protect configuration and communication against unauthorised changes.

---

## 8. Track Circuits and Axle Counters: Comparison

| Feature | Track Circuit | Axle Counter |
|---|---|---|
| Basic principle | Electrical behaviour of the rails | Counting axles at detection points |
| Main equipment | Track circuit equipment and rails | Wheel sensors and evaluation equipment |
| Rail electrical continuity | Relevant to operation | Not directly measured |
| Broken-rail detection | Possible for certain failures and designs | Cannot generally detect broken rails by axle counting alone |
| Trackside tuning | Depends on circuit type and design | No track-circuit tuning in the same sense |
| Occupancy determination | Based on track-circuit state | Based on evaluated axle counts and system logic |

The workshop notes highlighted the advantages of Frauscher Advanced Counter (FAdC) installations, including no electronic evaluation boards at the trackside detection point and no trackside earthing requirement for the wheel sensor arrangement described.

These installation characteristics should be confirmed against the specific system configuration and railway standards.

---

## 9. RSR180 Wheel Sensor

### 9.1 What Is RSR180?

RSR180 is a Frauscher wheel sensor used in axle-counter train detection systems.

It detects a passing wheel through changes in its electromagnetic field. The associated evaluation equipment processes the sensor response.

The workshop introduced the sensor's operating principle, two detection systems, trigger threshold, wheel-diameter range and temperature limits.

### 9.2 Basic Components

The wheel sensor arrangement discussed in the workshop includes:

- A transmitter coil
- Receiver coils associated with SYS1 and SYS2
- Electrical connections for power and signal transmission
- An evaluation unit that processes the resulting signals

### 9.3 Working Principle

**Step 1 — Normal condition**

When no wheel is passing, the sensor produces a normal electromagnetic response.

**Step 2 — Wheel approaches**

The metallic wheel changes the magnetic field around the sensor.

**Step 3 — Signal changes**

The wheel affects the magnetic coupling and changes the receiver-coil response.

**Step 4 — Evaluation**

The evaluation unit monitors the changes and determines whether the predefined detection conditions have been satisfied.

**Step 5 — Axle counting**

The event is processed by the axle-counter logic and contributes to determining the number of axles entering or leaving the relevant section.

### 9.4 Why Are There Two Systems, SYS1 and SYS2?

The two systems provide distinct detection responses that can be evaluated in sequence.

Their order of activation helps determine the direction of wheel movement.

- SYS1 → SYS2: Direction 1, recorded in the workshop notes as an in-count direction.
- SYS2 → SYS1: Direction 2, recorded in the workshop notes as an out-count direction.

The in-count and out-count labels depend on the configured direction of the track section.

### 9.5 RSR180 Parameters Recorded During the Workshop

| Parameter | Workshop note |
|---|---|
| Wheel diameter | 300–2100 mm |
| Trigger level | Approximately 70% threshold, as recorded |
| Temperature range | Approximately −40°C to +85°C in the detailed notes |
| Transmitter operating frequency | 250 kHz |
| Maximum traversing speed | 450 km/h stated as a maximum; 310 km/h noted for field conditions |

These are training-note values, not a substitute for the official product datasheet or the configuration-specific limits.

**Current-value clarification:** The detailed notes record a normal no-wheel current range of 2.8–5 mA for both systems. The rough notes contain conflicting units and sensor states. Confirm the exact current range, damped/undamped condition and trigger definition from the workshop slides before treating these as verified specifications.

---

## 10. FAdC — Frauscher Advanced Counter

### 10.1 What Is FAdC?

FAdC is an axle-counter-based train detection system.

It processes wheel-sensor events and determines whether a railway track section is occupied or clear, subject to its evaluation logic, configuration and safety conditions.

### 10.2 Main Functions

- Detect wheel passages.
- Evaluate axle counts.
- Determine train direction where supported by the configuration.
- Monitor track-section occupancy.
- Communicate evaluated status to signalling or interlocking equipment.
- Support diagnostics and fault handling.

### 10.3 Main Components

The workshop identified the following components:

- DP — Detection Point
- RSR180 — Wheel sensor
- AEB — Advanced Evaluation Board
- BSI — Overvoltage Protection Board, as recorded in the notes
- COM — Communication Board
- IO / IO-EXB — Input/output equipment
- PSC — Power Supply Controller, as recorded in the notes

AEB evaluates wheel-sensor information. COM supports communication with higher-level equipment. IO-EXB provides configured input/output interfaces.

The precise role and naming of each board should be confirmed against the product documentation for the installed FAdC version.

---

## 11. FAdC System Architecture

The workshop introduced three architecture types:

1. Centralised architecture
2. Modular architecture
3. Combined architecture

### 11.1 General Signal Path

The simplified arrangement recorded during the workshop was:

IXL → COM → AEB → BSI → DP

Where:

- **IXL:** Interlocking system
- **COM:** Communication board
- **AEB:** Advanced Evaluation Board
- **BSI:** Overvoltage protection equipment
- **DP:** Detection point, including the wheel sensor arrangement

This is a simplified representation of the equipment and communication relationships, not a complete wiring diagram.

### 11.2 Centralised Architecture

In a centralised arrangement, multiple detection points communicate with centrally arranged evaluation and communication equipment.

The architecture concentrates system equipment and communication paths at a central location.

The workshop notes describe data from multiple wheel sensors being handled through COM equipment, with a central communication path to the interlocking system.

### 11.3 Modular Architecture

A modular arrangement distributes evaluation equipment across modules according to the installation design.

This supports modular expansion and allocation of equipment to different counting heads or track sections.

### 11.4 Combined Architecture

Combined architecture uses elements of centralised and modular arrangements.

The appropriate arrangement depends on the number of detection points, track layout, required interfaces, system capacity and installation requirements.

### 11.5 Counting Heads and Detection Points

A counting head is an equipment arrangement associated with wheel detection and evaluation.

The workshop notes identify AEB, BSI and DP as parts of the counting-head arrangement.

An AEB processes the relevant wheel-sensor signals and evaluation logic. The complete system combines these events with the appropriate track-section configuration to determine occupancy.

**Configuration note:** The workshop notes mention three DPs for creating a track section and multiple counting heads per section. Confirm the exact counting-point arrangement and maximum supported configuration from the trainer's diagram or the relevant FAdC documentation.

---

## 12. Combined Architecture and IO Boards

The workshop discussed IO boards as part of the interface between the axle-counter system and signalling equipment.

### 12.1 Purpose of IO-EXB

The IO-EXB equipment provides configured input/output interfaces, including vital relay outputs and optocoupler-based input interfaces.

Depending on the implementation, these interfaces can help isolate electrical signals between connected systems.

### 12.2 Track Occupancy Output

The FAdC system evaluates the axle-counting information and can provide the resulting track-section status.

Typical outputs include:

- **Occupied:** The track section is considered occupied according to the configured evaluation logic.
- **Clear:** The system has determined the section to be clear, subject to its required safety conditions.
- **Direction information:** Provided where supported by the configured interface.

The workshop notes describe IO equipment supplying track-section information to the signalling room.

### 12.3 Serial and Parallel Interfaces

The workshop compared two interface approaches.

**Serial/Ethernet-based communication**

- Transfers digital data in accordance with the implemented protocol.
- Can carry more structured information than a small set of discrete relay outputs.
- Requires compatible communication interfaces and suitable configuration.

**Parallel/relay-based communication**

- Uses individual signal circuits or relay contacts.
- Can be useful where discrete status outputs are required.
- Carries information through the available configured signal lines.

The interface used depends on the system design and applicable railway requirements. Neither interface should be assumed to be universally preferable in every installation.

---

## 13. Redundancy Architecture

Redundancy means providing additional equipment or communication paths to improve system availability and tolerate certain failures.

The workshop discussed redundancy between COM boards and communication channels.

### Key Concepts

- Redundant communication paths can reduce dependence on a single communication link.
- Interconnected COM equipment may exchange relevant data to support the configured redundant arrangement.
- Equipment health and communication status must be monitored.
- Redundancy does not eliminate every possible failure and must be implemented according to the approved safety architecture.

The workshop notes refer to a COM-board hotlink used for data exchange between two COM boards.

**Further study:** Identify the primary and redundant paths in the workshop's FAdC architecture diagram and understand what happens when one communication path becomes unavailable.

---

## 14. Wireless and Wired Communication

The workshop mentioned three communication media:

- Wireless communication
- Copper cable
- Optical fibre

### Copper Cable

Copper cables carry electrical signals. Their use depends on cable characteristics, distance, interference and interface requirements.

### Optical Fibre

Optical fibre carries information as optical signals. It is useful for long-distance communication and electrical isolation between connected equipment.

### Wireless Communication

Wireless links transfer information through radio signals. In railway systems, the technology must meet the requirements of the particular application and operating environment.

The communication medium and the communication protocol are different concepts: the medium carries the signal, while the protocol defines how information is exchanged.

---

## 15. Other Railway Applications and Concepts

### 15.1 Level-Crossing Protection

Train detection information can contribute to level-crossing protection by supporting the detection of an approaching train and the operation of associated warning or protection equipment.

### 15.2 Switch-Point Protection

Train detection and signalling information can be used in the wider safety logic that prevents incompatible train movements through railway points.

### 15.3 Fallen-Off Detection for Axle Counters

The workshop notes mention fallen-off detection in the context of axle-counter equipment. The exact failure condition and detection method should be checked against the relevant training slide.

### 15.4 ERTMS Levels

The workshop listed ERTMS Levels 1, 2 and 3 as topics for further study.

ERTMS is the European Rail Traffic Management System. Its levels describe different arrangements for train control and communication. Detailed level-wise working was not captured in the Day 1 notes and should be added after further study.

### 15.5 Virtual-Reality Simulation

A VR simulation was mentioned during the workshop. Add the specific simulation activity and the concepts demonstrated once the details are available.

---

## 16. Technical Terms — Quick Revision

| Term | Meaning |
|---|---|
| FAdC | Frauscher Advanced Counter |
| FAdP | Frauscher Advanced Point System |
| FAdT | Frauscher Advanced Data Transmission |
| RSR180 | Frauscher wheel sensor |
| DP | Detection Point |
| AEB | Advanced Evaluation Board |
| BSI | Overvoltage protection board, as recorded in the notes |
| COM | Communication Board |
| IXL | Interlocking |
| IO-EXB | Input/output extension equipment |
| CBTC | Communication-Based Train Control |
| EULYNX | European railway signalling standardisation initiative |
| SCI | Standard Communication Interface |
| RAMS | Reliability, Availability, Maintainability and Safety |
| RAMSS | RAMS with Security additionally included in the terminology used in the notes |
| AFTC | Audio Frequency Track Circuit |
| GNSS | Global Navigation Satellite System |
| SIL | Safety Integrity Level |

---

## 17. Key Learning Outcomes

After Day 1, I developed an introductory understanding of:

1. Frauscher's product portfolio and its railway applications.
2. EULYNX and the importance of standardised signalling interfaces.
3. The differences between track circuits and axle counters.
4. The working principle of a wheel sensor using electromagnetic-field changes.
5. The use of SYS1 and SYS2 responses for wheel detection and direction evaluation.
6. The role of the FAdC system in determining track occupancy.
7. The purpose of AEB, COM, BSI, DP and IO-EXB equipment.
8. Centralised, modular and combined system architectures.
9. Redundancy and communication interfaces in railway signalling.
10. RAMS and the additional importance of security.

## 18. Questions for Further Study

- How does the FAdC evaluate axle counts and determine whether a track section is clear?
- How do SYS1 and SYS2 detect a wheel and determine its direction?
- What is the exact role of the AEB and COM boards in the FAdC architecture?
- How do serial and relay-based interfaces differ in a real railway installation?
- How does a CBTC fallback arrangement use alternative train detection?
- What are the differences between ERTMS Levels 1, 2 and 3?
- What are the official specifications and operating limits of the RSR180 wheel sensor?
- How are diagnostics, redundancy and safety conditions handled in the system?

## 19. Further Learning Resources

- [Frauscher Official Website](https://www.frauscher.com/)
- [Indian Railways Official Website](https://indianrailways.gov.in/)

**Planned learning:** EULYNX Academy Basic Course and further study of railway signal engineering, ERTMS and FAdC system architecture.

---

*This document records my Day 1 learning from the Frauscher workshop. It is intended for educational purposes and is not a substitute for official product documentation, approved railway signalling designs or operating procedures.*