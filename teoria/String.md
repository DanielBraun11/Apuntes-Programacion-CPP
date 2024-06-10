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
## at
Sirve para acceder a una posicion concreta de la variable. Es MUY IMPORTANTE recordar que en programación se empieza a contar desde la posicion 0 y no desde el 1 como estamos acostumbrados.
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};

    cout<<nombreVariablePalabra.at(1)<<endl;   //.at(posicion)  //->r

    cout<<nombreVariablePalabra.at(nombreVariablePalabra.size() - 5)<<endl;  //.at(12 - 5) //->a

    return 0;
}
```
## pop_back
Sirve para eliminar el ultima caracter de la cadena.
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};
    
    cout<<nombreVariablePalabra<<endl;  //->Programacion
    nombreVariablePalabra.pop_back();
    cout<<nombreVariablePalabra<<endl;  //->Programacio

    return 0;
}
```
## back y front
Estas funciones devuelven el primer caracter de la cadena .front() y el último caracter de la cadena .back()
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};
    
    cout<<nombreVariablePalabra.front()<<endl;  //->P
    cout<<nombreVariablePalabra.back()<<endl;   //->n

    return 0;
}
```
## append
Añade una cadena " " de texto AL FINAL de la cadena que se modifica. 
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};

    cout<<nombreVariablePalabra<<endl;              //->Programacion 
    nombreVariablePalabra.append(" se practica");
    cout<<nombreVariablePalabra<<endl;              //->Programacion se practica

    return 0;
}
```
## push_back
Añade un caracter ' ' AL FINAL de la cadena que se modifica
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariablePalabra {"Programacion"};

    cout<<nombreVariablePalabra<<endl;              //->Programacion
    nombreVariablePalabra.push_back('1');
    cout<<nombreVariablePalabra<<endl;              //->Programacion1

    return 0;
}
```
## operador +
Sirve para juntar dos cadenas de texto o para agregar texto a una cadena ya existente.
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariable1 {"Hola soy Daniel y soy "};
    string nombreVariable2 = "estudiante";

    string juntarVariables = nombreVariable1 + nombreVariable2;
    cout<<juntarVariables<<endl;
    
    //También se pueden juntar directamente en el cout
    cout<<nombreVariable1 + nombreVariable2<<endl;

    return 0;
}
```
## insert
Esta funcion introduce una cadena de texto antes de la posicion indicada.
```c++
#include<iostream>
using namespace std;

int main(){
    string nombreVariable1 {"Hola soy y me gusta programar"};
    string nombreVariable2 = " Dani";

    nombreVariable1.insert(8,nombreVariable2);  //.insertar(posicion desde donde se añade, lo que añade)

    cout<<nombreVariable1<<endl;  //->Hola soy Dani y me gusta programar

    return 0;
}
```
## erase
Elimina una porción de una cadena de texto
```c++
#include<iostream>
using namespace std;

int main(){
    string cadena = "Me gusta mucho el futbol";

    cadena.erase(9,5);  //.erase(posicion desde donde borro, numero de caracteres que borro)

    cout<<cadena<<endl;   //->Me gusta el futbol

    return 0;
}
```
## substr
Extrae una subcadena de otra cadena dada.
```c++
#include<iostream>
using namespace std;

int main(){
    string cadena = "Me gusta mucho el futbol";

    string subcadena = cadena.substr(3,5);  //.substr(posicion donde empieza la subcadena, posicion donde acaba la subcadena)

    cout<<cadena<<endl;     //->Me gusta mucho el futbol
    cout<<subcadena<<endl;  //->gusta

    return 0;
}
```
## find
Busca una cadena de texto dentro de otra.
```c++
#include<iostream>
using namespace std;

int main(){
    string cadena = "Me gusta mucho el futbol";

    cout<<cadena.find("futbol")<<endl;  //->18   //.find(cadena que busco)

    cout<<cadena.find("tenis")<<endl;   //->string::npos (No encontrado)

    //Busqueda desde una posicion de la cadena
    cout<<cadena.find("mucho",3)<<endl; //->9  //.find(cadena que busco, a partir de que posicion)

    return 0;
}
```
## empty
Función que devuelve true(1) si la cadena de texto está vacía y false(0) si está con contenido.
```c++
#include<iostream>
using namespace std;

int main(){
    string cadena1 {"Hola Mundo"};
    string cadena2 = "";

    cout<<cadena1.empty()<<endl;    //->0
    cout<<cadena2.empty()<<endl;    //->1
    
    //Se usa como booleano
    if(cadena1.empty()){
        cout<<"Cadena vacia"<<endl;
    }else{
        cout<<"Cadena rellenada"<<endl;
    }
    return 0;
}
```
