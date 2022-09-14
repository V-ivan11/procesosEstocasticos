# Cadenas de Markov

Sea $(\Omega, \digamma, P)$ un espacio de probabilidad (S,S) un espacio medible, y $\Gamma$ un conjunto arbitriario de "parámetros" o "índices".

### Definición:

> Una colección $X_t=\{X_t, t \in T\}$ de $vv,uu \quad X_t$ sobre $(\Omega, \digamma, P)$, con valores en $S$ se dice , que es un **Proceso estocástico (PE)**, o proceso aleatorio con espacio de estados $Sy$ conjunto de índice $T$.

Los PE's se pueden clasificar de varias maneras, en particular de términos de $T$ y $S$ los casos típicos son los siguientes:

- Si $T\subseteq \mathbb R$ a lo más numerable, se dice que $X_0$ es un PE a **tiempo discreto**.

- Si $T\subseteq \mathbb R$ es un intervalo, $X_0$ es un PE a **tiempo continuo**.

- Si $T \subseteq \mathbb R^n$ con $n\ge z$, $X_0$ un **tiempo aleatorio**.

- Si $S$ es un conjunto a lo más numerable, se dice que $X_0$ es un PE discreto.

- Si $S$ es continuo, $X_0$ es un PE es continuo
  $$
  \{APPL_t\}_{t=1}^{30}
  $$
  Por otra parte, un PE $X_0 = \{X_t, t\in T\}$ Se puede ver como una colección de funciones de de dos variables
  $$
  (t,w)\longrightarrow X_t(w)\\
  T\times\Omega \longrightarrow S
  $$
  Para cada $t\in T$, la función $W \rightarrow X_t(w)$, variable aleatoria de $\omega$ es $S$.

  Si fijamos $w\in\Omega$, entonces la asignación:
  $$
  t \longrightarrow X_t(\omega)
  $$
  es una trayectoria.

  #### Ejemplo

  Considere un proceso $x()\in \mathbb R^n$ definido por la ecuación diferencial
  $$
  x(t) = F(x(t)) \qquad \forall t \ge 0 \quad x(0) = x_0
  $$

  ### Propiedad de Markov
  
  $\vdots$
  
  En el caso continuo supongamos que $\mathit S \in \mathit B(\mathbb R)$ y la $\sigma-álgebra$ $\mathit S=\mathit B (S)$. Entonces (5) se puede escribir:
  $$
  P(X_{n+1} \in B | X_o = x_0,\cdots,x_n=x_n)= P(X_{n+1} \in B | x_n = x_n) \qquad (6)
  $$
  para todo $B\in \mathit B(S)$, $x_0, \cdots,x_n\in S$ y $n = 0,1,\cdots$
  
  Tomando $x_n = x$, la probabilidad condicional del lado derecho de (6), se llama la probabilidad de transición de $x$ a $B$ en un paso y escribimos:
  $$
  P(x,B)=P(X_{n+1} \in B | X_n = x) \qquad (7)
  $$
  *Nota:*  Cualquier conjunto numerable es de Borel
  
  En el caso $S$ numerable, podemos sustituir $B\in B(S)$ por un estado $y \in S$, y obtenemos lo siguiente
  $$
  \begin{eqnarray*}
  P(X_{n+1} = y | x_o,\cdots, x_n = x_n) &=& P(X_{n+1} = y | X_n = x_n)\\
  P_n(x,y) &=& P(X_{n+1}= y | X_n=x)
  \end{eqnarray*}
  $$
  Algunas veces escribiremos $P_n(x,y)$ como $P_{xy}^{(n)}$ ó $P_n^{xy}$  Cadenas Markovianas discretas. A menos de que se diga lo contrario siempre supondremos que la Cadena de Markov es homogénea (en el tiempo), lo cual significa que (7) no depende de $n$, es decir:
  $$
  P(x,y) = P(X_{n+1}= y | x_n=x) = P(x_1= y | x_0=x) \qquad (10)\\
  \forall n = 0,1,\cdots
  $$
  Ejemplo:
  $$
  P(x_n = SOL | x_{n+1}= AGUILA) = P(x_1 = SOL| x_o = AGUILA)
  $$
  La matriz $P=[P(x,y)] ≡ [P_{xy}]$ Nota: la probabilidad de que $x$ paso seguido de $y$ se llama la matriz de transición (en un paso) de la Cadena de Markov.
  $$
  \begin{matrix}
  & S_1 & S_2 & \cdots & S_n \\
  S_1 & P_{S_1S_1} & P_{S_1S_2} & \cdots & P_{S_1S_n}\\
  \vdots & \vdots & \vdots & \ddots & \vdots\\
  S_n & P_{S_nS_1} & P_{S_nS_2} & \cdots & P_{S_nS_n}
  \end{matrix}
  $$
  

