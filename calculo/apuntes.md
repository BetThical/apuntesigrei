# Ecuacions e sistemas de Ecuacions no Lineais

- dada $f: \mathbb{R} \longrightarrow \mathbb{R}$ (no lineal), atopar $x\in \mathbb{R} \quad \text{tal que} \quad f(x)=0$ para unha ecuacion

- dada $f: \mathbb{R}^n \longrightarrow \mathbb{R}^n$ (no lineal), atopar $x=(x_1,...,x_n)^t \in \mathbb{R}^n \quad \text{tal que} \quad f(x)=0$ para un sistema de ecuacions

## Metodos converxencia garantizada

### Existencia raices

#### Th. Valor Intermedio**

$$f:\quad [a,b]\longrightarrow \mathbb{R}$$
$$f(a) < f(b)\implies \forall z, f(a)<z<f(b),\exists \alpha \in (a,b), f(\alpha)=z$$

$f(a)\cdot f(b) <0 \implies z=0$ é valor intermedio (raiz)

Se ademais $f'(x) /neq 0,\quad \forall x \in (a,b)\implies\text{ a raiz e unica}$

#### Metodo de biseccion (como busqueda binaria)

- Ir facendo e comprobando se $f(x_r) = \frac{x_a + x_b}{2} = 0$
    - Se o é, $f(x_r)=0$ 
    - Se $f(x_a)\cdot x_r<0$, $f$ ten raiz en $(x_a,x_r)$ (repitese o proceso)
    - Se $f(x_a)\cdot x_r>0$, $f$ ten raiz en $(x_r,x_b)$ (repitese o proceso) 

- $e_k = \left| \alpha - x_k\right| \leq \frac{1}{2^k} (b-a) < \epsilon$ (para un epsilon ou erro maximo dado)
- $\frac{b-a}{\epsilon} < 2^k$ ; $ln(\frac{b-a}{\epsilon}) < k\cdot ln(2)$




