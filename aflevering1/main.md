# **Afleveringsopgave 1 - Geometri 1**
### **Tim Sehested Poulsen - tpw705**

## **Opgave A1**

### **(a)**
Da en kugle i $\R^3$ med radius $r_k$ og centrum $(x_0,y_0,z_0)$ er givet ved ligningen $(x- x_0)^2 + (y-y_0)^2 + (z-z_0)^2 = r^2$, kan vi genkende at i ligningen 
$$f_1(x,y,z) = x^2 + y^2 + z^2 = c_1 = 1$$
har at løsningsmængden må være en kugle med radius $r_{k} = \sqrt{c_1} = 1$, og 
centrum i $(0,0,0)$.

Derudover ved vi at en cirkel i $\R^2$ 
er givet ved ligningen $(x - x_0)^2 + (y- y_0)^2 = r_c^2$,
hvor radius er $r_c$ og centrum er $(x_0,y_0)$,
og derfor må vi kunne genkende at i ligningen 
$$f_2(x,y,z) = (x-\frac{1}{2})^2 + y^2 = c_2 = 1$$
har vi en cylinder med radius $r_c = a$ og centrum i $(\frac{1}{2},0, z)$.
Altså må symmetriaksen være $(\frac{1}{2}, 0, z)$.
Så løsningsmængden til begge disse ligninger må være fællesmængden af kuglen og en cylinderen hvilket er tilsvarende niveaumængden
$$ N := \{(x,y,z) \text{  } | \text{  } f(x,y,z) = c\}$$

### **(b)**
For at kunne udregne Jacobimatricen er det jo essentielt at funktionen $f$ er differentiabel,
og da begge koordiantefunktionerne for $f$ er givet ved en sum af sammensatte funktioner,
som hver især er differentiable, må $f$ være differentiabel.

Jacobimatricen $Df(p)$ for et $p=(x_0,y_0,z_0) \in \R^3$ er derfor givet ved
$$
Df(p) = 
\begin{bmatrix}
   \frac{\partial f_1}{\partial x}(p) & \frac{\partial f_1}{\partial y}(p) & \frac{\partial f_1}{\partial z}(p) \\[0.3cm]

   \frac{\partial f_2}{\partial x}(p) & \frac{\partial f_2}{\partial y}(p) & \frac{\partial f_3}{\partial z}(p) \\
\end{bmatrix}
=
\begin{bmatrix}
    2x_0 & 2y_0 & 2z_0 \\[0.3cm]
    2x_0 -1 & 2y_0 & 0 \\
\end{bmatrix}
$$

### **(c)**
Jeg vil først kigge på i hvilke $p \in \R^3$ hvor $Df(p)$ har rang strengt mindre end 2. For at gøre det reducerer jeg $Df(p)$ til rækkeechelonform, hvilket er:
$$
\begin{bmatrix}
    2x_0 & 2y_0 & 2z_0 \\[0.3cm]
    2x_0 -1 & 2y_0 & 0 \\
\end{bmatrix}
\longrightarrow
\begin{bmatrix}
    1 & 0 & z_0 \\[0.3cm]
    0 & y_0 & 2z_0(x_0 - \frac{1}{2}) \\
\end{bmatrix}
$$
Hvorfra det kan ses at rangen altid vil være minimum 1, eftersom den første række har et $1$ tal i indgang (1,1).
Vi kan derudover konkludere at Jacobimatricen kun vil have rang 1 når række 2 er en nulrække,
hvilket kun sker når $y_0 = 0$ og $x_0 = \frac{1}{2} \lor z_0 = 0$.
Da vi nu kan konkludere at $y_0$ skal være $0$, kan vi derfor også konkludere at $x \neq \frac{1}{2}$, da ligningen
$$ (x- \frac{1}{2})^2 + y^2 = a^2 $$
så ikke kan løses for $a > 0$. Altså må vi kunne konkludere at $z_0$ også skal være $0$,
 og der ingen begrænsning på $x_0$ for at Jacobimatricen skal have rang 1. 

Men da $p \in N$ og $0 < a < \frac{3}{2}$, har vi også at $x_0$ skal kunne løse ulighederne
$$ 
0 < (x_0 - \frac{1}{2})^2 + y_0^2 < \left(\frac{3}{2} \right)^2 \\
\iff 0 < (x_0 - \frac{1}{2})^2  < \left(\frac{3}{2} \right)^2 \\
\iff 0 < |x_0 - \frac{1}{2} | < \frac{3}{2} \\
\iff x_0 \in I_x :=(-1, \frac{1}{2}) \cup (\frac{1}{2}, 2) 
$$
Samtidig har vi også at $x_0$ skal være en løsning til $f_1(x,y,z) = 1$, hvilket er
$$
x_0^2 + y_0^2 + z_0^2 = 1 \\
\iff x_0^2 = 1 \\
\iff x_0 = \pm 1
$$
Da $x_0=-1$ ikke ligger i intervallet $I_x$ må vi konkludere at $p = (1,0,0)$ er det eneste punkt i $N$ hvor Jacobimatricen har rang strengt mindre end 2 og $0 < a < \frac{3}{2}$.
Vi kan derudover bemærke at det vil kun hænde for $a^2 = (1 - \frac{1}{2})^2 = \frac{1}{4}$ altså $a = \frac{1}{2}$.


### **(d)**
For et vilkårligt $p \in N$ når $a=\frac{1}{4}$ eller $a=1$ har vi lige vist at $Df(p)$ har rang 2.
Altså er rækkerne for $Df(p)$ lineært uafhængige. Et andet kriterie for sætningen om implicit givne funktioner er at $f$ er glat,
hvilket rimelig let kan ses ud fra $Df(p)$.

Altså siger sætningen[^1] at for et vilkårligt $p \in N$ at vi kan finde et åbent interval $W \subset \R^3$ omkring $p$ sådan at mængden $W \cap N$ kan blive parametriseret af en glat kurve, hvilket kan ses som grafen for en glat funktion $g: \R \to \R^2$, enten som $g(x) =(y,z)$, $g(y) = (x,z)$ eller $g(z) = (x,y)$,
hvor to af variablene er givet som funktion af den sidste variabel.


### **(e)**
Sætningen om implicitte funktioner siger intet om hvorvidt der findes en glat funktion omkring punktet $(1,0,0)$ bare fordi at i dette tilfælde er rækkerne i Jacobimatricen afhængige. Så det kunne sagtens være det stadig var muligt.

Jeg kan ikke løse opgaven stringent (altså ved at løse ligningnerne eksplicit) eftersom jeg ikke ved hvilke lignigner der skal løses.
Hvis jeg skal genaflevere opgaven (eftersom denne delopgave mangler) vil jeg gerne have et hint til hvordan det kan gøres, da jeg ikke gider argumentere ud fra en visualisering og det ikke føles som tilstrækkeligt.





[^1]: Jeg bruger specifikt korrolar 1.7 i bogen "Curves and Surfaces" af Henrik Schlichtkrull