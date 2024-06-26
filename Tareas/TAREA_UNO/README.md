# Tarea 1


Debe ejecutar el código con el siguiente comando dentro de la carpeta **src**:
```
g++ -o main.exe .\main.cpp .\Funciones.cpp
```

Favor visitar el siguiente sitio web para ver la página web generada por Doxygen:
```
https://jose-pablo-laurent.netlify.app/index.html
```
## Preguntas
1. ¿Cuál es la principal diferencia entre C y C++?


>C++ permite aplicar el paradigma de programación orientada a objetos, mientras que C no.


2. Explique el propósito y el uso de los siguientes comandos de Git: git init, git add, git
commit, git push, git pull, git clone, git branch, git merge.
```
-git init: Inicializa un nuevo repositorio en el directorio actual o especificado.
-git add: Agrega cambios para ser incluidos en el próximo commit.
-git commit: Crea un nuevo commit con los cambios realizados, se le puede agregar un mensaje descriptivo.
-git push: Sube los commits locales al repositorio remoto.
-git pull: Obtiene los cambios del repositorio remoto y los integra a la rama local, sirve para ver la sincronización entre el repositorio remoto y el local.
-git clone: Crea una copia local de un repositorio.
-git branch: Muestra las ramas disponibles en el repositorio.Se pueden agregar, renombrar, borrar y cambiar ramas.
-git merge: Une una rama en específico con la rama de trabajo actual, se suele utilizar para unir los cambios entre una rama secundaria y una rama principal.
```
3. ¿Qué es Git y cuál es su propósito en el desarrollo de software?


>Git es un sistema de control de versiones, el cual permite rastrear los cambios realizados en un archivos, así como coordinar proyectos que involucren el desarrollo de código, esto permite trabajar de manera remota un determinado proyecto, con múltiples colaboradores de una manera eficaz.


4. ¿Qué es un conflicto de fusión (merge conflict) en Git y cómo se resuelve?


>Es un conflicto que ocurre cuando dos colaboradores intentan alterar el mismo archivo en diferentes ramas y luego intentan fusionar dichas ramas. Para su solución se recomienda primero abrir el archivo, ver las discrepancias existentes entre ambas versiones de archivos, una vez visto las diferencias se procede a editarlo con las respectivas correcciones del código, una vez resuelto el conflicto de versiones, agregar un **git add archivo** , luego un **git commit -m "Mensaje descriptivo"** y finalmente un **git push**.


5. ¿Qué es un archivo .gitignore y para qué se utiliza?


>Un archivo .gitignore es una herramienta que permite ignorar tanto los archivos como directorios que deben ser ignorados por Git, se suele utilizar dicha herramienta para evitar incluir los archivos que se pueden generar con el código fuente como lo es un archivo de extensión **.exe**.




6. ¿Qué es una solicitud de extracción (pull request) en GitHub y cómo se utiliza?


>Es una herramienta que le permite a los desarrolladores solicitar la revisión y posterior aprobación de los cambios realizados en un archivo, antes de incorporarlos a la rama principal.
Primero desde el repositorio local se realizan los cambios en un determinado archivo, luego se crea una bifurcación de la rama principal, con el objetivo de trabajar en una rama auxiliar, esto mediante el comando **git checkout -b rama_auxiliar**, por lo que se hace un cambio de la rama **main** a **rama_auxiliar**. Luego se realiza un **git push** para subir el archivo editado desde la rama **rama_auxiliar**. Posteriormente desde la interfaz gráfica del repositorio remoto de Github, se podrá configurar el **pull request** con información de los colaboradores que realizará la revisión del archivo. Si el archivo tiene el visto bueno se incorpora el archivo a la rama principal y como buena práctica se recomienda eliminar tanto la **rama_auxiliar** desde la interfaz gráfica de GitHub como del repositorio local, esto último mediante un **git branch -d rama_auxiliar**.




