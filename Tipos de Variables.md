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
  
