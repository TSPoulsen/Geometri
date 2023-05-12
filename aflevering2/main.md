
\newcommand{\R}{\mathbb{R}}
# **Afleveringsopgave 2 - Geometri 1**
### **Tim Sehested Poulsen - tpw705**

## **Opgave A2**

### **(a)**
Vi kan se at det er en parametiriseret flade da $\sigma$ både er defineret på en åben mængde og er en funktion fra $\R^2$ til $\R^3$.
Derudover kan vi se at den er glat da hvor af koordinatfunktionerne er glatte. Det kan rimelig let ses at
$$
    D\sigma_p = \begin{bmatrix}
        1 & 0 \\
        1 & 1 \\
        2(u+v) & 2(u+v) \\
    \end{bmatrix}
$$
og hver af disse indgange kan også differentieres uendeligt mange gange.
Tangentervektorne er til koordinatkurverne er derfor givet ved søjlerne i $D\sigma$.
Altså er $\sigma_u' = (1, 1, 2(u+v))$ og $\sigma_v' = (0, 1, 2(u+v))$.

### **(b)**
For at vise at $\sigma$ er regulær skal jeg vise at $\sigma_u'$ og $\sigma_v'$ er lineært uafhængige.
Det kan ses eftersom
$$\begin{aligned}
    &t \cdot \sigma_u' + s \cdot \sigma_v' = (t, t+s, 2t+2s) = (0, 0, 0) \\ 
    &\implies t = t+s = 2t+2s = 0 \\
    &\implies t = s = 0
\end{aligned}$$
Altså er tangentvektorerne lineært uafhængige og $\sigma$ er derfor regulær.

En enhedsnormalvektoren for et $p=(u,v) \in \R^2$ er givet ved
$$\begin{aligned}
    &N(p) = \frac{\sigma_u' \times \sigma_v'}{\|\sigma_u' \times \sigma_v'\|} \\
    &=\| (0,-2(u+v),1) \| \cdot (0,-2(u+v), 1)  \\
    &=\frac{1}{\sqrt{4(u+v)^2+1}} \cdot (0, -2(u+v), 1) \\
    &= (0, -\frac{2(u+v)}{\sqrt{4(u+v)^2+1}}, \frac{1}{\sqrt{4(u+v)^2+1}}) \\
    &= (0, -\frac{3(u+v)}{4(u+v)^2+1}, \frac{1}{\sqrt{4(u+v)^2+1}}) \\
\end{aligned}$$

### **(c)**
Eftersom $(2,1,0)$ kan skrives som en lineær kombination af $\sigma_u'$ og $\sigma_v'$ for punktet $p= (0,0)$, hvilket kan ses fra
$$
    2 \sigma_u' - \sigma_v' = 2(1,1,0) - (0,1,0) = (2,1,0) 
$$
Må det gælde at $(2,1,0)$ ligger i tangentrummet $T_{(0,0)}\sigma$.
For at finde en kurve $\gamma(t) = (\sigma \circ \mu)(t)$, som har $\gamma(0) = (0,0,0)$ og $\gamma'(0) = (2,1,0)$, skal vi finde en funktion $\mu$ sådan at 
$$
    \gamma'(t) = \sigma_u'(\mu(t)) \cdot \mu_1'(t) + \sigma_v'(\mu(t)) \cdot \mu_2'(t) = (2,1,0)
$$
med inspiration fra beviset til theorem 2.4 kan jeg bestemme at $\mu(t) = (2t, -t)$. Hvorfra det kan ses at $\gamma(0) = (0,0,0)$ og
$$
\gamma'(0) = 
\begin{bmatrix}
    1 & 0 \\
    1 & 1 \\
    0 & 0 \\
\end{bmatrix}
\cdot
\begin{bmatrix}
    2 \\
    -1 \\
\end{bmatrix}
=
\begin{bmatrix}
    2 \\
    1 \\
    0 \\
\end{bmatrix}
$$
### **(d)**
Jeg udregnede $v_0 = \mu'(0) = (2,1)$ og faktisk også $D\sigma_p \cdot v_0 = (2,1,0)$ da dette også er $\gamma'(0)$.
    
### **(e)**
Hvis $(1,0,2) \in T_{p}\sigma$ for et $p \in \R^2$ så ville det gælde at den kunne skrives som en linear kombination af række vektorerne i $D\sigma_p$. Altså
$$\begin{aligned}
    &(1,0,2) = t \cdot (1,1,2(u+v)) + s \cdot (0,1,2(u+v)) \\
    &= (t, t+s, 2(u+v) \cdot (s+t)) \\
\end{aligned}
$$
De første koordinater bestmmer $t = 1$ og $s = -1$, men da det sidste koordinat så har ligningen:
$$
2(u+v)(1 - 1) = 0 \ne 2 
$$
hvilket er uafhængigt af $p =(u,v)$. Altså tilhører $(1,0,2)$ ikke tangentrummet for noget punkt $p \in \R^2$.


