# Apuntes-de-clase-Graficacion-unidad-2
Apuntes de clase del temario de graficacion unidad 2
# Unidad 2: Graficación 2D

## 2.1 Transformación bidimensional

Las transformaciones bidimensionales son operaciones matemáticas que permiten modificar la posición, tamaño, orientación o forma de objetos en un plano 2D. Estas transformaciones son fundamentales en gráficos por computadora, animación, videojuegos e interfaces visuales.

Las principales transformaciones en 2D son: traslación, escalamiento, rotación y sesgado. Estas pueden aplicarse de forma individual o combinada para lograr efectos más complejos.

---

### 2.1.1 Traslación

La traslación consiste en mover un objeto de una posición a otra sin alterar su forma, tamaño ni orientación.

Si un punto original es \( P(x, y) \), al trasladarlo se obtiene un nuevo punto:

$$
P'(x', y') = (x + t_x,\; y + t_y)
$$

Donde:
- \( t_x \): desplazamiento en el eje X  
- \( t_y \): desplazamiento en el eje Y  

---

### 2.1.2 Escalamiento

El escalamiento modifica el tamaño de un objeto. Puede ser uniforme (igual en ambos ejes) o no uniforme.

$$
P'(x', y') = (x \cdot s_x,\; y \cdot s_y)
$$

Donde:
- \( s_x \): factor de escala en X  
- \( s_y \): factor de escala en Y  

---

### 2.1.3 Rotación

La rotación permite girar un objeto alrededor del origen o de un punto específico.

$$
x' = x \cos(\theta) - y \sin(\theta)
$$

$$
y' = x \sin(\theta) + y \cos(\theta)
$$

Donde:
- \( \theta \): ángulo de rotación  

---

### 2.1.4 Sesgado (Shear)

El sesgado deforma un objeto inclinándolo en una dirección.

Sesgado en X:

$$
x' = x + k_x y
$$

$$
y' = y
$$

Sesgado en Y:

$$
x' = x
$$

$$
y' = y + k_y x
$$

---

## 2.2 Representación matricial de las transformaciones bidimensionales

Las transformaciones 2D pueden representarse mediante matrices, lo que facilita su implementación en programación y permite combinar varias transformaciones en una sola operación.

(x', y', 1) = (x, y, 1) * matriz de transformación
### Matrices básicas

**Traslación:**

$$
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

**Escalamiento:**

$$
\begin{bmatrix}
s_x & 0 & 0 \\
0 & s_y & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Rotación:**

$$
\begin{bmatrix}
\cos\theta & -\sin\theta & 0 \\
\sin\theta & \cos\theta & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

### Ejercicio sugerido: Control con teclas de dirección

Se puede implementar un programa donde un objeto (por ejemplo, un cuadrado) se mueva usando las teclas de dirección del teclado. Cada tecla aplica una traslación en el eje correspondiente:

- Flecha arriba → \( y + 1 \)  
- Flecha abajo → \( y - 1 \)  
- Flecha derecha → \( x + 1 \)  
- Flecha izquierda → \( x - 1 \)  

---

## 2.3 Trazo de líneas curvas

Las curvas permiten representar formas suaves y complejas que no pueden describirse con líneas rectas. Son fundamentales en diseño gráfico, animación y modelado.

---

### 2.3.1 Curvas de Bézier

Las curvas de Bézier se definen mediante puntos de control. La forma de la curva depende de estos puntos.

Para una curva cúbica:

$$
B(t) = (1-t)^3 P_0 + 3(1-t)^2 t P_1 + 3(1-t)t^2 P_2 + t^3 P_3
$$

Donde:
- \( t \in [0,1] \)  
- \( P_0, P_1, P_2, P_3 \): puntos de control  

---

### 2.3.2 Curvas B-Spline

Las curvas B-Spline son una generalización de las curvas de Bézier. Permiten mayor control y suavidad.

Características:
- No pasan necesariamente por los puntos de control  
- Son más estables para modelado complejo  
- Permiten modificaciones locales  

---

### Ejercicio sugerido: Dibujo de animación

Se puede realizar un programa donde:
- El usuario dibuje puntos de control  
- Se genere una curva Bézier en tiempo real  
- Se anime un objeto siguiendo la curva  

---

## 2.4 Fractales

Los fractales son estructuras geométricas complejas que se repiten a diferentes escalas. Se generan mediante procesos iterativos.

Características:
- Autosimilitud  
- Complejidad infinita  
- Generación algorítmica  

Ejemplos:
- Conjunto de Mandelbrot  
- Triángulo de Sierpinski  
- Curva de Koch  

---

## 2.5 Uso y creación de fuentes de texto

Las fuentes de texto son representaciones gráficas de caracteres.

### Uso
Se utilizan en:
- Interfaces de usuario  
- Videojuegos  
- Aplicaciones visuales  

Formatos comunes:
- `.ttf`  
- `.otf`  

### Creación
Implica:
- Diseño de caracteres  
- Uso de curvas Bézier  
- Definición de métricas  


## Conclusión

La graficación 2D es una base fundamental en la computación gráfica. A través de transformaciones, representación matricial, curvas y fractales, es posible crear desde interfaces simples hasta animaciones complejas. El manejo de texto y tipografía complementa estos elementos, permitiendo desarrollar aplicaciones visuales completas y profesionales.
