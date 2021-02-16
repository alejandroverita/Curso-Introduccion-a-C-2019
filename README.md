# CURSO DE INTRODUCCION A C 2019

## INTRODUCCION AL CURSO

¿Qué es el lenguaje C?

Es un lenguaje de propósito general, compilado y de nivel intermedio.

Cuando hablamos de propósito general nos referimos a que no esta diseñado para resolver un tipo especifico de problema, sino que este puede resolver cualquier tipo de problema.

Por otro lado cuando hablamos de compilado, hablamos de algo que para nosotros es sumamente familiar, ya que compilamos de una manera similar a la que hablamos.
La computadora solo puede interpretar instrucciones en código binario (0 y 1), generalmente se realiza una traducción del binario cuando compilamos, existen dos formas:

- Interpretada: Es en tiempo real, se traduce línea por línea.

	Estos suelen ser mas flexibles, entre estos lenguajes esta; PHP, ruby, nodejs.

- Compilada: Se analiza todo el texto del programa generando un gran archivo binario para finalmente ejecutarlo (los lenguajes compilados usan es función).

Son mas fiables (robustos) y eficientes (velocidad con la que se ejecutan) entre ellos se encuentran; C, C++, pascal.

Por último el termino de nivel intermedio se refiere a la abstracción, lo que se refiere a cuanto podemos despreocuparnos de que nuestro programa lo corra una computadora, lo que nos permite concentrarnos en el problema que deseamos resolver.
Existen diferentes tipos de niveles:

○ Lenguajes de Bajo Nivel: En este tipo de lenguajes debemos estar conscientes de todo lo que sucede dentro de la computadora.

○ Lenguaje de Nivel Medio o intermedio: Aquí podemos olvidarnos de ciertas cosas, como el manejo básico del hardware, sin descuidar el manejo de la memoria.

○ Lenguaje de Alto Nivel: Aquí podemos despreocuparnos de casi todo.
Orígenes.

Dennis Ritchie fue el creador de C, ha innovado bastante en el mundo computacional, pero la creación de C se resume en cuando se encontraba trabajando en los laboratorios Bell en la construcción de sistemas operativos, al trabajar con lenguajes de muy bajo nivel pensó en crear un lenguaje de alto nivel para ese entonces, donde no tuviera que preocuparse de varios detalles y problemas a nivel hardware, de esta manera surgió el poderosísimo C.

Al día de hoy C es utilizado en ambientes donde se requieres mucha eficiencia ejemplos de estos son sistemas operativos, sistemas de control o sistemas de tiempo real.
Al mismo tiempo C tiene algunos lenguajes que son variantes de el, alguno de ellos son: C++, C#, Java, PHP, JavaScript entre otros.

<br>

[========]
## HERRAMIENTAS PARA PROGRAMAR EN C

