# Generación de la Medida Producto

En el presente documento se tratará de hacer una descripción detallada del procedimiento para generar una medida en el producto cartesiano $X\times Y$, basado en la medida sobre conjuntos de la forma $A\times B$ con $A\in X$ y $B\in Y$. Para ello, intentaremos demostrar el siguiente Teorema:

$$\underline{\text{Teorema:}}\quad\text{Si } (X,\bold{X},\kappa)\text{ y }(Y,\bold{Y},\lambda)\text{ son espacios de medida, entonces existe una medida }\mu \text{ definida en } Z=X\times Y\text{ tal que,}$$
$$\mu(A\times B)=\mu(A)\mu(B) $$
$\text{para toda } A\in X\text{ y }B\in Y\text{. A esta medida le llamaremos Medida Producto y establecerá que la medida del producto de dos conjuntos medibles será el producto de sus medidas.}$

$\underline{\text{Demostración:}}$
Primero, consideremos a los rectángulos medibles $A\times B$ como uniones disjuntas de una sucesión de rectángulos de la forma $(A_i \times B_i)$, tal que
$$(A\times B)\subset\bigcup^{\infty}_{i=1}(A_i \times B_i)$$

Por definición de rectángulos medibles (una extensión del concepto de $n$-volumen), siendo $x\in A$ e $y\in B$ tenemos que,
$$\xi_{A\times B}(x,y)=\xi_{A}(x)\xi_{B}(y)$$

Ahora, por propiedad 3 de Medidas (axioma 3), tenemos que
$$\xi_{A\times B}(x,y)=\xi_{A}(x)\xi_{B}(y)=\sum_{i=1}^{\infty}\xi_{A_i}(x)\xi_{B_i}(y)$$

Para continuar con esta demostración, recordemos el siguiente teorema que nos será muy útil:

**Teorema Auxiliar (Convergencia Monótona):** Sea $\{f_n\}$ una sucesión monótona creciente de funciones en $\mathcal{M^+}$ que converge a $f$ puntualmente, entonces $f\in\mathcal{M^+}$ y además
$$\int f d\mu=\lim_{n \to \infty}\int f_n d\mu$$

Como $A\times B$ son rectángulos medibles y $(A_i \times B_i)$ una sucesión de rectángulos entonces, aplicando el Teorema anterior obtenemos que $(A_i\times B_i)$ son medibles y fijando ya sea $x$ o $y$, tenemos
$$\kappa(A)\xi_{B}(y)=\sum_{i=1}^{\infty}\kappa(A_i)\xi_{B_i}(y)$$
Ahora fijando $y$,
$$\kappa(A)\lambda(B)=\sum_{i=1}^{\infty}\kappa(A_i)\lambda(B_i)$$

Para continuar con la demostración, utilicemos el siguiente resultado

$$\underline{\text{Lema}}: \text{Sea }C=A\times B\text{ un rectángulo medible, entonces la unión finita de todos los rectángulos } C_0\text{ es un álgebra de subconjuntos de C}.$$

Esto es fácil de demostrar ya que,

* Con $\kappa$ y $\lambda$ bien definidas, podemos tomarnos cualquier rectángulo de medida cero y así obtener el conjunto vacío $\implies \emptyset\in C_0$
* Sea $R\in A_i \times B_i$ dentro de $C=A \times B$. El complemento $R^c$ de $R$ en $C$ se puede expresar como la unión de rectángulos que cubren el resto de $C$ sin solaparse con $R^c$. Esto se puede hacer dividiendo $C$ en rectángulos que no incluyen a $R$ y cuya unión junto con $R$ recomponen a $C$ $\implies$ si $R\in C_0$ entonces $R^c\in C_0$
* La unión finita de cualquier conjunto de rectángulos $C_0$ dentro de $C$ es simplemente otro subconjunto de $C$ que puede ser cubierto por una unión finita de rectángulos, cada uno de los cuales es un miembro de nuestra colección. Esto es porque podemos reorganizar o combinar estos rectángulos en un número finito de rectángulos más grandes, para cubrir la unión deseada sin salirnos de $C$.

Este lema nos sirve ya que si $R\in C_0$, entonces, por definición (y dado que es álgebra de $C$),

$$R=\bigcup_{i=1}^{n}(A_i\times B_i)$$

con $A_j\times B_j$ son rectángulos disjuntos. Al definir la medida $\mu$ como

$$\mu(R)=\sum_{i=1}^n\kappa(A_i)\lambda(B_i)$$

notamos que la medida queda bien definida ya que

* Sean $\kappa$ y $\lambda$ medidas bien definidas, $\mu(\emptyset)=\sum_{i=1}^n\kappa(\emptyset)\lambda(B_j)$=0 por propiedades de la medida.
* Como $\kappa(A_i)\geq0$ y $\lambda(B_i)\geq0\quad\forall i\implies \mu(R)\geq0\quad\forall R$

Por lo que $\mu$ está bien definida $\square$
