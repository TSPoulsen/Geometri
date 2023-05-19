
\newcommand{\R}{\mathbb{R}}
# **Afleveringsopgave 3 - Geometri 1**
### **Tim Sehested Poulsen - tpw705**

## **Opgave A3**

### **a)**
I beviset for sætning 3.3 bliver der givet at den omparametrisering som skal findes er givet ved $l^{-1}(t)$ hvor $l(t) = \int_{t_0}^t \| \gamma'(t) \| dt$, altså en arbitrær buelængde funktion for $\gamma$.
Det gør sig kun gældende for regulære kurver, hvilket vil blive vist senere i opgaven at $\gamma$ er, så for nu vil jeg tage det for givet. Jeg udregner derfor først integralet $l(t)$.
$$\begin{aligned}
l(t_1) = \int_{t_0}^{t_1} \| \gamma'(t) \| dt \\
= \int_{t_0}^{t_1} \| (3,4,-\frac{5t}{\sqrt{1-t^2}})\| dt \\
= \int_{t_0}^{t_1} \sqrt{ 3^2 + 4^2 + \left(-\frac{5t}{\sqrt{1-t^2}} \right)^2 } dt \\
= \int_{t_0}^{t_1} \sqrt{ 25 + 25\frac{t^2}{1-t^2}} dt \\
= \int_{t_0}^{t_1} \sqrt{ 25 \left( 1 + \frac{t^2}{1-t^2} \right)} dt \\
= \int_{t_0}^{t_1} 5 \sqrt{\frac{1}{1-t^2}} dt \\
= 5  \left[ \arcsin(t) + C \right]_{t_0}^{t_1}
\end{aligned}$$
Herfra kan vi bruge at $\arcsin(t)^{-1} = \sin(t)$, og derved kan vi give at $l^{-1}(t) = \frac{1}{5} \sin ( t )$, og som er den ompametrisering som vi skal bruge.
Så $(\gamma \circ l^{-1})(t)$ har enhedsfart.

### **b)**
Det kan hurtigt ses at de første to koordinatfunktioner er glatte, og derfor er $\sigma$ glat hvis og kun hvis $\sigma_3(u,v) = 5\sqrt{1-v^2}$ er glat.
Da vi kan differentiere til $u$ og få $0$, er det let løseligt og hvis vi differentierer med hensyn til $v$ får vi $\frac{\partial u}{\partial v}= -5v\sqrt{1-v^2}$, og generelt som vi differentierer denne funktion med hensyn til $v$ vil vi få et udtryk med $1-v^2$ i nævneren, og da $\sigma$ er definert for $v \in (-1,1)$ vil dette ikke være et problem da vi aldrig vil have 0 i nævneren så, altså er $\sigma$ glat.
Det kan rimelig let ses at $\gamma = \sigma \circ \mu$ med $\mu(t) = (t,t)$.
At $\gamma$ er glat følger af samme argument at $\sigma$ er glat.

$\sigma$ er kun regulære når $\sigma_u'(u,v) = (3,4,0)$ og $\sigma_v'(u,v) = (0,0,-5\frac{v}{\sqrt{1-v^2}})$ er lineært uafhængige, hvilket er tilfældet når $-5\frac{v}{\sqrt{1-v^2}} \ne 0 \iff v \ne 0$. Altså er $\sigma$ regulært for $p \in \{(u,v) \in \R \times (-1,1) \text{ | } v \ne 0 \}$.

### **c)**
da $\gamma'(t) = (3,4,-\frac{5t}{\sqrt{1-t^2}})$, må dens koordinater med hensynet til basen $(\sigma_u'(u,v), \sigma_v'(u,v))$ være trivielt givet ved $(1,1)$ da vi bruger det relativt til $\mu(t) = (t,t)$ for $t\ne 0$.

### **d)**
Jeg udregner komponent funktionerne for $\sigma$.
$$\begin{aligned}
E(u,v) = \| \sigma_u'(u,v) \|^2 = 3^2 + 4^2 = 25 \\
F(u,v) = \sigma_u'(u,v) \cdot \sigma_v'(u,v) = 0 \\
G(u,v) = \| \sigma_v'(u,v) \|^2 = 25 \frac{v^2}{1-v^2}
\end{aligned}$$

Arealet  er derfor givet ved
$$\begin{aligned}
A(\sigma, D) = \int_D \| \sigma_u' \times \sigma_v' \| dA \\
= \int_0^1 \int_{0}^{\frac{1}{2}} \sqrt{EG-F^2} dv du \\
= \int_0^1 \int_{0}^{\frac{1}{2}} 25^2 \frac{v^2}{1-v^2} dv du \\
= 25^2 \int_{0}^{\frac{1}{2}} \frac{v^2}{1-v^2} dv \\
\end{aligned}
$$
