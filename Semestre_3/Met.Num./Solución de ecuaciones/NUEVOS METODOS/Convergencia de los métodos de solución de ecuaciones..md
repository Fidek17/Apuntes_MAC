La convergencia se refiere a la velocidad ene que una sucesión se aproxima a un valor en especifico. 
El orden de convergencia se refiere a la velocidad, para mayor orden menor error.
El orden de convergencia se ve así: $O(h^n)$.

Las condiciones iniciales para los métodos de obtencion de raíces de ecuaciones se requiere que sean continuas y diferenciadles en su intervalo a buscar. 

##### Método de Bisección:
Si tomaomos los puntos medios de los intervalos sucesivos como la estimación de la raíz, una de las mitdes del intevalo en cuestion es una frontera o cota superior del error. 

$|e_n|=\frac{|b-a|}{2^n}$


##### Método de Newton-Raphson

==**La manera de conocer cuando un método es convergente es cuando la derivada de la forma iterativa en el punto que se esta evaluada es menor a cero, significa que si es convergente**==
Conocemos que el método converge a partir de un valor inicial $x_0$ en el intervalo. 
$f´(x))$ no puede ser cero porque signifficaria que no hay pendiente y no encontrariamos su conrte con el eje de las $x$.

Este método es cuadráticmanete convergerte dado que cuando se tiene un valor por decir que ya es la raíz y se expande el razonamiento será posible llegar a algo como esto: $$ g(x_n)=g(r)+\frac{g´´(3)}{2}(x_n-r)^2$$
Sabemos que $x_n-r$ se refiere al error ya que representa el error que existe entre nuestra última variable $x_n$ y nuestra raíz a encontrar $r$ por lo tanto es nuestro error y este también se encuentra al cuadrado, por lo tanto es cuadraticamente convergente. 
Su orden de convergencia por lo tanto será este:
$$\frac{g´´(\epsilon)}{2}(e_n)^2 = O(h^2)$$
##### Método de la posición falsa
Primero necesitamos encontrar la forma iterativa que se utilizará para encontrar la raíz $r$ y esta será nuestra $g(x)$ y necesitamos ahora sacar la derivada de esta $g(x)$. Si al evaluar esa derivada en la raíz se podra ver que el resultado no es cero por lo que podemos conlcuir que el método de la posición falsa es linealmente convergente debido a que no desaparece mi termino. 

##### Método de la secante
Al realizar el mismo proceso que antes, encontrar la forma itereativa y encontrar la derivada de estas, pero como estamos utilzando dos puntos 

|Método| Convergencia| $O(h^n)$|
|-| -| -|
|Bisección| Lineal| $$e_n=\frac{b-a}{2^n}$$|
|Newton-Raphson| Cuadrática|$$ \frac{g´´(\epsilon)}{2}(e_n)^2 $$|
|Posición Falsa| Lineal| $g(x)$|
|Secante| Super Lineal|$$ \frac{g´´(\epsilon_1, \epsilon_2)}{2}(e_n)(e_{n-1})$$|




