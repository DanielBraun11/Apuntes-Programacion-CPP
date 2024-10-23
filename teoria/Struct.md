# Struct
## ¿Qué es una estructura?

Una estructura en C++ es una colección de variables (de diferentes tipos o del mismo tipo) agrupadas bajo un mismo nombre. Las estructuras se usan cuando necesitas almacenar varios datos relacionados que tienen distintos tipos.

Son útiles para representar objetos del mundo real, como un producto, un empleado o un punto en un plano.
### Sintaxis básica
```c++
struct NombreEstructura {
    tipo_dato1 nombre_variable1;
    tipo_dato2 nombre_variable2;
    // Más variables si es necesario
};
```
Después de definir la estructura, puedes declarar variables del tipo NombreEstructura.
## Ejemplo 1: Estructura simple
Definir una estructura para representar una persona
```c++
#include <iostream>
#include <string>

struct Persona {
    string nombre;
    int edad;
    float altura;
};

int main() {
    // Crear una variable de tipo 'Persona'
    Persona persona1;
    
    // Asignar valores a los campos de la estructura
    persona1.nombre = "Juan";
    persona1.edad = 25;
    persona1.altura = 1.75;

    // Mostrar los valores
    cout << "Nombre: " << persona1.nombre << endl;
    cout << "Edad: " << persona1.edad << endl;
    cout << "Altura: " << persona1.altura << " metros" << endl;

    return 0;
}
```
### Salida:
```c++
Nombre: Juan
Edad: 25
Altura: 1.75 metros
```

## Ejemplo 2: Estructura con varios objetos

Puedes crear varias variables de tipo estructura para manejar múltiples datos a la vez.
```c++
#include <iostream>
#include <string>

struct Producto {
    std::string nombre;
    float precio;
    int stock;
};

int main() {
    // Crear dos variables de tipo 'Producto'
    Producto producto1, producto2;

    // Asignar valores a producto1
    producto1.nombre = "Laptop";
    producto1.precio = 799.99;
    producto1.stock = 10;

    // Asignar valores a producto2
    producto2.nombre = "Mouse";
    producto2.precio = 19.99;
    producto2.stock = 50;

    // Mostrar los datos de los productos
    cout << "Producto 1: " << producto1.nombre << ", Precio: " 
              << producto1.precio << "€, Stock: " << producto1.stock << endl;

    cout << "Producto 2: " << producto2.nombre << ", Precio: " 
              << producto2.precio << "€, Stock: " << producto2.stock << endl;

    return 0;
}
```
### Salida:
```c++
Producto 1: Laptop, Precio: 799.99€, Stock: 10
Producto 2: Mouse, Precio: 19.99€, Stock: 50
```
## Acceso y modificación de datos

Para acceder o modificar los miembros de una estructura, puedes usar el operador . (punto).
```c++
persona1.nombre = "Carlos";  // Cambiar el nombre de persona1 a "Carlos"
```

## Resumen:
- Una estructura agrupa variables bajo un mismo nombre.
- Los miembros de una estructura pueden ser de tipos diferentes (int, float, string, etc.).
- Usamos el operador . para acceder o modificar los miembros de una estructura.
