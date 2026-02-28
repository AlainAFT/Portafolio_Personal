

# consulta 1
#investigacion 
# ¿que es el principio de induccion completa y como se relaciona con la recursion?(consulta) 


## que es induccion completa o induccion matematica?

Es una herramienta para poder deducir propiedades o demostrarlas  . Estan relacionadas con el cnjunto de  numeros naturales.
Su fundamentación se basa en el Principio de Buena Ordenación y el conjunto de Axiomas de Peano.  
En la resolución de problemas, la inducción matemática no es sólo un medio para probar una fórmula existente, sino también una poderosa metodología para encontrar tales fórmulas en primer lugar.

## cuerpo de la induccion completa

![diagrama](https://github.com/AlainAFT/Portafolio_Personal/blob/main/imagenes%20conectadas/Pasted%20image%2020260206222512.png?raw=true)
### Base inductivo 

Es lo que suponemos que va a suceder para que empiece la secuencia o para verificar nuestra teoría 


La base inductiva nos quiere decir de que la preposición o propiedad que queremos demostrar tiene que ser validad para un caso o primer valor de n  .

### hipótesis inductiva



### Paso inductivo

Bajo el base inductivo , tenemos que corroborar de que se cumple en los demas casos que se puede tener con n 

Es ya con lo primero sucedido ,verificar que es continuo osea corroborar de que la propiedad o formula ocurre con todos los casos .

A todo esto se le llama el principio de la inducción completa o inducción matemática.

## ¿Cómo coño la inducción matemática  se relaciona esto con la recursividad?

se relacionan porque ambas quieren llegar al mismo punto pero lo hacen de diferente manera .

La inducción matemática es una forma de garantizar de que una formula o propiedad es cierta en todos los casos empezando por un valor inicial n .

por que prácticamente lo que que hace la inducción es buscar que se cumpla para el primer valor n y luego corroborar si se cumple para n+1 y si se da , eso nos garantiza de que sucede para los demas números sin necesidad de verificar con los con los números reales .

y a esto la recursividad le sirve para poder  estar  segura de que funcionara con todos los números y no solo con el caso base , La inducción es la que justifica matemáticamente que las definiciones recursivas funcionen bien en los números naturales.

La recursión define cómo calcular algo usando versiones más pequeñas de sí mismo. La inducción prueba que esa definición funciona y cubre todos los números naturales sin dejar huecos.


## EJEMPLO

### Basico de los naipes o fichas

Hablamos de las fichas paradas de manera consecutiva. 

Para poder empezar necesitamos que se cumpla para un caso del primer valor de N qur podemos decir que la primera ficha es N. 

suponiendo de que esa ficha se va caer, tenemos que verificar si n+1 cae igual. 

Si cae N y tumba la ficha de adelante suyo entoces tumba n+1 y eso corrobora de que sucede para las demas fichas. 


# consulta 2 

#investigacion 
# investigación sobre algoritmos de ordenamiento

## merge sort

Lo que define  a este algoritmo de ordenamiento es  *divide y conquista*

**mas o menos que va hacer?**

va a dividir el array o vector que nos dan con los números desordenados , y los va partir a la mitad y ordenara independientemente las dos sub vectores o arrays , y luego comparara los números de estas dos sub listas y para decidir en que orden van a entrar . 

**imagen para ilustrar como seria :**

![](https://media.geeksforgeeks.org/wp-content/uploads/20250923102849709166/arr_.webp)


**Paso a paso de lo que hace el merge sort :**
- *Dividir :* De manera recursiva va dividendo o partiendo  el array o lista a mitades hasta que no se puede dividir mas.


- *Conquistar :* Cada sub_array que se crea es ordenado de manera individual usando el algoritmo "Merge Sort"

- *Merge :* Aquí es donde se decide el orden en el que van a entrar los números en la lista o array original o principal

**Recurrencia Relacion de Merge Sort**

![[Pasted image 20260219111143.png]]

$$
T(n)= 2T(n/2)+O(n)
$$
- T(n)  -> El tiempo que le toma para ordenar la lista de numero de tamaño n

- O(n)  -> es el tiempo que se toma en ordenar la lista cuando ya tiene las dos mitades ordenadas de la lista primaria o principal

- 2T(n/2)  -> es el tiempo que se toma para ordenar la dos mitades que saco de manera recursiva 

**ventajas y desventajas**

*ventajas*
sus ventajas son la estabilidad que tiene este algoritmo , no importa el orden o como este el orden de los números en la lista siempre mantiene el orden relativo de los elementos en la lista.
Tiene el peor caso de complejidad de tiempo que  es  :
$$
O(N *log(N))
$$
lo cual responde bien para lista masivas .

*desventajas*

Usa mucho espacio en la memoria , para este ordenamiento necesitas espacio adicional durante el guardado de los arrays que han sido cortados a la mitad , asi que si tu problema o preocupación es el uso de memoria este tipo de ordenamiento no es el indicado.

## quick sort 

Este algoritmo de ordenamiento es muy parecido al merge sort por que lo toma como base su idea de **Divide y Conquista** pero tiene las diferencias para ser el ordenamiento y sus diferentes con resultados mas rápidos que los demas algoritmos de ordenamiento.

**Principales pasos del algoritmo**

1.  *Elegir un pivote *  -.  Se elige un elemento del array como pivote   ejemplos :(El primer elementos , el ultimo elemento , el elemento que esta al medio o de manera randomica)

2. *Partir el array * -. Se mueven los elementos acorde al pivote , a la izquierda los elementos menores que el y a la derecha los elementos mayores que el.

 3. *Aplicar recursividad * -. Se aplica de manera igual para las sub listas que se crearon

4. *Caso base *-. La recursión terminara cuando solo halla un elemento en la lista y ya este ordenado ese elemento .

**imagen para ilustrar :**

![](https://media.geeksforgeeks.org/wp-content/uploads/20240926172924/Heap-Sort-Recursive-Illustration.webp)

**Las formas de partir de la lista :**

- Naive partition : Lo que hace primero es introducir los numeros menores y luego los mayores , para finalmente en un lista temporal pasar los resultados a la lista orginal.

- Lomuto Partition : Es mas agradable para la memoria , lo que hace es guardar los índices de los elementos menores y moverlos hacia el lado izquierda de manera continua hasta llegar con la lista ordenada

- Hoare Partition : Este es el mas rápidos de todas la variaciones de este algoritmo de ordenación, 
  Aquí recorremos la matriz desde ambos lados y seguimos intercambiando un elemento mayor a la izquierda con el más pequeño a la derecha mientras la matriz no está dividida.



## heap sort


Se la ve a la lista de numeros  como arbol y se hace que el se repete el orden de que los numeros mas mayores por arriba de los menores y todo por nodoos o niveles y el primer nivel es donde nos topamos el mas mayor de los numeros, y lo que hacemos luego es enviar ese numero grande a ala ultima posicion de la lista y para la siguiente iteracion del algoritmo no tomamos en cuenta al ultimo porque suponemos que esta ya ordenado.

**Pasos importantes **

*tratarlo como arbol*

vemos que el inicio del árbol es el índice 0 y luego vemos que sus hijas son los siguientes índices *2i+1*  y *2i+2*  esto te da dos hijas una para la izquierda y otra para la derecha 

![](https://media.geeksforgeeks.org/wp-content/uploads/20240928160744/Visualize-the-array-as-a-complete-binary-tree.webp)

*Construir el Max heap*

Mueves los números de tal forma que en el 0 quede el numero mas grande 

![](https://media.geeksforgeeks.org/wp-content/uploads/20240927200909/Heapify-Binary-Tree-1.webp)


![](https://media.geeksforgeeks.org/wp-content/uploads/20240927200910/Heapify-Binary-Tree-3.webp)

*Enviar el numero mas grande a la ultima posición*

Se intercambia de posición con el ultimo numero en la lista  y luego se reduce el tamaño que tenemos en variable de la lista para que no tome en cuenta al ultimo numero porque ya esta ordenado.

![](https://media.geeksforgeeks.org/wp-content/uploads/20240928160828/Remove-from-Max-Heap-2.webp)


## Shell Sort


inventor : El método se denomina **Shell** en honor de su inventor [Donald Shell](https://es.wikipedia.org/w/index.php?title=Donald_Shell&action=edit&redlink=1 "Donald Shell (aún no redactado)").

Es un algoritmo que es in-place y es una optimización del insertion sort , reduce los números de intercambios en largas listas significativamente .

Compara los elementos que están apartados por el gap y gradualmente se reduce esta distancia permitiendo intercambios mas rápidos de elementos en la lista.

**Pasos**

*Elegir la distancia o gap en la que se va comparar normalmente es de la mitad de la lista de elementos *


*Ordenas los elementos dentro de cada gap con el algoritmo INSERTION SORT*

*Reduces la distancia o el gap hasta que te de 1 *


**inicio**

![](https://media.geeksforgeeks.org/wp-content/uploads/20251027160304040549/420046893.webp)


**Luego de cada iteración se va comparando los números , enviando los números menores al lado izquierdo **

![](https://media.geeksforgeeks.org/wp-content/uploads/20251027160304276659/420046894.webp)

**Cada vez que lleguemos hasta al final de la lista debemos reducir gradualmente la distancia o gap**

![](https://media.geeksforgeeks.org/wp-content/uploads/20251027160304699301/420046895.webp)

# consulta 3 
# ¿Qué es un paradigma?

Las definiciones que consulte están basadas y inspiradas en lo que decía `Thomas Kunh` en su libro sobre las `Revoluciones Cientificas`.

Un **Paradigma** es un conjunto de creencias , verdades , técnicas , practicas y valores aceptados por una comunidad de personas , aunque `Thomas Junh` comunidad científica por que hablaba mas sobre el campo científico. ==El Paradigma viene siendo los lentes o foco de como veremos el mundo y eso dependerá lo que se cree como verdad absoluta en ese momento de la historia==.

Quiere decir de que esa forma de ver el mundo , las cosas o el contexto no se cuestiona hasta que sal un paradigma dominante y lo remplace.  Esto es mas conocido como revoluciones científicas y `Thomas` decía que la ciencia estaba conformada por dichas revoluciones.

## revoluciones 

La revoluciones son el cambio de paradigma o la transición a un paradigma dominante porque el actual paradigma no tiene respuestas para ciertas anomalías o casos.

Estas revoluciones ocurren cuando se produces las dichas anomalías que nuestro paradigma actual no puede responder o no se puede hallar sentido a lo que esta ocurriendo , es aquí cuando encontramos una posible revolucion o ==CAMBIO DE PARADIGMA== porque se encuentran inconsistencias en la teoría existente.

`Thomas Kunh` igual explica la existencia de dos facciones que son la `Ciencia Normal` y `Ciencia Extraordinaria` que explica mas o menos como operan diciendo que la *Normal* no busca juzgar el paradigma existente y que la *Extraordinaria* busca juzgarla debido a la fallas de explicar ciertos fenómenos.

**Ejemplo : **

**Transición de la teoría geocéntrica a la heliocéntrica**

Esta cambio va naciendo porque la teoria geocentrica no podia explicar a ciertos fenomenos que sucedian que dicha teoria no podia explicar eficientemente. Entonces, los astromonos se lanzan en buscar una teoria nueva o dominante que sea respalda por un gran grupo de cientificos y remplazar el paradigma actual. 
El teoria heliocentrica se va dando forma con el astronomo Copernico que explica que es el SOL el que esta en el centro y los demas cuerpos celeste son los que orbitan alrededor de el. Esto se fue aceptando por la comunidad y hasta que remplazo la teoria existente .

# ¿Qué es un paradigma en la programación?

 la programación es resolver problemas humanos atreves del apoyo de las maquinas y la resolución de esos problemas pueden tener diferentes camino que algunos pueden ser decentes , peores o el mejor pero todos nos llevan al mismo resultado . 
 Pues esas formas o estructuras que seguimos son paradigmas en la programación.
Estos paradigmas ya están documentos donde especifican como es la estructura a seguir.

- Programación Estructurada -. Es secuencial , simple y la mas intuitiva para enseñar por su sencillez .  Empiezas de arriba hacia abajo , donde podemos repartir por funciones asi dividiendo el codigo pero cuando el proyecto o la cosa por hacer en muy grande , esta estructura queda muy expuesta porque es muy difícil de mantener el codigo porque se hace largo y difícil de detectar errores o agregar nuevas funcionalidades.

- Programacion Orienteada a Objetos : Es estructura que separa el sistema en entidades u objetos , hace de que cada entidad pueda tener caracteristicas y  metodos que pueden unicos. Aqui se puede aprender los terminos de herencia , polimorfismo , etc.

- Programacion Reactiva : Es una forma de programar que se dedica a ver los datos como fluyen hasta que tienen un cambio repentino y se realiza la ejecución del codigo.


- Programacion Funcional: Es una estructura basada en funciones , donde no se puede usar bucles y difurcaciones. 


# enlaces

[[TAREAS#consulta 2]]  enlace donde se saca info de esto : https://www.geeksforgeeks.org/