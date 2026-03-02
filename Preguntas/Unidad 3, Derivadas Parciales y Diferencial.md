# 1. **Derivadas parciales e interpretación geométrica.**  
   El concepto de derivada parcial se utiliza para determinar la velocidad o razon de cambio de una funcion f respecto a una de sus variables. Las derivadas parciuales tienen una interpretacion geometrica util. Si tomamos un valor y=y0 entonces z=f(x,y0) representa la curva de interseccion de la superficie z=f(x,y) con el plano y=y0 y por consiguiente fx (derivada en funcion de x) representa la pendiente de la curva en dirección de x

# 2. **Teorema de Schwartz (enunciado y condiciones).**  
   El **Teorema de Schwarz** (o de las derivadas cruzadas) establece la condición suficiente para que el orden de derivación en las derivadas parciales mixtas sea irrelevante.  
   Si una función *z*\=*f*(*x*;*y*) cumple con las condiciones de continuidad requeridas en un punto y su entorno, entonces las derivadas parciales mixtas son iguales en dicho punto

# 3. **Defina el diferencial de una función de dos variables independientes. Dé su interpretación grafica y geométrica.**
## 1. Definición Matemática

Para una función de dos variables independientes $z = f(x, y)$, el **diferencial total** $dz$ (o $df$) se define como la suma de los productos de las derivadas parciales por los incrementos de las variables independientes.
Matemáticamente, si $f$ es una función diferenciable:

$$dz = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy$$
Donde:
- $\frac{\partial f}{\partial x}$ y $\frac{\partial f}{\partial y}$ son las derivadas parciales evaluadas en un punto $(x, y)$.
- $dx$ y $dy$ son los cambios (o incrementos) en las variables independientes.

Este concepto es el que da origen a la forma $M(x, y) dx + N(x, y) dy$ que ves en tus apuntes de ecuaciones exactas.
## 2. Interpretación Geométrica

La interpretación geométrica del diferencial total es el **cambio en la altura ($z$) del plano tangente** a la superficie en un punto dado.

- **La Superficie vs. El Plano:** Imagina una sábana estirada y deformada (la superficie $z = f(x,y)$). Si apoyas un cartón rígido en un punto de esa sábana, ese es el **plano tangente**.
- **Diferencial ($dz$):** Cuando te movés una distancia pequeña $dx$ y $dy$ desde el punto de contacto, $dz$ es cuánto subiste o bajaste **sobre el cartón rígido** (plano tangente).
- **Incremento ($\Delta z$):** Es cuánto subiste o bajaste realmente **sobre la sábana** (superficie).
## 3. Interpretación Gráfica (Aproximación Lineal)

Gráficamente, el diferencial representa la **mejor aproximación lineal** del cambio de la función cerca de un punto.

- **Linealidad:** Al usar derivadas parciales (que son pendientes), estamos "aplanando" la función en ese punto.
- **Error de aproximación:** Para valores de $dx$ y $dy$ muy pequeños (infinitesimales), la diferencia entre el cambio real ($\Delta z$) y el aproximado ($dz$) es prácticamente despreciable.
- **Utilidad:** Se usa para calcular errores propagados o para estimar valores de funciones complicadas sin necesidad de evaluarlas directamente, usando solo la pendiente en un punto conocido

# 4. **Aplicación a errores del calculo diferencial**
### Problema: Estimación de Error en un Rectángulo

Supongamos que medís los lados de una placa rectangular. Obtenés que la base es $x = 10$ cm y la altura es $y = 20$ cm. Sin embargo, tu regla tiene un error de medición de hasta $0.1$ cm.
**¿Cuál es el error máximo aproximado en el cálculo del área?**
### Paso 1: Definir la función y los incrementos

El área de un rectángulo es una función de dos variables:
$$A(x, y) = x \cdot y$$
Los "errores" de medición son nuestros diferenciales (o incrementos pequeños):
- $dx = 0.1$ cm
- $dy = 0.1$ cm
### Paso 2: Calcular las derivadas parciales

