### Hash table (ESTRUTURA DE DATOS)

Las tablas hash son una estructura de datos que nos permite llaves y valores de tal forma de que nos dan una búsqueda de manera eficiente para el tiempo de búsqueda. 
Se puede implementar en vectores unidimensionales , bidimensionales o multidimensionales. pero aun asi con lo que puede aportar tiene varios posibles problemas que se puede enfrentar si de algunos casos.

#### llaves y valores , Función hash

Para poder definir la llave se necesita un algoritmo para poder sacarla , que puede ser a tu gusto pero tiene que ser bueno para que pueda ocupar todos los espacios de tu vector , asi que no te servirá cualquier cosa para la función hash.

==Ejemplo== 

se da la necesidad de querer guardar 10 contactos de personas , y pues lo que haríamos seria crear un vector y almacenarlos de manera secuencial empezando desde el uno , lo cual seria bien por el tamaño pero pongámonos mas locos y que pasa si tengo un millón de contactos , seria eterno la búsqueda para encontrar el numero de X persona porque podría iterar hasta el ultimo espacio del vector. 
En este caso podemos usar una **TABLA HASH** para poder ir directamente por el numero de la persona sin dar muchas vueltas pero ¿Cómo se haría?

Básicamente seria encontrar un algoritmo donde puedas sacar un índice único para la llave y que ese sea el espacio del valor que queremos guardar .

podemos usar diferentes cosas para sacar la llave pero en este caso pensaremos en la tabla ASCII
que nos dará valores de los caracteres del nombre y los sumaremos y luego le sacaremos un modulo de 100 para poder extraer una parte del numero y que ese sea su índice en el vector.
Asi seria una forma mucho mas rápida de llegar a nuestro valor sin pasar por los demas.



#### Colisiones de Hash

Básicamente seria el caso de que haríamos si una clave que obtenemos bota un índice que ya esta ocupado en el vector.

Realmente una buena Tabla hash se ve cuando sucede estos casos. o como la tabla hash evita que sucedan colisiones o que suceda el mínimo de colisiones posibles.

#### Posibles soluciones

###### OPCION A

Rehash o linear probing o oppen adressing son los nombres conocidos de esta posible solución que seria la mas rapida pero no eficiente .

Basicamente seria buscar el siguiente espacio libre en el vector para poder colocar la clave y guardarla pero vuelve a ocurrir el mismo problema y que pasa si ese igual esta ocupado o si todos estan ocupado , puedes caer en un bucle infinto o una busqueda demasiado larga si tu vector es demasiado grande.

###### Opcion B 

Abrir una lista enlazada , no conozco nda sobre esta posible solucion es primera vez que lo oigo pero lo que se haria sencillamente es que en ese indice se habrian mas espacios y no solo guardaria uno sino varios valores en ese indice y se tendria que iterar para poder acceder a los valores en ese indice.

IMAGEN COMO GRAFICA PARA PODER ENTENDER

![[Pasted image 20260207222750.png]]

Aunque la solucion es interesante se vuelve obtener el problema del principio de que pasaria si ese tamaño es demasiado grande entonces tomatia demasiado tiempo para poder encontrarlo.

######  Opcion C 

un poco Simple seria simple cambiar la formula o algoritmo que tenemos para poder sacar o obtener la llave y buscar uno de tal manera de que no suela dar numero repetidos aunque dará números repetidos en varios casos lo que no nos gustaría seria de que fuera a menudo .

por ejmplo , agregar multiplicacion despues de sumas los valores de los caracteres o X operacion para poder cumplir nuestro objetivo.