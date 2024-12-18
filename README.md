# **Load Capacity Analysis of the Geodesic Dome**

## **Table of Contents**

1. [Introduction](#introduction)
2. [Overview of the Geodesic Dome Structure](#overview)
3. [Load Capacity Calculations at the Center Point](#load-calculations)
   - [Material Properties and Geometric Parameters](#material-properties)
   - [Cross-Sectional Properties](#cross-sectional-properties)
   - [Bending Capacity of the Flat Ends](#bending-capacity)
   - [Axial Capacity of the Tubes](#axial-capacity)
   - [Calculation of Load Capacity at the Center Point](#center-point-load)
4. [Conservative Nature of the Estimate](#conservative-estimate)
   - [Load Sharing and Structural Redundancy](#load-sharing-and-structural-redundancy)
   - [Potential for Higher Load Capacity](#potential-capacity)
5. [Strength of Other Points in the Dome](#strength-other-points)
   - [Load Distribution in a Geodesic Dome](#load-distribution)
   - [Increased Strength at Other Points](#increased-strength)
6. [Conclusion](#conclusion)
7. [Recommendations](#recommendations)

---

<a name="introduction"></a>
## **1. Introduction**

This document presents a detailed analysis of the load capacity at the center point of an 18-meter diameter geodesic dome constructed with specific steel tube dimensions and configurations. The calculations aim to determine the load the center point can safely support before bending occurs in the structural members, focusing specifically on the flat compressed ends of the steel tubes.

---

<a name="overview"></a>
## **2. Overview of the Geodesic Dome Structure**

- **Diameter:** 18 meters
- **Height:** 7 meters
- **Steel Tubes:**
  - **Cylindrical Diameter:** 0.048 meters
  - **Wall Thickness:** 0.0025 meters (assuming compressed end thickness is 0.005 m and wall thickness is half that)
- **Compressed Ends (this is the weakest point of the structure, so we will focus on it for the analysis):**
  - **Thickness:** 0.005 meters
  - **Width:** 0.04 meters
  - **Flat Length:** 0.080 meters (from crease to bolt)
 
![IMG_2534 2](https://github.com/user-attachments/assets/152f08fe-90b7-4505-a822-c2d35bad6266)

- **Center Point Configuration:**
  - **Six Tubes (Type A):** Length 1.55 meters (including compressed portions)
  - **Ring 1:** Hexagon formed by six Type B tubes, each 1.528 meters long
- **Material Properties:**
  - **Yield Strength ($F_y$)**: 235 MPa (235 × 10^6 Pa)
  - **Modulus of Elasticity ($E$)**: 200 GPa (200 × 10^9 Pa)

<img width="928" alt="Screenshot 2024-12-18 at 13 25 52" src="https://github.com/user-attachments/assets/a3214f30-395c-4bb5-a2b0-3ee976c37d4c" />


---

<a name="load-calculations"></a>
## **3. Load Capacity Calculations at the Center Point**

<a name="material-properties"></a>
### **3.1 Material Properties and Geometric Parameters**

**Determining the Angle ($\theta_1$) Between Tubes and the Horizontal Plane:**

<img width="979" alt="Screenshot 2024-12-18 at 13 37 39" src="https://github.com/user-attachments/assets/9d123373-b95c-4d7a-a30c-22374d2a7fa6" />


**Side Length of Hexagon (after overlap):**

$$
L_{\text{hex}} = 1.528\,\text{m} - 2 \times 0.030\,\text{m} = 1.468\,\text{m}
$$

**Radius of Ring 1 ($r_1$)**

$$
r_1 = \frac{L_{\text{hex}}}{2 \sin(\pi/6)} = \frac{1.468}{2 \times 0.5} = 1.468\,\text{m}
$$

**Height from Center Point to Ring 1 ($h_1$)**

Given Tube A length $L_A = 1.55\,\text{m}$:

$$
h_1 = \sqrt{L_A^2 - r_1^2} = \sqrt{1.55^2 - 1.468^2} = \sqrt{2.4025 - 2.1546} = \sqrt{0.2479} = 0.4989\,\text{m}
$$

**Angle to Horizontal ($\theta_1$)**

$$
\theta_1 = \arctan\left(\frac{h_1}{r_1}\right) = \arctan\left(\frac{0.4989}{1.468}\right) \approx 18.8^\circ
$$

---

<a name="cross-sectional-properties"></a>
### **3.2 Cross-Sectional Properties**

**a. Hollow Cylindrical Tubes**

**Outer Diameter ($D_o$)**

$$
D_o = 0.048\,\text{m}
$$

**Inner Diameter ($D_i$)**

$$
D_i = D_o - 2t = 0.048\,\text{m} - 2 \times 0.0025\,\text{m} = 0.043\,\text{m}
$$

**Cross-Sectional Area ($A_{\text{tube}}$)**

$$
A_{\text{tube}} = \frac{\pi}{4}(D_o^2 - D_i^2) = \frac{\pi}{4}(0.048^2 - 0.043^2) = 0.000357\,\text{m}^2
$$

**Moment of Inertia ($I_{\text{tube}}$)**

$$
I_{\text{tube}} = \frac{\pi}{64}(D_o^4 - D_i^4) = 9.24 \times 10^{-8}\,\text{m}^4
$$

**b. Flat Compressed Ends**

**Width ($b$)**

$$
b = 0.04\,\text{m}
$$

**Thickness ($t$)**

$$
t = 0.005\,\text{m}
$$

**Cross-Sectional Area ($A_{\text{flat}}$)**

$$
A_{\text{flat}} = b \times t = 0.04\,\text{m} \times 0.005\,\text{m} = 0.0002\,\text{m}^2
$$

**Moment of Inertia ($I_{\text{flat}}$)**

$$
I_{\text{flat}} = \frac{b t^3}{12} = \frac{0.04 \times (0.005)^3}{12} = 4.17 \times 10^{-10}\,\text{m}^4
$$

**Section Modulus ($S_{\text{flat}}$)**

$$
S_{\text{flat}} = \frac{I_{\text{flat}}}{t/2} = \frac{4.17 \times 10^{-10}\,\text{m}^4}{0.0025\,\text{m}} = 1.668 \times 10^{-7}\,\text{m}^3
$$

---

<a name="bending-capacity"></a>
### **3.3 Bending Capacity of the Flat Ends**

**Maximum Bending Moment ($M_{\text{max}}$) Before Yielding:**

$$
M_{\text{max}} = F_y \times S_{\text{flat}} = 235 \times 10^6\,\text{Pa} \times 1.668 \times 10^{-7}\,\text{m}^3 = 39.33\,\text{N}\cdot\text{m}
$$

**Assuming an Eccentricity ($e$) of 1 mm (0.001 m):**

**Maximum Axial Load ($P_{\text{bending}}$) Without Exceeding Bending Capacity:**

$$
P_{\text{bending}} = \frac{M_{\text{max}}}{e} = \frac{39.33\,\text{N}\cdot\text{m}}{0.001\,\text{m}} = 39,333\,\text{N} = 39.33\,\text{kN}
$$

---

<a name="axial-capacity"></a>
### **3.4 Axial Capacity of the Tubes**

**Axial Yield Capacity ($P_{\text{axial}}$) of Flat Ends:**

$$
P_{\text{axial}} = A_{\text{flat}} \times F_y = 0.0002\,\text{m}^2 \times 235 \times 10^6\,\text{Pa} = 47,000\,\text{N} = 47\,\text{kN}
$$

**Conclusion:** Since $P_{\text{bending}} < P_{\text{axial}}$, bending governs the design.

---

<a name="center-point-load"></a>
### **3.5 Calculation of Load Capacity at the Center Point**

**Vertical Load Contribution per Tube**

The limiting axial load per tube is $P_{\text{bending}} = 39.33\,\text{kN}$.

Angle from horizontal: $\theta_1 = 18.8^\circ$.

Vertical component:

$$
F_{\text{vertical}} = P_{\text{bending}} \times \sin(\theta_1) = 39.33\,\text{kN} \times 0.322 \approx 12.66\,\text{kN}
$$

**Total Vertical Load at Center Point**

Number of tubes $n = 6$ :

$$
P_{\text{total}} = n \times F_{\text{vertical}} = 6 \times 12.66\,\text{kN} = 75.96\,\text{kN}
$$

Convert to kilograms ( $g = 9.81\,\text{m/s}^2$ ):

$$
\text{Total Load (kg)} = \frac{75,960\,\text{N}}{9.81\,\text{m/s}^2} \approx 7,740\ \text{kg}
$$


---

<a name="conservative-estimate"></a>
## **4. Conservative Nature of the Estimate**

<a name="load-sharing-and-structural-redundancy"></a>
### **4.1 Load Sharing and Structural Redundancy**

- Conservative Calculations: This analysis is focused on the weakest vertex in the structure.
- Load Redistribution: The calcuation is based only on the strength, length and angles of the steal. We are not taking into account the fact that the rest of the dome will share load, reducing stress on individual vertices. The actual maximum capacity for the center point of the dome is likely much higher due to shared load distribution.

<a name="potential-capacity"></a>
### **4.2 Potential for Higher Load Capacity**

- Global Analysis: Considering all members should reveal higher capacity.
- FEA: Complex interactions modeled in software.
- Inherent Strength: Dome shape distributes forces efficiently, likely supporting more load.

---

<a name="strength-other-points"></a>
## **5. Strength of Other Points in the Dome**

<a name="load-distribution"></a>
### **5.1 Load Distribution in a Geodesic Dome**

- Structural Interconnectivity: The dome’s triangular network distributes loads globally.
- Redundancy: Multiple load paths reduce stress on any single member.
- Global Behavior: The dome acts as an integrated whole.

<a name="increased-strength"></a>
### **5.2 Increased Strength at Other Points**

- Less-Stressed Areas: Points away from the center see lower stress.
- Steeper Angles: More vertical tubes increase vertical load capacity.
- Additional Support: Rings and interconnections enhance strength.

---

<a name="conclusion"></a>
## **6. Conclusion**

The calculated **safe load capacity at the center point** of the geodesic dome is about **7,740 kilograms**, considering bending in the flat ends. This is a conservative estimate focusing on the weakest component and not considering global load sharing. When determining safe rigging, it's important to apply a safety factor of 10:1.

**Key Points:**

- **Bending Governs:** Flat ends’ bending capacity is the limiting factor.
- **Other Points Stronger:** Due to geometry and redundancy, other points may carry more load.
- **Load Distribution Helps:** The interconnected structure can share loads and increase capacity.

---

<a name="recommendations"></a>
## **7. Recommendations**

1. **Comprehensive Structural Analysis:**
   - Use FEA to model the entire dome.
   - Consider environmental and dynamic loads.

2. **Optimize Design:**
   - Improve connections to minimize eccentricities.
   - Divide rigs among multiple points to share load

3. **Consult a Structural Engineer:**
   - Validate calculations and ensure code compliance.

4. **Quality Construction:**
   - Precise fabrication and assembly reduce imperfections.
   - Regular inspections and maintenance.

---

**Disclaimer:** These calculations are based on given approximations and standard engineering formulas and serve as a preliminary assessment. A professional engineer should review and validate the calculations to confirm this analysis.
