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

Sea $X_0 = \{x_0, x_1, \cdots\}$ una cadena de markov con espacio de estándar $S$. A la variable aleatoria se le llama estado inicial de la cadena de markov y su distribución degamos 
$$
\mathbb \Pi(x) = P(X_0 = x) \quad \forall x\in S
$$
Se le llama distribución inicial: Ai además $X_0$ tiene matriz de transición $P$, entonces $x$ dice que $X_0$ s una cadena de markov $(\Pi, P)$.

### Proposición 1.4

> Un Proceso estocástico $X_0= \{X_n, n=0,1,\cdots\}$ es una cadena de Markov $(\Pi, P)$ si y sólo si para cualquier $n= 0,1,\cdots$ y $x_0, \cdots, x_n \subset S$
> $$
> P(X_0 = x_0, X_1=x_1,\cdots, X_n=x_n) = \Pi(x_o)P(x_0,x_1)\cdots P(x_m, x_n)
> $$

### Proposición 1.5

> Sea $X_0=\{x_n, n=0,1,\cdots\}$ un Proceso estocástico de tiempo discreto con espacio de estudio $S$ directo. Las siguientes afirmaciones son equivalentes:
>
> - **a)** $X_0$ una Cadena de Markov $(\Pi, P)$
> - **b)** $$P(x_{n+1}=Y_n,\cdots,X_{n+m} = Y_m |X_0 = x_0, \cdots,X_n=x_n)\\=P(x,y_1)P(y_1,y_2)\cdots P(y_{n-1}, y_m)$$ $\forall n\ge0, m\ge1$ y estados $X_0, \cdots, X_m,X_1,Y_1,\cdots,Y_m\in S$