Siguiendo la definición de la imagen, necesitamos $M = \frac{\partial A}{\partial x}$ y $N = \frac{\partial A}{\partial y}$:
- $\frac{\partial A}{\partial x} = y$ (derivamos $x \cdot y$ respecto a $x$, $y$ queda como constante).
- $\frac{\partial A}{\partial y} = x$ (derivamos $x \cdot y$ respecto a $y$, $x$ queda como constante).   
### Paso 3: Armar el Diferencial Total ($dA$)

Aplicamos la fórmula de la definición 2.4.1:
$$dA = \frac{\partial A}{\partial x} dx + \frac{\partial A}{\partial y} dy$$
$$dA = y \cdot dx + x \cdot dy$$
### Paso 4: Calcular el error absoluto

Evaluamos con los datos del problema:

$$dA = (20 \, \text{cm}) \cdot (0.1 \, \text{cm}) + (10 \, \text{cm}) \cdot (0.1 \, \text{cm})$$
$$dA = 2 \, \text{cm}^2 + 1 \, \text{cm}^2 = \mathbf{3 \, \text{cm}^2}$$

Esto significa que, por culpa de esos $0.1$ cm de error en cada lado, el área que calculaste ($200 \, \text{cm}^2$) podría estar corrida hasta en **$3 \, \text{cm}^2$**.

---

### ¿Por qué usamos el diferencial ($dA$) y no el incremento real ($\Delta A$)?

Podríamos haber calculado el área real con el error: $(10.1 \cdot 20.1) = 203.01$. El error real ($\Delta A$) es $3.01 \, \text{cm}^2$.

Como ves, el diferencial $dA = 3$ es una aproximación **casi perfecta** y mucho más rápida de calcular, especialmente cuando las funciones son más complejas (como senos, logaritmos o raíces).

> [!IMPORTANT]
> 
> En el examen, si te piden "error relativo", simplemente dividís el diferencial por el valor total:
> 
> $$\text{Error Relativo} = \frac{dA}{A} = \frac{3}{200} = 0.015 \, (1.5\%)$$

# 5. **Explique cómo se utiliza el concepto de diferencial para la estimación de errores. ¿Cuándo un campo escalar en $R^2$ es diferenciable? Explique.**
## 1. Estimación de Errores mediante el Diferencial

El concepto fundamental es que, para variaciones pequeñas de las variables independientes ($dx$ y $dy$), el **incremento real** de la función ($\Delta z$) es aproximadamente igual al **diferencial total** ($dz$).

### El Modelo Matemático

Si tenemos una magnitud calculada mediante una función $z = f(x, y)$, y las mediciones de $x$ e $y$ tienen errores (incertidumbres) representados por $dx$ y $dy$, el error propagado en $z$ se estima como:

$$dz = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy$$

### Tipos de Errores a calcular:

- **Error Absoluto:** Es el valor de $|dz|$. Nos da una idea de la magnitud máxima de la desviación.
    
- **Error Relativo:** Se calcula como $\frac{dz}{z}$. Es una medida adimensional que compara el error con el valor total.
    
- **Error Porcentual:** Es el error relativo multiplicado por 100 ($\frac{dz}{z} \times 100\%$).
    

> [!NOTE]
> 
> Esta aproximación es válida siempre que los errores de medición $dx$ y $dy$ sean pequeños en comparación con los valores de $x$ e $y$. Si los errores son grandes, la aproximación lineal del diferencial pierde precisión.

---

## 2. Diferenciabilidad de un Campo Escalar en $\mathbb{R}^2$

En una variable, la existencia de la derivada garantiza la diferenciabilidad. En $\mathbb{R}^2$, esto es más complejo: **la existencia de las derivadas parciales no garantiza que la función sea diferenciable**.

