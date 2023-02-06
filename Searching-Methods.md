# Searching Methods













### Búsqueda en Amplitud o Anchura (BFS) 

Es un algoritmo con el que recorremos y/o buscamos elementos de un grafo. La búsqueda de ancho se utiliza para aquellos algoritmos donde es crítico elegir el mejor camino posible en cada momento del recorrido. Este algoritmo de grafos es muy útil en diversos problemas de programación. Por ejemplo, halla la ruta más corta cuando el peso entre todos los nodos es 1, cuando se requiere llegar con un movimiento de caballo de un punto a otro con el menor número de pasos, cuando se desea transformar algo un numero o cadena en otro realizando ciertas operaciones como suma producto, pero teniendo en cuenta que no sea muy grande el proceso de conversión, o para salir de un laberinto con el menor número de pasos, etc. Podrán aprender a identificarlos con la práctica. 

Características 
Proceso para implementar la Búsqueda en Profundidad 

Declarar una cola de tamaño igual al número de nodos que tenemos. 

Seleccionar nuestro nodo raíz para que, a partir de este, comenzamos a recorrer nuestro grafo. 

A partir de que visitamos nuestro nodo raíz, pasamos a los nodos vecinos. Es decir, los que se encuentra a profundidad I y no I+1. 

Después de visitar al segundo nodo, pasamos al vecino de este, sin olvidar que al nodo que ya visitamos debemos expandirlo en caso de ser necesario. 

Este paso lo repetimos hasta visitar todos los nodos (en caso de ser necesario ya que como mencionamos este algoritmo busca optimizar y por lo tanto si encuentra antes el nodo objetivo, ya no es necesario que busque en los demás nodos. 

En caso de que se recorran todos los nodos y no encontremos solución, comenzaremos a extraer datos de nuestra cola empezando por el más antiguo ya que seguimos el procedimiento de FIFO 

Repetimos los pasos 3, 4 y 5 mientras la cola tenga elementos. 

Aplicaciones del Algoritmo BFS 

Redes sociales: En las redes sociales, podemos encontrar personas dentro de una distancia dada 'k' de una persona utilizando Breadth First Search hasta niveles 'k'.   

Sistemas de navegación GPS: Breadth First Search se utiliza para encontrar todas las ubicaciones vecinas.   

Rastreadores en motores de búsqueda: Los rastreadores construyen un índice usando Breadth First. La idea es comenzar desde la página fuente y seguir todos los enlaces desde la fuente y seguir haciendo lo mismo. Depth First Traversal también se puede usar para rastreadores, pero la ventaja de Breadth First Traversal es que la profundidad o los niveles del árbol construido pueden ser limitados. 

Radiodifusión en red: En las redes o en motores de búsqueda, un paquete difundido sigue la búsqueda primero en amplitud para llegar a todos los nodos.   

Búsqueda de caminos: Podemos usar primero la amplitud o primero el recorrido transversal para encontrar si hay un camino entre dos vértices.   

Procesamiento de imágenes: BFS se puede usar para llenar una imagen con un color particular o para encontrar componentes conectados de píxeles. 

Ejemplo Búsqueda en Amplitud o Anchura 

Para nuestro ejemplo ocupamos un grafo con 14 nodos, sin embargo, no fue necesario recorrer todos esto es lo más importante, em primer entra primera imagen podemos observar la creación de nuestra cola del tamaño de nuestros nodos. Comenzamos visitando nuestro nodo raíz que en este seleccionamos al de menor profundidad en este caso es A, lo visitamos y como no es el nodo que estamos buscando lo agregamos a nuestra cola, de igual forma podemos observar que expandimos los nodos vecinos de la raíz como observamos son D, F, G. 

A continuación, observamos que pasamos al nodo D, como observamos se agrega a la lista ya que de igual forma no es la solución que estamos buscando. Por otra parte, aunque podemos observar los nodos hijos de D y F, los únicos que hemos expandido son los nodos de D ya que como explique este nodo ya fue visitado. 

 

En esta segunda imagen observamos que avanzamos al nodo F, dado que nuevamente no es la solución óptima la agregamos a la cola, es importante recalcar que se ordenan de esa forma ya que siguen el principio FIFO, como podemos observar en el siguiente paso los nodos de F ya se expandieron esto como consecuencia de que ya recorrimos este nodo, pasamos a G y de la misma manera se añade a la cola al no ser la solución que buscamos , sin embargo una diferencia importante que observamos es que este nodo no tiene hijos es por esto que no observamos conexiones debajo de él. 

En esta tercera imagen observamos que avanzamos al siguiente nivel y comenzamos con los hijos del nodo más antiguo después del que es raíz, por lo tanto, son los hijos de D que en este caso son H y C, comenzamos con H y vemos que se añade a la cola esto como consecuencia de que no es aún solución, en la siguiente imagen observamos que ya se expandió H y tiene un solo hijo sin embargo esto ya no es relevante, ya que a continuación tenemos el Nodo c, que es el nodo que estamos buscando  por lo tanto ya no se expandió este nodo ni los que siguen. 

Este algoritmo reinicia el recorrido para verificar que el camino que encontró sea el óptimo, es por eso que de nueva cuenta comenzamos en A, ya que este nodo era el más antiguo que se encontraba en nuestra cola y aplicando el procedimiento FIFO, el más antiguo es el primero en salir, por esta misma razón es que el nodo que continua es B y como observamos estos dejan de estar en la cola. 

 

De igual forma en esta imagen continuamos con el mismo proceso que el anterior, al ser F el que sigue en la cola sale y continuamos con G de esta forma el algoritmo verifica que la secuencia que obtuvo en el primer recorrido sea la correcta.  

Por último, en esta imagen observamos que nuestro algoritmo termina de verificar que efectivamente tomo el camino optimo y correcto. Ya que la lista queda vacía y obtuvo el mismo recorrido y llego al nodo que estaba buscando. Otro punto importante a destacar es la confirmación de que efecto a pesar de que los nodos puedan tener hijos no es necesario recorrerlos a todos para encontrar el mejor camino.  


