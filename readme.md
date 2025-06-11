# Preguntas para el examen de EDAII

Conjunto de preguntas para el examen de estructura de datos y algoritmica II.

## Pregunta 1: Como asegurar que un algortimo recursivo no desborde la pila.

R: Se busca garantizar la convergencia de las iteraciones dentro de las llamadas recursivas, eliminando comportamientos divergentes, delimitando un caso base efectivo, utilizando el backtracking para evitar seguir iterando en caminos donde el resultado no converge al caso base, usando estados parciales donde se resuelva parte del problema, ademas de mecanismos apropiados para elimina llamadas del stack

## Pregunta 2: Diferencias de la declaracion final en un atributo primitivo, un string, un objeto, una clase y un metodo.

R: La declaracion de un final normalmente puede llevar a dos resultados, un bloqueo de referencia o atributos en caso de primitivos.

En caso de los primitivos: Casa primitivo es distinto, se bloquean los valores tanto como la referencia.

En caso de los strings: se vuelven inmutables, no pueden ser modificados por ninguna operacion

en caso de objetos: sus referencias se vuelven inmutables, pero los atributos dentro de ellas pueden ser modificados sin problema.

en caso de clases: deja de poder ser heredable, es una clase inextendible.

En caso de un metodo: se vuelve inmune al polimorfismo y no puede ser modificado despues de ser heredado.

## Que es un hash?

R: un valor correspondiente a algun atributo, que ha pasado por una transformacion unidireccional, que garantiza una manera facil de encontrar el valor, ademas de una comprobacion ante la modificacion del mismo, evita coliciones y previene duplicados del mismo valor.

## por que no es posible un conjunto desordenado?

R: un conjunto es una agrupacion hecha tomando en cuenta las caracteristicas de algo, no puede existir un orden dentro de un conjunto debido a que es algo cualitativo, las cualidades no pueden tener orden

## Que aporta la inmutabilidad a la programacion funcional

R: la inmutabildad hace mas facil la concurrencia, es decir, se pueden realizar varias operaciones sobre un conjunto de datos y estar seguros que estos no se veran afectados si varias funciones estan trabajando sobre ellas, garantizando un flujo de trabajo sin errores, quitando una carga de desarrollo al implementarse

## Como se puede ordenar sin comparar?

R: Al aprovechar las propiedaes matematicas dentro de los valroes para evitar compararlos

Couting sort: se utiliza con datos no muy grandes, elige el valor mas grande, inicializa el array despues con el total maximo, luego le agrega a la posicion la cantidad encontrada por indice, una vez esta todo este recorrido, se va vaciando el indice y se agrega al array el numero correspondiente

Bucket sort: distribuye los valores dentro de cubos imaginarios que comprenden un rango de valores, donde se ordenan adentro, aprovechando el paradigma divide and conquer, tomando una suposicion que si es uba distribucion uniforme se repartira la carga entre varios, este es un algoritmo mixto, ya que toma las propiedades matematicas para la clasificacion y luego se ordena con comparacion

radix sort: procesa datos ediante multiples pasadas usando indice, comiensa desde el digito menos significativo hasta el mas, ordenando los elemento mediante la examinacion de cada posicion del mismo.

## como lo recursivo se vuelve iterativo

r: 1. Se crea una pila explicita, para simular la pila de llamadas

2. identificar estado: lo que se guarda en la pila

3. inicializar: se coloca el estado inicial

4. se implementa el bucle

5. se simulan las llamadas, agregando estados

6. se simula el retorno

## como lo iterativo se vuelve Recursivo:

1. identificar las variables de estado

2. convertir en parametros las variables de estado

3. definir el caso base

4. implementar el caso recursivo con las variables de estado

## Que es una interface?

r: Un contrato para implementar metodos comunes dentro de clases que les implementan, notese que ahora estas pueden venir ya implementadas

## que es un mapeo?

R: una manera de transforman elementos de una coleccion a otros elementos, se usa para conversiones de tipo, extraciones de propiedades, transformaciones matematicas y de objetos.

## Que es el Mapeo unidimensonal:

