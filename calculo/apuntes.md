# Localizacion de raíces nunha ecuacion ou sistema

- **Atopar raíces** -> (puntos onde $f(x_i)=0$ )

## Métodos de converxencia garantida

### Th. Valor Intermedio 

*f continua en [a,b], acadará todos os valores entre f(a) e f(b)*

Sexa $f[a,b]\longrightarrow \mathbb{R}$ continua en $[a,b]$ ,  $f(a) < f(b)$ , enton:

- $\forall z,\quad f(a) < z < f(b)\qquad \exists \alpha \in (a,b), f(\alpha )= z$

Se ademais, $f(a)\cdot f(b) < 0$ , entón:

- $\exists z=0$ , polo que dicimos que ten raíz

Se ademais de ter raiz, $f'(x)\neq 0$ no intervalo $(a,b)$

- A raíz é única

### Método de bixeccion

*O obxetivo seria acotar o maximo posible a raiz unha vez sabemos que existe nese intervalo polo teorema anterior*

Sendo os extremos do intervalo $x_a, x_b$

- $x_r = \frac{x_a + x_b}{2}$, *é dicir, o punto intermedio de* $(x_a,x_b)$ ; neste punto existen **3 posibilidades**
    - $f(x_a)\cdot f(x_r)=0$ -> **a raíz será** $x_r$
    - $f(x_a)\cdot f(x_r)>0$ -> a raiz estará no intervalo $(x_r,x_b)$ ; repetimos o metodo nese intervalo
    - $f(x_a)\cdot f(x_r)<0$ -> a raiz estará no intervalo $(x_a,x_r)$ ; repetimos o metodo nese intervalo

Sendo $k$ os pasos realizados, e $x_k = x_r$ para cada caso:

 - A cota de erro do metodo é $e_k := \left| \alpha - x_k\right| \leq (\frac{1}{2})^k \cdot (b-a)$
 - Sendo a raiz procurada $\alpha = \lim{k \to \infty} x_k$

O erro reducirase a metade en cada paso, e poderiamos facer o metodo ata que chegue ata unha certa tolerancia

#### Atopar k necesario para obter un erro menor dun $\epsilon$ dado

- $\frac{b-a}{\epsilon} < 2^k$. (aplicando log neperianos)
    - $k > \frac{ln(\frac{b-a}{\epsilon})}{ln(2)}$ (para facilitar os calculos usar log base 2)