+1

### Definición Formal

Un campo escalar $f(x, y)$ es **diferenciable** en un punto $(a, b)$ si el incremento total $\Delta z = f(a + \Delta x, b + \Delta y) - f(a, b)$ puede expresarse de la siguiente forma:

$$\Delta z = f_x(a, b) \Delta x + f_y(a, b) \Delta y + \epsilon_1 \Delta x + \epsilon_2 \Delta y$$

Donde los errores $\epsilon_1$ y $\epsilon_2$ deben tender a cero cuando $(\Delta x, \Delta y) \to (0, 0)$.

### Condiciones de Diferenciabilidad

Para que un campo sea diferenciable, se suelen verificar estos criterios:

1. **Condición Necesaria:** Si $f$ es diferenciable en $(a, b)$, entonces es **continua** en ese punto y existen sus derivadas parciales $f_x$ y $f_y$.
    
2. **Condición Suficiente:** Si las derivadas parciales $f_x$ y $f_y$ existen en una vecindad del punto $(a, b)$ y son **continuas** en $(a, b)$, entonces la función es diferenciable en ese punto.
    

### ¿En qué cambia esto tu análisis?

Si una función es diferenciable, tenés la seguridad de que:

- Existe un **plano tangente** único en ese punto.
    
- La superficie es "suave" (no tiene picos ni saltos).
    
- La aproximación lineal mediante el diferencial es válida.

# 6. **¿Qué es un extremo relativo o local? ¿Cómo se define un máximo y un mínimo? ¿Qué significa geométricamente la condición necesaria para la existencia de un punto crítico de una función dada en $R^2$?**
## 1. ¿Qué es un extremo relativo o local?

Un **extremo relativo** es un punto en el dominio de la función donde el valor de $z$ es mayor (o menor) que en todos los puntos que están "cerca" de él. No necesariamente es el punto más alto de toda la montaña, pero sí es el punto más alto de su entorno inmediato.

### Definición de Máximo y Mínimo Relativo

Sea una función $f(x, y)$ definida en una región que contiene al punto $(a, b)$:

- **Máximo Local:** Se dice que $f$ tiene un máximo local en $(a, b)$ si existe un disco centrado en dicho punto tal que:
    
    $$f(a, b) \geq f(x, y)$$
    
    para todo $(x, y)$ dentro de ese disco.
    
- **Mínimo Local:** Se dice que $f$ tiene un mínimo local en $(a, b)$ si existe un disco centrado en dicho punto tal que:
    
    $$f(a, b) \leq f(x, y)$$
    
    para todo $(x, y)$ dentro de ese disco.
    

---

## 2. Condición Necesaria para la existencia de un Punto Crítico

Para que una función diferenciable tenga un extremo local en un punto $(a, b)$, es **necesario** (pero no suficiente) que las derivadas parciales de primer orden sean nulas en ese punto:

$$\frac{\partial f}{\partial x}(a, b) = 0 \quad \text{y} \quad \frac{\partial f}{\partial y}(a, b) = 0$$

A los puntos que cumplen esto se los llama **puntos críticos**.

> [!WARNING]
> 
> Que sea un punto crítico no garantiza un extremo. También podría ser un **Punto Silla** (donde sube en una dirección y baja en otra, como una silla de montar).

---

## 3. Significado Geométrico de la Condición

Geométricamente, esta condición significa que en el punto crítico, el **plano tangente a la superficie es horizontal** (paralelo al plano $xy$).

### ¿Por qué sucede esto?

1. Si $\frac{\partial f}{\partial x} = 0$, la recta tangente en dirección $x$ es horizontal.
    
2. Si $\frac{\partial f}{\partial y} = 0$, la recta tangente en dirección $y$ es horizontal.
    
3. Al ser ambas horizontales, el plano que contienen (el plano tangente) no tiene inclinación.
    

