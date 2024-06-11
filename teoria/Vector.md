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
