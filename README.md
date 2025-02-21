# DOCUMENTACION DEL CODIGO.

Este proyecto implementa tres algoritmos de ordenación diferentes (Bubble Sort, Insertion Sort y Selection Sort) para ordenar una lista de libros basada en diferentes criterios (año de publicación, número de reservas y título).

## Lista de Libros.

se representa como un arreglo de objetos, donde cada objeto contiene el título del libro, el año de publicación y el número de reservas.

````javascript
const libros = [
  { titulo: "Algoritmos Avanzados", año: 2018, reservas: 120 },
  { titulo: "Introducción a JavaScript", año: 2020, reservas: 90 },
  { titulo: "Estructuras de Datos", año: 2015, reservas: 60 },
  { titulo: "Sistemas Operativos", año: 2019, reservas: 110 }
];
````
## Bubble Sort

````javascript
const bubbleSort = (array, key) => {
  let swapped;
  for (let i = array.length - 1; i > 0; i--) { 
    swapped = false; 
    for (let j = 0; j < i; j++) { 
      if (array[j][key] > array[j + 1][key]) { 
        [array[j], array[j + 1]] = [array[j + 1], array[j]];
        swapped = true; 
      }
    }
    if (!swapped) break; 
  }
  return array;
};
````
- Se declara una variable swapped para llevar el registro de si se realizaron intercambios durante la iteración.

- Se realiza un bucle externo que recorre la lista de atrás hacia adelante.

- Dentro del bucle externo, hay un bucle interno que compara elementos adyacentes y los intercambia si están en el orden incorrecto.

- Si no se realizaron intercambios (swapped es false), el bucle se rompe para optimizar el rendimiento.

- La función devuelve el arreglo ordenado.
  
````javascript
console.time('Bubble Sort por Año');
const librosOrdenados = bubbleSort(libros, 'año');
console.timeEnd('Bubble Sort por Año');
console.log(librosOrdenados);
````

# ORDENAMINETO DE INSERTION:



Código:
````javascript
const insertionSort = (array, key) => {
  for (let i = 1; i < array.length; i++) {
    let current = array[i];
    let j = i - 1;
    while (j >= 0 && array[j][key] > current[key]) {
      array[j + 1] = array[j];
      j--;
    }
    array[j + 1] = current;
  }
  return array;
};
````

- Se guarda el elemento actual en la variable current.

- Se compara el elemento actual con los elementos de la lista ya ordenada y se desplaza hacia la derecha los elementos mayores.

- Se inserta el elemento actual en su posición correcta.

- La función devuelve el arreglo ordenado.


Para ordenar los libros por el número de reservas utilizando Insertion Sort, se mide el tiempo de ejecución con console.time y console.timeEnd.

````javascript
console.time('Insertion Sort por Reservas');
const librosOrdenadosreservas = insertionSort(libros1, 'reservas');
console.timeEnd('Insertion Sort por Reservas');
console.log(librosOrdenadosreservas);
````

# ORDENAMIENTO DE SELECCION: 

````javascript
Código:
javascript
function selectionSort(arr, key) {
  let n = arr.length;
  for (let i = 0; i < n - 1; i++) {
    let minIndex = i;
    for (let j = i + 1; j < n; j++) {
      if (arr[j][key].localeCompare(arr[minIndex][key]) < 0) {
        minIndex = j;
      }
    }
    if (minIndex !== i) {
      [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
    }
  }
  return arr;
}
````

Se busca el elemento mínimo en la sublista no ordenada.

Se intercambia el elemento mínimo encontrado con el primer elemento de la sublista no ordenada.

Se repite el proceso hasta que toda la lista esté ordenada.

La función devuelve el arreglo ordenado.





