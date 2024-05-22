# Tipos de Variables
## Variable String
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
String es un tipo de dato mas complejo que por ejemplo int, float o char. A la hora de guardar datos que puede introducir alguien por el terminal debemos hacerlo utilizando getline().
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

  