Pensalo como una pelota apoyada justo en la cima de una colina o en el fondo de un cuenco: en ese instante exacto, si apoyaras una tabla sobre la pelota, la tabla quedaría perfectamente nivelada.

---

### Resumen para tu final 

> [!IMPORTANT] Esquema de Optimización
> 
> 1. **Punto Crítico:** Candidato a extremo (Gradiente = 0).
>     
> 2. **Significado:** Plano tangente horizontal.
>     
> 3. **Clasificación:** Necesitás el **Hessiano** (derivadas segundas) para saber si es máximo, mínimo o punto silla.
>

# 7. **¿Cuál es la condición suficiente (Hessiano) para la existencia de extremos relativos?** 

Que las derivadas parciales mixtas sean iguales, por el Teorema de Clairaut

Una vez que has identificado los **puntos críticos** (donde las derivadas parciales de primer orden son cero), la **condición suficiente** nos permite clasificar si esos puntos son máximos, mínimos o puntos silla. Esta condición utiliza las derivadas parciales de segundo orden organizadas en la **Matriz Hessiana**.

---

## 1. La Matriz Hessiana y el Discriminante

Para una función $f(x, y)$ con segundas derivadas parciales continuas, la matriz Hessiana $H$ en un punto crítico $(a, b)$ es:

$$H(a, b) = \begin{pmatrix} f_{xx}(a, b) & f_{xy}(a, b) \\ f_{yx}(a, b) & f_{yy}(a, b) \end{pmatrix}$$

El **determinante de la Hessiana** (también llamado discriminante $D$) se calcula como:

$$D = f_{xx}(a, b) \cdot f_{yy}(a, b) - [f_{xy}(a, b)]^2$$

---

## 2. El Criterio de la Segunda Derivada

Dependiendo del valor de $D$ y del signo de $f_{xx}$ (o $f_{yy}$), clasificamos el punto crítico $(a, b)$ de la siguiente manera:

### Caso 1: Máximo Local

- **Condición:** $D > 0$ y $f_{xx}(a, b) < 0$.
    
- **Explicación:** El determinante positivo indica que la superficie tiene la misma curvatura en todas las direcciones, y $f_{xx} < 0$ indica que es cóncava hacia abajo (un "pico").
    

### Caso 2: Mínimo Local

- **Condición:** $D > 0$ y $f_{xx}(a, b) > 0$.
    
- **Explicación:** El determinante positivo indica curvatura uniforme, y $f_{xx} > 0$ indica que es cóncava hacia arriba (un "valle").
    

### Caso 3: Punto Silla (Saddle Point)

- **Condición:** $D < 0$.
    
- **Explicación:** La superficie sube en una dirección y baja en otra. No es ni máximo ni mínimo. El valor de $f_{xx}$ no importa en este caso.
    

### Caso 4: Prueba Inconclusiva

- **Condición:** $D = 0$.
    
- **Explicación:** El test no aporta información. El punto podría ser un máximo, un mínimo o un punto silla. Se requiere un análisis de orden superior (Taylor) o estudiar el comportamiento de la función cerca del punto.
    

---

## 3. Resumen para Obsidian

> [!ABSTRACT] Criterio del Hessiano
> 
> Sea $(a, b)$ un punto crítico tal que $\nabla f(a, b) = \vec{0}$:
> 
> 1. **$D > 0$ y $f_{xx} > 0$** $\implies$ **Mínimo relativo**.
>     
> 2. **$D > 0$ y $f_{xx} < 0$** $\implies$ **Máximo relativo**.
>     
> 3. **$D < 0$** $\implies$ **Punto silla**.
>     
> 4. **$D = 0$** $\implies$ **No se sabe nada**.
>

# 8. **Explique el método de los multiplicadores de Lagrange para resolver problemas de Máximos / Mínimos sujetos a restricciones.** 
El método de los **Multiplicadores de Lagrange** es la herramienta estándar para encontrar los extremos (máximos y mínimos) de una función cuando no podés moverte libremente por todo el dominio, sino que estás obligado a permanecer sobre una curva o superficie específica (la **restricción**).

