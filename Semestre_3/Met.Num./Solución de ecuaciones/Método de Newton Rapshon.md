Retomando lo que se hizo en la clase anterior, se deberá encontrar una raíz dentro con la función que nos proporcionen y con ayuda de GeoGebra graficar y buscar su derivada. Esto se hará de esta manera debido a que puede llegar a ser muy complicado encontrar una derivada y nos apoyaremos en una herramienta como lo es GeoGebra. 
Se utiliza GeoGebra Clásico para poder usar la hoja de cálculo que nos otorgue la facilidad de calcular la derivada de la función que sea. 
Para poder encontrar una raíz compleja deseada, será necesario utilizar un número complejo cercano a la raíz compleja. 

**Características**
- Puede converger a una raíz distinta de la que se busca o ni siquiera encontrarla si es que se toma un $(x_0)$ lejano de la raíz en cuestión.
- Converge más rápido pero debe tenerse en cuenta los costos de las operaciones a realizar para usarlo.
- El método también es capaz de encontrar raíces complejas, pero se deberá tomar un valor inicial como un número complejo. 

Se realiza haciendo una aproximación lineal de la función, utilizando la recta tangente.

Su convergencia es cuadrática, por lo que converge de manera más rápida que una lineal. También se debe tener en cuenta que es más costosa aunque sea más rápida. 


**Deducción por serie de Taylor**
A partir de la serie infinita de Taylor se puede llegar a este método, ya que sobre estas se sustenta. SI se observa la serie de Taylor seremos capaces de encontrar las similitudes con la manera de calcular la $(x_0)$ que cambia constantemente.
	$$f(x_0+h)=f(x_0)+h\frac{f´(x_0)}{dx}+...+\frac{h^n}{n!}\frac{d^nf(x_0)}{dx^n} $$
	Como se puede observar la parte que realmente nos interesa es: $(f(x_0+h)=f(x_0)+h\frac{f´(x_0)}{dx})$ ya que es la que se parece a nuestra manera de encontrar la siguiente $(x_0)$ a evaluar hasta llegar a la raíz. La manera de utilizará es evaluar la función en un punto $(x_0+h)$ lo suficientemente pequeño que ocasione que no sea posible calcular las derivadas segundas o terceras o las que sean, es decir, trucar la serie. Haciendo distintas operaciones algebraicas a partir de esa serie será posible llegar a la manera que especificamos para encontrar nuestras siguientes $(x_0)$: 
	$$x_{n+1} = x_n-\frac{f(x_n)}{f´(x_n)}$$
Este método fallará también si se llegan a tomar funciones especificas lo suficientemente simétricas como para que se atrape el método en un ciclo infinito, estas excepciones serán llamadas casos patológicos. 