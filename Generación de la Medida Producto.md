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

Como $A$ y $B$ son rectángulos medibles y $(A_i \times B_i)$ una sucesión de rectángulos entonces, aplicando el Teorema anterior obtenemos que $A_i$ y $B_i$ son medibles y fijando ya sea $x$ o $y$, tenemos
$$\kappa(A)\xi_{B}(y)=\sum_{i=1}^{\infty}\kappa(A_j)\xi_{B_i}(y)$$
Ahora fijando $y$,
$$\kappa(A)\lambda(B)=\sum_{i=1}^{\infty}\kappa(A_j)\lambda(B_j)$$