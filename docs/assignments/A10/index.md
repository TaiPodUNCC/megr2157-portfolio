# A10: Lead Screw Translating System

# Project Description and Objectives

The objective of this project is to conceptually design a mechanically driven tensile testing machine capable of applying a maximum axial tensile load of **2 kN** while maintaining a controllable crosshead speed between **1 and 50 mm/min**.

The design incorporates two identical leadscrews, compatible nuts and flanges, a crosshead, and a supporting frame. The system must provide accurate, repeatable loading while maintaining structural strength and minimizing crosshead deflection.

# Design Requirements

| Parameter | Value |
|---|---|
| Maximum tensile load, ΣP | 2,000 N |
| Number of leadscrews, N<sub>s</sub> | 2 |
| Load per leadscrew, P | 1,000 N (equal-load assumption) |
| Crosshead linear speed, \|v\| | 1–50 mm/min |
| Minimum purchased leadscrew length, l<sub>min</sub> | 18 in (457.2 mm) |
| Design safety factor, SF | 4 |
| Maximum crosshead deflection, δ<sub>max</sub> | 0.1 mm |
| Thread type | Acme; modeled as square threads where directed in lecture |
| Crosshead model | Simply supported beam (lecture assumption) |
| Number of thread starts on selected screw | 1 |

## 2. Leadscrew Diameter — Jason Corum

### 2.1 Initial Knowns, Unknowns, and Assumptions

The leadscrew design began by identifying the operating requirements, unknown design parameters, and assumptions needed for preliminary engineering analysis.

Both leadscrews are assumed to have identical geometry and material properties, carry equal axial loads, and rotate synchronously. The material is treated as homogeneous and isotropic. For initial axial sizing, local thread-root stress concentrations, component weights, misalignment, and inertial effects are neglected.

**Notation:** The symbol **Ø** represents diameter. **Ø<sub>maj</sub>** is the major (nominal) diameter; **Ø<sub>R</sub>** or **Ø<sub>min</sub>** is the minor/root diameter; **Ø<sub>p</sub>** is the pitch diameter. These are different dimensions.

![Page 1: Knowns, Unknowns, and Assumptions](images/A10_01_Design_Knowns_Unknowns_Assumptions.jpg)

*Figure 1. Initial knowns, unknowns, governing conditions, and assumptions.*

### 2.2 Axial Stress Analysis

The maximum applied load is assumed to be distributed equally between the two leadscrews:

**P = ΣP / N<sub>s</sub>**

**P = (2,000 N) / 2 = 1,000 N per leadscrew**

The individual leadscrew free-body diagram establishes an axial load of 1,000 N and an equal and opposite support reaction in static equilibrium.

The governing nominal axial stress is:

**σ<sub>n</sub> = P / A<sub>cs</sub>**

For a circular cross section based on the root diameter:

**A<sub>cs</sub> = π Ø<sub>min</sub><sup>2</sup> / 4**

The allowable nominal stress is:

**σ<sub>allow</sub> = σ<sub>Y</sub> / SF**

Requiring **σ<sub>n</sub> ≤ σ<sub>allow</sub>** and solving symbolically for the minimum root diameter gives:

**Ø<sub>min</sub> ≥ √[4 P (SF) / (π σ<sub>Y</sub>)]**

### 2.3 Material Research

The McMaster-Carr catalog lists material classification, tensile strength, hardness, and fastener strength grade, but does not explicitly provide a guaranteed yield strength for the selected leadscrew. Supplementary research was performed using the *Machinery's Handbook* and published material-property references.

The professor advised using the least strength supported by the research and verifying the correct steel specification. Accordingly, the following are **provisional comparison values**, not manufacturer-certified yield strengths for McMaster part 98935A914.

| Investigated material | Investigated yield-strength values | Interpretation |
|---|---|---|
| Carbon steel | 31,900–57,000 psi | Includes comparisons to AISI 1018 and SAE Grade 2 material conditions |
| Zinc-plated carbon steel | 34,000 psi | Assumed comparable to the underlying carbon steel; coating alone does not establish a different yield strength |
| Alloy steel | 60,200–105,000 psi | Strongly dependent on the alloy and strength class |
| 18-8 stainless steel | 30,000–31,200 psi | Values associated with investigated annealed/Class 1 conditions |
| 316 stainless steel | 30,000 psi (minimum investigated) | Value associated with an investigated annealed/Class 1 condition |

A conservative assumed yield strength of **σ<sub>Y</sub> = 30,000 psi** was used for the overall candidate screening. The selected carbon-steel screw still requires verification of its actual yield strength.

### 2.4 Numerical Axial Diameter Results

