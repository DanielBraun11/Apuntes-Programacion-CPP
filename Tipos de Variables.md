# Tipos de Variables
## String
La variable string nos sirve para almacenar cadenas de texto, ya sean palabras o frases.
Para crear una variable string solo pondremos la palabra reservada 'string' acompañada del nombre que le queramos poner a la variable.
Para inicializar una variable string se puede hcaer de muchas formas pero siempre pondremos su contenido entre comillas dobles "".
```c++
#include<iostream>
using namespace std;

int main(){
  string nombreVariable1{"Hola Mundo"};
  string nombreVariable2 = "Hola Mundo";
  string nombreVariable3;

  nombreVariable3 = "Hola mundo";

return 0;
}
```
## Entrada y salida de datos en Strings
String es un tipo de dato mas complejo que por ejemplo int, float o char. A la hora de guardar datos que puede introducir alguien por el terminal debemos hacerlo utilizando **getline()**.
La estructura de este sera: getline(cin, nombre de la variable donde guardemos nuestra cadena de texto);
Para mostrar estas cadenas de texto lo unico que deberemos hacer es un cout al igual que con las variables de tipo int, float y char.
Veamos un ejemplo:
```c++
#include<iostream>
using namespace std;

int main(){
  string nombreVariable;

  //Solicitar y guardar dato
  cout<<"Introduce una palabra o frase: "<<endl;  //Solicito
  getline(cin,nombreVariable);   //Guardo

  //Mostrar dato almacenado
  cout<<"El dato que has introducido es: "<<nombreVariable<<endl;
  

return 0;
}
```
# Funciones del tipo String
## size o lenght
Ambas funciones devuelven el tamaño del dato que esta almacenado en la variable string. Este tamaño puede ser de una palabra solo o de un texto. En el caso del texto, contará también los espacion ' ' entre las palabras que lo componen. Para su uso haremos .size() al nombre de la variable de la que queramos saber el tamaño: nombreVariable.size()
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};
    string nombreVariableTexto = "Voy a la uni en autobus";

    cout<<nombreVariablePalabra.size()<<endl;   //->12
    cout<<nombreVariableTexto.length()<<endl;   //->23

    return 0;
}
```
## resize
Modifica el tamaño a mayor o menor. Cuando modificas el tamaño de un string a uno menor, pierdes información del dato guardado que se reduce al tamaño nuevo que indicas al llamar a la funcion .resize(nuevoTamaño). Sin embargo, si modificas el tamaño a uno mayor, el contenido no se ve alterado y lo unico que cambia es el tamaño de esta variable. Veamos un ejemplo:
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};
    string nombreVariableTexto = "Voy a la uni en autobus";

    //Modificar el tamaño
    nombreVariablePalabra.resize(6);     //.resize(nuevoTamaño)
    cout<<nombreVariablePalabra<<endl;   //->Progra

    //Modificar variable a mayor
    cout<<"El tamanio inicial antes del resize() es:"<<nombreVariableTexto.size()<<endl;
    
    nombreVariableTexto.resize(50);
    cout<<nombreVariableTexto<<endl;     //->Voy a la uni en autobus

    cout<<"El tamanio despues del resize() es: "<<nombreVariableTexto.length()<<endl;

    return 0;
}
```
## clear
Borra el contenido completo almacenado en una variable string
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};
    string nombreVariableTexto = "Voy a la uni en autobus";

    //Borrar contenido
    nombreVariablePalabra.clear();
    cout<<nombreVariablePalabra<<endl;   //->

    //Antes de borrar
    cout<<nombreVariableTexto<<endl;     //->Voy a la uni en autobus
    //Borramos
    nombreVariableTexto.clear();
    //Despues de borrar
    cout<<nombreVariableTexto<<endl;     //->


    return 0;
}
```
  