---

## 1. El Problema: Optimización con Restricciones

Supongamos que queremos maximizar o minimizar una función objetivo $f(x, y)$ sujeta a una restricción de la forma $g(x, y) = k$.

- **$f(x, y)$**: Lo que querés optimizar (ej: el volumen de una caja).
    
- **$g(x, y) = k$**: El límite que tenés que respetar (ej: la cantidad de material disponible).
    

---

## 2. La Intuición Geométrica

En un punto extremo bajo una restricción, las curvas de nivel de la función $f$ son **tangentes** a la curva de la restricción $g$.

Si las curvas son tangentes, sus vectores normales (los **gradientes**) deben ser paralelos. Matemáticamente, esto significa que el gradiente de $f$ debe ser un múltiplo escalar del gradiente de $g$.

---

## 3. El Método Paso a Paso

Para resolver estos problemas, introducimos una variable adicional llamada **$\lambda$ (Lambda)**, que es el Multiplicador de Lagrange.

### Paso 1: Formar la Función de Lagrange

Se define una nueva función $L$:

$$L(x, y, \lambda) = f(x, y) - \lambda [g(x, y) - k]$$

### Paso 2: Plantear el Sistema de Ecuaciones

Buscamos los puntos donde las derivadas parciales de $L$ sean cero. Esto genera un sistema de 3 ecuaciones con 3 incógnitas ($x, y, \lambda$):

1. $\frac{\partial L}{\partial x} = 0 \implies f_x = \lambda g_x$
    
2. $\frac{\partial L}{\partial y} = 0 \implies f_y = \lambda g_y$
    
3. $\frac{\partial L}{\partial \lambda} = 0 \implies g(x, y) = k$ (la restricción original)
    

### Paso 3: Resolver y Comparar

Una vez que encontrás los puntos críticos $(x, y)$ resolviendo el sistema:

1. Evaluás la función original $f(x, y)$ en cada punto hallado.
    
2. El valor más grande será el **máximo sujeto a la restricción**.
    
3. El valor más chico será el **mínimo sujeto a la restricción**.
    

---

## 4. Resumen 

> [!TIP] ¿Cuándo usar Lagrange?
> 
> Usalo siempre que el enunciado diga frases como:
> 
> - "Sujeto a..."
>     
> - "Con la condición de que..."
>     
> - "Sobre la curva / superficie..."
>     
> - "De todos los [objetos] que cumplen [condición], hallar el de mayor/menor..."
>     

### Significado de $\lambda$

En términos económicos o físicos, $\lambda$ representa la **tasa de cambio** del valor óptimo de la función respecto a los cambios en el valor de la restricción $k$. Se le suele llamar "precio sombra".

## Ejemplo: El Rectángulo de Área Máxima

Queremos encontrar las dimensiones ($x$ e $y$) de un rectángulo que tenga el **área máxima**, dado que su **perímetro** debe ser exactamente $P$ (una constante).

### 1. Definir las funciones

- **Función Objetivo (lo que queremos maximizar):** El área $f(x, y) = x \cdot y$.
    
- **Función de Restricción:** El perímetro $g(x, y) = 2x + 2y = P$.
    

### 2. Plantear la Ecuación de Lagrange

Siguiendo el método, igualamos los gradientes $\nabla f = \lambda \nabla g$:

1. **Derivada respecto a $x$:** $\frac{\partial f}{\partial x} = \lambda \frac{\partial g}{\partial x}$
    
2. **Derivada respecto a $y$:** $\frac{\partial f}{\partial y} = \lambda \frac{\partial g}{\partial y}$
    
3. **Restricción:** $g(x, y) = P$
    

### 3. Calcular las derivadas parciales

