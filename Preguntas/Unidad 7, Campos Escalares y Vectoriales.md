
# 1. **Condiciones necesarias para que un campo vectorial sea un gradiente o sea conservativo**
Para que un campo vectorial $\vec{F}$ sea un **gradiente** (es decir, que exista una función potencial $f$ tal que $\vec{F} = \nabla f$), se deben cumplir ciertas condiciones de simetría en sus derivadas.

---

### 1. En el plano ($\mathbb{R}^2$)

Si tenemos un campo $\vec{F}(x, y) = P(x, y)\hat{i} + Q(x, y)\hat{j}$ definido en una región $D$, la condición necesaria es el **Criterio de Exactitud**:

- **Condición:** $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
    
- **Por qué:** Si el campo es un gradiente, entonces $P = \frac{\partial f}{\partial x}$ y $Q = \frac{\partial f}{\partial y}$. Por el Teorema de Clairaut, las derivadas cruzadas deben ser iguales: $f_{xy} = f_{yx}$.
    

---

### 2. En el espacio ($\mathbb{R}^3$)

Para un campo $\vec{F}(x, y, z) = P\hat{i} + Q\hat{j} + R\hat{k}$, la condición necesaria es que el **Rotor** del campo sea el vector nulo:

- **Condición:** $\nabla \times \vec{F} = \vec{0}$
    
- **Lo que implica:** Esto genera tres igualdades que deben cumplirse simultáneamente:
    
- $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
    
- $\frac{\partial P}{\partial z} = \frac{\partial R}{\partial x}$
    
- $\frac{\partial Q}{\partial z} = \frac{\partial R}{\partial y}$
    

---

### 3. Diferencia entre "Necesaria" y "Suficiente" (Ojo acá)

Es muy común que en el final te pregunten si con que el rotor sea cero ya alcanza para decir que es conservativo. La respuesta es **no siempre**.

- **Condición Necesaria:** Si es conservativo $\implies$ el rotor es cero.
    
- **Condición Suficiente:** Para asegurar que es conservativo, el dominio debe ser **simplemente conexo** (no debe tener "agujeros" o "túneles" donde el campo no esté definido).
    

---

### Resumen 

> [!IMPORTANT] Check de Conservatividad
> 
> 1. **Continuidad:** Los componentes del campo y sus derivadas deben ser continuos.
>     
> 2. **Simetría:** $\nabla \times \vec{F} = \vec{0}$ (las derivadas cruzadas deben coincidir).
>     
> 3. **Dominio:** Si la región es "agujereada", el rotor cero no garantiza independencia de la trayectoria.
>

# 2. **Defina Gradiente, Divergencia y Rotacional usando el operador Nabla y dé ejemplos físicos**
Para dominar estos conceptos en el final, es clave entender al **operador Nabla ($\nabla$)** como un "vector de derivadas". En $\mathbb{R}^3$, se define como:

$$\nabla = \left( \frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z} \right)$$

Aquí tenés las definiciones y sus aplicaciones físicas para que las copies directamente a tu Obsidian:

---

### 1. Gradiente ($\nabla f$)

Se aplica sobre un **campo escalar** (una función que devuelve un número) y el resultado es un **campo vectorial**.

- **Definición:** $\nabla f = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \right)$
    
- **Significado:** Indica la dirección y magnitud de la máxima tasa de aumento de la función en un punto.
    
- **Ejemplo Físico:** **Gradiente de Temperatura.** Si tenés una habitación con una estufa, $\nabla T$ es un vector que apunta hacia donde el calor aumenta más rápido. El calor fluye naturalmente en dirección opuesta ($-\nabla T$).
    

---

### 2. Divergencia ($\nabla \cdot \vec{F}$)

Se aplica sobre un **campo vectorial** mediante un producto escalar. El resultado es un **campo escalar**.

- **Definición:** $\nabla \cdot \vec{F} = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$
    
- **Significado:** Mide la tendencia de un campo a dispersarse desde un punto (fuente) o acumularse en él (sumidero).
    
- **Ejemplo Físico:** **Flujo de aire en un neumático.** Si el neumático tiene un pinchazo, la divergencia del campo de velocidades del aire en el agujero es positiva ($\nabla \cdot \vec{v} > 0$), porque el aire está "saliendo" de ese punto.
    

