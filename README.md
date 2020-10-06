# taller-de-programacion-1-veiga-contador-de-palabras

Alumno: Robinson Fang
Padrón: 97009

## Entorno de trabajo

### Valgrind

Valgrind es una herramienta de análisis que facilita la depuración de un programa. Permite encontrar memoria que se reservó y luego de ser utilizada no es liberada, lecturas/escrituras en memoria liberada o fuera de los límites reservados.

Entre sus opciones más comunes se encuentran:

- **quiet**
	> muestra únicamente mensajes de errores
	
- **verbose**
	> muestra información adicional
	
- **leak-check**=full/yes/no
	> habilita/deshabilita la funcionalidad de detección de fugas de memoria
	
- **show-reachable**=yes/no
	> habilita/deshabilita la detección de memoria de la que no se conservan referencias


### sizeof()

sizeof() devuelve el tamaño en bytes que ocupa en memoria un tipo de datos o estructura.

El sizeof(char) es siempre 1 byte independientemente de la arquitectura del computador utilizado. Pero para el tipo de dato entero, el tamaño que ocupa en memoria puede variar según la arquitectura o el computador. Para una arquitectura de 32 o 64 bits, por ejemplo, el tamaño de un entero es de 4 bytes.

No necesariamente el sizeof() de una struct de C es igual a la suma del sizeof() de cada uno sus elementos. Esto se debe a que por una cuestión de performance a la hora de acceder a memoria, los datos se alinean de forma tal que el acceso a memoria sea de a bloques múltiplos de 4 bytes. Es por esto que si se tiene la siguiente estructura:
```
struct char_and_int {
	char a;
	int i;
};
```
Aunque el tipo de dato char ocupe un byte, se utilizará un bloque de 4 para almacenarlo. El tamaño de la struct es de 8 bytes.

### STDIN, STDOUT y STDERR

- STDIN (entrada estándar) son los datos que recibe para su ejecución.
- STDOUT (salida estándar) son los datos que devuelve un programa luego de su ejecución.
- STDERR (error estándar) es la devolución de los errores presentados durante la ejecución de un programa. Es un canal distinto de la salida estándar, lo que permite distinguir el manejo de la obtención de uno u otro. 

Con el comando '>' se puede redirigir el output de un proceso hacia un archivo o dispositivo. Usualmente la salida de un programa se muestra por pantalla en la terminal, pero con el uso de la redirección de output se puede volcar la salida a un archivo o agregarla a la información preexistente con '>>'.
De forma análoga el operador < permite alimentar la entrada de un proceso.

Se puede alimentar la entrada de un proceso con la salida secuencialmente y de forma unidireccional utilizando '|' con la siguiente sintaxis:
```
proceso1 | proceso2 | proceso3
```

## Paso 0:

Se realizó un programa simple que imprime por pantalla el mensaje “Hola Mundo”.

![image](./img/paso0.png)
[texto](./img/paso0.png)

## Paso 1: SERCOM - Errores de generación y normas de programación

