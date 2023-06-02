
\newcommand{\R}{\mathbb{R}}
# **Afleveringsopgave 5 - Geometri 1**
### **Tim Sehested Poulsen - tpw705**

## **Opgave A5**

#### **a)**
Jeg indsætter koordinatfunktionerne for $\sigma$ i ligningen og ser at den løser den
$$
u^2(uv-v) - uu^2v + u^2v = u^3v - u^2v - u^3v + u^2v = 0
$$


#### **b)**
Jeg udregner først $\sigma_u'$ og $\sigma_v'$:
$$
\sigma_u' = (1,v,2uv) \\
\sigma_u' = (0,u-1,u^2) \\
$$
Hvorfra det let kan ses at de er lineært uafhængige da de altid har forskellige første koordinater. Altså er $\sigma$ regulær. Jeg bestemmer nu en normalvektor til $T_{p}\sigma$ for et vilkårlig $p \in \R^2$ ved at bestemme $\sigma_u' \times \sigma_v'$:
$$
\text{N}_p = \sigma_u' \times \sigma_v' = (u^2v-2uv(u-1),-u^2,u-1) 
= (uv(2-u), -u^2, u-1)
$$
Hvorfra det kan ses at det ikke kan være nulvektoren, da det ville kræve at $u=0$ for 2. koordinatet og $u=1$ for tredje koordinatet.
At $T_p\sigma = \text{span}_{\R}(e_1,e_3)$ for $p=(1,0)$ kan tjekkes ved at se at normalvektoren er en skalering af $e_2$.
Så jeg udregner $N_{(1,0)}$:
$N_{(1,0)} = (1\cdot 0 \cdot (2-1), -(1)^2, 1-1) = (0,-1,0) $
Da er normalvektoren for tangentrummet en skalering af $e_2$ og dermed er $T_{(1,0)}\sigma = \text{span}_{\R}(e_1,e_3)$.

#### **c)**
Jeg udregner alle de forskelle komponent funktioner:
$$\begin{align*}
&E = \| \sigma_u' \|^2 = 1 + 0^2 + (2\cdot 1 \cdot 0)^2 = 1 \\
&F = \sigma_u' \cdot \sigma_v' = 0 + 0\cdot (1-1) + 2\cdot 1 \cdot 0 \cdot 1^2 = 0 \\
&G = \| \sigma_v' \|^2 = 0^2 + (1-1)^2 + 1^2 = 1 \\
&L = \frac{\text{N}_p}{\|\text{N}_p\|} \cdot \sigma_{uu}'' = (0,-1,0) \cdot (0,0,2) = 0\\
&M = \frac{\text{N}_p}{\|\text{N}_p\|} \cdot \sigma_{uv}'' = (0,-1,0) \cdot (0,1,2) = -1\\
& N = \frac{\text{N}_p}{\|\text{N}_p\|} \cdot \sigma_{vv}'' = (0,-1,0) \cdot (0,0,0) = 0\\
\end{align*}
$$

#### **d)**
For at bestemme hovedkrumningerne bruger jeg korollar 5.5.2 og løser ligningen for $\kappa$:
$$\text{det}\left(
    \begin{pmatrix}
        E & F \\
        F & G
    \end{pmatrix}^{-1}
    \begin{pmatrix}
        L & M \\
        M & N
    \end{pmatrix}
    -\kappa
    \begin{pmatrix}
        1 & 0 \\
        0 & 1
    \end{pmatrix}
    \right) = 0
$$
$$
    \begin{pmatrix}
        E & F \\
        F & G
    \end{pmatrix}^{-1}
    \begin{pmatrix}
        L & M \\
        M & N
    \end{pmatrix}
    =
    \begin{pmatrix}
        1 & 0 \\
        0 & 1
    \end{pmatrix}^{-1}
    \begin{pmatrix}
        0 & -1 \\
        -1 & 0 
    \end{pmatrix}
    = 
    \begin{pmatrix}
        0 & -1 \\
        -1 & 0 
    \end{pmatrix}
$$
$$
    \det \left(
    \begin{pmatrix}
        0 & -1 \\
        -1 & 0 
    \end{pmatrix}
    -\kappa
    \begin{pmatrix}
        1 & 0 \\
        0 & 1
    \end{pmatrix}
    \right)
    = 
    \det
    \begin{pmatrix}
        -\kappa & -1 \\
        -1 & -\kappa
    \end{pmatrix}
    =
    \kappa^2 - 1
$$
$$
\kappa^2 -1 = 0 \iff \kappa = \pm 1
$$
Altså er hovedkrumningnerne $\kappa_1 = 1$ og $\kappa_2 = -1$.
Hvor jeg kan finde de tilhørende hovedretninger ved at løse ligningen:
$$
\begin{pmatrix}
    E & F \\
    F & G
\end{pmatrix}^{-1}
\begin{pmatrix}
    L & M \\
    M & N
\end{pmatrix}
\begin{pmatrix}
    a \\
    b
\end{pmatrix} 
=
\kappa_i
\begin{pmatrix}
    a \\
    b
\end{pmatrix} 
$$
Jeg får dem til at være
$$
\begin{pmatrix}
    0 & -1 \\
    -1 & 0
\end{pmatrix}
\begin{pmatrix}
    a \\
    b
\end{pmatrix}
= 
\pm 1
\begin{pmatrix}
    a \\
    b
\end{pmatrix}
\iff b = \pm a 
$$
Altså får jeg for $\kappa_1 = 1$ hovedretningen $(t,-t)$ og for $\kappa_2 = -1$ hovedretningen $(t,t)$ for $t \in \R$ og $t \ne 0$.