---

### 3. Rotacional ($\nabla \times \vec{F}$)

Se aplica sobre un **campo vectorial** mediante un producto vectorial. El resultado es un **campo vectorial**.

- **Definición:** $\nabla \times \vec{F} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R \end{vmatrix}$
    
- **Significado:** Mide la tendencia de las líneas de campo a "girar" o formar remolinos alrededor de un punto.
    
- **Ejemplo Físico:** **Campo Magnético o Hidrodinámica.** En un río con corriente, si ponés una pequeña paleta de madera y esta empieza a girar, el rotacional del agua en ese punto es distinto de cero. El vector rotacional te indica el eje sobre el cual gira la paleta.
    

---

### Cuadro comparativo para no pifiarle

|**Operación**|**Símbolo**|**Entrada**|**Salida**|**¿Qué mide?**|
|---|---|---|---|---|
|**Gradiente**|$\nabla f$|Escalar|Vector|Pendiente máxima.|
|**Divergencia**|$\nabla \cdot \vec{F}$|Vector|Escalar|Expansión / Compresión.|
|**Rotacional**|$\nabla \times \vec{F}$|Vector|Vector|Circulación / Remolino.|

> [!TIP] Para el final
> 
> Acordate que si el **Rotacional** es cero, el campo es **conservativo** (irrotacional). Si la **Divergencia** es cero, el campo es **solenoidal** (incompresible).

# 3. **Plano tangente y recta normal a una superficie**

# 4. **Diferencie entre integrales de superficie de un campo escalar y flujo de un campo vectorial**

# 5. **Enuncie el Teorema de la Divergencia (Gauss) y su aplicación**

# 6. **Enuncie el Teorema de Stokes y explique qué ocurre con la circulación si el rotacional es cero**
El **Teorema de Stokes** es el puente definitivo entre el movimiento a lo largo de un borde y la rotación en una superficie. Es, básicamente, el Teorema de Green pero con la libertad de "curvarse" en las tres dimensiones del espacio.

---

## 1. Definición Formal

Sea $S$ una superficie orientada, suave a trozos, limitada por una curva frontera $C$ cerrada, simple y suave a trozos, con orientación positiva. Si $\vec{F}$ es un campo vectorial cuyas componentes tienen derivadas parciales continuas en una región que contiene a $S$, entonces:

$$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\nabla \times \vec{F}) \cdot d\vec{S}$$

O, escrito de forma expandida:

$$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\text{rot } \vec{F}) \cdot \mathbf{n} \, dS$$

---

## 2. Los Requisitos (Para el Final)

Para que el teorema sea válido, debés mencionar estas condiciones:

- **Superficie con "borde":** $S$ no puede ser una superficie cerrada (como una esfera completa), debe ser algo como un hemisferio o un disco, donde haya una "curva frontera" $C$.
    
- **Orientación compatible:** La orientación de la curva $C$ y de la superficie $S$ debe seguir la **Regla de la Mano Derecha**. Si tus dedos siguen el sentido de la curva $C$, tu pulgar debe apuntar en la dirección del vector normal $\mathbf{n}$ de la superficie.
    
- **Continuidad:** El campo $\vec{F}$ debe ser "bueno" (C1) en toda la superficie y su borde.
    

---

## 3. ¿Qué significa realmente?

- **Físicamente:** Te dice que la circulación neta de un fluido a lo largo de un lazo cerrado $C$ es igual a la suma de todos los "micro-remolinos" (rotores) que atraviesan cualquier superficie que tenga a ese lazo como borde.
    
- **La "Magia" de Stokes:** Lo más increíble de este teorema es que la integral de superficie **no depende de la forma de la superficie**, siempre y cuando el borde sea el mismo. Podés integrar sobre un disco plano o sobre una red de pescar gigante y deformada; si el aro (borde) es el mismo, el resultado no cambia.
    

---

## 4. Comparativa con Green

Si te preguntan la diferencia en el examen, recordá esto:

- **Green:** Solo funciona en el plano $xy$. El rotor siempre apunta en dirección $\mathbf{k}$.
    
