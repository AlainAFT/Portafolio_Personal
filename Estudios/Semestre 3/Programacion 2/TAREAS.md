

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

## heap sort

## binary search


# enlaces

[[TAREAS#consulta 2]]  enlace donde se saca info de esto : (https://www.geeksforgeeks.org/dsa/merge-sort/)