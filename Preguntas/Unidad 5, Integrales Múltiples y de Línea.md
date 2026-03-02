 **Unidad 5: Integrales Múltiples y de Línea**

# 1. **¿Qué significación básica ofrece el cálculo de integrales dobles tanto a nivel geométrico como físico? Y las integrales triples? Ejemplificar. Aplicaciones físicas de las integrales dobles y triples.** Centro de masa. Momento de inercia. Integrales de superficie (área). Densidad.  
## 1. Integrales Dobles ($\iint$)

Geométricamente, la integral doble representa el **volumen** de un sólido limitado superiormente por la superficie $z = f(x, y)$ e inferiormente por una región $D$ en el plano $xy$.

- **Caso Especial:** Si la función $f(x, y) = 1$, el resultado de la integral es simplemente el **área** de la región $D$ sobre la cual estás integrando.
    
- **Significación Física:** Si interpretamos $f(x, y)$ como la **densidad ($\sigma$)** de una placa delgada (lámina), la integral doble representa la **masa total** de esa placa.
    
- **Ejemplo:** Imagina calcular la cantidad de nieve acumulada en un patio circular. El patio es la región $D$ y la altura de la nieve en cada punto es $f(x, y)$. El volumen total de nieve es la integral doble.
    

---

## 2. Integrales Triples ($\iiint$)

Las integrales triples extienden este concepto a una región sólida $E$ en el espacio tridimensional.

- **Significación Geométrica:** Si la función que integrás es $f(x, y, z) = 1$, la integral triple representa el **volumen** del sólido $E$. Si la función es distinta de 1, representa un "hipervolumen" en 4D, que es difícil de visualizar pero muy útil en física.
    
- **Significación Física:** Si $f(x, y, z)$ es la **densidad ($\rho$)** de un objeto sólido en cada punto, la integral triple nos da la **masa total** del objeto.
    
- **Ejemplo:** Calcular la masa de una roca cuya densidad aumenta hacia el centro debido a la presión. La roca es el sólido $E$ y la función densidad varía en las tres dimensiones.
    

---

## 3. Aplicaciones Físicas y Fórmulas Clave

Para estas aplicaciones, recordamos que trabajamos sobre regiones definidas en el plano o el espacio.

- **Masa y Densidad:** La masa es la integral de la densidad sobre la región. $M = \iint_D \sigma(x, y) dA$ para láminas o $M = \iiint_E \rho(x, y, z) dV$ para sólidos.
    
- **Momentos de Primer Orden:** Se usan para encontrar el equilibrio. El momento respecto al eje $x$ es $M_x = \iint_D y \sigma(x, y) dA$.
    
- **Centro de Masa $(\bar{x}, \bar{y})$:** Es el punto donde el objeto se equilibraría perfectamente. Se calcula dividiendo los momentos por la masa total: $\bar{x} = \frac{M_y}{M}$ y $\bar{y} = \frac{M_x}{M}$.
    
- **Momento de Inercia ($I$):** Representa la resistencia de un objeto a rotar. Se calcula integrando el cuadrado de la distancia al eje de rotación: $I_x = \iint_D y^2 \sigma(x, y) dA$.
    
- **Integrales de Superficie (Área):** Se usan para calcular el área de una superficie curva (como la cáscara de una naranja). Si la superficie es $z = g(x, y)$, el área es $A = \iint_D \sqrt{1 + (g_x)^2 + (g_y)^2} dA$.
    

---

### Resumen para Obsidian

> [!INFO] Aplicaciones de Integrales Múltiples
> 
> - **$\iint 1 dA$**: Área de una región plana.
>     
> - **$\iint f dA$**: Volumen bajo una superficie o Masa de una lámina.
>     
> - **$\iiint 1 dV$**: Volumen de un sólido 3D.
>     
> - **$\iiint \rho dV$**: Masa de un sólido con densidad variable.

## Ejemplo Centro de Masa
### Problema: Centro de Masa de un Semicírculo

Dada la región $D$ definida por $x^2 + y^2 \leq a^2$ con $y \geq 0$, y una densidad constante $k$.

### Paso 1: Calcular la Masa Total ($M$)

Como la densidad es constante, la masa es simplemente la densidad por el área de la región.

- El área de un círculo completo es $\pi a^2$, por lo que el área del semicírculo es $\frac{1}{2}\pi a^2$.
    
- $M = \iint_D k \, dA = k \cdot \text{Área} = \frac{k \pi a^2}{2}$.
    

### Paso 2: Análisis de Simetría ($\bar{x}$)

- La figura es simétrica respecto al eje $y$.
    
- La densidad es uniforme.
    
