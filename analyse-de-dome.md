Voici la traduction en français :

---

# **Analyse de la capacité de charge du dôme géodésique**

## **Table des matières**

1. [Introduction](#introduction)  
2. [Vue d’ensemble de la structure du dôme géodésique](#overview)  
3. [Calculs de la capacité de charge au point central](#load-calculations)  
   - [Propriétés des matériaux et paramètres géométriques](#material-properties)  
   - [Propriétés des sections transversales](#cross-sectional-properties)  
   - [Capacité en flexion des extrémités aplaties](#bending-capacity)  
   - [Capacité axiale des tubes](#axial-capacity)  
   - [Calcul de la capacité de charge au point central](#center-point-load)  
4. [Caractère conservateur de l’estimation](#conservative-estimate)  
   - [Répartition des charges et redondance structurelle](#load-sharing-and-structural-redundancy)  
   - [Potentiel d’une capacité de charge supérieure](#potential-capacity)  
5. [Résistance d’autres points du dôme](#strength-other-points)  
   - [Répartition des charges dans un dôme géodésique](#load-distribution)  
   - [Résistance accrue à d’autres points](#increased-strength)  
6. [Conclusion](#conclusion)  
7. [Recommandations](#recommendations)

---

<a name="introduction"></a>  
## **1. Introduction**

Ce document présente une analyse détaillée de la capacité de charge au point central d’un dôme géodésique de 18 mètres de diamètre, construit avec des tubes en acier de dimensions et configurations spécifiques. Les calculs visent à déterminer la charge que le point central peut supporter en toute sécurité avant que ne survienne une flexion des éléments structuraux, en se concentrant spécifiquement sur les extrémités aplaties comprimées des tubes en acier.

---

<a name="overview"></a>  
## **2. Vue d’ensemble de la structure du dôme géodésique**

- **Diamètre :** 18 mètres  
- **Hauteur :** 7 mètres  
- **Tubes en acier :**  
  - **Diamètre extérieur cylindrique :** 0,048 m  
  - **Épaisseur de paroi :** 0,0025 m (en supposant une épaisseur d’extrémité comprimée de 0,005 m et une épaisseur de paroi égale à la moitié de cette valeur)  
- **Extrémités comprimées (point le plus faible de la structure, sur lequel porte l’analyse) :**  
  - **Épaisseur :** 0,005 m  
  - **Largeur :** 0,04 m  
  - **Longueur plate :** 0,080 m (de la pliure au boulon)

![IMG_2534 2](https://github.com/user-attachments/assets/152f08fe-90b7-4505-a822-c2d35bad6266)

- **Configuration du point central :**  
  - **Six tubes (Type A) :** Longueur 1,55 m (y compris parties comprimées)  
  - **Anneau 1 :** Hexagone formé de six tubes de type B, chacun d’une longueur de 1,528 m  
- **Propriétés des matériaux :**  
  - **Limite d’élasticité ($F_y$) :** 235 MPa (235 × 10^6 Pa)  
  - **Module d’élasticité ($E$) :** 200 GPa (200 × 10^9 Pa)

<img width="928" alt="Screenshot 2024-12-18 at 13 25 52" src="https://github.com/user-attachments/assets/a3214f30-395c-4bb5-a2b0-3ee976c37d4c" />

---

<a name="load-calculations"></a>  
## **3. Calculs de la capacité de charge au point central**

<a name="material-properties"></a>  
### **3.1 Propriétés des matériaux et paramètres géométriques**

**Détermination de l’angle ($\theta_1$) entre les tubes et le plan horizontal :**

<img width="979" alt="Screenshot 2024-12-18 at 13 37 39" src="https://github.com/user-attachments/assets/9d123373-b95c-4d7a-a30c-22374d2a7fa6" />

**Longueur du côté de l’hexagone (après recouvrement) :**

$$
L_{\text{hex}} = 1,528\,\text{m} - 2 \times 0,030\,\text{m} = 1,468\,\text{m}
$$

**Rayon de l’anneau 1 ($r_1$)**

$$
r_1 = \frac{L_{\text{hex}}}{2 \sin(\pi/6)} = \frac{1,468}{2 \times 0,5} = 1,468\,\text{m}
$$

**Hauteur du point central à l’anneau 1 ($h_1$)**

Étant donné la longueur du tube A $L_A = 1,55\,\text{m}$ :

$$
h_1 = \sqrt{L_A^2 - r_1^2} = \sqrt{1,55^2 - 1,468^2} = \sqrt{2,4025 - 2,1546} = \sqrt{0,2479} = 0,4989\,\text{m}
$$

**Angle par rapport à l’horizontale ($\theta_1$)**

$$
\theta_1 = \arctan\left(\frac{h_1}{r_1}\right) = \arctan\left(\frac{0,4989}{1,468}\right) \approx 18,8^\circ
$$

---

<a name="cross-sectional-properties"></a>  
### **3.2 Propriétés des sections transversales**

**a. Tubes cylindriques creux**

**Diamètre extérieur ($D_o$)**

$$
D_o = 0,048\,\text{m}
$$

**Diamètre intérieur ($D_i$)**

$$
D_i = D_o - 2t = 0,048\,\text{m} - 2 \times 0,0025\,\text{m} = 0,043\,\text{m}
$$

**Aire de la section transversale ($A_{\text{tube}}$)**

$$
A_{\text{tube}} = \frac{\pi}{4}(D_o^2 - D_i^2) = \frac{\pi}{4}(0,048^2 - 0,043^2) = 0,000357\,\text{m}^2
$$

**Moment d’inertie ($I_{\text{tube}}$)**

$$
I_{\text{tube}} = \frac{\pi}{64}(D_o^4 - D_i^4) = 9,24 \times 10^{-8}\,\text{m}^4
$$

**b. Extrémités aplaties**

**Largeur ($b$)**

$$
b = 0,04\,\text{m}
$$

**Épaisseur ($t$)**

$$
t = 0,005\,\text{m}
$$

**Aire de la section transversale ($A_{\text{flat}}$)**

$$
A_{\text{flat}} = b \times t = 0,04\,\text{m} \times 0,005\,\text{m} = 0,0002\,\text{m}^2
$$

**Moment d’inertie ($I_{\text{flat}}$)**

$$
I_{\text{flat}} = \frac{b t^3}{12} = \frac{0,04 \times (0,005)^3}{12} = 4,17 \times 10^{-10}\,\text{m}^4
$$

**Module de section ($S_{\text{flat}}$)**

$$
S_{\text{flat}} = \frac{I_{\text{flat}}}{t/2} = \frac{4,17 \times 10^{-10}\,\text{m}^4}{0,0025\,\text{m}} = 1,668 \times 10^{-7}\,\text{m}^3
$$

---

<a name="bending-capacity"></a>  
### **3.3 Capacité en flexion des extrémités aplaties**

**Moment fléchissant maximal ($M_{\text{max}}$) avant limite d’élasticité :**

$$
M_{\text{max}} = F_y \times S_{\text{flat}} = 235 \times 10^6\,\text{Pa} \times 1,668 \times 10^{-7}\,\text{m}^3 = 39,33\,\text{N}\cdot\text{m}
$$

**En supposant une excentricité ($e$) de 1 mm (0,001 m) :**

**Charge axiale maximale ($P_{\text{bending}}$) sans dépasser la capacité en flexion :**

$$
P_{\text{bending}} = \frac{M_{\text{max}}}{e} = \frac{39,33\,\text{N}\cdot\text{m}}{0,001\,\text{m}} = 39\,333\,\text{N} = 39,33\,\text{kN}
$$

---

<a name="axial-capacity"></a>  
### **3.4 Capacité axiale des tubes**

**Capacité axiale à la limite d’élasticité ($P_{\text{axial}}$) des extrémités aplaties :**

$$
P_{\text{axial}} = A_{\text{flat}} \times F_y = 0,0002\,\text{m}^2 \times 235 \times 10^6\,\text{Pa} = 47\,000\,\text{N} = 47\,\text{kN}
$$

**Conclusion :** Puisque $P_{\text{bending}} < P_{\text{axial}}$, la flexion est le facteur limitant.

---

<a name="center-point-load"></a>  
### **3.5 Calcul de la capacité de charge au point central**

**Contribution de la charge verticale par tube**

La charge axiale limitante par tube est $P_{\text{bending}} = 39,33\,\text{kN}$.

Étant donné que la composante horizontale de la force est contrainte par les anneaux, nous ne considérons que la composante verticale.

Angle par rapport à l’horizontale : $\theta_1 = 18,8^\circ$.

Composante verticale :

$$
F_{\text{vertical}} = P_{\text{bending}} \times \sin(\theta_1) = 39,33\,\text{kN} \times 0,322 \approx 12,66\,\text{kN}
$$

**Charge verticale totale au point central**

Nombre de tubes $n = 6$ :

$$
P_{\text{total}} = n \times F_{\text{vertical}} = 6 \times 12,66\,\text{kN} = 75,96\,\text{kN}
$$

Conversion en kilogrammes ( $g = 9,81\,\text{m/s}^2$ ) :

$$
\text{Charge totale (kg)} = \frac{75\,960\,\text{N}}{9,81\,\text{m/s}^2} \approx 7\,740\ \text{kg}
$$

---

<a name="conservative-estimate"></a>  
## **4. Caractère conservateur de l’estimation**

<a name="load-sharing-and-structural-redundancy"></a>  
### **4.1 Répartition des charges et redondance structurelle**

- Calculs conservateurs : L’analyse porte sur le nœud le plus faible de la structure.
- Redistribution des charges : Le calcul se base uniquement sur la résistance, la longueur et les angles de l’acier. Il ne prend pas en compte la répartition des charges par le reste du dôme, ce qui réduirait la sollicitation sur chaque nœud individuel. La capacité réelle est probablement plus élevée grâce à cette répartition.

<a name="potential-capacity"></a>  
### **4.2 Potentiel d’une capacité de charge supérieure**

- Analyse globale : La prise en compte de tous les éléments révélera sans doute une capacité plus importante.
- FEA : Les interactions complexes peuvent être modélisées par des logiciels de calcul par éléments finis.
- Solidité intrinsèque : La forme du dôme répartit efficacement les forces, suggérant une capacité de charge réelle plus élevée.

---

<a name="strength-other-points"></a>  
## **5. Résistance d’autres points du dôme**

<a name="load-distribution"></a>  
### **5.1 Répartition des charges dans un dôme géodésique**

- Interconnexion structurelle : Le réseau triangulé du dôme répartit les charges globalement.
- Redondance : De multiples chemins de charge réduisent la contrainte sur un seul élément.
- Comportement global : Le dôme agit comme un ensemble intégré.

<a name="increased-strength"></a>  
### **5.2 Résistance accrue à d’autres points**

- Zones moins sollicitées : Les points éloignés du centre subissent des contraintes moindres.
- Angles plus raides : Des tubes plus verticaux augmentent la capacité de charge verticale.
- Soutien additionnel : Les anneaux et les interconnexions renforcent la résistance globale.

---

<a name="conclusion"></a>  
## **6. Conclusion**

La capacité de charge sécuritaire calculée au point central du dôme géodésique est d’environ **7 740 kilogrammes**, en tenant compte de la flexion des extrémités aplaties. Il s’agit d’une estimation conservatrice centrée sur le point le plus faible, sans considérer le partage global des charges. Lors de la détermination d’une charge de sécurité, il est recommandé d’appliquer un facteur de sécurité de 10:1.

**Points clés :**

- **La flexion est déterminante :** La capacité en flexion des extrémités aplaties limite la charge.
- **Autres points plus résistants :** Grâce à la géométrie et à la redondance, d’autres points peuvent supporter davantage de charge.
- **Répartition des charges avantageuse :** L’interconnexion structurelle du dôme augmente la capacité globale.

---

<a name="recommendations"></a>  
## **7. Recommandations**

1. **Analyse structurelle complète :**  
   - Utiliser la méthode des éléments finis (FEA) pour modéliser l’ensemble du dôme.  
   - Prendre en compte les charges environnementales et dynamiques.

2. **Optimisation du design :**  
   - Améliorer les connexions pour minimiser les excentricités.  
   - Répartir les points d’accroche pour partager la charge.

3. **Consulter un ingénieur structure :**  
   - Valider les calculs et garantir la conformité aux normes.

4. **Qualité de la construction :**  
   - Une fabrication et un assemblage précis réduisent les imperfections.  
   - Effectuer des inspections et un entretien réguliers.

---

**Avertissement :** Ces calculs sont basés sur des approximations fournies et sur des formules standard de génie civil. Ils constituent une évaluation préliminaire. Un ingénieur professionnel devrait réviser et valider ces calculs pour confirmer cette analyse.