Usando las reglas de derivación que vimos para campos escalares:

- $f_x = y$
    
- $f_y = x$
    
- $g_x = 2$
    
- $g_y = 2$
    

### 4. Resolver el sistema de ecuaciones

Sustituimos en las fórmulas de Lagrange:

1. $y = \lambda \cdot 2 \implies \lambda = \frac{y}{2}$
    
2. $x = \lambda \cdot 2 \implies \lambda = \frac{x}{2}$
    
3. $2x + 2y = P$
    

Igualamos las dos expresiones de $\lambda$:

$$\frac{y}{2} = \frac{x}{2} \implies \mathbf{y = x}$$

### 5. Hallar las dimensiones finales

Sustituimos $y = x$ en la ecuación del perímetro (la restricción):

$$2x + 2(x) = P$$

$$4x = P \implies \mathbf{x = \frac{P}{4}}$$

Como $y = x$, entonces $\mathbf{y = \frac{P}{4}}$.

---

### Conclusión Geométrica

El método de Lagrange nos demuestra matemáticamente que, de todos los rectángulos con un perímetro determinado, **el que encierra el área más grande es el cuadrado** ($x = y$).

> [!CHECK] ¿Por qué es útil esto para el final?
> 
> Este procedimiento de "igualar las lambdas" para encontrar una relación entre $x$ e $y$ (en este caso $y=x$) es el truco más común para resolver sistemas de Lagrange rápidamente sin volverse loco con el álgebra.


# 9. **Pregunta de Conexión: ¿Cuál es la jerarquía de implicación entre continuidad, derivabilidad y diferenciabilidad?** 

   Si es diferenciable es continua y derivable, pero que sea continua no necesariamente implica que sea derivable
### 1. La Implicación Principal (La "Reina")

Si una función es **diferenciable** en un punto $(a, b)$, entonces se cumplen automáticamente estas dos cosas:

- **Es Continua** en $(a, b)$.
- **Es Derivable** en $(a, b)$ (es decir, existen sus derivadas parciales $\frac{\partial f}{\partial x}$ y $\frac{\partial f}{\partial y}$).

> **Diferenciabilidad $\implies$ Continuidad + Existencia de Derivadas Parciales**

### 2. Las Implicaciones que NO funcionan (Las "Trampas")

A diferencia del cálculo en $\mathbb{R}$, en $\mathbb{R}^2$ las piezas no encajan tan fácil:

- **Derivabilidad $\not\implies$ Continuidad:** Una función puede tener derivadas parciales en un punto y ser discontinua ahí mismo (algo que no pasa en una variable).
- **Derivabilidad $\not\implies$ Diferenciabilidad:** El hecho de que existan las derivadas parciales no garantiza que la función sea diferenciable ni que exista un plano tangente.
- **Continuidad $\not\implies$ Diferenciabilidad:** Al igual que en una variable, una función puede ser continua pero tener un "pico" o "punta", lo que impide que sea diferenciable.

---

### 3. El "Puente" (Condición Suficiente)

Para que las derivadas parciales logren "comprar" la diferenciabilidad, necesitan un requisito extra: la **continuidad**.

- Si las derivadas parciales existen y además **son continuas** en una vecindad del punto, entonces la función es **diferenciable**.

> **Derivadas Parciales Continuas $\implies$ Diferenciabilidad $\implies$ Continuidad**

---

### Tabla Resumen de Jerarquía

|**Si la función es...**|**¿Es Continua?**|**¿Existen las Parciales?**|**¿Es Diferenciable?**|
|---|---|---|---|
|**Diferenciable**|**SÍ**|**SÍ**|**SÍ**|
|**Derivable (existen $f_x, f_y$)**|No necesariamente|**SÍ**|No necesariamente|
|**Continua**|**SÍ**|No necesariamente|No necesariamente|