- **Stokes:** Funciona en el espacio $\mathbb{R}^3$. El rotor puede apuntar en cualquier dirección y la superficie puede ser una cáscara curva.
    

> [!TIP] Uso Estratégico
> 
> Usamos Stokes cuando la integral de línea es horrible de parametrizar pero el **Rotacional** del campo es sencillo (por ejemplo, un vector constante o con muchos ceros).

# 7. **Explique la relación entre los Teoremas de Green, Stokes y Divergencia**
## 1. Divergencia ($\text{div } \vec{F}$ o $\nabla \cdot \vec{F}$)

La divergencia mide cuánto se "expande" o "comprime" un campo en un punto. Es un **campo escalar** (el resultado es un número).

- **Fórmula:** Si $\vec{F} = \langle P, Q, R \rangle$, entonces $\text{div } \vec{F} = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$.
    
- **Significado Físico:**
    
- **$\text{div } \vec{F} > 0$:** El punto actúa como una **fuente** (sale más de lo que entra).
    
- **$\text{div } \vec{F} < 0$:** El punto actúa como un **sumidero** (entra más de lo que sale).
    
- **$\text{div } \vec{F} = 0$:** El campo es **solenoidal** (incompresible, como el agua).
    

---

## 2. Rotor o Rotacional ($\text{rot } \vec{F}$ o $\nabla \times \vec{F}$)

El rotor mide la tendencia de un campo a "rotar" alrededor de un punto. Es un **campo vectorial** (el resultado tiene dirección y magnitud).

- **Fórmula:** Se calcula mediante el determinante simbólico:
    
    $$\text{rot } \vec{F} = \nabla \times \vec{F} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R \end{vmatrix}$$
    
- **Significado Físico:** Si pusieras una pequeña hélice en el fluido, el rotor te diría hacia dónde apuntaría el eje de rotación y qué tan rápido giraría.
    
- **$\text{rot } \vec{F} = \vec{0}$:** El campo es **irrotacional**. Esto es equivalente a decir que el campo es **conservativo**.
    

---

## 3. Conexión con los Grandes Teoremas

Aquí es donde todo cobra sentido para tu examen:

### Teorema de la Divergencia (Gauss)

Relaciona el flujo a través de una superficie con lo que pasa adentro (la divergencia).

- **Lógica:** "La cantidad neta de fluido que sale por la cáscara es igual a la suma de todas las fuentes y sumideros que hay adentro".
    
- **Fórmula:** $\iint_S \vec{F} \cdot d\vec{S} = \iiint_V (\text{div } \vec{F}) \, dV$.
    

### Teorema de Stokes

Relaciona la circulación por el borde con la rotación en la superficie.

- **Lógica:** "La tendencia del fluido a girar en el borde es igual a la suma de todos los pequeños remolinos (rotores) que hay en la superficie".
    
- **Fórmula:** $\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\text{rot } \vec{F}) \cdot d\vec{S}$.
    

---

### Resumen de Propiedades (Clave para Verdadero/Falso)

> [!IMPORTANT] Identidades Vectoriales
> 
> - **Rotor de un Gradiente:** $\text{rot}(\nabla f) = \vec{0}$ (Todo campo gradiente es irrotacional).
>     
> - **Divergencia de un Rotor:** $\text{div}(\text{rot } \vec{F}) = 0$ (Las líneas de rotación no tienen fuentes ni sumideros).

## Green
Podés ver a Green de dos formas distintas: como un **Teorema de Stokes en el plano** (Rotor) o como un **Teorema de Gauss en el plano** (Divergencia)
### 1. Green y el Rotor (Forma de Circulación)

Esta es la versión estándar que ya vimos: $\oint_C P dx + Q dy = \iint_D (Q_x - P_y) dA$.

- **La conexión:** Si definís un campo 3D que solo vive en el plano, como $\vec{F} = P\hat{i} + Q\hat{j} + 0\hat{k}$, y calculás su rotor ($\nabla \times \vec{F}$), el resultado es:
    
    $$\text{rot } \vec{F} = (Q_x - P_y)\hat{k}$$
    
- **Interpretación:** El término $(Q_x - P_y)$ es la componente vertical del rotor. Green nos dice que la suma de todos los "micro-giros" (rotores) dentro de la región es igual a la circulación total en el borde.
    