Se tiene que P es una matriz estocástica

- **a)** $P(x.y)\ge 0\quad \forall x,y \in S$ (11)
- **b)** $\sum_{y\in S}P(x,y) = 1 \forall$

### Ejemplo (caminata aleatoria)

Sea variables $\epsilon_o = \{\epsilon_0, \epsilon_1, \cdots, \}$ identicamente independientes distribuidas, con distribución:
$$
P(\epsilon_0 = 1) = P, \quad P(\epsilon_0=-1) = q= 1-p \qquad (12)\\
0 \le p \le 1
$$


Sea
$$
x_n = \sum_{k=0}^n\epsilon_k \quad n=0,1,\cdots
$$
Nótese que 
$$
X_{n+1}=x_n+\epsilon_{n+1}
$$
y que $\epsilon_{n+1}$ es independiente de $x_0,\cdots,x_n$ y esto $\forall n\in \mathbb N$. De aquí se rige la propiedad de Markov.
$$
P(x_{n+1} = y | x_0, x_0, \cdots, x_{n+1}=x_{n+1}, x_n=x)=P(x_{n+1}= y | x_n=x) \qquad (13)\\
\begin{eqnarray*}
&=& P(\epsilon_{n+1}+\sum_{k=0}^n \epsilon_k^n = y |x_0=x_1,\cdots,x_{n+1}= x_{n+1}, x_n= x)\\
&=& P(\epsilon_{n+1}= y - \sum_{n=0}^n\epsilon_k | x_0 = x_0, \cdots, x_{n-1}, x_n=x )\\
&=&P(\epsilon_{n+1}= y-x_n | x_0=x_0, \cdots,x_{n+1}=x_{n-1}, x_n = x)\\
&=& P(\epsilon_{n+1}= y-x| x_0 = x_0, \cdots, x_n=x)\\
&=&P(\epsilon_{n+1}=y | x_n=x)\\ 
&=&P(\epsilon_{n+1}+x=y | x_n=x)\\ 
\end{eqnarray*}
$$
$X_0={x_n}$ es una Cadena de Markov con un espacio de estados $S = {0, \pm1, \pm2, \cdots} = \mathbb Z$

Además, por $(12)$ y $(13)$

> Nota:
> $$
> P(\epsilon_m = 1)=P(\epsilon_0=1)= P(\epsilon_n = 1)\\
> P(\epsilon_m = -1)=P(\epsilon_0=-1)= P(\epsilon_n = -1)\\
> \forall n
> $$

$$
P(x,y) = P(\epsilon_0= y-x)\\
= P(X_{n+1} = y | X_n = x)
$$

$$
P(x,y) = \left\lbrace
\begin{array}{ll}
p \quad si \quad y \quad = 1+x\\
q \quad si \quad y \quad = -1+x\\
0 \qquad \text{en otro caso}
\end{array}\right. \\
$$

Sea $X_0 = \{x_0, x_1, \cdots\}$ una cadena de markov con espacio de estándar $S$. A la variable aleatoria se le llama estado inicial de la cadena de markov y su distribución digamos 
$$
\mathbb \Pi(x) = P(X_0 = x) \quad \forall x\in S
$$
Se le llama distribución inicial: Ai además $X_0$ tiene matriz de transición $P$, entonces $x$ dice que $X_0$ s una cadena de markov $(\Pi, P)$.

