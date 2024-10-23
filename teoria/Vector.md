# Vector
El vector es un tipo de dato contenedor con la característica de que su tamaño es infinito. Es una variable que puede contener tantos datos como queramos de un mismo tipo de dato (int,float,char,string,array...). Para hacer uso de este tipo de dato debemos importar la libreria #include<vector>. Si no la importamos tendremos errores de compilación en nuestro código.
## Estructura e inicialización
En este ejemplo veremos que ya no hace falta especificar el tamaño que tendrá nuestro contenedor dado que este tiene un tamaño infinito. Por ello solo especificamos el tipo de datos que almacenará. Ejemplo:
```c++
#include<iostream>
#include<vector>
using namespace std;

int main(){
    //vector<tipo de datos que almacena> nombreVector;
    vector<int> almacen1 {1,2,3,4};
    vector<char> almacen2 = {'a','e','i','o','u'};
    vector<string> almacen3 {"Daniel", "Marcos", "Urosa"};

    return 0;
}
```
## Entrada y salida de datos
### Entrada
```c++
#include <iostream>
#include <vector>

int main() {
    vector<int> numeros;
    int cantidad, valor;

    cout << "¿Cuántos números quieres ingresar? ";
    cin >> cantidad;

    for (int i = 0; i < cantidad; i++) {
        cout << "Introduce el número " << i + 1 << ": ";
        cin >> valor;
        numeros.push_back(valor);  // Agregar valor al vector
    }

    cout << "Números en el vector: ";
    for (int i = 0; i < numeros.size(); i++) {
        cout << numeros[i] << " ";  // Mostrar los números almacenados
    }
    
    return 0;
}
```

### Salida
```c++
#include <iostream>
#include <vector>
#include <string>

int main() {
    vector<std::string> palabras;
    int cantidad;
    string palabra;

    cout << "¿Cuántas palabras quieres ingresar? ";
    cin >> cantidad;

    // Entrada de palabras
    for (int i = 0; i < cantidad; i++) {
        cout << "Introduce la palabra " << i + 1 << ": ";
        cin >> palabra;
        palabras.push_back(palabra);  // Agregar palabra al vector
    }

    // Salida de palabras
    cout << "Palabras en el vector: ";
    for (int i = 0; i < palabras.size(); i++) {
        cout << palabras[i] << " ";  // Mostrar las palabras
    }

    return 0;
}
```

## Funciones para vectores
## Push back
Esta función agrega un elemento al final del vector.
```c++
#include <iostream>
#include <vector>

int main() {
    vector<int> numeros;
    numeros.push_back(5);  // Añade el número 5 al final
    numeros.push_back(10); // Añade el número 10 al final

    cout << "Vector: ";
    for (int i = 0; i < numeros.size(); i++) {
        cout << numeros[i] << " ";  // Muestra: 5 10
    }

    return 0;
}
```
## At
Puedes acceder a los elementos del vector usando el índice ([]) o la función at().
```c++
int valor1 = numeros[0];  // Accede al primer elemento (5)
int valor2 = numeros.at(1);  // Accede al segundo elemento (10)
```
## Size
La función size() devuelve el número de elementos en el vector.
```c++
cout << "El vector tiene " << numeros.size() << " elementos." << endl;
```
## Pop Back
Esta función elimina el último elemento del vector.
```c++
numeros.pop_back();  // Elimina el 10 (último)
```
## Empty
La función empty() devuelve true si el vector no tiene elementos.
```c++
if (numeros.empty()) {
    cout << "El vector está vacío." << endl;
} else {
    cout << "El vector NO está vacío." << endl;
}
```
## Clear
Esta función vacía completamente el vector.
```c++
numeros.insert(numeros.begin(), 3);  // Inserta el número 3 en la primera posición
```
## Insert
Puedes insertar un elemento en cualquier posición del vector usando la función insert().
```c++
numeros.insert(numeros.begin(), 3);  // Inserta el número 3 en la primera posición
```
## Erase
Puedes eliminar un elemento de una posición determinada usando erase().
```c++
numeros.erase(numeros.begin());  // Elimina el primer elemento
```


