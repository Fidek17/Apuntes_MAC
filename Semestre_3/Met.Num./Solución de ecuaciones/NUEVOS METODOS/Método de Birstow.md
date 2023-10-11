Este método será capaz de encontrar todas las raíces, ya sean reales o **complejas conjugadas** de un polinomio $P(x)$. 
El método se deduce a partir de un algoritmo de división sintética para binomios empleando así una ecuación cuadrática de prueba $(x^2-rx-s)$.

Para comprender esta deducción será necesario partir desde dos polinomios: $P_n(x)$ y $Q_{n-2}(x)$. Estos quieren decir que el polinomio $P_n(x)$ es de $n$ grado por lo que el polinomio $Q_{n-2}(x)$ será de grado $n-2$ es decir, dos grados inferiores.


COntinuar explicacion de la deduccion

Como sabemos que $P_n(x)=(x^2-rx-s)x(Q_{n-2}(x))$ se buscara 

La idea que se tiene es que el polinomio $Q$ esta recortado por dos grados a $P(x)$ , esto significa que le falta algo de este tipo $(b_1x^1+b_0)$ para ser igual con $P(x)$, lo que deseamos es que al realizar una división sintética entre $P$ y $Q$ no exista residuo, pero es inevitable que no lo haya, ya que si como se recuerda de una división sintética de polinomios, se pueden ver como una resta entre $P$ y $Q$ pero como a $Q$ le falta un cacho $(b_1x^1+b_0)$ pues sobrara, representaran el residuo de la división.
Deseamos que el residuo sea cero ya que si es cero significa que encontramos la raíz, por lo tanto buscamos que tanto $b_1$ como $b_0$ sean cero ya que al ser multiplicados con $x$ serán iguales a cero y por lo tanto no hay residuo y se consiguió por consiguiente la raíz.

Tenemos una herramienta muy poderosa que es la chicharronera o la formula general para la obtención de 

En la idea general sobre como aplicar y como se creo este sistema tiene que ver con la forma de pensar de divide y vencerás, si somos capaces de dividir un polinomio de grado n en otros polinomios de grado 2, podemos encontrar cada una de las raíces de cada polinomio de grado 2 por medio de la fórmula general que a su vez, la multiplicación de cada polinomio de grado 2 con los otros polinomios de grado 2 nos da de resultado el polinomio de grado n. 
$$ P_n(x)= (x^2-rx-s)(x^2-ax-b)...(x^2-cx-d)$$