7. ¿Cuáles son las diferencias fundamentales entre un lenguaje de programación compilado
y uno interpretado? Proporcione ejemplos de situaciones en las que sería más óptimo utilizar un lenguaje
compilado y otras en las que sería más adecuado un lenguaje interpretado.


>La diferencia radica en que en un lenguaje compilado el compilador se encarga de convertir todo el código fuente en código ejecutable en un único paso antes de ejecutar el programa, como resultado los lenguajes de este tipo suelen ser más rápidos, mientras que en un lenguaje interpretado el intérprete procesa el código línea por línea mientras el programa se va ejecutando, lo que ocasiona que el lenguaje de programación sea más lento.


>Con respecto a escenarios de uso, los lenguajes compilados tienen la ventaja de ser más rápidos que un lenguaje interpretado, sin embargo cuando un lenguaje de programación compilado se ejecuta este crea un ejecutable el cual no va a funcionar dependiendo del sistema operativo en que se ejecute, a diferencia de un lenguaje interpretado, que esto no sucede. Tomando lo anterior en cuenta, se suele utilizar los lenguajes compilados en el desarrollo de software de sistemas operativos, aplicaciones gráficas, controladores, en aplicaciones donde se deba hacer una manipulación muy fina de la memoria del programa, por otro lado, un lenguaje interpretado se suele utilizar en el desarrollo web, desarrollo de scripts entre otro más.


8. Explique qué es un linker en el contexto de un lenguaje de programación compilado.
¿Cuál es su función principal y por qué es esencial en el proceso de compilación?


>En términos generales un **linker** es una herramienta que funciona como un editor de texto encargado de copiar y pegar, donde se copian todas la funciones necesarias a las que hace referencia el programa y posteriormente crea un archivo ejecutable. Cuando un lenguaje de programación es compilado, este convierte el archivo fuente en código de byte cuya extensión es **.OBJ**, este último es un conjunto de instrucciones que serán leídas por la arquitectura del computador, posterior a la creación del archivo  **.OBJ** el **linker** se encargará de resolver las referencias del programa, específicamente se encargará de enlazar el archivo  **.OBJ** con librerías estándar u otros archivos **.OBJ**.




9. Describa el flujo de trabajo básico en Git para agregar cambios a un repositorio.


>Primero de debe crear una rama, esto se puede hacer con el comando **git checkout -b rama_auxiliar**, luego se debe realizar algún cambio en el repositorio, como lo puede ser añadir, editar, borrar un archivo. Una vez hecho esto, se debe crear una solicitud de incorporación de cambios es decir un **pull request**, el cual ya fue explicado con anterioridad, donde se le solicita a los colaboradores realizar una revisión de los cambios realizados en el repositorio. Posteriormente los colaboradores deben ofrecer realimentación sobre el pull request, una vez aceptado el **pull request** se fusionan los cambios realizados a la rama principal. Finalmente se debe borrar la rama creada, esto con el fin de concretar el trabajo y evitar que se utilicen ramas antiguas por accidente.


10. Defina qué significa inicializar y declarar una variable.


>Declaración en términos generales hace referencia a la introducción de un nuevo nombre en el programa, por ejemplo:
```c++
int a;
```
>Por otro lado inicialización hace referencia a la asignación de un determinado valor en tiempo de construcción, por ejemplo:
```c++
int a = 0;
```


11. ¿Qué es la sobrecarga de funciones en C++ y cuáles son sus beneficios?


>La sobrecarga de funciones en C++ hace referencia a que dos o más funciones pueden tener el mismo nombre siempre y cuando la cantidad o el tipo de argumento sean distintos. Entre sus beneficios destacan la legibilidad del código, reutilización y ahorro de memoría, ya que no se está creando una función distinta.


12. ¿Qué es un puntero y cómo se utiliza? Explique con un ejemplo de la vida real.


