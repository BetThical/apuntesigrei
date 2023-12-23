# Loxica booleana (V/F, nunca V e F)

## Calculo de proposicions

- **Alfabeto**: $p$ , $q$ , $r$ ,...
- **Conectores**: $\neg$ , $\land$ , $\lor$ , $\implies$

1. Toda letra do alfabeto e unha proposicion
2. Sendo $a$ e $b$ proposicions
    1. $\neg a$ e outra proposicion
    2. $a\land b\quad a\lor b\quad a\implies b$ son proposicions
3. Nada que non resulte das reglas anteriores e proposicion
4. Usanse parenteses para deixar clara a forma da proposicion

### Taboas de verdade (metodo NON recomendado)

| p | $\neg p$ |
| - | -------- |
| V | F |
| F | V |

| p | q | $p\lor q$ | $p\land q$ | $p\implies q$ |
| - | - | --------- | ---------- | ------------- |
| V | V | V | **V** | V |
| V | F | V | F | **F** |
| F | V | V | F | V |
| F | F | **F** | F | V |

### Valores distinguidos (mellor opcion)

- $p\lor q$ : verdade se $p$ , $q$ verdade 
- $p\land q$ : falso se $p$ , $q$ falso
- $p\implies q$ : falso se $p$ verdade e $q$ falso

#### Exemplo

$(p\land q)\implies r$
```
   f
  / \
 v   f
/ \
v v
```

$(p\land q)\implies r$ e falsa se $p$ ,$q$ verdade e $r$ falso

### "Tipos" de proposicions

 - **Tautoloxias**: só poden ser verdade
 - **Contradicions**: so poden ser falsas
 - **Continxentes**: poden tomar ambos valores

### Equivalencia semantica 

Mesmos valores de variables, proposicions con mesmos valores de verdade


$p\land q \equiv p\equiv p\lor q$

$p\implies q\equiv \neg p \lor q$

$\neg (p\land q)\equiv \neg p \lor \neg q$

$\neg (p\lor q)\equiv \neg p \land \neg q$

### Consecuencias semanticas

$p\vDash q$ : $q$ é consecuencia semantica de $p$ cando para todos os casos onde $p$ é V, $q$ é V

se $p\vDash$ , entón $p\implies q\quad (\top)$