- Por lo tanto, el centro de masa debe estar sobre el eje $y$.
    
- $\mathbf{\bar{x} = 0}$.
    

### Paso 3: Calcular el Momento respecto al eje $x$ ($M_x$)

Usamos la fórmula $M_x = \iint_D y \sigma(x, y) \, dA$. Para facilitar el cálculo, pasamos a **coordenadas polares** ($y = r \operatorname{sen} \theta$) e incluimos el Jacobiano $r$:

- Límites: $0 \leq r \leq a$ y $0 \leq \theta \leq \pi$.
    
- $M_x = \int_{0}^{\pi} \int_{0}^{a} (r \operatorname{sen} \theta) \cdot k \cdot r \, dr \, d\theta$
    
- $M_x = k \int_{0}^{\pi} \operatorname{sen} \theta \, d\theta \int_{0}^{a} r^2 \, dr$
    
- Integral angular: $\int_{0}^{\pi} \operatorname{sen} \theta \, d\theta = [-\cos \theta]_{0}^{\pi} = -(-1) - (-1) = 2$.
    
- Integral radial: $\int_{0}^{a} r^2 \, dr = \frac{a^3}{3}$.
    
- Resultado: $M_x = k \cdot 2 \cdot \frac{a^3}{3} = \frac{2 k a^3}{3}$.
    

### Paso 4: Hallar la coordenada $\bar{y}$

Dividimos el momento por la masa total:

- $\bar{y} = \frac{M_x}{M} = \frac{\frac{2 k a^3}{3}}{\frac{k \pi a^2}{2}}$
    
- Simplificando: $\bar{y} = \frac{2 a^3}{3} \cdot \frac{2}{\pi a^2} = \mathbf{\frac{4a}{3\pi}}$
    

---

### Resultado Final

El centro de masa se encuentra en el punto:

$$(0, \frac{4a}{3\pi})$$

> [!NOTE]
> 
> Curiosamente, el centro de masa de un semicírculo no depende de su densidad (siempre que sea constante), solo depende de su radio $a$. El valor $\frac{4a}{3\pi}$ es aproximadamente $0.424a$, es decir, está un poco más abajo de la mitad del radio.

# 2. **Cambios de variables a coordenadas polares. Utilidad del cambio de variables y qué representa el Jacobiano.** 
## 1. Cambio de Variables a Coordenadas Polares

En el plano $\mathbb{R}^2$, pasamos de las coordenadas rectangulares $(x, y)$ a las polares $(r, \theta)$ mediante las siguientes ecuaciones de transformación:

- **$x = r \cos \theta$**: Define la componente horizontal en función del radio y el ángulo.
    
- **$y = r \sin \theta$**: Define la componente vertical.
    
- **$x^2 + y^2 = r^2$**: Es la identidad fundamental que simplifica muchísimas integrales.
    
- **$\theta = \arctan(y/x)$**: Permite hallar el ángulo de barrido.
    

---

## 2. Utilidad del Cambio de Variables

¿Por qué nos tomamos el trabajo de cambiar las coordenadas?

- **Simplificación de Regiones:** Regiones que en cartesianas son horribles (como círculos, anillos o sectores de torta), en polares se describen con límites constantes (ej: $0 \leq r \leq 1, 0 \leq \theta \leq 2\pi$).
    
- **Simplificación del Integrando:** Funciones que contienen la expresión $x^2 + y^2$ se reducen simplemente a $r^2$, eliminando raíces cuadradas y potencias complicadas.
    
- **Integración en Regiones $R$:** Al igual que en las ecuaciones exactas trabajamos sobre regiones rectangulares $R$ del plano $xy$, el cambio de variables busca transformar una región curva compleja en una región rectangular en el plano $(r, \theta)$.
    

---

## 3. El Jacobiano: ¿Qué representa?

Cuando cambiamos de variables, no podemos simplemente reemplazar $dx \, dy$ por $dr \, d\theta$. Necesitamos un "factor de corrección" llamado **Jacobiano**.

### Definición y Cálculo

Para el cambio a polares, el Jacobiano $J$ es el determinante de la matriz de derivadas parciales:

$$J = \begin{vmatrix} \frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} \\ \frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta} \end{vmatrix} = \begin{vmatrix} \cos \theta & -r \sin \theta \\ \sin \theta & r \cos \theta \end{vmatrix} = r(\cos^2 \theta + \sin^2 \theta) = \mathbf{r}$$

### ¿Qué representa geométricamente?

- **Factor de Escala de Área:** Representa cuánto se "estira" o "encoge" un diferencial de área al pasar de un sistema a otro.
    