- **Resumen:** Green (forma tangencial) es el **Teorema de Stokes en 2D**.
    

---

### 2. Green y la Divergencia (Forma de Flujo)

Existe otra versión de Green que relaciona el flujo neto que sale de una curva con la expansión del campo adentro.

- **La fórmula:** $\oint_C \vec{F} \cdot \mathbf{n} \, ds = \iint_D (\text{div } \vec{F}) \, dA$
    
- **En componentes:** $\oint_C P dy - Q dx = \iint_D (P_x + Q_y) \, dA$
    
- **Interpretación:** Aquí no integramos el campo tangente a la curva, sino el campo **perpendicular** (normal) a ella. Nos dice que el flujo total que atraviesa la frontera es igual a la suma de las fuentes y sumideros (divergencia) dentro de la región.
    
- **Resumen:** Green (forma normal) es el **Teorema de la Divergencia en 2D**.

## Tabla comparativa

| **Concepto**          | **Green (Circulación)**                       | **Green (Flujo)**                         |
| --------------------- | --------------------------------------------- | ----------------------------------------- |
| **Operador**          | Rotor (2D) $\implies Q_x - P_y$               | Divergencia (2D) $\implies P_x + Q_y$     |
| **Integral de línea** | Tangencial ($\vec{F} \cdot \mathbf{T} \, ds$) | Normal ($\vec{F} \cdot \mathbf{n} \, ds$) |
| **Significado**       | Mide la tendencia a rotar (remolino).         | Mide la tendencia a expandirse (fuente).  |
| **Extensión a 3D**    | Se convierte en **Teorema de Stokes**.        | Se convierte en **Teorema de Gauss**.     |

## Ejemplo:
Este ejercicio es el "final boss" para entender la diferencia entre lo que gira y lo que fluye. Vamos a usar un campo vectorial muy simple: $\vec{F}(x, y) = \langle x, y \rangle$ (un campo que apunta siempre hacia afuera del origen) y la curva será el círculo unitario $x^2 + y^2 = 1$.

---

### 1. El Escenario: Identificar componentes

- **Campo:** $P = x$ y $Q = y$.
    
- **Derivadas:** $P_x = 1$, $P_y = 0$, $Q_x = 0$, $Q_y = 1$.
    

### 2. Cálculo de la Circulación (¿Cuánto gira?)

Usamos la forma de **Rotor** de Green:

- **Fórmula:** $\oint_C \vec{F} \cdot d\vec{r} = \iint_D (Q_x - P_y) \, dA$
    
- **Cálculo:** $\iint_D (0 - 0) \, dA = 0$.
    
- **Conclusión:** La circulación es **0**. Esto tiene sentido porque el campo apunta radialmente hacia afuera; no tiene ninguna tendencia a "hacer girar" nada alrededor del círculo. Es un campo **irrotacional** (conservativo).
    

### 3. Cálculo del Flujo (¿Cuánto sale?)

Usamos la forma de **Divergencia** de Green:

- **Fórmula:** $\oint_C \vec{F} \cdot \mathbf{n} \, ds = \iint_D (P_x + Q_y) \, dA$
    
- **Cálculo:** $\iint_D (1 + 1) \, dA = \iint_D 2 \, dA$.
    
- **Resultado:** Como la integral de $1 \, dA$ es el área del círculo ($\pi \cdot 1^2$), el flujo total es $2\pi$.
    
- **Conclusión:** El flujo es **$2\pi$**. Esto significa que hay una "fuente" neta de fluido saliendo del círculo. El campo está "empujando" hacia afuera de la frontera.
    

---

### Resumen Comparativo para tu Final

|**Pregunta de Examen**|**¿Qué debés calcular?**|**Resultado en este ejemplo**|
|---|---|---|
|**¿Trabajo / Circulación?**|$\iint_D (Q_x - P_y) \, dA$|**0** (No hay remolinos)|
|**¿Flujo Neto?**|$\iint_D (P_x + Q_y) \, dA$|**$2\pi$** (Hay expansión)|

