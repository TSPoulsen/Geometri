
\newcommand{\R}{\mathbb{R}}
# **Afleveringsopgave 4 - Geometri 1**
### **Tim Sehested Poulsen - tpw705**

## **Opgave A4**

### **a)**
$\gamma(t) = (t, t^2 + t^3, t^4 - t^2)$ må være regulær da $\gamma'(t) = (1, 2t + 3t^2, 4t^3 - 2t)$ er forskellig fra $(0,0,0)$ for alle $t \in \R$, ret trivielt da $1\ne 0$.

Jeg udregner krumningen i $t=0$:
$$ \gamma''(t) = (0, 6t + 2, 12t^2 -2) $$
$$ \| \gamma'(0) \times \gamma''(0)  \| = \| (1,0,0) \times (0,2,-2) \| = \| (0,2,-2) \| = \sqrt{2^2+(-2)^2} = \sqrt{8} $$
$$ \frac{\| \gamma'(0) \times \gamma''(0)  \|}{\|\gamma'(0)\|^3} = \sqrt{8} $$ 

Det vil sige at krumningen er $\sqrt{8}$ i $t=0$.

### **b)**
Jeg bestemmer de $t$ så $\gamma'(t) \in \Sigma$ hvilket er når:
$$ 2t +3t^2 + 4t^3 - 2t = 0  \iff 4t^3 + 3t^2 = 0 \iff t^2(4t-3) = 0 \iff t = 0 \lor t = - \frac{3}{4}$$
Altså er $\gamma'(t)$ indeholdt i planen $\Sigma$ når $t=0$ eller $t=-\frac{3}{4}$.

### **c)**
Jeg bestemmer de værdi er af $t$ hvor $\text{span}\left(\{\gamma'(t),\gamma''(t)\} \right) = \Sigma$. Det kan hurtigt ses at $\gamma''(t)$ og $\gamma'(t)$ er lineært uafhængige for alle $t \in \R$. Altså skal jeg undersøge for hvilke $t$ at både $\gamma'(t)$ og $\gamma''(t)$ er indeholdt i $\Sigma$. Jeg udregner at $\gamma''(t)$ er indeholdt i $\Sigma$ når:
$$ 6t + 2 + 12t^2 - 2 = 0 \iff t(12t + 6) = 0 \iff t = 0 \lor t = -\frac{1}{2}$$

Da $t=0$ er den eneste værdi hvor både $\gamma'(t)$ og $\gamma''(t)$ er indeholdt i $\Sigma$ er det den eneste værdi hvor $\text{span}\left(\{\gamma'(t),\gamma''(t)\} \right) = \Sigma$.


## **d)**
Jeg udregner først $\gamma'''(t)$:
$$ \gamma'''(t) = (0, 6, 24t) $$
Jeg udregner torsionen $\tau$ af $\gamma$ i $t=1$:

$$\begin{aligned}
&\tau = \frac{\det[\gamma'(1),\gamma''(1),\gamma'''(1)]}{\|\gamma'(1) \times \gamma''(1)\|^2}  \\
&=\frac{\det[(1,5,2),(0,8,10),(0,6,24)]}{\|(1,5,2) \times (0,8,10)\|^2}  \\
&=\frac{\det[(8,10),(6,24)]}{\|(50-16,10,8)\|^2} \\
&=\frac{192-60}{34^2 + 10^2 + 8^2} \\
&=\frac{132}{1320} \\
&=\frac{1}{10} \\
\end{aligned}$$
Det vil sige at torsionen er $\frac{1}{10}$ i $t=1$.
