
# Teoría de errores

## Concepto de error

## fuentes de error

## precisión y exactitud

## error absoluto 
## error porcentual relativo
# [[ecuaciones lineales y no lineales]]

las lineales serian las que tendrían solo coeficientes en las variables que podrían ser una o varias variables de búsqueda
$$
x + y = 2 
$$

$$
2x + 2y = 4
$$


las no lineales vendrían siendo cosas mas complicadas y complejas  y es por eso que pueden adoptar como respuestas como conjuntos de respuestas , .

$$
x^2 + y^2 = 12  ;
 xy = 16

$$

# raíz de una ecuación 

Son los cortes en el eje x que serian las soluciones para la ecuación

# teorema de [[Bernhard Bolzano ]]



Explica básicamente que si en una función continua con intervalos cerrados ej: a y b  y toma valores de signo contrarios en los extremos , es casi 100 % seguro de que hay un punto de corte en el eje X o intersección osea al menos un valor tal que pertenezca dentro del rango a y b  y que sea 0 en y.

![[Pasted image 20260209220451.png]]

![[Pasted image 20260209220506.png]]

![[Pasted image 20260209220523.png]]

En este teorema es de suma importancia que la función sea continua, esto nos permite representar su gráfica como una cuerda que consta de una sola pieza. Si la recta horizontal ![](https://cdn-blog.superprof.com/blog_all/wp-content/uploads/latex/e501a40c21748382df3bef6e16458c350ce7fcf7.png) representa el eje ![](https://cdn-blog.superprof.com/blog_all/wp-content/uploads/latex/4c3ad613bf7d49cecebabe36592057611e792683.png) y los extremos de la cuerda se encuentran en lados opuestos respecto al eje ![](https://cdn-blog.superprof.com/blog_all/wp-content/uploads/latex/4c3ad613bf7d49cecebabe36592057611e792683.png), entonces la cuerda tiene que pasar sobre dicho eje coordenado, esto es, intersecta al eje ![](https://cdn-blog.superprof.com/blog_all/wp-content/uploads/latex/4c3ad613bf7d49cecebabe36592057611e792683.png) por lo que es una raíz de la función.

basta aclarar de que el teorema de Bolzano solo afirma o garantiza de que aun una intersección en el eje X pero no nos dice como hallarla .

![[IMG_20260209_221353_edit_90134195663167.jpg]]

Forma de hallar raíces. 
# método de la bisección


Es un [[algoritmo]] o metodo que se usa en las matematicas para poder hallar raices que trabaja diviendo el intervalo a la mitad que tenemos y sellecionando un subintervalo que tiene la raiz 

El método consiste en lo siguiente:

- Debe existir seguridad sobre la continuidad de la función f![{\displaystyle f}](https://wikimedia.org/api/rest_v1/media/math/render/svg/132e57acb643253e7810ee9702d9581f159a1c61) en el intervalo [a,b]![{\displaystyle [a,b]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/9c4b788fc5c637e26ee98b45f89a5c08c85f7935)
- A continuación se verifica que f(a)⋅f(b)<0![{\displaystyle f(a)\cdot f(b)<0}](https://wikimedia.org/api/rest_v1/media/math/render/svg/3a213db28622fa329e3458fb3a239503141ef762)
- Se calcula el punto medio m![{\displaystyle m}](https://wikimedia.org/api/rest_v1/media/math/render/svg/0a07d98bb302f3856cbabc47b2b9016692e3f7bc) del intervalo [a,b]![{\displaystyle [a,b]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/9c4b788fc5c637e26ee98b45f89a5c08c85f7935) y se evalúa f(m)![{\displaystyle f(m)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/be96847d02a80c6308e98140025d550f5c2262da) si ese valor es igual a cero, ya hemos encontrado la raíz buscada
- En caso de que no lo sea, verificamos si f(m)![{\displaystyle f(m)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/be96847d02a80c6308e98140025d550f5c2262da) tiene signo opuesto con f(a)![{\displaystyle f(a)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/368cb4b81ba5754d7a354a4ce49c2f1084bdaace) o con f(b)![{\displaystyle f(b)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/adbef9aaf500c30a3f107e5d7efb7a8627d3bba9)
- Se redefine el intervalo [a,b]![{\displaystyle [a,b]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/9c4b788fc5c637e26ee98b45f89a5c08c85f7935) como [a,m]![{\displaystyle [a,m]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/ce903ed54046fcc9c50f5a45ca62e545f4e71def) o [m,b]![{\displaystyle [m,b]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/3bf458d30458fded25e1eea62d0ed25828436344) según se haya determinado en cuál de estos intervalos ocurre un cambio de signo
- Con este nuevo intervalo se continúa sucesivamente encerrando la solución en un intervalo cada vez más pequeño, hasta alcanzar la precisión deseada

En la siguiente figura se ilustra el procedimiento descrito.

El método de bisección es menos eficiente que el [método de Newton](https://es.wikipedia.org/wiki/M%C3%A9todo_de_Newton "Método de Newton"), pero es mucho más seguro para garantizar la convergencia. Si f![{\displaystyle f}](https://wikimedia.org/api/rest_v1/media/math/render/svg/132e57acb643253e7810ee9702d9581f159a1c61) es una [función continua](https://es.wikipedia.org/wiki/Funci%C3%B3n_continua "Función continua") en el intervalo [a,b]![{\displaystyle [a,b]}](https://wikimedia.org/api/rest_v1/media/math/render/svg/9c4b788fc5c637e26ee98b45f89a5c08c85f7935) y f(a)f(b)<0![{\displaystyle f(a)f(b)<0}](https://wikimedia.org/api/rest_v1/media/math/render/svg/bcf828d0f70a94d206b1a11efe2d032da7610fd2), entonces este método [converge](https://es.wikipedia.org/wiki/Convergencia_\(matem%C3%A1ticas\) "Convergencia (matemáticas)") a la raíz de f![{\displaystyle f}](https://wikimedia.org/api/rest_v1/media/math/render/svg/132e57acb643253e7810ee9702d9581f159a1c61). De hecho, una cota del error absoluto es:

> |b−a|2n![{\displaystyle {\frac {\left|b-a\right|}{2^{n}}}}](https://wikimedia.org/api/rest_v1/media/math/render/svg/adc9a5d3c6cd57ab2a252858b52003595fb43adf)

en la _n_-ésima iteración. La bisección [converge linealmente](https://es.wikipedia.org/wiki/Orden_de_convergencia "Orden de convergencia"), por lo cual es un poco lento. Sin embargo, se garantiza la convergencia si f(a)![{\displaystyle f(a)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/368cb4b81ba5754d7a354a4ce49c2f1084bdaace) y f(b)![{\displaystyle f(b)}](https://wikimedia.org/api/rest_v1/media/math/render/svg/adbef9aaf500c30a3f107e5d7efb7a8627d3bba9) tienen distinto signo.

Si existieran más de una raíz en el intervalo entonces el método sigue siendo convergente pero no resulta tan fácil caracterizar hacia qué raíz converge el método.



# metodo de puntos
