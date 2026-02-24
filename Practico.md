
# 1. ¿Cómo tienen que ser inicializados los atributos en una pila y cola vacía?

**Pilas**

Tienen que inicializarse con el puntero que se dirige al inicio de la pila conocido como  `puntero TOP` y su valor de este puntero tiene que ser `puntero TOP = 0` para indicar de que no tiene ningún elemento. El tamaño seria de 0

**Colas**

Tienes que definir varias cosas como el inicio , el detrás y el tamaño.

```
queue.front =-1
queue.rear=-1
queue.size = 0

```

claro si son punteros tienen que ser `NULL`

# 2. Ilustre la siguiente secuencia de operaciones sobre una pila vacía implementada en un arreglo S`[1 . . . 6]`: Push(S,4), Push(S,1), Push(S,3), Pop(S), Push(S,8), Pop(S)

`S[6];` el arreglo de 6 elementos

1. PUSH(S,4)
se introduce 4
   `S[6] = | 4 |  |  |  |  |  |`

2. PUSH(S,1)
se ingresa 1 
`S[6]=| 4 | 1 |  |  |  |  |`

3.PUSH(S,3)
`S[6]=| 4 | 1 | 3 |  |  |  |`

4. POP(S)
se sale 3 que es el ultimo elemento
`S[6] =| 4 | 1 |  |  |  |  |`
5. Push(S,8)
se introduce 8
`S[6] =| 4 | 1 | 8 |  |  |  |`

6. Pop(S)
se retira el ultimo elemento que es 8
`S[6] =| 4 | 1 |  |  |  |  |`

# . Explique como implementar dos `[pilas]` sobre un arreglo `A[1 . . . n]` de tal forma que ninguna inserción haga `“overflow”` a menos que el numero total de elementos en las dos `[pilas]` sea n. Todas las operaciones deben correr en tiempo constante


Bueno tendrían que empezar la primera pila desde el inicio del array y la segunda desde el final del arreglo.
```
Arr[]=| | | | | | | | | | | |  |
       ^                      ^
    pila1                   pila2
   
```

la pila1 crecería para el lado derecho  y la pila2 crecería para el lado izquierdo

```
A[1]  →→→→→→→→→→→→→→→→  A[n]
[Pila 1 crece →]   [← Pila 2 crece]
```


el `overflow ` ocurría cuando el top de la pila1 alcanza al top2 de la pila2 osea 

```
if(top1+1==top2) cout<<"overflow"
return arr[top++]
```


# 4. Ilustre la siguiente secuencia de operaciones sobre una cola vacıa implementada en un arreglo Q`[1 . . . 6]:` En queue(Q,4), En queue(Q,1),En queue(Q,3), De queue(Q), En queue(Q,8), De queue(Q) 

![[IMG_20260224_173316_edit_46075102690235.jpg]]


#  Mientras las colas y pilas permiten la inserción/eliminación de elementos en un solo lado, una deque (double-ended queue) permite la inserci´on/eliminaci´on de elemenetos en ambos lados. Escriba 4 operaciones de tiempo constante para insertar/eliminar elementos de ambos lados de un dequeu implementado sobre un arreglo