### Proposición 1.4

> Un Proceso estocástico $X_0= \{X_n, n=0,1,\cdots\}$ a tiempo discreto es una cadena de Markov $CM(\Pi, P)$ si y sólo si para cualquier $n= 0,1,\cdots$ y $x_0, \cdots, x_n \in S$
> $$
> P(X_0 = x_0, X_1=x_1,\cdots, X_n=x_n) = \Pi(x_o)P(x_0,x_1)\cdots P(x_m, x_n)
> $$

### Proposición 1.5

> Sea $X_0=\{x_n, n=0,1,\cdots\}$ un Proceso estocástico de tiempo discreto con espacio de estudio $S$ numerable. Las siguientes afirmaciones son equivalentes:
>
> - **a)** $X_0$ una Cadena de Markov $(\Pi, P)$
>
> - **b)** $$P(x_{n+1}=Y_1,\cdots,X_{n+m} = Y_m |X_0 = x_0, \cdots,X_n=x_n)\\=P(x,y_1)P(y_1,y_2)\cdots P(y_{m-1}, y_m)$$ $\forall n\ge0, m\ge1$ y estados $X_0, \cdots, X_{n-1},X_1,Y_1,\cdots,Y_m\in S$
>
> - **c)** Si $A_0, \cdots,A_{n-1}$ son subconjuntos de $S$, entonces 
>   $$
>   \begin{eqnarray*}
>   P(X_{n+1} &=& y_1, \cdots,X_{n+m} = Y_m | X_0\in A_0, \cdots, X_{n-1}\in A_{n-1}, X_N= x)\\
>   &=&P(x_1y_2)P(y_1,y_2)\cdots P(y_{n-1}y_m)\\
>   \forall &\quad& n\ge1, m\ge 1, \text{} \quad x, y_1, \cdots, y_m \text{ en } S
>   \end{eqnarray*}
>   $$
>
> - **d)** Si $A_0, \cdots,A_{n-1}, B_1, \cdots, $ son subconjuntos de S
>   $$
>   P(X_{n+1}\in B_1, \cdots, X_{n+m} \in B_m | x_0 \in A_0, \cdots, X_{n-1} \in A_{n-1}, X_n = x)\\
>   = \sum_{y_i \in B_1}\cdots \sum_{y_m \in B_m}P(x_1y_1)P(y_1, y_2) \cdots P(Y_{m-1},Y_m) 
>   $$
>   Además, de las probabilidades de transición de un pasos, consideramos las probabilidades de transición de $n $ pasos $P_n(x,y)$, definiendo
>   $$
>   P_n(x,y) = P(X_N= y | X_0 = x) = P(X_{n+m}=y|X_m = x)
>   $$
>   Definimos la matriz de transición de $n$ pasos 
>   $$
>   P_n = [P_n(x,y)]
>   $$
>   

$$
S = \{S_1, S_2, \cdots, S_n\}\\\\
P_n = 
\begin{matrix}
& S_1 & S_2 & \cdots & S_j \\
S_1 & &  &  & \\
\vdots &  & P_n(S_i,S_j) &  & \\
S_i &  &  &  & 
\end{matrix}
$$

Para cualquier $n,m= 0,1,\cdots$
$$
P_{n+m}= P_nP_m = P^nP^m = P^{n+m} \qquad (17) \\
P_{n+m}(x,y) = \sum_{z\in S}P_n(x,z)P_m(z,y) \quad \forall x,y \in S \qquad (18)
$$

### Ejemplo

Considere la Cadena de Markov $\{X_n\}$ $X_N = \epsilon_0+\cdots+\epsilon_n$, donde las $\epsilon_n$ son variables aleatorias y linealmente independientes e idénticamente distribuidas (iid)
$$
P(\epsilon_0=1)=P,\quad P(\epsilon=0)=1-p=q
$$
Calcular la matriz de transición de un sólo paso y la de $n$ pasos