| Assumed yield strength, σ<sub>Y</sub> | Calculated minimum root diameter, Ø<sub>min</sub> |
|---|---|
| 34,000 psi | 4.6611 mm (0.18351 in) |
| 105,000 psi | 2.65235 mm (0.104423 in) |
| 30,000 psi | 4.9621 mm (0.19536 in) |

The most restrictive result from the investigated axial-stress assumptions was:

**Ø<sub>min,axial</sub> = 4.9621 mm = 0.19536 in**

This axial-stress requirement alone suggests that several relatively small Acme leadscrews could be sufficient. It does not address the stability of a long screw under compression.

![Page 2: Axial Stress and Material Selection](images/A10_02_Leadscrew_FBD_Axial_Stress_and_Materials.jpg)

*Figure 2. Individual leadscrew FBD, symbolic axial-stress derivation, material research, and numerical minimum-diameter calculations.*

---

## 3. Buckling Analysis — Jason Corum

### 3.1 Buckling Model

A supplementary buckling analysis was performed to assess a conservative compressive-load case. The leadscrew was idealized as a solid circular column with pinned supports at both ends, giving the effective-length factor:

**K = 1.0 (pinned–pinned)**

The Euler critical buckling load is:

**P<sub>cr</sub> = π<sup>2</sup> E I / (K l<sub>u</sub>)<sup>2</sup>**

For a solid circular cross section evaluated at the minimum root diameter:

**I = π Ø<sub>min</sub><sup>4</sup> / 64**

Requiring a safety factor of 4 against Euler buckling:

**P<sub>cr</sub> ≥ (SF) P**

Solving for the minimum root diameter yields:

**Ø<sub>min,buckling</sub> ≥ [64 P (SF) K<sup>2</sup> l<sub>u</sub><sup>2</sup> / (π<sup>3</sup> E)]<sup>1/4</sup>**

where **E** is Young's modulus, **I** is the minimum second moment of area, **l<sub>u</sub>** is the unsupported length, and **K** is the effective-length factor.

### 3.2 Numerical Results

The preliminary calculations used the following values:

- **P = 1,000 N ≈ 224.81 lbf** per leadscrew.
- **E ≈ 29 × 10<sup>6</sup> psi** for steel.
- **K = 1.0** for pinned–pinned end conditions.
- **SF = 4.0**.
- Two assumed unsupported lengths: **18 in** and **24 in**.

| Assumed unsupported length, l<sub>u</sub> | Calculated minimum root diameter, Ø<sub>min,buckling</sub> |
|---|---|
| 18 in | 0.37948 in |
| 24 in | 0.43819 in |

The more restrictive result is:

**Ø<sub>min,buckling</sub> = 0.43819 in (for l<sub>u</sub> = 24 in)**

![Page 3: Root Diameter Selection and Buckling Setup](images/A10_03_Axial_Diameter_Selection_and_Buckling.jpg)

*Figure 3. Preliminary Acme thread screening and Euler buckling derivation.*

### 3.3 Leadscrew Selection Based on Buckling

According to Table 2b in the *Machinery's Handbook*, 32nd edition, the minimum limiting external minor diameter for the considered **5/8"-8, Class 2G Acme** thread is approximately:

**Ø<sub>R,min</sub> = 0.4570 in**

Comparison with the conservative 24-inch buckling requirement:

**0.4570 in > 0.43819 in**

Thus, the selected thread passes this **preliminary Euler buckling screening**. For the 24-inch assumed unsupported length, the estimated Euler critical load is approximately **1,064 lbf**, and the estimated buckling safety factor is approximately **4.73** for a 1,000 N axial compressive load.

**Engineering limitation:** The 24-inch purchased length is not necessarily the actual unsupported length. The final assembly must establish the actual end restraints, load path, whether the screws are in compression or tension during the test, and the unsupported spans. Euler buckling is an idealized stability model, not a substitute for verifying those conditions.

![Page 4: Buckling Results and Leadscrew Selection](images/A10_04_Buckling_Results_and_Rotational_Speed_FBD.jpg)

*Figure 4. Pinned–pinned buckling results, selection of the 5/8"-8 Acme thread, and rotational-speed FBDs.*

---

## 4. Selected Leadscrew — Jason Corum

Following the nominal axial-stress analysis, conservative buckling analysis, and catalog screening, the preliminary selected component is:

**McMaster-Carr Part Number: 98935A914**