- **Elemento de Área:** En polares, el diferencial de área es $dA = r \, dr \, d\theta$. La $r$ extra compensa el hecho de que, para un mismo ángulo $d\theta$, el arco es más largo cuanto más lejos estás del origen.
    
- **Transformación Local:** Al igual que el diferencial total $dz$ nos daba una aproximación lineal local de la función, el Jacobiano nos da una aproximación lineal local de cómo se transforma el área en ese punto.
    

---

### Resumen 

> [!IMPORTANT] Regla de Oro
> 
> Nunca te olvides de la **$r$** al pasar a polares:
> 
> $$\iint_R f(x, y) \, dx \, dy = \iint_{R^*} f(r \cos \theta, r \sin \theta) \cdot \mathbf{r} \, dr \, d\theta$$
# 3. **Defina integral de línea para el caso de un campo vectorial $F: R^2 → R^2$**  
## Definición Matemática

Sea $\vec{F}: \mathbb{R}^2 \to \mathbb{R}^2$ un campo vectorial continuo definido por $\vec{F}(x, y) = P(x, y)\hat{i} + Q(x, y)\hat{j}$, y sea $C$ una curva suave orientada parametrizada por $\vec{r}(t) = x(t)\hat{i} + y(t)\hat{j}$ para $a \leq t \leq b$. La **integral de línea de $\vec{F}$ a lo largo de $C$** se define como:

$$\int_C \vec{F} \cdot d\vec{r} = \int_a^b \vec{F}(\vec{r}(t)) \cdot \vec{r}'(t) \, dt$$

Donde:

- **$\vec{F}(\vec{r}(t))$** es el campo vectorial evaluado en los puntos de la curva.
    
- **$\vec{r}'(t)$** es el vector tangente a la curva en cada punto (la velocidad de la partícula).
    
- **$\cdot$** representa el producto escalar, que mide cuánto del campo "empuja" en la dirección del movimiento.
    

---

## Formas de Escritura y Relación con Diferenciales

Es muy común ver esta integral escrita en su **forma diferencial**, que se conecta directamente con lo que vimos de ecuaciones exactas:

- **Forma Diferencial:** $\int_C P(x, y) \, dx + Q(x, y) \, dy$.
    
- **Vínculo Teórico:** Si el campo es conservativo, esta expresión es el diferencial total de una función potencial $f(x, y)$.
    
- **Notación de Trabajo:** Físicamente, esta integral representa el trabajo ($W$) realizado por una fuerza $\vec{F}$ al mover un objeto sobre la trayectoria $C$.
    

---

## Interpretación Geométrica y Física

- **Producto Escalar:** En cada punto de la curva, proyectamos el vector del campo sobre el vector tangente. Si el campo es perpendicular a la trayectoria, el aporte es cero.
    
- **Independencia de la Trayectoria:** Si el campo cumple que $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$, entonces la integral solo depende de los puntos extremos y no del camino elegido.
    
- **Sentido de Integración:** A diferencia de las integrales de línea de campos escalares, aquí el signo de la integral cambia si recorremos la curva en sentido opuesto.
# 4. **Describa las aplicaciones de la integral de línea y los teoremas de integración.**  
 ## 1. Aplicaciones de la Integral de Línea

La integral de línea nos permite integrar funciones a lo largo de una curva $C$ en lugar de sobre un intervalo o región plana.

- **Trabajo de una Fuerza:** Es la aplicación estrella. Si una fuerza $\vec{F}$ mueve una partícula a lo largo de una trayectoria $C$, el trabajo realizado es $W = \int_C \vec{F} \cdot d\vec{r}$.
    
- **Masa de un Alambre:** Si tenés un alambre cuya densidad lineal varía según $\rho(x, y)$, la masa total es $M = \int_C \rho(x, y) \, ds$.
    
- **Flujo y Circulación:** En mecánica de fluidos, se usa para medir cuánto fluido atraviesa una curva o cuánto "rota" el fluido a lo largo de un camino cerrado.
    

---

## 2. Teoremas de Integración (Los 4 Pilares)

Estos teoremas son herramientas para simplificar cálculos horribles, convirtiendo integrales difíciles en otras más fáciles.

### A. Teorema Fundamental para Integrales de Línea

Dice que si el campo es **conservativo** (es decir, proviene de un gradiente $\nabla f$), la integral solo depende de los puntos finales.

- **Relación Teórica:** Un campo es conservativo si cumple el criterio de exactitud que vimos antes: $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$.
    
- **Fórmula:** $\int_C \nabla f \cdot d\vec{r} = f(\text{Final}) - f(\text{Inicio})$.
    

### B. Teorema de Green