[CodeBlocks](https://sourceforge.net/projects/codeblocks/files/Binaries/17.12/Windows/ "CodeBlocks")

1.  vas a SourceForge
2.  En el buscador colocas Code::Blocks
3.  Das click en Files
4.  Das click en Binaries
5.  Das click en la carpeta 17.12
6.  Seleccionas la carpeta de tu sistema operativo
7.  Descargas el archivo 17.12mingw-setup.exe

[Terminal de comando](https://platzi.com/clases/terminal/ "Terminal de comando")

<br>

[========]


## COMPILACIÓN Y EJECUCIÓN DE UN PROGRAMA EN C

    #include <stdio.h> 
    //Zona donde incluimos nuestras librerias. 
    //Oficialmente llamada Directivas de precompilador (Preprocessors Comands).
    
    int main()  //Funcion principal, aqui es donde la ejecucion de mi programa comienza. Todo el codigo va aqui dentro.
    {
        /*Asi se escribe un comentario en C*/
        printf("Hola Mundo"); //=> imprime en terminal
        return 0; //=> return 0 termina la funcion. Siempre que ponga 0 en un return dentro de una funcion main, va a cerrar dicha funcion
}


<br>

[========]


## TIPO DE DATOS

<img src="./tipoDeDatos.png" alt="Tipo de datos">

Bit a Bit: Compara los bytes en función del tipo de operador (& , | , ^) y devuelve el resultado filtrando por la compuerta lógica especificada.


Por Ejemplo:

42 = 0 0 1 0 1 0 1 0

215 = 1 1 0 1 0 1 1 1

Si aplicamos el operador &(compuerta logica AND): (solo es verdadero si ambas condiciones lo son)

0 1 | 0

1 1 | 1

0 1 | 0

1 0 | 0

0 1 | 0

1 0 | 0

0 1 | 0

0 1 | 0

El nuevo resultado es 0 0 0 0 0 0 1 0 (En decimal el numero 2)

Si aplicamos el operador | (compuerta logica OR): (establece dos condiciones y si una es verdadera el resultado es verdadero.)

0 1 | 1

1 1 | 1

0 1 | 1

1 0 | 1

0 1 | 1

1 0 | 1

0 1 | 1

0 1 | 1

El nuevo resultado es 1 1 1 1 1 1 1 1 (En decimal el numero 255)

Si aplicamos el operador ^ (compuerta logica XOR): (si ambas son verdaderas o falsas la condición es falsa. si una de ambas es verdadera la condición es verdadera.)

0 1 | 1

1 1 | 0

0 1 | 1

1 0 | 1

0 1 | 1

1 0 | 1

0 1 | 1

0 1 | 1


El nuevo resultado es 1 1 1 1 1 1 0 1 (En decimal el numero 253)


<br>

[========]

## DEFINICIÓN DE VARIABLES

Las variables tienen asociado al igual que las expresiones, un tipo de dato.
Solo podemos almacenar en esas variables, datos compatibles con el tipo de esas variables.

### Operadores Unarios

Aplican a variables

![operadoresUnarios.JPG](https://static.platzi.com/media/user_upload/operadoresUnarios-cb7a5486-aa07-4024-975f-f78439fbaddd.jpg)

<br>

[========]


## CONTROL DE FLUJOS

Define como se mueven los datos a través de nuestros programas. Tenemos estructuras de flujo condicionales y estructuras repetitivas.

    // **IF**
    int main()
    {
        //un igual es operador de asignacion
    	int a =1;
    
        // dos iguales es operador de comparacion
    	if(a==1){
    		a=2;
    	}else{
    		a=3;
    	}
    }
    
    // **SWITCH**
    int main()
    {
        int a =1;
    
        switch(a){
            case 1:
                a=10;
                break;
            case 2:
                a=20;
                break;
            case 3:
                a=30;
                break;
            default:
                a=100;
                break;
        }
    }
    


La estructura while es 0-x, es decir no se ejecuta al menos que se cumpla la condición especificada.

   int main()
    {
    	int n = 1, acum = 10;
    
    	while ( acum < 10 ) {
    		acum += n;
    		n++;
    	}	
    
    	return acum;
    }



La estructura do-while es 1-x, es decir se ejecuta al menos una vez.


    int main()
    {
    	int n = 1, acum = 10;
    
    	do {
    		acum += n;
    		n++;
    	} while ( acum < 10 );	
    
    	return acum;
    }

La estructura for se utiliza cuando sabemos de antemano cuantas veces queremos que se ejecute el ciclo.

    int main()
    {
    	int i, acum = 0;
    
    	for ( i = 0; i < 10; i++ ) {
    		acum += i;
    	}	
    
    	return acum;
    }

Resultado

    valor de i —> 1 valor de acum —> 1
    valor de i —> 2 valor de acum —> 3
    valor de i —> 3 valor de acum —> 6
    valor de i —> 4 valor de acum —> 10
    valor de i —> 5 valor de acum —> 15
    valor de i —> 6 valor de acum —> 21
    valor de i —> 7 valor de acum —> 28
    valor de i —> 8 valor de acum —> 36
    valor de i —> 9 valor de acum —> 45
 


<br>

[========]

## USO Y DEFINICIÓN DE FUNCIONES

### RUTINAS

Conjunto de instrucciones que se ejecutan con cierta periodicidad.

### DEFINICION DE FUNCION

Una función tiene un tipo de dato de retorno, un nombre y eventualmente puede tener una lista de argumentos.

1. Valor retornado
2. Nombre
3. Lista de argumentos
4. Conjunto de instrucciones



    ```// Funcion f
    // que recibira un argumento de tipo entero
    // y internamente en la funcion se conocera como a

    int f(int a){
        return a * 2;
    }

    // Funcion main
    int main(){
        return f(5);
    }
    
    //Resultado esperado 10

	
<br>

[========]

## DIRECTIVAS DE PRE-COMPILADOR

Las directivas del prepocesador empiezan con #

En el caso de **#include <algo>** indican al compilador que se va a incluir otro archivo antes de empezar el proceso de compilación.

El preprocesador es el primer programa que invoca el compilador de C antes de empezar a traducir el código a lenguaje máquina.

Algunas de las mas importantes:

`#include: inclusión de ficheros.`

`#define: Creación de constantes simbólicas.`

`#undef: Eliminación de constantes simbólicas.`

`#if (#else, #enif): inclusión condicional del código.`

`printf:`

`%d: numero entero.`

`%f: numero real (flotante.`

`%c: caracter.`

`%s: string.`

![placeholders.jpg](https://static.platzi.com/media/user_upload/placeholders-8c52f983-b804-4281-adea-5be7fcb6ef4d.jpg)




<br>

[========]