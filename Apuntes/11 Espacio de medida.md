# Espacio de medida

Un espacio de medida es una terna $(\Omega, \digamma, \mu)$ cuyos componentes definimos en esta sección.

#### 1.1 Definición: 

> Sea $ \Omega$ un conjunto no vacío y $\digamma$ una familia de subconjuntos de $\Omega$. Decimos que $\digamma$ es una $\sigma-álgebra$ si:
>
> - **a)** $\Omega \in \digamma$
>
> - **b)** Si $A\in\digamma$, entonces $A^c\in\digamma$
>
> - **c)** Si $\{A_n\}_{n\in\mathbb N}$  es una sucesión de conjuntos en $\digamma$ 
>
>   $\left(A_n\in\digamma\quad\forall n\in\digamma\right)$, entonces $\bigcup_{n\in\mathbb N}A_n\in \digamma$

#### 1.2 Proposición: 

> Si $\digamma$ es una $\sigma-álgebra$ de $\Omega$, entonces
>
> - **a)** $\varnothing \in \digamma$
> - **b)** Si $\{A_n\}$ es una sucesión en $\digamma$ entonces $\bigcap_{n\in\mathbb N}A_n\in\digamma$

#### Demostración

En efecto, como $\digamma$ es una $\sigma-álgebra$ de la definición **1.1a** , $\Omega \in \digamma$ y de la definición **1.1b**

Tenemos que $\bigcap_{n\in\mathbb N}A_n = \left(\left(\bigcap_{n\in\mathbb N} A_n\right)^c\right)^c$  

como $A_n\in\digamma$, $\forall_n\in\mathbb N$ de la definición **1.1b**

$A_n^c\in\digamma$, $$\forall_n\in\mathbb N$$ y de la definición **1.1c**

$\bigcap_{n\in\mathbb N}A_n^c \in \digamma$ y nuevamente utilizando la definición **1.1b**

$A_n = \left(\bigcup_{n\in\mathbb N}A_n^c\right)^c \in \digamma$

#### 1.3 Definición

> Si $\digamma$ una $\sigma-álgebra$ de $\Omega$ se dice que el par $(\Omega, \digamma)$ es un espacio medible. Si A es un conjunto en $\digamma,\quad(A\in\digamma)$ decimos que $A$ medible.

A $\omega$ se le conoce como elemento seguro y al $\varnothing$ como elemento imposible.

#### 1.4 Ejemplo

#### 1.5 Definición

> Sea $\mu = \mathbb R$ y a $A$ una familia de todos los intervalos abiertos $[a,b]\subseteq\mathbb R$
>
> Entonces la $\sigma-álgebra$ se llama la $\sigma-álgebra$ de **Borel** de $\mathbb R$ y se denota por $B(\mathbb R)$ Si $B\in B( \mathbb R)$ se dice que $B$ es un *Conjunto de Borel de** $\mathbb R$.
>
> La definición anterior se puede extender al caso "vectorial" $\mu = \mathbb R^n$ como sigue. Si $\mathbb a = (a_1, a_2, \cdots, a_n)$ y $\mathbb b = (b_1, b_2, \cdots, b_n)$ son valores en $\mathbb R^n$, decimos que $a<b$ si $a_i\subset b_i$, para $i = 1,2,\cdots,n$.

#### 1.6 Definición

> Sea $\mu=\mathbb R^n$ y sea $A$ la familia de todos los rectángulos $(\mathbb a, \mathbb b)$ en $\mathbb R^n$ La $\sigma-álgebra$ generada por $A$ se llama la $\sigma-álgebra$  de **Borel** de $\mathbb R^n$ y se denota por $B(\mathbb R^n)$.
>
> Si B está  $B(\mathbb R^n)$ se dice que B es un **conjunto de Borel** en $\mathbb R^n$.

#### 1.7 Definición

> Sea $(\mu, \digamma)$ un espacio medible y $\bar{\mathbb R} = \mathbb R \cup\{-\infty, \infty\}$.
>
> Se dice que la función $\mu:\digamma \rightarrow\bar{\mathbb R}$ es una medida de $\digamma$ si:
>
> - **a)** $\mu(\varnothing)=0$
>
> - **b)**$\mu(A)=\ge0 \quad \forall A\subset\digamma$
>
> - **c)** $\mu$ es $\sigma-aditiva$, $\mu$ si $\{A_n\}^{+\infty}_{n=1}$ es una sucesión de conjuntos ajenos a $\digamma$ $A_n \cap A_m \neq \varnothing \forall_{n\neq m}$ entonces
>
>   $$\mu\left(\bigcup_{n=1}^{+\infty}A_n\right)=\sum_{n=1}^{+\infty}\mu(A_n)$$

En este caso se dice que $(\Omega, \digamma, \mu)$ es un espacio de medida:

- A $\mu(A)$ se le llama la medida de A con respecto a $\mu$ 
- Si $\mu(\Omega)<\infty$, se dice que $\mu$ es una medida finita