Conecta una integral de línea alrededor de una curva cerrada $C$ con una integral doble sobre la región $D$ que encierra.

- **Utilidad:** Muy útil para calcular áreas o cuando la integral de línea es muy compleja.
- **Fórmula:** $\oint_C (P \, dx + Q \, dy) = \iint_D (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) \, dA$.

### C. Teorema de Stokes

Es la versión 3D del Teorema de Green. Relaciona la circulación de un campo vectorial alrededor del borde de una superficie con el flujo del **rotor** de ese campo a través de la superficie.

- **Fórmula:** $\oint_{\partial S} \vec{F} \cdot d\vec{r} = \iint_S (\text{rot } \vec{F}) \cdot d\vec{S}$.

### D. Teorema de la Divergencia (Gauss)

Relaciona el flujo de un campo vectorial a través de una superficie cerrada con la integral de la **divergencia** del campo sobre el volumen encerrado.

- **Aplicación:** Fundamental en electromagnetismo y termodinámica para entender cómo se expande o contrae un fluido.
- **Fórmula:** $\iint_{\partial V} \vec{F} \cdot d\vec{S} = \iiint_V (\text{div } \vec{F}) \, dV$.

---

> [!TIP] Estrategia de Examen
> 
> Si te piden una integral de línea sobre una curva **cerrada**, lo primero que tenés que pensar es en aplicar **Green** (si es en $\mathbb{R}^2$) o **Stokes** (si es en $\mathbb{R}^3$). Casi siempre simplifica la vida.
# 6. **Teorema fundamental de las integrales de línea.**  
- El teorema fundamental de las integrales de linea establece que si el campo vectorial F es conservativo, entonces la integral de linea entre dos puntos cualesquiera es simplemente la diferencia de los valores de la funcion potencial evaluados en ambos puntos
## 1. Definición del Teorema

Sea $C$ una curva suave parametrizada por $\vec{r}(t)$ con $a \leq t \leq b$. Si $\vec{F}$ es un **campo vectorial conservativo** (es decir, existe una función potencial $f$ tal que $\vec{F} = \nabla f$), entonces:

$$\int_C \vec{F} \cdot d\vec{r} = \int_C \nabla f \cdot d\vec{r} = f(\vec{r}(b)) - f(\vec{r}(a))$$

En palabras simples: la integral de línea de un campo conservativo es igual a la diferencia de los valores de su función potencial en los puntos final e inicial de la trayectoria.

---

## 2. Consecuencias Clave (Ideales para el Final)

- **Independencia de la Trayectoria**: El valor de la integral no depende del camino que elijas para ir de A a B, solo de dónde empezás y dónde terminás.
    
- **Trayectorias Cerradas**: Si la curva $C$ es cerrada (empieza y termina en el mismo lugar), la integral de línea es **siempre cero**.
    
- **Conservación de Energía**: En física, esto explica por qué el trabajo realizado por una fuerza conservativa (como la gravedad) en un camino cerrado es nulo.
    

---

## 3. Cómo saber si podés usar este teorema

Para aplicar este "atajo", primero tenés que demostrar que el campo es conservativo. Aquí es donde entra lo que ya venías estudiando:

- **Criterio de Exactitud**: Un campo $\vec{F} = P \hat{i} + Q \hat{j}$ es conservativo si cumple la condición de que sus derivadas parciales cruzadas sean iguales.
- **Verificación**: Debés comprobar que $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$, que es el mismo criterio que usás para identificar una **ecuación diferencial exacta**.
- **Función Potencial**: Si se cumple la igualdad, podés integrar $P$ respecto a $x$ (o $Q$ respecto a $y$) para reconstruir la función $f(x, y)$, tal como vimos en el proceso de resolución de exactas.

## Resumen

> [!IMPORTANT] Teorema Fundamental
> 
> - **Requisito**: El campo debe ser conservativo ($\nabla \times \vec{F} = 0$).
>     
> - **Ventaja**: Te evitás parametrizar la curva y hacer el producto escalar complejo.
>     
> - **Cálculo**: Solo hallás la función "madre" $f$ y restás: $f(\text{Final}) - f(\text{Inicio})$.
>

### como hallas la funcion potencial?
Hallar la función "madre" (técnicamente llamada **función potencial**) es el proceso de reconstruir la función original $f(x, y)$ a partir de sus derivadas parciales. Es exactamente el mismo procedimiento que usamos para resolver las **Ecuaciones Diferenciales Exactas**.
#### Procedimiento de Reconstrucción

Si tenés un campo $\vec{F} = \langle M, N \rangle$ que ya verificaste que es conservativo (donde $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$), hacés lo siguiente:

