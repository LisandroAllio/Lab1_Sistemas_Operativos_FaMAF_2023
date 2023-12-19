# Laboratorio 1: MyBash #

# Objetivos #
-Utilizar los mecanismos de concurrencia y comunicación de gruesa granularidad que brinda UNIX.

-Comprender que un intérprete de línea de comandos refleja la arquitectura y estructura interna de las primitivas de comunicación y concurrencia.

-Implementar de manera sencilla un intérprete de línea de comandos (shell).

-Utilizar buenas prácticas de programación: estilo de código, tipos abstractos de datos (TAD), prueba unitaria (unit testing), prueba de caja cerrada (black box testing), 
programación defensiva; así como herramientas de debugging de programas y memoria.


# Objetivos de implementación #
**Codificar un shell al estilo de bash (Bourne Again SHell) al que llamaremos mybash. El programa debe tener las siguientes funcionalidades generales:**

-Ejecución de comandos en modo foreground y background

-Redirección de entrada y salida estándar.

-Pipe entre comandos.


**En particular deberán:**

-Implementar los comandos internos  cd, help y exit.

-Poder salir con CTRL-D, el caracter de fin de transmisión (EOT).

-Ser robusto ante entradas incompletas y/o inválidas.

**Para la implementación se pide en general:**

-Utilizar TADs opacos.

-No perder memoria.

-Seguir buenas prácticas de programación (coding style, modularización, buenos comentarios, buenos nombres de variables, uniformidad idiomática, etc).

# Algunos consejos #
-Antes que nada completar y probar la implementación del TAD que será la interfaz de comunicación entre los módulos propuestos.

-Dividir el trabajo entre los integrantes del grupo. Esto servirá para trabajar en paralelo y focalizar a cada uno en una tarea particular. Luego si cada uno hizo bien su trabajo, 
se requerirá una etapa final de integración que no hay que subestimar en el tiempo que puede tomar.

-Hay muchísimas cosas de comportamiento no especificado, como por ejemplo qué hacer con ls > out | wc < in, o definir si el padre espera a todos los hijos de un pipe o solo al último. 
Aunque no es necesario definir todos estos detalles y hacer que nuestro shell se comporte de esta manera, podemos deducir el comportamiento del programa haciendo experimentos en la línea 
de comandos de nuestro *NIX favorito.

-Codificar rápidamente el ciclo principal de entrada; parse; execute con stubs en todas las rutinas, para tener una base sobre la cual ir codificando y probando de manera interactiva.

-Tratar en lo posible de ir haciendo la integración de los módulos de manera incremental, a fin de no encontrar sorpresas en la etapa final de integración.

-Testear la implementación de manera exhaustiva, sobre todo en cuanto a su robustez. Pensar siempre que el usuario puede ser además de un enemigo, un gran conocedor de los bugs típicos que 
puede tener un shell.