>Un puntero es un tipo de dato capaz de almacenar la dirección en memoria de otro tipo de dato, ya sea variable, función, estructura o clase, entre otro más. Ejemplo de su use:
```c++
//Variable de tipo entero almacena número 3
int var1 = 3;
//Puntero de tipo entero
int* pointer;
//Puntero apunta hacia la dirección de memoria de var1
pointer = &var1;
//Se desreferencia el puntero y este almacena la variable 3
cout << "Contenido de pointer " << *pointer <<endl;
```
Una analogía de los punteros con la vida real es la siguiente, imagine que hace muchos años usted escondió un tesoro, sin embargo ha olvidado dónde lo escondió, no obstante escribió en una papel (puntero) la ubicación donde guardó el tesoro.


13. ¿Qué es un branch (rama) en Git y cómo se utiliza?
>En Git un branch es una rama, es decir es un elemento que permite realizar bifurcaciones con la rama **main**, para realizar cambios en el repositorio sin afectar, inmediatamente, el **main**, hasta que se realice un **pull request**, es posible crear una nueva rama con el comando: **git checkout -b rama_auxiliar** y tambien cambiar entre ramas con el comando: **git checkout nombre_de_la_rama**.


14. ¿Cuál es la principal diferencia entre un bucle do-while y un bucle while?


>La principal diferencia entre el bucle do-while y el bucle while, yace en el bucle **do-while** ejecuta el código y luego evalua la condición, lo que garantiza que el código se ejecute al menos una vez, mientras que el bucle **while** evalua primero la condición y luego ejecuta el código, por lo que no hay garantía de que se ejecute al menos una vez el código.


15. Explique por qué es útil y común dividir el código en archivos .hpp, .cpp y main.cpp
en C++. Describa el propósito específico de cada tipo de archivo.


>Es útil segmentar el código en archivos de extensión **.hpp**, **.cpp** y **main.cpp**, debido a que ayudan a mantener la legibilidad del código, su orden , mantenimiento,  reutilización, mejora tiempos de copilación al tener los archivos separados.


>Archivos **.hpp**: Estos archivos contienen las declaraciones de variables, funciones, estructuras y clases.


>Archivos **.cpp**: Estos archivos contienen la lógica y el desarrollo de las declaraciones ya sea de variables, funciones, estructuras y clases, hechas en los archivos **.hpp**.


>Archivo **main.cpp**: En este archivo se realiza la ejecución del programa y el llamado a las variables, funciones, estructuras y clases, mediante la inclusión de los archivos **.hpp"**.




16. ¿Dónde y cómo se guardan las variables que se crean en C++? Explique la diferencia
entre el almacenamiento de variables locales y globales.


>Variables locales: Se almacenan en el **stack**, se declaran dentro de una función y solo son accesibles dentro esa misma función, siendo su vida útil cada vez que se llama a la función que albergan, luego mueren.


>Variables globales: Se almacenan en el área de **static storage class**, se declaran fuera de cualquier función y son accesibles en cualquier parte del programa, finalmente su vida útil es durante todo el programa.


17. ¿Cuál es la diferencia entre pasar parámetros por valor, por referencia y por puntero?


>Por valor: se envía como parámetro la copia de una determinada variable, al ser una copia no se puede modificar la variable original.


```c++
void swap(int a,int b){
    //En este caso no modifico las variables originales
    int aux = a;
    a = b;
    b = aux;
}
main(){
    int a =1, b =2;
    swap(a,b);
    return 0;
}


```


>Por referencia: Permite modificar la variable original sin necesidad de crear una copia.


```c++
void swap(int &a,int &b){
    //Modifico los valores originales del las variables que tengo de parametros
    int aux = a;
    a = b;
    b = aux;
}
main(){
    int a =1, b =2;
    swap(a,b);
    return 0;
}


```


>Por puntero: Se envía como parámetro la dirección de memoria de una determinada variable, al ser la dirección de memoria, permite modificar la variable original.