> [!TIP] Mnemotecnia
> 
> - **Rotor (Circulación):** Restás las cruzadas ($Q_x - P_y$). Pensá en "restar" para ver si hay diferencia de giro.
>     
> - **Divergencia (Flujo):** Sumás las directas ($P_x + Q_y$). Pensá en "sumar" todo lo que sale.


# Relación entre divergencia y la integral triple
### 1. Definición de Flujo en 3D

El flujo de un campo vectorial $\vec{F}$ a través de una superficie cerrada $S$ representa la "cantidad neta" de campo que atraviesa esa superficie por unidad de tiempo.

- **Matemáticamente:** $\Phi = \iint_S \vec{F} \cdot \mathbf{n} \, dS$.
    
- **El problema:** Calcular esta integral directamente suele ser una pesadilla porque requiere parametrizar la superficie y hallar el vector normal $\mathbf{n}$.
    

---

### 2. El Teorema de Gauss (El "Atajo" Maestro)

El teorema establece que el flujo a través de una superficie cerrada es igual a la integral de la **divergencia** del campo sobre el volumen $V$ encerrado por esa superficie:

$$\iint_S \vec{F} \cdot \mathbf{n} \, dS = \iiint_V (\text{div } \vec{F}) \, dV$$

Donde $\text{div } \vec{F} = P_x + Q_y + R_z$.

---

### 3. Ejemplo: De la Circunferencia a la Esfera

Usemos el campo radial en 3D: $\vec{F}(x, y, z) = \langle x, y, z \rangle$ y la superficie de la esfera unitaria $x^2 + y^2 + z^2 = 1$.

- **Paso 1 (Divergencia):** Calculamos cuánto se expande el campo.
    
    $$\text{div } \vec{F} = \frac{\partial(x)}{\partial x} + \frac{\partial(y)}{\partial y} + \frac{\partial(z)}{\partial z} = 1 + 1 + 1 = \mathbf{3}$$
    
- **Paso 2 (Integral Triple):** Aplicamos Gauss.
    
    $$\iiint_V 3 \, dV = 3 \iiint_V dV$$
    
- **Paso 3 (Resultado):** La integral de $dV$ es simplemente el **volumen de la esfera** ($V = \frac{4}{3}\pi r^3$).
    
    $$\Phi = 3 \cdot \left( \frac{4}{3} \pi \cdot 1^3 \right) = \mathbf{4\pi}$$
    

---

### Comparativa: ¿Qué aprendimos?

- **En 2D (Círculo):** La divergencia era $2$ y el flujo fue $2 \cdot (\text{Área}) = 2\pi$.
    
- **En 3D (Esfera):** La divergencia es $3$ y el flujo es $3 \cdot (\text{Volumen}) = 4\pi$.
    

> [!TIP] Interpretación Física
> 
> Este campo $\vec{F} = \langle x, y, z \rangle$ es como una explosión constante. El teorema de Gauss nos dice que para saber cuánto "estallido" sale por la superficie, solo tenemos que sumar toda la "fuerza de la explosión" (divergencia) que hay adentro.

---

### Resumen Final para tu examen del 30

1. **¿Te piden Flujo en superficie cerrada?** $\to$ Usá **Gauss** (Integral triple de la divergencia).
    
2. **¿Te piden Trabajo en curva cerrada?** $\to$ Usá **Stokes** (Integral de superficie del rotor).
    
3. **¿Te piden Área en el plano?** $\to$ Usá **Green** (Integral de línea con $P$ y $Q$ especiales)

# Que pasa cuando no es un campo conservativo?
Cuando el rotacional es diferente de cero ($\nabla \times \vec{F} \neq \vec{0}$), significa que el campo vectorial tiene **vorticidad**. En términos prácticos para tu examen: el campo "gira" y, por lo tanto, **no es conservativo**.

+1

Aquí tenés el desglose de qué implica, cómo se calcula y qué trampas te pueden poner en el parcial o final.

---

### 1. ¿Qué significa que $\text{rot } \vec{F} \neq \vec{0}$?

- **No es un campo gradiente:** No existe una función "madre" $f$ tal que $\nabla f = \vec{F}$.
    
- **Dependencia de la trayectoria:** El trabajo para ir de A a B depende de qué camino elijas.
    
- **Circulación no nula:** Si integrás el campo en una curva cerrada, el resultado probablemente no sea cero.
    
