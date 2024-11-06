# **Analyse de la Capacité de Charge du Dôme Géodésique**

## **Table des Matières**

1. [Introduction](#introduction)
2. [Aperçu de la Structure du Dôme Géodésique](#aperçu)
3. [Calculs de Capacité de Charge au Point Central](#calculs-charge)
   - [Propriétés des Matériaux et Paramètres Géométriques](#propriétés-matériaux)
   - [Propriétés de la Section Transversale](#section-transversale)
   - [Capacité en Flexion des Extrémités Plates](#capacité-flexion)
   - [Capacité Axiale des Tubes](#capacité-axiale)
   - [Calcul de la Capacité de Charge au Point Central](#charge-point-central)
4. [Résistance d'Autres Points du Dôme](#résistance-autres-points)
   - [Distribution de la Charge dans un Dôme Géodésique](#distribution-charge)
   - [Augmentation de la Résistance aux Autres Points](#augmentation-résistance)
5. [Nature Conservative de l'Estimation](#estimation-conservative)
   - [Partage de Charge et Redondance Structurelle](#partage-charge)
   - [Potentiel d'une Capacité de Charge Plus Élevée](#potentiel-capacité)
6. [Conclusion](#conclusion)
7. [Recommandations](#recommandations)

---

<a name="introduction"></a>
## **1. Introduction**

Ce document présente une analyse détaillée de la capacité de charge au point central d'un dôme géodésique de 18 mètres de diamètre, construit avec des tubes en acier de dimensions et configurations spécifiques. Les calculs visent à déterminer la charge maximale que le point central peut supporter avant que la flexion ne se produise dans les éléments structurels, en se concentrant spécifiquement sur les extrémités plates comprimées des tubes en acier.

---

<a name="aperçu"></a>
## **2. Aperçu de la Structure du Dôme Géodésique**

- **Diamètre :** 18 mètres
- **Hauteur :** 7 mètres
- **Tubes en Acier :**
  - **Diamètre Cylindrique :** 0,048 mètre
  - **Épaisseur de Paroi :** 0,0025 mètre (en supposant que l'épaisseur des extrémités comprimées est de 0,005 mètre et que l'épaisseur de la paroi est la moitié)
- **Extrémités Comprimées :**
  - **Épaisseur :** 0,005 mètre
  - **Largeur :** 0,04 mètre
  - **Longueur Plate (de la pliure au boulon) :** 0,080 mètre
- **Configuration du Point Central :**
  - **Six Tubes (Type A) :** Longueur de 1,55 mètre (y compris les portions comprimées)
  - **Anneau 1 :** Hexagone formé par des tubes de type B (6 tubes, longueur de 1,528 mètre)
- **Matériaux :**
  - **Qualité de l'Acier :** S235 (Limite d'Élasticité \( F_y = 235 \) MPa)
  - **Module d'Élasticité :** \( E = 200 \) GPa

---

<a name="calculs-charge"></a>
## **3. Calculs de Capacité de Charge au Point Central**

<a name="propriétés-matériaux"></a>
### **3.1 Propriétés des Matériaux et Paramètres Géométriques**

- **Limite d'Élasticité (\( F_y \)) :** 235 MPa (\( 235 \times 10^6 \) Pa)
- **Module d'Élasticité (\( E \)) :** 200 GPa (\( 200 \times 10^9 \) Pa)
- **Angle des Tubes par Rapport au Plan Horizontal (\( \theta_h \)) :** Déterminé à partir de la géométrie

**Détermination de l'Angle (\( \theta_h \)) entre les Tubes et le Plan Horizontal :**

#### **Longueur du Côté de l'Hexagone (après soustraction du chevauchement)**

$$
L_{\text{hex}} = 1,528\, \text{m} - 2 \times 0,030\, \text{m} = 1,468\, \text{m}
$$

#### **Rayon de l'Anneau 1 (\( r_1 \))**

$$
r_1 = \frac{ L_{\text{hex}} }{ 2 \times \sin\left( \dfrac{ \pi }{ 6 } \right) } = \frac{ 1,468 }{ 2 \times \sin\left( \dfrac{ \pi }{ 6 } \right) } = \frac{ 1,468 }{ 2 \times 0,5 } = 1,468\, \text{m}
$$

#### **Hauteur du Point Central à l'Anneau 1 (\( h_1 \))**

$$
h_1 = \sqrt{ L_A^2 - r_1^2 } = \sqrt{ 1,55^2 - 1,468^2 } = \sqrt{ 2,4025 - 2,1546 } = \sqrt{ 0,2479 } = 0,4989\, \text{m}
$$

#### **Angle par Rapport à l'Horizontale (\( \theta_h \))**

$$
\theta_h = \arctan\left( \dfrac{ r_1 }{ h_1 } \right) = \arctan\left( \dfrac{ 1,468 }{ 0,4989 } \right) \approx 71,87^\circ
$$

---

<a name="section-transversale"></a>
### **3.2 Propriétés de la Section Transversale**

#### **a. Tubes Cylindriques Creux**

**Diamètre Extérieur (\( D_o \))**

$$
D_o = 0,048\, \text{m}
$$

**Diamètre Intérieur (\( D_i \))**

$$
D_i = D_o - 2t = 0,048\, \text{m} - 2 \times 0,0025\, \text{m} = 0,043\, \text{m}
$$

**Aire de la Section Transversale (\( A_{\text{tube}} \))**

$$
A_{\text{tube}} = \frac{\pi}{4} \left( D_o^2 - D_i^2 \right ) = \frac{\pi}{4} \left( 0,048^2 - 0,043^2 \right ) = 0,000357\, \text{m}^2
$$

**Moment d'Inertie (\( I_{\text{tube}} \))**

$$
I_{\text{tube}} = \frac{\pi}{64} \left( D_o^4 - D_i^4 \right ) = 9,24 \times 10^{-8}\, \text{m}^4
$$

#### **b. Extrémités Plates Comprimées**

**Largeur (\( b \))**

$$
b = 0,04\, \text{m}
$$

**Épaisseur (\( t \))**

$$
t = 0,005\, \text{m}
$$

**Aire de la Section Transversale (\( A_{\text{plat}} \))**

$$
A_{\text{plat}} = b \times t = 0,04\, \text{m} \times 0,005\, \text{m} = 0,0002\, \text{m}^2
$$

**Moment d'Inertie (\( I_{\text{plat}} \))**

$$
I_{\text{plat}} = \frac{ b t^3 }{ 12 } = \frac{ 0,04\, \text{m} \times (0,005\, \text{m})^3 }{ 12 } = 4,17 \times 10^{-10}\, \text{m}^4
$$

**Module de Section (\( S_{\text{plat}} \))**

$$
S_{\text{plat}} = \frac{ I_{\text{plat}} }{ c } = \frac{ I_{\text{plat}} }{ t/2 } = \frac{ 4,17 \times 10^{-10}\, \text{m}^4 }{ 0,0025\, \text{m} } = 1,668 \times 10^{-7}\, \text{m}^3
$$

---

<a name="capacité-flexion"></a>
### **3.3 Capacité en Flexion des Extrémités Plates**

**Moment de Flexion Maximal (\( M_{\text{max}} \)) Avant Rupture**

$$
M_{\text{max}} = F_y \times S_{\text{plat}} = 235 \times 10^6\, \text{Pa} \times 1,668 \times 10^{-7}\, \text{m}^3 = 39,33\, \text{N}\cdot\text{m}
$$

**En Supposant une Excentricité (\( e \)) de 1 mm (0,001 m)**

**Charge Axiale Maximale (\( P_{\text{flexion}} \)) Sans Dépasser la Capacité en Flexion**

$$
P_{\text{flexion}} = \frac{ M_{\text{max}} }{ e } = \frac{ 39,33\, \text{N}\cdot\text{m} }{ 0,001\, \text{m} } = 39\,333\, \text{N} = 39,33\, \text{kN}
$$

---

<a name="capacité-axiale"></a>
### **3.4 Capacité Axiale des Tubes**

**Capacité à la Rupture en Compression Axiale (\( P_{\text{axial}} \)) des Extrémités Plates**

$$
P_{\text{axial}} = A_{\text{plat}} \times F_y = 0,0002\, \text{m}^2 \times 235 \times 10^6\, \text{Pa} = 47\,000\, \text{N} = 47\, \text{kN}
$$

**Conclusion :** Puisque \( P_{\text{flexion}} < P_{\text{axial}} \), **la flexion gouverne la conception**.

---

<a name="charge-point-central"></a>
### **3.5 Calcul de la Capacité de Charge au Point Central**

**a. Contribution de la Charge Verticale par Tube**

**Angle par Rapport à l'Horizontale (\( \theta_h = 71,87^\circ \))**

**Sécante de l'Angle (\( \sec(\theta_h) \))**

$$
\sec(\theta_h) = \frac{1}{\cos(\theta_h)} = \frac{1}{\cos(71,87^\circ)} = \frac{1}{0,3145} = 3,178
$$

**Charge Verticale par Tube (\( F_{\text{vertical}} \))**

$$
F_{\text{vertical}} = P_{\text{flexion}} \times \sec(\theta_h) = 39,33\, \text{kN} \times 3,178 = 125,00\, \text{kN}
$$

**b. Capacité Totale de Charge au Point Central**

**Nombre de Tubes (\( n = 6 \))**

**Charge Verticale Totale (\( P_{\text{total}} \))**

$$
P_{\text{total}} = n \times F_{\text{vertical}} = 6 \times 125,00\, \text{kN} = 750,00\, \text{kN}
$$

**Conversion en Kilogrammes (\( g = 9,81\, \text{m/s}^2 \))**

$$
\text{Capacité Totale de Charge} = \frac{ P_{\text{total}} }{ g } = \frac{ 750\,000\, \text{N} }{ 9,81\, \text{m/s}^2 } \approx 76\,455\, \text{kg}
$$

**c. Application d'un Facteur de Sécurité**

**En Supposant un Facteur de Sécurité de 2,0**

$$
\text{Capacité de Charge Sécuritaire} = \frac{ 76\,455\, \text{kg} }{ 2,0 } = 38\,227\, \text{kg}
$$

**d. Résumé**

- **Charge Maximale Avant Flexion (avec Facteur de Sécurité) :** Approximativement **38 227 kg**

---

<a name="résistance-autres-points"></a>
## **4. Résistance d'Autres Points du Dôme**

<a name="distribution-charge"></a>
### **4.1 Distribution de la Charge dans un Dôme Géodésique**

- **Interconnexion Structurelle :** Le réseau de triangles du dôme géodésique permet aux charges appliquées en tout point d'être distribuées dans l'ensemble de la structure.
- **Redondance :** Des chemins de charge multiples réduisent le stress sur les éléments individuels, améliorant la résistance globale.
- **Comportement Global :** Le dôme agit comme un tout intégré plutôt que comme une collection d'éléments isolés.

<a name="augmentation-résistance"></a>
### **4.2 Augmentation de la Résistance aux Autres Points**

- **Zones Moins Sollicitées :** Les points éloignés du centre subissent généralement moins de stress en raison de la géométrie du dôme et de la distribution des charges.
- **Angle d'Inclinaison :** Les tubes à d'autres points peuvent être plus verticaux, réduisant les moments de flexion et augmentant la capacité de charge axiale.
- **Support Supplémentaire :** Les anneaux et les éléments interconnectés fournissent un support supplémentaire, rendant ces points plus résistants que le point central.

**Exemple :**

- **Aux Points Inférieurs du Dôme :**
  - **Angles par Rapport à l'Horizontale Plus Petits**, signifiant que les tubes sont plus verticaux.
  - **Moments de Flexion Réduits**, car les excentricités ont moins d'impact.
  - **Charges Axiales Supportées Plus Efficacement**, augmentant la capacité de charge.

---

<a name="estimation-conservative"></a>
## **5. Nature Conservative de l'Estimation**

<a name="partage-charge"></a>
### **5.1 Partage de Charge et Redondance Structurelle**

- **Calculs Conservateurs :** L'analyse se concentre sur le composant le plus faible (extrémités plates au point central) sans considérer la capacité globale du dôme à distribuer les charges.
- **Redistribution des Charges :** En réalité, la géométrie du dôme permet un partage des charges parmi de nombreux éléments, réduisant la charge sur chaque composant individuel.
- **Marge de Sécurité :** La capacité calculée est intentionnellement conservatrice pour assurer la sécurité.

<a name="potentiel-capacité"></a>
### **5.2 Potentiel d'une Capacité de Charge Plus Élevée**

- **Analyse Structurelle Globale :** Une analyse complète considérant tous les éléments et connexions pourrait révéler une capacité de charge plus élevée.
- **Analyse par Éléments Finis (AEF) :** L'utilisation de logiciels AEF peut modéliser les interactions complexes et prédire plus précisément les capacités de charge.
- **Force Inhérente des Dômes Géodésiques :** La forme du dôme distribue intrinsèquement les forces de manière efficace, pouvant supporter des charges supérieures à celles calculées dans une analyse localisée.

---

<a name="conclusion"></a>
## **6. Conclusion**

La **capacité de charge sécuritaire calculée au point central** du dôme géodésique est d'environ **38 227 kilogrammes**, en considérant la capacité en flexion des extrémités plates comprimées et en appliquant un facteur de sécurité de 2,0. Cette estimation est conservatrice, se concentrant sur le composant le plus faible et ne tenant pas compte des capacités globales de distribution de charge du dôme.

**Points Clés :**

- **La Capacité en Flexion Gouverne la Conception :** La susceptibilité des extrémités plates à la flexion sous de petites excentricités limite la capacité de charge.
- **Les Autres Points sont Plus Résistants :** En raison de la redondance structurelle et de la géométrie, d'autres points du dôme peuvent supporter des charges plus importantes.
- **La Distribution des Charges Améliore la Capacité :** La structure interconnectée du dôme permet un partage des charges, augmentant potentiellement la capacité de charge globale.

---

<a name="recommandations"></a>
## **7. Recommandations**

1. **Effectuer une Analyse Structurelle Globale :**
   - Utiliser l'Analyse par Éléments Finis pour modéliser l'ensemble du dôme et capturer les effets de distribution globale des charges.
   - Considérer tous les cas de charge, y compris les charges environnementales et dynamiques.

2. **Optimiser la Conception :**
   - **Augmenter l'Épaisseur des Extrémités Plates :** Amélioration de la capacité en flexion.
   - **Utiliser de l'Acier de Plus Haute Résistance :** Pour augmenter les capacités axiales et en flexion.
   - **Améliorer les Connexions :** Concevoir des connexions pour minimiser les excentricités et améliorer le transfert de charge.

3. **Consulter un Ingénieur Structurel :**
   - Une évaluation professionnelle est essentielle pour valider les calculs et assurer la sécurité.
   - Un ingénieur peut fournir des insights sur les améliorations potentielles de la conception et la conformité aux codes du bâtiment.

4. **Mettre en Œuvre des Pratiques de Construction de Qualité :**
   - Assurer une fabrication et un assemblage précis pour minimiser les imperfections et les désalignements.
   - Réaliser des inspections régulières et une maintenance pour détecter et résoudre rapidement tout problème structurel.

---

**Avertissement :** Les calculs fournis sont basés sur les informations données et les formules d'ingénierie standard. Ils sont destinés à des fins d'évaluation préliminaire. Un ingénieur structurel professionnel doit revoir et valider ces calculs avant de prendre des décisions de conception ou de procéder à la construction.

---

**Annexe :**

Pour une compréhension approfondie, il est recommandé de :

- **Étudier le comportement des dômes géodésiques sous charge.**
- **Se référer à des manuels d'ingénierie structurelle** pour des explications détaillées sur la flexion, le flambement et la distribution des charges.
- **Consulter les codes du bâtiment et les normes** pertinents à votre localisation et à la portée du projet.

---

**Note :** Toutes les expressions mathématiques ont été formatées en utilisant la syntaxe LaTeX entourée de doubles signes dollar `$$ ... $$` pour assurer un rendu correct sur GitHub. Les équations sont introduites avec des titres ou du texte en gras, et nous avons pris soin d'éviter de placer des équations au sein d'éléments de liste pour prévenir les problèmes d'affichage.

---