R: mapeo que aplana los resultados, eliminando estructuras anidadas, convierte muchos a uno

## Que es el filtrado:

r: Una operacion que permite la selecion de elementos que cumples condiciones especiricas

## Que es el reduce:

r: operacion que transforma multiples elementos a uno. se usa para sumas de listas, concatenacion, calculo de totales, o encontrar minimo o maximo

## cuales son las 3 maneras de hacer bucles

con estrucuturas de control while, for, pueden ser incrementales, decrementales o por flags.

## fases iteracion:

r:

1. inicializacion

2. condicion de continuacion

3. actualizacion

4. cuerpo del bucle

## Que es la fase de ida y que es la fase de vuelta (backtracking)

R: en la fase ida se exploran soluciones nuevas que van hacia una convergencia dentro del caso base, buscando estados intermedios de resolucion, la fase de vuelta en cambio solo ocurre cuando no existen un estado intermedio valido, donde se regresa a la parte anterior de la pila con el conocimiento de que el camino tomado no es el adecuado, esto se da hasta que exploren todas las opciones y sean eliminadas de la pila, garantizando que se evite el desbordamiento y no se gasten recursos en explorar ramas sin resolucion

## Ordenacion estable vs inestable

r: Un algoritmo de ordenación estable mantiene el orden relativo de los elementos con claves iguales después de ordenar, es decir, si dos elementos son iguales, aparecerán en el mismo orden que tenían originalmente. En cambio, un algoritmo de ordenación inestable puede cambiar el orden relativo de esos elementos, por lo que no garantiza que los elementos iguales conserven su posición original tras la ordenación.

## diferencias entre eficiencia y complejidad temporal en algoritmos

r:

1. La complejidad temporal es una medida teórica del tiempo de ejecución dependiendo del tamaño de entrada.

2. La eficiencia es la capacidad real del algoritmo de usar recursos de forma óptima, considerando factores prácticos como el hardware, la implementación y má

## Clasificacion metodos de ordenamiento

1. Según su método de funcionamiento

   Intercambio (Swap o Exchange):
   Ejemplos: Bubble Sort, Quick Sort
   Funcionan intercambiando pares de elementos para ordenarlos.

   Inserción:
   Ejemplo: Insertion Sort
   Construyen la lista ordenada insertando elementos uno a uno en su posición correcta.

   Selección:
   Ejemplo: Selection Sort
   Repetidamente seleccionan el elemento mínimo (o máximo) y lo colocan en su posición final.

   Fusión (Merge):
   Ejemplo: Merge Sort
   Dividen la lista en sublistas, las ordenan y las fusionan.

   Distribución (Distribution o Radix):
   Ejemplos: Counting Sort, Radix Sort, Bucket Sort
   Distribuyen los elementos en “cubetas” o utilizan técnicas de conteo/clasificación por dígitos.

2. Según su complejidad y rendimiento

   Algoritmos simples (no eficientes para grandes volúmenes):
   Bubble Sort, Selection Sort, Insertion Sort (O(n²))

   Algoritmos eficientes (usados en la práctica):
   Merge Sort, Quick Sort, Heap Sort (O(n log n))

   Algoritmos lineales (bajo ciertas condiciones):
   Counting Sort, Radix Sort, Bucket Sort (O(n))

3. Según su naturaleza

   Comparativos: Comparan elementos para ordenarlos.
   Ejemplos: Bubble Sort, Merge Sort, Quick Sort, Heap Sort

   No comparativos: No comparan elementos entre sí, sino que utilizan propiedades de los datos.
   Ejemplos: Counting Sort, Radix Sort, Bucket Sort

4. Según la estabilidad

   Estables: Mantienen el orden relativo de elementos iguales.
   Ejemplos: Bubble Sort, Merge Sort, Insertion Sort, Counting Sort

   No estables: Pueden cambiar el orden relativo de elementos iguales.
   Ejemplos: Quick Sort, Heap Sort, Selection Sort

5. Según su implementación

   Internos: Ordenan la estructura completa en memoria principal.
   Externos: Ordenan datos almacenados en memoria secundaria (archivos grandes).