- **Paso 1: Plantear las derivadas parciales.** Sabés que $f_x = M$ y que $f_y = N$.
- **Paso 2: Integrar la primera componente.** Integrás $M$ con respecto a $x$. Esto te da la función casi completa, pero con una "constante" que puede depender de $y$: $f(x, y) = \int M \, dx + g(y)$.
- **Paso 3: Derivar respecto a la otra variable.** Derivás el resultado del paso anterior con respecto a $y$. Te va a quedar algo como: $f_y = \frac{\partial}{\partial y} [\int M \, dx] + g'(y)$.
- **Paso 4: Igualar y simplificar.** Igualás este resultado a $N$ (porque sabés que $f_y = N$). En este punto, todos los términos que tengan $x$ deberían cancelarse mágicamente, dejándote solo una expresión para $g'(y)$.
- **Paso 5: Hallar la constante final.** Integrás $g'(y)$ con respecto a $y$ para obtener $g(y)$. Ahora solo reemplazás esa $g(y)$ en la función del Paso 2 y ya tenés tu función potencial $f(x, y)$.
    

---

#### Ejemplo rápido con tus apuntes

Si tu campo fuera $\vec{F} = \langle x^2y^3, x^3y^2 \rangle$ (como en el ejemplo de la captura):
- Integrás $x^2y^3$ respecto a $x$: te queda $\frac{1}{3}x^3y^3 + g(y)$.
- Derivás respecto a $y$: te queda $x^3y^2 + g'(y)$.
- Igualás a $N$ ($x^3y^2$): ves que $g'(y) = 0$, por lo que $g(y) = C$.
- La función "madre" es $f(x, y) = \frac{1}{3}x^3y^3 + C$.
# 6. **Condiciones para la independencia del camino de una integral de línea: enunciado y demostración.**  
- Las condiciones para la “independencia del camino”, es decir que no dependa del recorrido que hace la partícula, es que el campo vectorial sea conservativo (o tambien llamado campo gradiente). Para que esto ocurra deben cumplirse dos condiciones:  
* la irrotacionalidad: el rotacional del campo debe ser nulo   
* dominio simplemente conexo: el dominio del campo no debe tener “huecos”  
## 1. Enunciado del Teorema

Sea $\vec{F}(x, y) = P(x, y)\hat{i} + Q(x, y)\hat{j}$ un campo vectorial continuo en una región abierta y conexa $D$. La integral de línea $\int_C \vec{F} \cdot d\vec{r}$ es **independiente del camino** en $D$ si y solo si $\vec{F}$ es un **campo vectorial conservativo**; es decir, existe una función potencial $f$ tal que $\nabla f = \vec{F}$.

### Condiciones Equivalentes

- Existe una función escalar $f$ tal que $\vec{F} = \nabla f$ (donde $P = f_x$ y $Q = f_y$).
    
- La integral de línea alrededor de cualquier curva cerrada $C$ en $D$ es cero ($\oint_C \vec{F} \cdot d\vec{r} = 0$).
    
- En una región simplemente conexa, se cumple que $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$.
    

---

## 2. Demostración (Sentido: Conservativo $\implies$ Independiente)

Esta es la parte que suelen pedir en el examen oral o escrito. Queremos demostrar que si existe $f$, entonces la integral no depende de la curva.

**Paso 1: Parametrización**

Sea $C$ una curva suave cualquiera desde $A(x_1, y_1)$ hasta $B(x_2, y_2)$ definida por $\vec{r}(t)$ con $t \in [a, b]$.

**Paso 2: Aplicar la definición de Integral de Línea**

$$\int_C \vec{F} \cdot d\vec{r} = \int_a^b \vec{F}(\vec{r}(t)) \cdot \vec{r}'(t) \, dt$$

**Paso 3: Sustituir el Gradiente**

Como $\vec{F} = \nabla f$, la integral queda:

$$\int_a^b \nabla f(\vec{r}(t)) \cdot \vec{r}'(t) \, dt$$

**Paso 4: Regla de la Cadena Multivariable**

Por la regla de la cadena, sabemos que $\frac{d}{dt} [f(\vec{r}(t))] = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)$. Sustituimos:

$$\int_a^b \frac{d}{dt} [f(\vec{r}(t))] \, dt$$

**Paso 5: Teorema Fundamental del Cálculo**

Por el TFC de una variable, la integral de la derivada es la función evaluada en los límites:

$$f(\vec{r}(b)) - f(\vec{r}(a)) = f(B) - f(A)$$

**Conclusión:** El resultado depende exclusivamente de los puntos finales $A$ y $B$, no de la forma de la curva $C$.