- **Física:** Si el campo fuera un fluido, una partícula pequeña puesta en ese punto empezaría a rotar sobre su propio eje.
    

---

### 2. ¿Cómo se calcula? (El método del determinante)

Para un campo $\vec{F} = \langle P, Q, R \rangle$, usás el determinante simbólico con el operador Nabla:

$$\nabla \times \vec{F} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R \end{vmatrix}$$

Al desarrollarlo (por cofactores), obtenés el vector:

$$\text{rot } \vec{F} = \left( \frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z} \right) \mathbf{i} - \left( \frac{\partial R}{\partial x} - \frac{\partial P}{\partial z} \right) \mathbf{j} + \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) \mathbf{k}$$

---

### 3. ¿Qué te pueden pedir que calcules? (Los 3 clásicos)

#### A. Determinar si el campo es conservativo

Te dan un campo y te preguntan: "¿Es conservativo?".

- **Tu respuesta:** Calculás el rotacional. Si te da distinto de $\vec{0}$, decís: "No es conservativo porque su rotacional es no nulo". Si te da $\vec{0}$ y el dominio es simplemente conexo, decís que sí lo es.
    

#### B. Calcular la circulación mediante el Teorema de Stokes

Este es el ejercicio de 10 puntos. Te piden la integral de línea $\oint_C \vec{F} \cdot d\vec{r}$ sobre una curva cerrada $C$ en el espacio (que suele ser un embole de parametrizar).

- **El truco:** Usás **Stokes** para pasar a una integral de superficie:
    
    $$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\nabla \times \vec{F}) \cdot \mathbf{n} \, dS$$
    
- Aquí calculás el rotacional, hacés el producto escalar con el vector normal a la superficie $S$ que encierra esa curva, e integrás. Generalmente el rotacional queda algo simple (como un vector constante), lo que facilita mucho la cuenta.
    

#### C. Hallar componentes desconocidas

A veces te dan un campo con una incógnita, tipo $\vec{F} = \langle ax^2, by, cz \rangle$, y te dicen: "Sabiendo que el campo es irrotacional, halle $a, b, c$".

- **Tu respuesta:** Igualás cada componente del rotacional a cero y despejás las letras.
    

---

> [!WARNING] Cuidado en el oral
> 
> Si te preguntan: "¿Si el rotacional es distinto de cero, puedo usar el Teorema Fundamental de Integrales de Línea?".
> 
> **Respuesta:** ¡NO! El Teorema Fundamental solo sirve para campos conservativos (rotacional cero). Si hay rotacional, tenés que parametrizar la curva o usar Stokes

# Stokes
El **Teorema de Stokes** es el puente definitivo entre el movimiento a lo largo de un borde y la rotación en una superficie. Es, básicamente, el Teorema de Green pero con la libertad de "curvarse" en las tres dimensiones del espacio.

---

## 1. Definición Formal

Sea $S$ una superficie orientada, suave a trozos, limitada por una curva frontera $C$ cerrada, simple y suave a trozos, con orientación positiva. Si $\vec{F}$ es un campo vectorial cuyas componentes tienen derivadas parciales continuas en una región que contiene a $S$, entonces:

$$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\nabla \times \vec{F}) \cdot d\vec{S}$$

O, escrito de forma expandida:

$$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\text{rot } \vec{F}) \cdot \mathbf{n} \, dS$$

---

## 2. Los Requisitos (Para el Final)

Para que el teorema sea válido, debés mencionar estas condiciones:

- **Superficie con "borde":** $S$ no puede ser una superficie cerrada (como una esfera completa), debe ser algo como un hemisferio o un disco, donde haya una "curva frontera" $C$.
- **Orientación compatible:** La orientación de la curva $C$ y de la superficie $S$ debe seguir la **Regla de la Mano Derecha**. Si tus dedos siguen el sentido de la curva $C$, tu pulgar debe apuntar en la dirección del vector normal $\mathbf{n}$ de la superficie.
- **Continuidad:** El campo $\vec{F}$ debe ser "bueno" (C1) en toda la superficie y su borde.

---

## 3. ¿Qué significa realmente?

