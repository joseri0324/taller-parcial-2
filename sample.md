# Algoritmos de Ordenación

Este proyecto proporciona una implementación práctica de tres algoritmos de ordenación clásicos: Bubble Sort, Insertion Sort y Selection Sort. Se comparan sus tiempos de ejecución al ordenar una lista de libros por diferentes criterios.

## Algoritmos Implementados

### Bubble Sort

El algoritmo **Bubble Sort** es un algoritmo de ordenación simple que recorre repetidamente la lista, compara elementos adyacentes y los intercambia si están en el orden incorrecto. Este proceso se repite hasta que la lista esté ordenada.

#### Ventajas
- Fácil de entender e implementar.
- Útil para listas pequeñas o casi ordenadas.



### Insertion

El algoritmo **Insertion** Sort construye la lista ordenada de forma gradual, insertando cada nuevo elemento en su posición correcta en la lista ya ordenada.


#### Ventajas
- Eficiente para listas pequeñas.

- Estable (mantiene el orden de los elementos iguales).

#### Desventajas
- Ineficiente para listas grandes debido a su complejidad temporal O(n^2).

### Selection

El algoritmo **Selection** encuentra el elemento mínimo de la sublista no ordenada y lo intercambia con el primer elemento de esa sublista. Este proceso se repite hasta que toda la lista esté ordenada.

#### Ventajas
- Fácil de entender e implementar.

- No requiere memoria adicional.

#### Desventajas
- Ineficiente para listas grandes debido a su complejidad temporal O(n^2).

- No es estable (no mantiene el orden de los elementos iguales).
  
  ### LA MEJOR OPCION EN LOS 3 ALGORITMOS

   si necesitas estabilidad y estás trabajando con listas pequeñas, **Insertion** es una buena opción. Para listas casi ordenadas, Bubble Sort puede ser útil.