---

## 3. El Criterio de la Derivada Cruzada

Para que un campo sea independiente del camino en una región simplemente conexa (sin "huecos"), es necesario y suficiente que su diferencial sea exacta:

- **Condición:** $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$.
    
- **Relación:** Si esto se cumple, el campo es conservativo y, por ende, independiente del camino.
    

> [!CAUTION] Ojo con la Región
> 
> Si la región tiene un "agujero" (como el origen en un campo que no está definido en $(0,0)$), el criterio de las derivadas cruzadas puede cumplirse pero la integral en una curva que rodea el hueco puede NO ser cero. Siempre aclará "región simplemente conexa".
# 7. **¿Qué significa que una integral de línea sea independiente de la trayectoria y qué método se usa para determinarlo?**

   Una integral de linea es independiente de la trayectoria cuando se encuentra expuesta a un campo conservativo, es independiente de la trayectoria porque solo interesa la distancia recorrida, puesto que la distancia total es el trayecto en el que se ve influenciado por la fuerza constante, si hace curvas, o se corta o etc el campo se anula a si mismo haciendo independiente la trayectoria
## 1. ¿Qué significa la Independencia de la Trayectoria?

Significa que el valor de la integral de línea $\int_C \vec{F} \cdot d\vec{r}$ depende únicamente de los **puntos inicial y final** de la curva $C$, y no del camino específico que los une.

- **Geométricamente:** Si tenés dos puntos $A$ y $B$, podés ir por una línea recta, una parábola o un zig-zag; el resultado numérico de la integral será exactamente el mismo.
    
- **Físicamente:** Indica que el campo de fuerzas es **conservativo**. El trabajo realizado para mover una partícula entre dos puntos no se pierde por el camino (como pasaría con el rozamiento).
    
- **Trayectorias cerradas:** Una consecuencia directa es que si el punto de inicio y fin coinciden ($A = B$), el valor de la integral sobre esa curva cerrada es **cero**.
    

---

## 2. Método para determinarlo

Para saber si una integral es independiente de la trayectoria, el método estándar consiste en verificar si el campo vectorial $\vec{F} = M(x, y)\hat{i} + N(x, y)\hat{j}$ es **conservativo**.

### Paso 1: Criterio de las Derivadas Cruzadas

En una región simplemente conexa, el campo es independiente de la trayectoria si cumple con el **Criterio para una diferencial exacta** (Teorema 2.4.1):

$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

- Debés derivar el componente $M$ respecto a $y$ y el componente $N$ respecto a $x$.
    
- Si los resultados son idénticos, la expresión $M dx + N dy$ es una **diferencial exacta**.
    

### Paso 2: Búsqueda de la Función Potencial

Si se cumple la igualdad anterior, existe una función escalar $f(x, y)$ (llamada función potencial) tal que $\nabla f = \vec{F}$. Para hallarla:

- Integrás $M$ respecto a $x$ (tratando a $y$ como constante).
    
- Derivás el resultado respecto a $y$ e igualás a $N$ para encontrar la parte que falta.
    
- Este proceso es el mismo que usamos para resolver **Ecuaciones Diferenciales Exactas**.
    

---

### Resumen para Obsidian

> [!SUCCESS] Resumen de comprobación
> 
> - **¿Es independiente?** Solo si $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$.
>     
> - **¿Cómo se resuelve?** Usás el Teorema Fundamental: $f(\text{Final}) - f(\text{Inicio})$.
>     
> - **Diferencia clave:** Si NO son iguales, la integral es **dependiente** de la trayectoria y debés parametrizar la curva sí o sí.
>
# 8. **Enuncie y demuestre el Teorema de Green. Desarrolle su aplicación al cálculo de Áreas en el Plano.**  
## 1. Enunciado del Teorema de Green

Sea $C$ una curva cerrada simple, suave a trozos y orientada positivamente (en sentido antihorario) en el plano, y sea $D$ la región limitada por $C$. Si $P(x, y)$ y $Q(x, y)$ tienen derivadas parciales continuas en una región abierta que contiene a $D$, entonces:

$$\oint_C (P \, dx + Q \, dy) = \iint_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) dA$$

---

## 2. Demostración (para una región simple)

Para demostrar el teorema, probamos que $\oint_C P \, dx = -\iint_D \frac{\partial P}{\partial y} \, dA$ y que $\oint_C Q \, dy = \iint_D \frac{\partial Q}{\partial x} \, dA$ por separado.

### Parte A: Demostración para $P$

1. Supongamos que $D$ es una región de Tipo I: $D = \{ (x, y) \mid a \leq x \leq b, g_1(x) \leq y \leq g_2(x) \}$.
    
