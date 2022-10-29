Esta silumación ayuda a modelar ciertos fenómenos complejos, mediante variables aleatorias y procesos estocásticos.

Consideramos repetidamente un evento independiente de un experimento aleatorio. Definido por la secuencia $X_1, X_2, X_3, \cdots$.
$$
\sum_{i=1}^k P(A\cap B_i) = \sum_{i=1}^kP(A|B_i)P(B_i)
$$

## Ejemplo 1.8 daltónico:

|        | Daltónico | Población EU |
| ------ | --------- | ------------ |
| Hombre | 7%        | 49%          |
| Mujer  | 0.4%      | 51%          |

$$
\begin{eqnarray}
P(C) &=& P(D|H)P(H)+P(D|M)P(M)\\
&=& (0.07)(0.49)+(0.004)(0.51)\\
&=& 0.03634
\end{eqnarray}
$$

## Ejemplo 1.9 carta:

$$
P(C) = P(C|MC)P(MC)+P(C|MNC)P(MNC)
$$

## Regla general de Bayes:

$$
P(B_i|A)=\frac{P(A|B_i)P(B_i)}{\sum_jP(A|B_j)P(B_j)}
$$

## Ejemplo polígrafo

- $\frac{1}{100}$ es un ladrón en una empresa
- $P(P|L)=0.95$ de que detecte que un ladrón si es un ladrón
- $0.1$ el polígrafo da un falso positivo

$$
\begin{matrix}
&TRUE&FALSE\\
PP&95\% & 5\%\\
FP&10\% & 90\%
\end{matrix}
$$

Asumimos que un empleado aleatorio es testado diciendo que no es un ladrón. El polígrafo detectó que está mintiendo. 

Calcular la probabilidad de que el empleado está mintiendo.
$$
\begin{eqnarray}
P(L|P)&=&\frac{P(P|L)P(L)}{P(P|L)P(L)+P(P|L')P(L')}\\
&=&\frac{(0.95)(0.01)}{(0.95)(0.01)+(0.1)(0.99)}\\
&=& 0.088
\end{eqnarray}
$$

## Ejemplo 1.12

Supongamos que Max escoge un número aleatorio entre 1 y 100 que llamamos $X$. si Mary escoge un entero uniforme $Y$  entre 1 $x$. Encontrar la probailidad condicional de $Y$ dado $X=x$.

$P(Y=y|X=x)= \frac{1}{x}$

## Ejemplo 1.13

$$
P(X=x|Y=y)=\frac{x+y}{18}\quad \text{for }x,y = 0,1,2
$$

Encuentre la probabilidad condicional de $Y$ dado $X=x$.
$$
f(y) = P(Y=y| X=x)= \frac{P(Y=y, X=x)}{P(X=x)}
$$

$$
\begin{eqnarray}
P(\{X=x\}) &=& P(\{X=x\}\cup \Omega)\\
&=& P(\{X=x\}\cup \bigcup_{y=0}^2\{Y=y\})\\
&=&\sum_{y=0}^2P(X=x, Y=y)\\
&=& \frac{3x}{18}+\frac{3}{18}=\frac{x+1}{6}
\end{eqnarray}
$$

## Ejemplo 1.14

Una bolsa de canicas tiene 2 rojas, 3 azules y 4 blancas. Tres canicas son tomadas de la bolsa sin reemplazarlas. Sea $B$ el número de canicas azules tomadas y sea $R$ el nímero de canicas rojas tomadas. Encontrar la probabilidad condicional de $B$ dado $R=1$.
$$
\begin{eqnarray}
f(x) = P(B = x|R=1)
\end{eqnarray}
$$

## Ejemplo 1.16

Toma toma un valor $X$ entre $[0,1]$, después Larisa toma un número $Y$ dado $(0, x)$

- Encuentre la distribución de $Y$ dado $X = x$
  $$
  P(Y=y| X= x) = \frac{1}{x}
  $$
  
- Encuentre la distribución conjunta de $X$ y $Y$
  $$
  \begin{eqnarray}
  P(Y=y| X= x) &=& \frac{P(Y=y, X=x)}{P(X= x)}\\
  P(Y = y,X =x )&=& P(Y=y|X=x)P(X=x) \qquad 0 < y <x<1
  \end{eqnarray}
  $$
  
- Encuentre la densidad marginal de $Y$

## Esperanza condicional

$$
E(Y|X=x)=\lbrace\begin{matrix}\sum_yyP(Y=y|X=x) \text{ , discreto}\\ \int_{-\infty}^\infty yf_{Y|X}(y|x)dy \text{ , continuo}\end{matrix}\rbrace)
$$

### Ejemplo 1.17

Tenemos la siguiente tabla de probabilidad, donde Y es en número de personas en la primera caja y X el número de personas en la segunda caja.
$$
\begin{eqnarray}
E[Y|X=1]&=&\sum_{y=0}^4yP(Y=y|x=1)\\
&=& \sum_{y=0}^4y\frac{P(Y=y, X=1)}{P(X=1)}\\
&=& 0.81
\end{eqnarray}
$$

### Ejemplo 1.18

Sea $X$ una variable aleatoria independiente de Poisson con sus respectivos parámetros $\lambda$ y $\mu$. Encuentra la esperanza condicional de $Y$ dado $X+Y=n$

Recordemos la distribución de Poisson como:
$$
P[X=k]=\frac{e^{-\lambda} \lambda^k}{k!}
$$
tenemos que:


$$
\begin{eqnarray}
E(Y|X+Y=n)&=&\sum_k kf(k)\\
P(Y=k|X+Y=k)&=&\frac{P(X=n-k)}{P(X+Y=n)}\\
P(X+Y=n, y\ge 0) &=& P(X+Y=n, \bigcup_{l=0}^\infty \{Y=l\})\\
&=& \sum_{l=0}^\infty
\end{eqnarray}
$$