- Espacio de estados $S = \{0,1,\cdots, n\}, \quad \forall n \in \mathbb N$

- $$
  P(i,j) = \left\lbrace
  \begin{array}{ll}
  q \quad si \quad i=j\\
  p \quad si \quad i = j-1\\
  0 \qquad \text{en otro caso}
  \end{array}\right. \\
  $$

  $$
  \begin{eqnarray*}
  P(i,j) &=& P(X_1=j | x_0=i)\\
  &=& P(X_1 = j | X_0=1)\\
  &=& P(\epsilon_0+\epsilon_1 = j | \epsilon_0 = i)\\
  &=& P(i+\epsilon_1=j| \epsilon_0 =i)\\
  &=& P(\epsilon_1=i-j | \epsilon_0 = i)\\
  &=& P(\epsilon_1 = j-i)
  \end{eqnarray*}
  $$

  

- 

- $$
  P(S_i,S_j) = \begin{matrix}
  & S_1 & S_2 & \cdots & S_n \\
  S_1 & q & p & \cdots & 0\\
  S_2 & 0 & q & \cdots & 0\\
  S_3 & 0 & 0 & \cdots & 0\\
  \vdots & \vdots & \vdots & \ddots & \vdots\\
  S_n & 0 & 0 & \cdots & q
  \end{matrix}
  $$

- $$
  \begin{eqnarray}
  P_n(i,j)&=& P(X_n=j | X_0=i)\\
  &=& P\left(\sum_{k=0}^n \epsilon_k = j | \epsilon_0 = i\right)\\
  &=& P\left(\sum_{k=1}^n \epsilon_k +\epsilon_0 = j | \epsilon_0 = i\right)\\
  &=& P\left(\sum_{k=0}^n \epsilon_k + i = j | \epsilon_0 = i\right)\\
  &=& P\left(\sum_{k=0}^n \epsilon_k = j - i | \epsilon_0 = i\right)\\
  &=& P\left(\sum_{k=0}^n \epsilon_k = j - i\right) = \frac{n}{j-i}p^{j-i}q^{n-j+i}\\
  \sum_{k=1}\epsilon_n\sim Bim
  \end{eqnarray}
  $$

Para cada $n=0,1,\cdots$ denotaremo $\Pi_n = \{\Pi_n(x), \quad x \in B\}$ la distribución de $x_n$ es decir
$$
\Pi_n(x)= P(x_n=x)
$$
En particular, $\Pi_0$ es la distribución inicial de la Cadena de Markov, $x_0=\{x_n\}$. Interpretando $\Pi_n$ como un vector fila. Se detiene que 
$$
\Pi_n=\Pi_0P_n=\Pi_oP^n,\quad \forall n = 1,2,\cdots
$$
o bien
$$
\Pi_n=\Pi_0P_{n-1},\quad \forall n = 1,2,\cdots
$$

### El problema de la ruina del jugador

Supongamos que un jugador comienza operaciones con un capital de $x$ dólares y juega contra un oponente con capital $b-x$ dólares.

En cada juego nuestro jugador tiene probabilidad de ganar $p$ y probabilidad de perder $q=1-p$. Los juegos se asumen independientes con $0<p<1, \quad 0<x<b$, el proceso continua hasta que el capital de nuestro jugador alcance el $0$ *la ruina* o el capital $b$ *victoria*.

Sea $A = \{\text{eventual ruina}\}$, $B_1=\{\text{El jugador gana el primer juego}\}$ y $B_2= \{\text{El jugador pierde el primer juego}\}$
$$
\begin{eqnarray}
P(A) &=& P(A\cap(B_1\cup B_2)) = P((A\cap B_1) \cup (A\cap B_2))\\
&=& P(A\cap B_1) + P(A\cap B_2)\\
&=& \left(\frac{P(A\cap B_1)}{P(B_1)}\right)P(B_1)+\left(\frac{P(A\cap B_2)}{P(B_2)}\right)P(B_2)\\
&=& P(A | B_1)P(B_1)+P(A | B_2)P(B_2)\\
&=& P(A | B_1)p+P(A | B_2)q
\end{eqnarray}
$$
**Nota:**Se tiene que para $B_1$ y $B_2$ eventos tales que $B_1\cup B_2 = \Omega \quad P(B_1), P(B_2)\neq0 \quad B_1\cap B_2 = 0$  $P(A)= P(A | B_1)p+P(A | B_2)q$  como Teorema de probabilidad total. 