2. Calculamos la integral doble de la derecha: $\iint_D \frac{\partial P}{\partial y} \, dA = \int_a^b \int_{g_1(x)}^{g_2(x)} \frac{\partial P}{\partial y} \, dy \, dx$.
    
3. Por el Teorema Fundamental del Cálculo: $\int_a^b [P(x, g_2(x)) - P(x, g_1(x))] \, dx$.
    
4. Ahora, calculamos la integral de línea $\oint_C P \, dx$ dividiendo $C$ en cuatro tramos ($C_1$ inferior, $C_2$ derecho, $C_3$ superior, $C_4$ izquierdo).
    
5. En los tramos verticales ($C_2$ y $C_4$), $dx = 0$, por lo que la integral es nula.
    
6. En $C_1$: $x$ va de $a$ a $b$, $y = g_1(x)$. En $C_3$: $x$ va de $b$ a $a$, $y = g_2(x)$.
    
7. $\oint_C P \, dx = \int_a^b P(x, g_1(x)) \, dx + \int_b^a P(x, g_2(x)) \, dx = \int_a^b [P(x, g_1(x)) - P(x, g_2(x))] \, dx$.
    
8. Comparando los resultados: $\oint_C P \, dx = -\iint_D \frac{\partial P}{\partial y} \, dA$.
    

La demostración para $Q$ es análoga usando una región de Tipo II. Al sumar ambas partes, obtenemos el teorema completo.

---

## 3. Aplicación al cálculo de Áreas

Si queremos calcular el área $A$ de la región $D$, sabemos que $A = \iint_D 1 \, dA$. Para usar el Teorema de Green, debemos elegir funciones $P$ y $Q$ tales que $\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = 1$.

Existen tres formas comunes de expresar el área como una integral de línea:

- **Opción 1 ($P=0, Q=x$):** $A = \oint_C x \, dy$
    
- **Opción 2 ($P=-y, Q=0$):** $A = -\oint_C y \, dx$
    
- **Opción 3 ($P=-y/2, Q=x/2$):** $A = \frac{1}{2} \oint_C (x \, dy - y \, dx)$
    

### Ejemplo de Utilidad

Calcular el área de una **elipse** $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ usando la Opción 3:

- Parametrizamos: $x = a \cos t$, $y = b \operatorname{sen} t$ con $t \in [0, 2\pi]$.
- Diferenciales: $dx = -a \operatorname{sen} t \, dt$, $dy = b \cos t \, dt$.
- Sustituimos: $A = \frac{1}{2} \int_0^{2\pi} [(a \cos t)(b \cos t) - (b \operatorname{sen} t)(-a \operatorname{sen} t)] \, dt$.
- Simplificamos: $A = \frac{1}{2} \int_0^{2\pi} ab (\cos^2 t + \operatorname{sen}^2 t) \, dt = \frac{1}{2} ab [t]_0^{2\pi} = \mathbf{\pi ab}$    

---

> [!CHECK] Vínculo con Exactas
> 
> Notá que si el campo es conservativo, $\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = 0$, lo que hace que la integral de línea en una curva cerrada sea cero. Esto coincide perfectamente con el criterio de independencia de la trayectoria que vimos antes.

# 9. **Enuncie el Teorema de Green para regiones múltiplemente conexas.**
El Teorema de Green no se limita a regiones "simples" o macizas; también funciona perfectamente en regiones con **agujeros** (técnicamente llamadas regiones múltiplemente conexas). La clave aquí es cómo recorremos los bordes para que la matemática siga siendo coherente.

---

## 1. Enunciado del Teorema

Sea $D$ una región múltiplemente conexa y sea $C$ su frontera completa. El teorema establece que si $P$ y $Q$ tienen derivadas parciales continuas en $D$, entonces:

$$\oint_C (P \, dx + Q \, dy) = \iint_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) dA$$

Donde la integral de línea sobre la frontera $C$ es la **suma** de las integrales sobre cada una de las curvas que forman el borde:

$$\oint_C = \oint_{C_{exterior}} + \oint_{C_{interior_1}} + \oint_{C_{interior_2}} + \dots$$

---

## 2. La Regla de la Orientación (Crucial para el Final)

Para que el signo de la integral sea correcto, la frontera $C$ debe estar **orientada positivamente**. Esto significa que al caminar sobre la curva, la región $D$ siempre debe quedar a tu **izquierda**.

- **Borde Exterior ($C_{ext}$):** Se recorre en sentido **antihorario** (como siempre).
    
- **Bordes Interiores (agujeros):** Se deben recorrer en sentido **horario**.
    

