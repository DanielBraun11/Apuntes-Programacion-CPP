# Array
El array es un tipo de dato contenedor. Consiste en una variable que contiene datos de otro tipo de datos concreto y con un tamaño especificado y limitado.
Para hacer uso de este tipo de dato debemos importar su libreria #include <array>. Si no ponemos la libreria nos dará un error al compilar nuestro código.

![Texto alternativo](https://i0.wp.com/somoshackersdelaprogramacion.es/wp-content/uploads/2022/05/arrays01.jpg?resize=500%2C189&ssl=1)

## Estructura e inicialización
```c++
#include<iostream>
#include<array>
using namespace std;

int main(){
    //array<Tipo de dato que almacen, Tamaño del array> nombreArray;
    array<int,3> almacen1 = {1,2,3};
    array<char,4> almacen2 {'a','e','i','o','u'};  //ERROR
    array<string,4> almacen3 {"Daniel","Diego"};   //VALIDO
    
        
    return 0;
}
```
Como vemos en el ejemplo anterior, si creamos un array y lo rellenamos con un número de datos menor al espacio con el que contamos no hay ningun problema.
Sin embargo si creamos un array de un determinado tamaño y lo inicilizamos con un número mayor de datos como ocurre en el 'almacen2' nos dará un error de compilación.
## Entrada y salida de datos de un array
```c++
#include<iostream>
#include<array>
using namespace std;

int main(){
    array<int,4> almacen1 {1,2,3,4}; //Inicializado rellenado
    array<float,3> almacen2 {}; //Inicializado vacio

    //Para rellenar usamos bucles for( ; ; )
    for(int i{0} ; i<almacen2.size() ; i++){
        cout<<"Dato "<<i<<": ";
        cin>>almacen2.at(i);
    }

    //Para mostrar los datos usamos bucles for( : ) también
    for(float numero : almacen2){
        cout<<numero<<", ";
    }

    cout<<endl;

    //Mostrar con el for(; ;)
    for(int i{0} ; i<almacen2.size() ; i++){
        cout<<almacen1.at(i)<<", ";
    }
    
    cout<<endl;

    return 0;
}
```
Es importante recordar que en programación las posiciones se empiezan a contar desde el numero 0. También que si introducimos en el array un valor que no pertenece 
al tipo de datos que almacena el array nos dará un error de compilación. En esta inicialización recorremos el array increemtnando su posicion en 1 hasta llegar a su 
maximo tamaño y vamos introduciendo los valores que se almacenar en esas posiciones. Por eso a la hora de mostrar volvemos a recorrer el array posición por posición 
mostrando su contenido.