```c++
void swap(int *a,int *b){
    //Modifico los valores originales del las variables que tengo de parametros
    //Desreferencio el puntero
    int aux = *a;
    *a = *b;
    *b = aux;
}
main(){
    int a = 1, b =2;
    //Parametros por referencia por puntero
    swap(&a,&b);
    return 0;
}


```


18. Cuando se usa un puntero para apuntar a un arreglo en C++, ¿a qué valor o dirección
apunta inicialmente? Describa cómo sería la forma de acceder a todos los datos de ese
arreglo mediante el puntero.


>El puntero apunta hacia la dirección de memoria del primer elemento del arreglo.
Para acceder a cada uno de los datos del puntero este se debe iterar y desreferencia ***(ptr + i)**.
```C++
int arr[] = {1, 2, 3, 4};
//Dirección de memoria del primer elemento del arreglo
int *ptr = arr;  
for (int i = 0; i < arr.size(); i++) {
    // Itero y accedo a los elementos del arreglo
    cout << "Dato " << i << ": " << *(ptr + i) << endl;  
}
```


19. Explique para qué son empleados los punteros dobles en C++. Proporcione ejemplos
de situaciones en las que los punteros dobles son necesarios o beneficiosos.


>Los punteros dobles en C++ son utilizados para almacenar la dirección de memoria de un puntero, se pueden emplear para modificar otros punteros, realización de matrices, etc.


```C++


    int result_init = 2905;
    //Puntero simple
    int* ptr_1;
    //Referencio el puntero con la direccion en memoria de result_init
    ptr_1 = &result_init;


    cout <<"Direccion memoria de result_init: " << &result_init<< endl;
    cout <<"Direccion memoria de ptr_1: " << ptr_1<< endl;


    //Se crea un puntero doble que apunta al valor de memoria de ptr1
    int** ptr_ptr_1;
    ptr_ptr_1 = &ptr_1 ;


    cout <<" ptr_2: " << ptr_ptr_1<< endl;
    cout << "Direcion de &ptr_1: " << &ptr_1<<endl;
    cout << "Direccion de &ptr_2: " << &ptr_ptr_1<<endl;
```


20. ¿Para qué se utiliza la directiva #ifndef?


> La directiva **#ifndef** se implementa cuando dos archivos pretenden importar el mismo encabezado es decir un archivo de extensión **.hpp**, por tal motivo se implementa el condicional **#ifndef**, en el caso se de ser leído por el primer archivo se define el contenido del encabezado mediante la sentencia **define**, posteriormente se cierra el condicional, debido a que el contenido ya fue definido el segundo archivo  no leerá el contenido del **#ifndef** debido a que este ya fue previamente definido, este proceso es útil ya que ahorra tiempo y espacio en memoria.


21. ¿Qué es el puntero this en C++?


>En C++ el puntero this se utiliza para acceder a los atributos de una clase, ya sea para inicializarlos o modificarlos.


22. ¿Cuál es la diferencia entre un arreglo y una lista en C++?


>Arreglo: Es una estructura de datos capaz de almacenar elementos del mismo tipo, es de un tamaño fijo, por lo tanto su tamaño no puede ser variado una vez que se ha creado y sus elementos se acceden mediante índices debido a que están ordenados en memoria.


>Lista: Es una estructura de datos capaz de almacenar elementos de distinto tipo, no es de un tamaño fijo, es decir su tamaño puede ser alterado para acomodar nuevos elementos, sus elementos se encuentran esparcidos en memoria, es decir no están ordenados.


23. ¿Investigue qué es un memory leak?
>Un memory leak, es una fuga de memoria, esto ocurre cuando se asigna memoria a un determinado proceso, pero esta no se libera una vez ejecutada la labor. Cuando esto ocurre la memoria asignada se pierde, por tal motivo el programa intentará solventar dicha carencia con un uso excesivo de la memoria. En el caso de c++ se recomienda que cada vez que se utilice el comando **new** para asignar memoria, se debe posteriormente utilizar **delete** ,una vez ejecutada la labor, con el fin de evitar estas fugas.



