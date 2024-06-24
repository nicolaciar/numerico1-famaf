Para que la función $s(x)$ sea una spline cúbica, debe cumplir las siguientes condiciones en el punto $x = 1$:

1. Continuidad: $s(x)$ debe ser continua en $x = 1$.
2. Continuidad de la primera derivada: $s'(x)$ debe ser continua en $x = 1$.
3. Continuidad de la segunda derivada: $s''(x)$ debe ser continua en $x = 1$.

Dado que $s(x)$ está definida como:

$$
s(x) = \begin{cases}
ax^3 + bx^2 + cx, & \text{si } x \in [0,1], \\
x^3 + 7x^2 + 2x + 1, & \text{si } x \in [1,2],
\end{cases}
$$

Primero, verificamos la continuidad en $x = 1$:

### 1. Continuidad en $x = 1$:

$$
\lim_{x \to 1^-} s(x) = \lim_{x \to 1^-} (ax^3 + bx^2 + cx) = a(1)^3 + b(1)^2 + c(1) = a + b + c
$$

$$
\lim_{x \to 1^+} s(x) = \lim_{x \to 1^+} (x^3 + 7x^2 + 2x + 1) = 1^3 + 7(1)^2 + 2(1) + 1 = 1 + 7 + 2 + 1 = 11
$$

Para que $s(x)$ sea continua en $x = 1$:

$$
a + b + c = 11 \quad \text{(1)}
$$

### 2. Continuidad de la primera derivada en $x = 1$:

Derivamos $s(x)$:

Para $x \in [0,1]$:

$$
s'(x) = 3ax^2 + 2bx + c
$$

Para $x \in [1,2]$:

$$
s'(x) = 3x^2 + 14x + 2
$$

Evaluamos en $x = 1$:

$$
\lim_{x \to 1^-} s'(x) = 3a(1)^2 + 2b(1) + c = 3a + 2b + c
$$

$$
\lim_{x \to 1^+} s'(x) = 3(1)^2 + 14(1) + 2 = 3 + 14 + 2 = 19
$$

Para que $s'(x)$ sea continua en $x = 1$:

$$
3a + 2b + c = 19 \quad \text{(2)}
$$

### 3. Continuidad de la segunda derivada en $x = 1$:

Derivamos $s'(x)$:

Para $x \in [0,1]$:

$$
s''(x) = 6ax + 2b
$$

Para $x \in [1,2]$:

$$
s''(x) = 6x + 14
$$

Evaluamos en $x = 1$:

$$
\lim_{x \to 1^-} s''(x) = 6a(1) + 2b = 6a + 2b
$$

$$
\lim_{x \to 1^+} s''(x) = 6(1) + 14 = 6 + 14 = 20
$$

Para que $s''(x)$ sea continua en $x = 1$:

$$
6a + 2b = 20 \quad \text{(3)}
$$

### Resolución del sistema de ecuaciones:

Tenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
a + b + c = 11, \\
3a + 2b + c = 19, \\
6a + 2b = 20.
\end{cases}
$$

Primero resolvemos la tercera ecuación para $b$:

$$
6a + 2b = 20 \implies 3a + b = 10 \implies b = 10 - 3a \quad \text{(4)}
$$

Sustituimos $b$ en las primeras dos ecuaciones:

$$
a + (10 - 3a) + c = 11 \implies a + 10 - 3a + c = 11 \implies -2a + c = 1 \implies c = 1 + 2a \quad \text{(5)}
$$

$$
3a + 2(10 - 3a) + c = 19 \implies 3a + 20 - 6a + c = 19 \implies -3a + 20 + c = 19 \implies -3a + c = -1
$$

Sustituimos $c$ de la ecuación (5) en la última ecuación:

$$
-3a + (1 + 2a) = -1 \implies -3a + 1 + 2a = -1 \implies -a + 1 = -1 \implies -a = -2 \implies a = 2
$$

Usamos $a = 2$ en las ecuaciones (4) y (5):

$$
b = 10 - 3(2) = 10 - 6 = 4
$$

$$
c = 1 + 2(2) = 1 + 4 = 5
$$

Por lo tanto, los valores son:

$$
a = 2, \quad b = 4, \quad c = 5.
$$

Entonces, la función $s(x)$ es:

$$
s(x) = \begin{cases}
2x^3 + 4x^2 + 5x, & \text{si } x \in [0,1], \\
x^3 + 7x^2 + 2x + 1, & \text{si } x \in [1,2].
\end{cases}
$$