[View the selected leadscrew on McMaster-Carr](https://www.mcmaster.com/98935A914/)

### Selected Specifications

| Specification | Value |
|---|---|
| Supplier | McMaster-Carr |
| Part number | **98935A914** |
| Quantity | **2 identical screws** |
| Material | Carbon steel |
| Fastener strength class | SAE Grade 2 |
| Thread | 5/8"-8 Acme, Class 2G |
| Thread direction | Right-hand |
| Nominal major diameter, Ø<sub>maj</sub> | 0.625 in |
| Threads per inch | 8 TPI |
| Number of thread starts | 1 |
| Pitch, p | 0.125 in |
| Lead, L | 0.125 in/rev = 3.175 mm/rev |
| Purchased length | 24 in |
| Minimum limiting root diameter, Ø<sub>R,min</sub> | 0.4570 in (handbook table) |
| Catalog tensile strength | 64,000 psi (not yield strength) |
| Catalog hardness | Rockwell B61 |

### Downloadable SOLIDWORKS CAD File

**[Download McMaster 98935A914 Leadscrew (.SLDPRT)](files/A10_McMaster_98935A914_Carbon_Steel_Acme_Lead_Screw.SLDPRT)**

The downloaded supplier model will be used as a geometry reference in the group CAD assembly. Compatibility with the final nut, flange, supports, and surrounding components must be checked.

---

## 5. Rotational Speed Analysis — Jason Corum

### 5.1 Knowns and Assumptions

The required crosshead speed range is:

**|v<sub>min</sub>| = 1 mm/min**

**|v<sub>max</sub>| = 50 mm/min**

The selected **5/8"-8** Acme thread has one thread start. Therefore, its lead equals its pitch:

**L = p = 1/8 in/rev = 0.125 in/rev = 3.175 mm/rev**

The two screws are assumed to rotate synchronously, and the kinematic model neglects backlash, slip, and elastic elongation.

### 5.2 Symbolic Derivation

The relationship between crosshead linear speed and screw rotational speed is:

**|v| = L n**

Solving for rotational speed:

**n = |v| / L**

Therefore:

**n<sub>min</sub> = |v<sub>min</sub>| / L**

**n<sub>max</sub> = |v<sub>max</sub>| / L**

The speed range difference is:

**Δn = n<sub>max</sub> − n<sub>min</sub>**

### 5.3 Numerical Results

Minimum rotational speed:

**n<sub>min</sub> = (1 mm/min) / (3.175 mm/rev) = 0.3150 rpm**

Maximum rotational speed:

**n<sub>max</sub> = (50 mm/min) / (3.175 mm/rev) = 15.748 rpm**

Difference between limits:

**Δn = 15.748 − 0.3150 = 15.433 rpm**

Thus, each synchronized leadscrew must rotate between approximately **0.3150 rpm and 15.748 rpm**.

---

## 6. Maximum Driving Torque Analysis — Jason Corum

### 6.1 Known Values and Assumptions

The torque investigation uses the same loading and force balance shown in the rotational-speed free-body diagrams in Figure 4.

| Parameter | Value |
|---|---|
| Total tensile load, ΣP | 2,000 N |
| Load per leadscrew, P | 1,000 N |
| Lead, L | 3.175 mm/rev |
| Assumed mechanical efficiency, η | 0.25 (25%) |
| Number of leadscrews, N<sub>s</sub> | 2 |

The **25% mechanical efficiency** is a provisional estimate for an Acme screw with a bronze nut. This preliminary model neglects inertial torque and additional drivetrain, support-bearing, and misalignment losses. Actual efficiency depends on the final nut and operating conditions.

### 6.2 Symbolic Solution

For one leadscrew, the required steady-state driving torque is estimated as:

**T<sub>d</sub> = P L / (2 π η)**

For the two identical leadscrews together:

**ΣT<sub>d</sub> = (ΣP) L / (2 π η)**

### 6.3 Numerical Solution

Torque required **per leadscrew**:

**T<sub>d,max</sub> = (1,000 N)(3.175 mm/rev) / [2 π (0.25)]**

**T<sub>d,max</sub> = 2,021.267 N·mm = 2.021 N·m**

Estimated combined required torque **for both leadscrews**:

**ΣT<sub>d,max</sub> = (2,000 N)(3.175 mm/rev) / [2 π (0.25)]**

**ΣT<sub>d,max</sub> = 4,042.535 N·mm = 4.043 N·m**

For independent drives, each drive must supply the per-screw torque. For a common 1:1 drive, the drive system must supply the combined screw torque plus additional drivetrain losses.

![Page 5: Rotational Speed and Driving Torque Calculations](images/A10_05_Rotational_Speed_and_Torque_Calculations.jpg)

*Figure 5. Rotational-speed calculations, required driving torque, and the provisional Acme screw/bronze nut efficiency assumption.*

---

## 7. Summary of Leadscrew Design Results

| Parameter | Preliminary result |
|---|---|
| Selected part | McMaster **98935A914** |
| Material | Carbon steel |
| Thread | 5/8"-8 Acme, right-hand |
| Purchased length | 24 in |
| Conservative provisional yield strength for comparison | 30,000 psi |
| Axial-stress minimum root diameter | 0.19536 in |
| Buckling minimum root diameter, 18-in assumed unsupported length | 0.37948 in |
| Buckling minimum root diameter, 24-in assumed unsupported length | 0.43819 in |
| Selected thread's minimum limiting root diameter | 0.4570 in |
| Estimated buckling safety factor, 24-in assumed unsupported length | 4.73 |
| Minimum rotational speed | 0.3150 rpm |
| Maximum rotational speed | 15.748 rpm |
| Maximum required torque, each leadscrew | 2.021 N·m |
| Combined required screw torque | 4.043 N·m |

### Engineering Conclusions

The axial-stress analysis permitted a significantly smaller root diameter than the conservative Euler buckling analysis. Under the pinned–pinned compression model with a 24-inch unsupported length, the preliminary buckling requirement governed the diameter selection.

The selected 5/8"-8 carbon-steel Acme leadscrew meets the nominal axial-strength screening requirement and the assumed Euler buckling requirement. Its lead provides the required crosshead linear-speed range at a relatively low shaft rotational speed. The torque calculations depend on the provisional 25% mechanical efficiency.

**Remaining checks:** Verify the actual steel strength, purchased product geometry and tolerance, axial-plus-torsional stress, actual support conditions and unsupported length, tension/compression load path, critical speed where relevant, nut thread capacity, flange mounting, and drivetrain efficiency before finalizing the complete assembly.

# Designing Crosshead (Tai Podvojsky):
I began by selecting my arbitrary dimensions (length and base) for my crosshead design. To accomplish this I considered other comparable designs I found on the internet as well as the diameter of the nut and lead screw chosen by my teammates. Ultimately I decided on values of .3m and .05m respectively. From there I chose carbon steel for my material to match the material used for the lead screw. Next I parametrically solved for the height (or thickness) of the crosshead by modeling it as a simply loaded beam and applying stress analysis.

<img width="424" height="546" alt="Screenshot 2026-11-16 at 11 34 23 PM" src="https://github.com/user-attachments/assets/f4eda676-b99c-4978-9b7f-6b4aabce9581" />

Next I performed deflection analysis on the same beam to ensure the height determined, gives strain within tolerance under the given load and safety factor. After confirming my material and dimensions for my design I applied them to a multi-view drawing to reference when completing my 3d CAD model. I converted all of my dimensions to inches to match the parts sourced from the McMaster website.

<img width="410" height="556" alt="Screenshot 2026-11-16 at 11 37 23 PM" src="https://github.com/user-attachments/assets/480b1413-5048-4f25-9827-848280a30176" />

After I completed my sketch I began modeling my crosshead design in SOLIDWORKS. I started by extruding a rectangular prism to the outer dimensions of my sketch.

 <img width="518" height="243" alt="Screenshot 2026-11-16 at 11 45 04 PM" src="https://github.com/user-attachments/assets/cc191077-9909-4630-9e0c-b14bf6e3bb53" />

 Next, I extruded UNF threaded holes to match the dimensions of the chosen mounting screws and lead screws.
 
<img width="559" height="296" alt="Screenshot 2026-11-16 at 11 44 27 PM" src="https://github.com/user-attachments/assets/bbbacd7e-3620-472c-b924-be290463b192" />

Finally I added the nut chosen by teammate Gavin to an assembly with my cross head and confirmed the two parts fit together correctly. This concluded the crosshead designing process.

<img width="528" height="155" alt="Screenshot 2026-11-16 at 11 49 20 PM" src="https://github.com/user-attachments/assets/40703115-5534-4b70-a8d7-996341ac6b2d" />

# Tabulating Costs (Tai Podvojsky):
## Bill of Materials

| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
| ---: | ---: | --- | ---: | ---: | --- |
| 1 | 1 | 932 Bearing Bronze Acme Flange Nut | $138.20 | $138.20 | [Buy here] (https://www.mcmaster.com/95120A119/ |
| 2 | 2 | Carbon Steel Acme Lead Screw | $10.29 | $20.58 | [Buy here](https://www.mcmaster.com/98935A914/) |
| 3 | 4 | Super-Corrosion-Resistant 316 Stainless Steel Socket Head Screw | $0.63 | $6.32 (pack of 10) | [Buy here](https://www.mcmaster.com/90666A013/) |
| 4 | 2 | T-Slotted Framing Rails (2ft) | $38.12 | $76.42 | [Buy here](https://www.mcmaster.com/products/4658n31/) |
| 5 | 4 | T-Slotted Framing Rails (1.5ft) | $29.08 | $116.32 | [Buy here](https://www.mcmaster.com/products/4658n31/) |
| 6 | 1 | Crosshead | $30.00 | $30.00 | Designed |
| | | | **Total Cost** | **$387.84** | |