Denotamos la probabilidad de eventual ruina con capital inicial $x$ como $h(x)$ luego del razonomiento analítico:
$$
\begin{matrix}
h(x)= & ph(x+1) & + &q(x-1)\\
P(A) & P(A| B_1) & & P(A|B_2)
\end{matrix}
$$

$$
h(x) = P(A) = P(A\cap (B_1\cup B_2)) = P((A \cap B_1) \cup (A\cap B_2))\\
h:\{0,1,\cdots,b\}\rightarrow [0,1]
$$



- ¿Qué pasa con $h(0)$?$\qquad h(0) = 1$

- ¿Qué pasa con $h(b)$ $\qquad h(b) = 0$



La ecuación diferencial anterior se puede escribir en forma estándar como sigue:
$$
ph(x+2)-h(x+1)+qh(x) = 0\\
x = 0,1,2,\cdots, b-2,\qquad h(0) = 1 \quad h(b)= 0
$$
Para resolver lo anteior asumimos 
$$
h(x) = \lambda^x=e^{x\ln \lambda}
$$
entonces:
$$
P\lambda^{x+2}-\lambda^{x+1}+q\lambda^x=\lambda^x(p\lambda^2-\lambda+q)=0
$$


Con $\lambda^x\neq 0$, tenemos que
$$
\begin{eqnarray}
(&p&\lambda^2-\lambda+q)= 0 \quad \text{y}\\
\lambda&=&\frac{1}{2p}(1\pm \sqrt{1-4pq})\\
&=& \frac{1}{2p}(1\pm |p-q|)
\end{eqnarray}
$$
Porque
$$
\begin{eqnarray}
(p-q)^2&=&p^2-2pq+q^2\\
&=&p^2-2pq-4pq+q^2\\
&=&(p+q)^2-4pq\\
&=&1-4pq
\\
1-p &=& q
\end{eqnarray}
$$

$$
\begin{eqnarray}
\lambda_1 &=& \frac{1}{2p}(1+p-q)\\
&=& \frac{1+p-q}{2p}\\
&=&1
\end{eqnarray}
$$

$$
\begin{eqnarray}
\lambda_2 &=& \frac{1}{2p}(1-p+q)\\
&=& \frac{q}{p}
\end{eqnarray}
$$

$$
\begin{eqnarray}
p-q&=&p-(1-p)\\
&=&|2p-1|
\end{eqnarray}
$$

**Caso 1** $\quad p\neq q$ Entonces $\lambda_1 \neq \lambda_2$ y
$$
\text{Ecuación general: }\quad
h(x)= A\lambda_1^x+C\lambda_2^x = A + C\left(\frac{q}{p}\right)^x\\
1=h(0) = A+C\\
0=h(b)=A+C\left(\frac{q}{p}\right)^x
$$
Resolviendo el sistema anterior
$$
A = \frac{-\left(\frac{q}{p}\right)^b}{1-\left(\frac{q}{p}\right)^b} \qquad C = \frac{1}{1-\left(\frac{q}{p}\right)^b}\\\\
\therefore \quad h(x)=\frac{\left(\frac{q}{p}\right)^x-\left(\frac{q}{p}\right)^b}{1-\left(\frac{q}{p}\right)^b}
$$
**Caso 2** $\quad p=q=\frac{1}{2}$

$\lambda_1=1,\quad \lambda_2=1$ Luego tenemos raíces repetidos en caso la solución.
$$
h(x)= A\lambda^x+Cx\lambda^x = A+Cx\\
1=h(0)= A
0=h(b)= A+Cb
$$

$$
A = 1 \qquad C = \frac{-1}{b}\\\\
\therefore \quad h(x)=1-\frac{1}{b}x=\frac{b-x}{b}
$$

