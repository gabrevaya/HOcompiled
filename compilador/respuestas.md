# Respuestas

1. Espero lo siguiente de cada paso:
	* `make preprocessing` se encargue de las directivas _#_, como los _includes_ y las _macros_.
	* `make assembler` realice la *Compilación I*, traduciendo el código desde C a assembler y pasando por el *front end*, *middle end* y *back end*.
	* `make object` realice la *Compilación II*, traduciendo el código assembler a código de máquina, generando los objetos en binario.
	* `make executable` haga el linkeo entre el objeto binario y un ejecutable, teniendo en cuenta las restricciones específicas del sistema (por ej., restricciones de espacios de memoria utilizables).

2. El preprocesador agregó el header del código y lo que incluye la librería *stdio.h*, incluida en el header.

3. La función es definida en

```
add_numbers:
.LFB1:
	.cfi_startproc
	push	rbp
	.cfi_def_cfa_offset 16
	.cfi_offset 6, -16
	mov	rbp, rsp
	.cfi_def_cfa_register 6
	mov	DWORD PTR [rbp-4], edi
	mov	DWORD PTR [rbp-8], esi
	mov	edx, DWORD PTR [rbp-4]
	mov	eax, DWORD PTR [rbp-8]
	add	eax, edx
	pop	rbp
	.cfi_def_cfa 7, 8
	ret
	.cfi_endproc
```

y llamada dentro de `.LFB0` mediante `call	add_numbers`.