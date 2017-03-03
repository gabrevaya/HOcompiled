# Respuestas

1. Espero lo siguiente de cada paso:
	* `make preprocessing` se encargue de las directivas _#_, como los _includes_ y las _macros_.
	* `make assembler` realice la *Compilación I*, traduciendo el código desde C a assembler y pasando por el *front end*, *middle end* y *back end*.
	* `make object` realice la *Compilación II*, traduciendo el código assembler a código de máquina, generando los objetos en binario.
	* `make executable` haga el linkeo entre el objeto binario y un ejecutable, teniendo en cuenta las restricciones específicas del sistema (por ej., restricciones de espacios de memoria utilizables).

2. El preprocesador agregó el header del código y lo que incluye la librería *stdio.h*, incluida en el header.