En particular si $\mu(\Omega)= 1$, es una medida de probabilidad $P= \mu$ $A(\mu, \tau,P)$, le llamaremos espacio probabilístico y a $P(A)$. $P(\varnothing)= 0$

## 1ra Proposición (Propiedades de P)

Sea $(\mu, \digamma, \varphi)$ un espacio de eventos en $\digamma$

- **a)** $P(A^c)=1-P(\mu)$

- **b)** $P(B|A) = P(B)-P(B\cap A)$ 

  Si $A\subset B$

  $P(B|A)=P(B)-P(A)$

- **c)** Monotonía

  $A\subset B \Longrightarrow P(A)\le P(B)$

- **d)** $P(A\cup B) = P(A)+P(B)-P(A\cap B)$

- **e)** Si $A_1, \cdots,A_n$ está en $\digamma$

  $$P\left(\bigcup_{i=1}^{n}A_i\right)\le\sum_{i=1}^nP(A_i)$$

### 1.11 Proposición

C Continuidad de P con respecto a secuencias monótonas

...

Y los cuales $A_1, (A_2|A_1), (A_3|A_2), \dots, (A_n|A_{n-1})$
$$
P(A⁺)=P(A_1\cup (A_2|A_1) \cup \cdots) \\ 
= P(A_1)+ \sum_{n=1}^{+\infty} P(A_{kn})-P(A_k)\\
= \lim_{n\rightarrow\infty} P(A_n)
$$

$\bigcap_{n=1}^{+\infty}A_n$

 **b)** Toma
$$
A^{-c}=\left(\bigcap_{n=1}^{+\infty} A_n\right)^c\\
= \bigcup_{n=1}^{+\infty}A_n^c \qquad \text{Observe que } A_1^c\subset A_2^c\subset \cdots A_{n+1}^c\\
= \lim_{n\rightarrow\infty}P(A_n^c)= \lim_{n\rightarrow\infty} 1-P(a_n)\\
= 1 - \lim_{n\rightarrow\infty}P(a_n)
$$
Se sigue que $P(A⁻)=\lim_{n\rightarrow\infty}P(a_n)$

### 1.12 Colorario 

Si ${A_n}$ es una sucesión de eventos entonces:
$$
P\left(\bigcup_{n=1}^{+\infty} A_n\right) \le \sum_{n=1}^{+\infty}P(A_n)
$$

$$
A^c \qquad \text{A no ocurre } A_1\\
A\text{ y } B
$$



...

### 4.1 Definición

Sea $(\Omega, \digamma, \mu)$ un espacio de medida. Se dice que $X:\Omega\rightarrow\mathbb R$ es una función $\digamma-medible$ (o medible con respecto a $\digamma$) si:
$$
f^{-1}([-\infty, x])= \{\omega\in \Omega | f(\omega) \in (-\infty, x)\} \in \digamma
$$

- **a)** Si $\mu= P$ es una medida de probabilidad decimos que $X$ es una variable aleatoria.
- **b)** Si $(\Omega, \digamma)= (\mathbb R, B(\mathbb R))$ y $X:\mathbb R \rightarrow\mathbb R$, decimos que es una función de Borel.

#### Ejemplo

Si $(\Omega, \digamma)$ es un espacio discreto:
$$
(\Omega = \{w_1, w_2, \cdots,\w_n\})\\
= \{w_n | n\in\mathbb N\}
$$
entonces cualquier función $X:\Omega\rightarrow\mathbb R$ es una variable aleatoria pues el conjunto $\digamma$ cumple $\digamma=2^\Omega$.



Supongamos que tiramos 2 dados al aire:
$$
\Omega = \{(i,j) | 1 \le i,j \le 6\}\\
|\Omega| = 36, \quad (\Omega, 2^\Omega)\\
|2^\Omega| = 2^{36}
$$
Una variable aleatorio que se puede definir, es la siguiente:
$$
X(i,j) = i+j\\
1)\qquad X(\omega= (i,j)) = i+j\\
2) \qquad Y(\omega= (i,j)) = i\\
3) \qquad Z(\omega=(i,j)) = min(i,j)
$$


La probabilidad del evento
$$
X:(\Omega, \digamma)\rightarrow (\mathbb R, B(\mathbb R))\\
B \in B(\mathbb R), \quad X^{-1}(B)\\
f_x(x) = P(X(\[-\alpha, x ]))\\
\{X\le x\} = X^{-1}([\infty, x])\\
\qquad= \{\omega \in \Omega | x(\omega \le X)\} \quad x\in \mathbb R\\
\{x \in B\} = X^{-1}(B)
$$


### Proposición

Si $X$ es una variable aleatoria su función de distribución $F_x$ satisface que:

- **a)** $F_x$ es no-creciente, es decir, si $x<y$  entonces $F_x(x) \le F_x(y)$

- **b)** 
  $$
  F_x(+\infty) = \lim_{y\rightarrow\infty} F_x(y)=1\\
  F_x(-\infty) = \lim_{y\rightarrow -\infty} F_x(y)=0
  $$
  