---

## 3. ¿Por qué funciona? (La técnica del "Corte")

La demostración para estas regiones se basa en transformar la región compleja en una simplemente conexa mediante **cortes transversales**:

- Se traza una línea (un "tajo") que conecte el borde exterior con el interior.
    
- Recorremos la frontera entrando por el corte, dando la vuelta al agujero y saliendo por el mismo corte.
    
- Como pasamos por el corte dos veces en direcciones opuestas, esas integrales se cancelan entre sí.
    
- Lo que queda es la suma de las integrales de los bordes con las orientaciones que mencionamos antes.
    

---

## 4. Aplicación Práctica: El caso del Campo "Agujereado"

Este teorema es el que explica por qué, en campos como $\vec{F} = \langle \frac{-y}{x^2+y^2}, \frac{x}{x^2+y^2} \rangle$ (que no está definido en el origen):

- La integral sobre cualquier curva que **no** rodea al origen es $0$.
    
- La integral sobre cualquier curva que **sí** rodea al origen da el mismo resultado (generalmente $2\pi$), sin importar la forma de la curva.
    

> [!TIP] Tip de Examen
> 
> Si te dan una integral de línea sobre una curva rara que rodea un "agujero" donde la función no existe, no intentes parametrizar la curva rara. Dibujá un círculo chiquito alrededor del agujero y usá Green para decir que la integral de la curva rara es igual a la del círculo.

## Ejemplo
### El Problema "Trampa"

Calculá la integral de línea $\oint_C \vec{F} \cdot d\vec{r}$ donde:

$$\vec{F}(x, y) = \left( \frac{-y}{x^2+y^2}, \frac{x}{x^2+y^2} \right)$$

Y la curva $C$ es una **elipse deformada** muy difícil de parametrizar que rodea al origen $(0,0)$.

### Paso 1: Verificar las derivadas cruzadas

Si hacés las cuentas (es un buen ejercicio de derivada del cociente), vas a ver que:

- $\frac{\partial P}{\partial y} = \frac{y^2-x^2}{(x^2+y^2)^2}$
    
- $\frac{\partial Q}{\partial x} = \frac{y^2-x^2}{(x^2+y^2)^2}$
    
    Son iguales. Esto significaría que la integral en una curva cerrada es cero... **¡PERO SOLO SI** la región fuera simplemente conexa! Como el campo no existe en $(0,0)$, tenemos un agujero.
    

### Paso 2: Aplicar Green en la región con el agujero

Dibujamos un círculo chiquito $C_r$ de radio $R$ centrado en el origen, dentro de nuestra curva difícil $C$. El teorema de Green para esta región $D$ (lo que queda entre la curva y el círculo) dice:

$$\oint_C \vec{F} \cdot d\vec{r} + \oint_{C_r} \vec{F} \cdot d\vec{r} = \iint_D (Q_x - P_y) \, dA$$

Como $Q_x - P_y = 0$ en toda la región $D$ (porque ahí no está el origen), la integral doble es cero. Esto implica que:

$$\oint_C = -\oint_{C_r} \text{ (con } C_r \text{ en sentido horario)}$$

O, lo que es lo mismo: **la integral de la curva difícil es igual a la integral del círculo fácil (ambas antihorarias).**

### Paso 3: Resolver la integral fácil (el círculo)

Parametrizamos el círculo de radio $R=1$: $x = \cos t$, $y = \operatorname{sen} t$, con $t \in [0, 2\pi]$.

- $dx = -\operatorname{sen} t \, dt$
    
- $dy = \cos t \, dt$
    
- $x^2 + y^2 = 1$
    
    Sustituimos en la integral:
    
    $$\oint_{C_r} \frac{-y}{x^2+y^2} dx + \frac{x}{x^2+y^2} dy = \int_0^{2\pi} \frac{-\operatorname{sen} t}{1}(-\operatorname{sen} t \, dt) + \frac{\cos t}{1}(\cos t \, dt)$$
    
    $$\int_0^{2\pi} (\operatorname{sen}^2 t + \cos^2 t) \, dt = \int_0^{2\pi} 1 \, dt = \mathbf{2\pi}$$
    

---

### Conclusión para tu examen

No importa qué tan deformada sea la curva $C$, mientras rodee al origen una vez, el resultado será siempre $2\pi$. Si la curva no rodeara al origen, el resultado sería $0$ porque la región sería simplemente conexa.

> [!CAUTION] Error común
> 
> Muchos alumnos ponen que da $0$ porque las derivadas cruzadas son iguales. Siempre fijate si el "agujero" donde la función explota está adentro de tu curva. Si está adentro, usás este truco.