- **Físicamente:** Te dice que la circulación neta de un fluido a lo largo de un lazo cerrado $C$ es igual a la suma de todos los "micro-remolinos" (rotores) que atraviesan cualquier superficie que tenga a ese lazo como borde.
- **La "Magia" de Stokes:** Lo más increíble de este teorema es que la integral de superficie **no depende de la forma de la superficie**, siempre y cuando el borde sea el mismo. Podés integrar sobre un disco plano o sobre una red de pescar gigante y deformada; si el aro (borde) es el mismo, el resultado no cambia.

---

## 4. Comparativa con Green

Si te preguntan la diferencia en el examen, recordá esto:

- **Green:** Solo funciona en el plano $xy$. El rotor siempre apunta en dirección $\mathbf{k}$.
- **Stokes:** Funciona en el espacio $\mathbb{R}^3$. El rotor puede apuntar en cualquier dirección y la superficie puede ser una cáscara curva.

> [!TIP] Uso Estratégico
> 
> Usamos Stokes cuando la integral de línea es horrible de parametrizar pero el **Rotacional** del campo es sencillo (por ejemplo, un vector constante o con muchos ceros).

# Stokes Relacion con resto de teoremas
## 1. El Árbol Genealógico: Del Plano al Espacio

Todos estos teoremas son versiones del **Teorema Fundamental del Cálculo**, pero en dimensiones superiores. Todos dicen lo mismo: _"Lo que pasa dentro de una región es igual a lo que fluye o circula por su borde"_.

### La Familia de la Circulación (Rotor)

- **2D - Teorema de Green:** Relaciona un área plana $D$ con su borde $C$.
    
    $$\oint_C \vec{F} \cdot d\vec{r} = \iint_D (\text{rot } \vec{F}) \cdot \mathbf{k} \, dA$$
    
- **3D - Teorema de Stokes:** Relaciona cualquier superficie curva $S$ (como un sombrero o una cáscara) con su borde $C$.
    
    $$\oint_C \vec{F} \cdot d\vec{r} = \iint_S (\text{rot } \vec{F}) \cdot \mathbf{n} \, dS$$
    

> **Relación:** Green es un caso especial de Stokes donde la superficie $S$ es "plana" y está pegada al plano $xy$. En ese caso, el vector normal $\mathbf{n}$ es simplemente el vector $\mathbf{k}$.

### La Familia del Flujo (Divergencia)

- **2D - Green (forma normal):** Relaciona el flujo que sale de una curva con la divergencia dentro del área.
    
    $$\oint_C \vec{F} \cdot \mathbf{n} \, ds = \iint_D (\text{div } \vec{F}) \, dA$$
    
- **3D - Teorema de Gauss (Divergencia):** Relaciona el flujo que sale de un volumen con la divergencia dentro de ese cuerpo.
    
    $$\iint_S \vec{F} \cdot \mathbf{n} \, dS = \iiint_V (\text{div } \vec{F}) \, dV$$
    

---

## 2. ¿Cómo "vive" Stokes en esta jerarquía?

Stokes es el puente entre las líneas y las superficies. Su función principal es **simplificar el cálculo de una circulación**.

- **El concepto:** Si tenés una curva cerrada $C$ en el espacio, no importa qué superficie $S$ elijas para "tapar" ese agujero; mientras el borde sea $C$, el resultado de la integral de Stokes será el mismo.
    
- **Por qué es potente:** A veces parametrizar la curva $C$ es una pesadilla (por ejemplo, una intersección de un cilindro con un plano inclinado), pero calcular el rotor e integrarlo sobre la tapa plana de ese cilindro es un trámite de dos minutos.
    

---

## 3. Resumen de Conexiones para el Teórico

| **Teorema**          | **Región**        | **Frontera**           | **Operador Clave**     |
| -------------------- | ----------------- | ---------------------- | ---------------------- |
| **Fundamental (1D)** | Interval $[a, b]$ | Puntos $a, b$          | Derivada común $f'$    |
| **Green (2D)**       | Área plana $D$    | Curva cerrada $C$      | Rotor (componente $k$) |
| **Stokes (3D)**      | Superficie $S$    | Curva cerrada $C$      | **Rotor vectorial**    |
| **Gauss (3D)**       | Volumen $V$       | Superficie cerrada $S$ | Divergencia            |