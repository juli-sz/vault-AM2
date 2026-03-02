Todo conjunto no vacío, o espacio, entre cuyos elementos se define una **distancia** se denomina **espacio métrico**. Es usual definir una distancia en cualquier espacio no vacío $E$, como una función $E \times E \to \mathbb{R}$, indicando que para cada par de puntos de $E$ le corresponde un único número real, llamado distancia entre ambos.
### Axiomas de la Distancia

La función distancia se cumple en un conjunto $E$ si y solo si se verifican los siguientes axiomas:
1. La distancia entre un punto $a$ y $b$ es mayor a **0**.
2. La distancia entre un punto $a$ y $b$ es **0** si y solo si $a = b$.
3. La distancia de $a$ a $b$ es igual a la distancia de $b$ a $a$.
4. **Desigualdad Triangular:** Para todo $a, b, c$, la distancia entre $a$ y $c$ es menor o igual a la distancia de $a$ a $b$ más la distancia de $b$ a $a$.
### Distancia Euclídea en $\mathbb{R}^n$
Para el conjunto $\mathbb{R}^n$, la regla geométrica que da la distancia entre dos puntos por aplicación del **Teorema de Pitágoras** es:
$$d(\bar{a}, \bar{b}) = \left[ \sum_{i=1}^{n} (a_i - b_i)^2 \right]^{1/2}$$