La **Diferenciabilidad** es una condición mucho más fuerte que la simple existencia de derivadas. Es la que te asegura que la superficie es "suave" y que el diferencial total $dz$ realmente se comporta como una aproximación lineal de la función
# 10. **Aproximacion lineal. Desarrollo de Taylor**

Este punto de tu programa es la continuación natural de lo que vimos sobre diferenciales. Si el diferencial total te daba una aproximación del **cambio** ($\Delta z \approx dz$), la **Aproximación Lineal** y el **Desarrollo de Taylor** te dan la **función aproximada** completa.

Aquí tenés el desglose para que lo rompas en el final:

---

## 1. Aproximación Lineal (Polinomio de Taylor de Grado 1)

La aproximación lineal de una función $f(x, y)$ en un punto $(a, b)$ es simplemente la ecuación del **plano tangente** en ese punto. Se denota como $L(x, y)$.

### La Fórmula:

$$L(x, y) = f(a, b) + f_x(a, b)(x - a) + f_y(a, b)(y - b)$$

Donde:

- $f(a, b)$ es el valor de la función en el punto inicial.
    
- $f_x(a, b)$ y $f_y(a, b)$ son las derivadas parciales evaluadas en el punto.
    
- $(x - a)$ y $(y - b)$ son los desplazamientos $dx$ y $dy$.
    

**Interpretación:** Estamos diciendo que, cerca de $(a, b)$, la superficie curva de la función se parece mucho a un plano. Es la "linealización" de la función.

---

## 2. Desarrollo de Taylor (Generalización)

Cuando la aproximación lineal (plano) no es suficiente porque la función es muy "curva", usamos el **Polinomio de Taylor**. Este agrega términos de potencias superiores (cuadráticos, cúbicos, etc.) para que la aproximación sea más precisa.

### Polinomio de Taylor de Segundo Grado ($P_2$)

Es el más común en los exámenes de Calculus 2. Agrega la curvatura a la aproximación:

$$P_2(x,y) = \underbrace{f(a,b) + f_x(a,b)\Delta x + f_y(a,b)\Delta y}_{\text{Aproximación Lineal}} + \underbrace{\frac{1}{2!} [f_{xx}(a,b)\Delta x^2 + 2f_{xy}(a,b)\Delta x \Delta y + f_{yy}(a,b)\Delta y^2]}_{\text{Términos Cuadráticos}}$$

- Aquí, $\Delta x = (x - a)$ y $\Delta y = (y - b)$.
    
- $f_{xx}, f_{xy}, f_{yy}$ son las **derivadas parciales de segundo orden**.
    

---

## 3. Comparativa: ¿En qué se diferencian?

|**Concepto**|**Representación Geométrica**|**¿Para qué sirve?**|
|---|---|---|
|**Diferencial ($dz$)**|Un cambio de altura sobre el plano tangente.|Calcular errores o variaciones pequeñas.|
|**Aprox. Lineal ($L$)**|El **Plano Tangente** mismo.|Sustituir una función difícil por una lineal cerca de un punto.|
|**Desarrollo Taylor**|Una **Superficie Tangente** (paraboloide si es grado 2).|Obtener una precisión mucho mayor en regiones más amplias.|

---

## 4. El Resto de Taylor (Error)

Toda aproximación tiene un error. El desarrollo completo de Taylor incluye un término llamado **Resto o Residuo** ($R_n$):

$$f(x, y) = P_n(x, y) + R_n(x, y)$$

Para que una función sea **diferenciable** en un punto, el resto debe tender a cero más rápido de lo que los incrementos tienden a cero.

> [!IMPORTANT]
> 
> En el examen, si te piden "linealizar" la función, solo llegá hasta las primeras derivadas ($L$). Si te piden "Taylor de orden 2", vas a tener que calcular las 5 derivadas parciales necesarias ($f_x, f_y, f_{xx}, f_{yy}, f_{xy}$).

# 11. **Aproximación lineal de diferenciales (conceptual)**