# Localizacion de raíces nunha ecuacion ou sistema

- **Atopar raíces** --> (puntos onde $f(x_i)=0$ )

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
    - $f(x_a)\cdot f(x_r)=0$ --> **a raíz será** $x_r$
    - $f(x_a)\cdot f(x_r)>0$ --> a raiz estará no intervalo $(x_r,x_b)$ ; repetimos o metodo nese intervalo
    - $f(x_a)\cdot f(x_r)<0$ --> a raiz estará no intervalo $(x_a,x_r)$ ; repetimos o metodo nese intervalo

Sendo $k$ os pasos realizados, e $x_k = x_r$ para cada caso:

 - A cota de erro do metodo é $e_k := \left| \alpha - x_k\right| \leq (\frac{1}{2})^k \cdot (b-a)$
 - Sendo a raiz procurada $\alpha = \lim{k \to \infty} x_k$

O erro reducirase a metade en cada paso, e poderiamos facer o metodo ata que chegue ata unha certa tolerancia

#### Atopar k necesario para obter un erro menor dun $\epsilon$ dado

- $\frac{b-a}{\epsilon} < 2^k$. (aplicando log neperianos)
    - $k > \frac{ln(\frac{b-a}{\epsilon})}{ln(2)}$ (para facilitar os calculos usar log base 2)

## Métodos de converxencia veloz

### Metodo de Newton-Raphson (conversión cuadrática)

*Converxencia non garantida usando as tanxentes para atopar a raíz; a funcion debe ser derivable en todos os puntos, ademais, a derivada debe ser distinta de 0*

- Etapa $k$, sendo $x_k$ o iterante e $f(x_k)\neq 0$
    - tanxente en $(x_k,f(x_k))$ --> $y = f(x_k) + f'(x_k)\cdot (x-x_k)$
    - pto de corte con eixo OX --> $f(x_k) + f'(x_k)\cdot (x-x_k) = 0$
        - $x_{k+1} := x$
        - $x_{k+1} := x_k - \frac{f(x_k)}{f'(x_k))}$ , para $k = 0,1,2,...$ 

#### Teorema 1

Se temos:

$$m_1 \leq min_{x\in [a,b]} \left| f'(x)\right| \qquad max_{x\in [a,b]} \left| f''(x)\right| \leq M_2$$

Supoñemos $m_1>0$ ; dado $x_0\in [a,b] \text{, sexa } \{x_k\} _{k\in \mathbb{N}}$ a sucesion obtida por Newton-Raphson, supoñendo $x_k \in [a,b], \forall k/in /mathbb{N}$ , entón:

- $\left| \alpha - x_{k+1}\right| \leq C\cdot \left| /alpha - x_k \right| ^2$
- $C = \frac{M_2}{2\cdot m_1}$

#### Teorema 2

Se temos:

$$m_1 \leq min_{x\in [a,b]} \left| f'(x)\right| \qquad max_{x\in [a,b]} \left| f''(x)\right| \leq M_2$$

Supoñemos $m_1>0$ ; dado $x_0\in [a,b] \text{, sexa } \{x_k\} _{k\in \mathbb{N}}$ a sucesion obtida por Newton-Raphson, supoñendo $x_k \in [a,b], \forall k/in /mathbb{N}$ , entón:

- $\left| \alpha - x_{k+1}\right| \leq C\cdot \left| x_{k+1} - x_k  \right| ^2
- $C = \frac{M_2}{2\cdot m_1}$

Neste caso a cota de erro queda en funcion de duas iteracipns, puidendo saber asi o numero de iteracions necesario para obter un erro menor que a constante

#### Criterio de detencion

Basicamente buscamos que $\left| x_k - x_{k+1} \right|$ sexa moi pequeno debido a unhas inecuacion expesadas na bitacora 3

### Metodo da secante

*Moi similar ao de Newton, de mais facil converxencia e algo menos eficiente.*

Habería que cambiar $f'(x)$ por $\frac{f(x_k)-f(x_{k-1})}{x_k-x_{k-1}}$ ; entón:

- $x_{k+1}:= x_k -f(x_k)\cdot \frac{f(x_k)-f(x_{k-1})}{x_k-x_{k-1}}$
- Este meotdo considera dous puntos iniciais $(x_0,x_1)$

orde de converxencia $p=\frac{1+\sqrt{5}}{2}$







