# Set
## ¿Qué es un set?

Un set es un contenedor de la STL (Standard Template Library) de C++ que almacena elementos únicos (no permite duplicados) en un orden específico.
Es muy útil cuando quieres asegurarte de que no haya elementos repetidos.

### Características:
- No permite duplicados.
- Ordenado automáticamente (generalmente en orden ascendente).
- La inserción, eliminación y búsqueda son eficientes (tiempo logarítmico).

### Sintaxis básica
```c++
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> conjunto;  // Declarar un set de enteros
}
```
### Insertar y acceder a elementos de un set
```c++
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> numeros;

    // Insertar elementos en el set
    numeros.insert(10);
    numeros.insert(5);
    numeros.insert(15);

    // Intentar insertar un duplicado (no se añadirá)
    numeros.insert(10);

    // Mostrar los elementos del set
    cout << "Elementos en el set: ";
    for (int num : numeros) {
        cout << num << " ";  // Salida: 5 10 15 (orden ascendente)
    }
    cout << endl;

    return 0;
}
```
### Salida
```c++
Elementos en el set: 5 10 15
```
## Funciones para set
## Insert
Añade un elemento al set. Si el elemento ya está presente, no se añadirá.
```c++
numeros.insert(20);  // Añade el 20 al set
```
## Erase
Elimina un elemento del set.
```c++
numeros.erase(10);  // Elimina el elemento 10 del set
```
## Find
Busca si un elemento está presente en el set. Devuelve un iterador al elemento si lo encuentra, o al final del set si no lo encuentra.
```c++
if (numeros.find(5) != numeros.end()) {
    cout << "El número 5 está en el set." << endl;
}
```
## Size
Devuelve el número de elementos en el set.
```c++
cout << "El set tiene " << numeros.size() << " elementos." << endl;
```
## Empty
Comprueba si el set está vacío.
```c++
if (numeros.empty()) {
    cout << "El set está vacío." << endl;
} else {
    cout << "El set NO está vacío." << endl;
}
```
## Size
Elimina todos los elementos del set.
```c++
numeros.clear();  // Elimina todos los elementos
```
## Ejemplo completo
```c++
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<string> nombres;

    // Insertar nombres en el set
    nombres.insert("Ana");
    nombres.insert("Juan");
    nombres.insert("Carlos");

    // Verificar si "Ana" está en el set
    if (nombres.find("Ana") != nombres.end()) {
        cout << "Ana está en el set." << endl;
    }

    // Eliminar "Juan"
    nombres.erase("Juan");

    // Mostrar el tamaño del set
    cout << "El set tiene " << nombres.size() << " elementos." << endl;

    return 0;
}
```
### Salida
```c++
Ana está en el set.
El set tiene 2 elementos.
```