### Resumiendo

En resumen tenemos lo siguiente;

*grafica*
$$
h(x)= \left\lbrace 
\begin{matrix}
\frac{\left(\frac{q}{p}\right)^x-\left(\frac{q}{p}\right)^b}{1-\left(\frac{q}{p}\right)^b} &\quad si \quad p\neq q\\
\frac{b-x}{b} & si \quad p=q = \frac{1}{2}
\end{matrix} \right.
$$
donde la gráfica anterior, es la gráfica $x$ contra $h(x)$ ($x$ el capital inicial del jugador y $h(x)$ la probabilidad de ruina con dicho capital).

Similarmente, sea $g(x)$ la probabilidad de victoria eventual, empezando con un capital de $x$ dólares. No podemo concluir inmediatamente que $g(x)=1-h(x)$ puesto que existe la posibilidad de que el juego nunca termine, esto es que la fortuna del jugador oscile entre $1$ y $b-1$ 
$$
p^iq^j\qquad i+j=n \quad 0 \le i,j \le 1\\\\
\therefore \qquad \lim_{n\rightarrow \infty} p^iq^j\le \lim_{n\rightarrow \infty} \max\{p,q\}^n = 0
$$
Considerando $R_i$ como la ganancia obtenida por el jugador en el $i-ésimo$ intento.
$$
P(R_i=1)= P,\qquad P(R_i=-1)= q
$$
Luego el capital del jugador en el $n-ésimo$ juego es:
$$
x+\sum_{i=1}^n R_i
$$
Y entonces $h(x)$ la podemos definir como:
$$
h(x) = P\left(\{\text{Para algun, } x+\sum_{i=1}^nR_i\}=0, \quad 0< x+\sum_{i=1}^k R_i < b, \qquad k = 1,2,\cdots, n-1\}\right)\\
$$
El modelo anterior, puede ser identificado como una caminata aleatoria con estados --absorventes, $0$ y $b$.

--

### Hacia la caminata aleatoria

Tenemos 2 jugadores, cada uno con capital, el primer jugador tiene $x$ dólares iniciales y el segundo jugador tiene $x-b$ dólares iniciales, durante cada partida el jugador $1$ tiene la probabilidad de ganar $p$ y el jugador 2 de $q$ donde $q = 1-p$, este proceso sigue hasta que nuestro jugador alcance $0$ ó $b$ capital.
$$
v_n = x+ \sum_{i=1}^n R_i\\\\
P(\epsilon_0=1)= p=1-q\\
P(x,y) = \left\lbrace
\begin{array}{ll}
p \quad si \quad y \quad = 1+x\\
q \quad si \quad y \quad = -1+x\\
0 \qquad \text{en otro caso}
\end{array}\right. \\
$$


 

--

Ahora investigaremos el efecto de remover uno o ambos estaos absorbentes. Si $h_b(x)$ la probabilidad de ruina eventual comenzando en $X$, cuando la capital total es $b$. Es razonable esperar que 
$$
\lim_{b\rightarrow \infty} h_b(x)
$$
sea la probabilidad de ruina eventual comenzando en $x$, cuando el jugador posee la mala fortuna de enfrentarse a un adversario con capital infinito. Llamemos a tal probabilidad $h^*(x)$ . Tenemos que 
$$
h^*(x) = P(A)=\\ P\{\text{Para algun entero positivo b, el capital del jugador alcanza el 0 antes que el capital b}\}
$$
 Sea $A_b = \{\text{0 es alcanzado antes que b}\}$, por lo que $A_{n-1} \sube A_n$, recordando que 
$$
P\left(\bigcup_{n=1}^\infty A_n\right)  = \lim_{n\rightarrow \infty} P(A_n)
$$

$$
\lim_{b\rightarrow \infty}h^*(x)= \left\lbrace 
\begin{matrix}
\left(\frac{q}{p}\right)^x &\quad si \quad p > q\\
1 & \quad p \ge q
\end{matrix} \right.
$$

