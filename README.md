# TP1
TP1 del curso de Programación Cfp410 Prof. Cristian Giambruni

>*Las funciones en cada etapa están silenciadas, de modo que para accederlas deberá quitar las triples comillas.*

```
from modulos.mod import *
"""
#Parte1
diccionario_interactivo()

#Parte2
texto_plano('modo_interactivo.txt')


#Parte3
sys_modo()
"""
#Parte4
nueva_oportunidad()
```

## PRIMERA ETAPA.
` diccionario_interactivo() `

se abre un archivo en modo escritura.
se abre el archivo de diccionario dentro de un **try** en caso de no tener un diccionario.
se genera un **input**, hasta que el usuario dicte `@fin`.
Se abre el primer archivo pero en modo lectura.
Se reemplazan los caracteres con acentos, especiales y se quitan los signos de puntuación solo para realizar la busqueda comparativa en el diccionario.
Cada palabra no encontrada se aloja en una **lista**.
Se informa el resultado segun un contador.
Se imprimen las palabras listadas no encontradas.

## SEGUNDA ETAPA.
` texto_plano('file.txt') `

A partir de un archivo existente `.txt `, se lo abre en modo lectura.
Se abre el archivo `.lst `correspondiente al diccionario. Nuevamente dentro de un **try** para manejar las excepciones.
Se reptite el proceso de la primera etapa.

## TERCERA ETAPA.
` sys_modo() `

Se importa el modulo **sys**.
se asigna una variable que contenga la cantidad de **argumentos** ingresados por consola.
Segun la cantidad de argumentos, el primero va a ser el `.py` del tp, el segundo va a ser un archivo `.txt` (opcional).
En caso de no declarar un segundo argumento el programa va a correr la funcción `diccionario_interactivo()` creada para trabajar sobre un archivo interactivo.
En caso de declarar un segundo argumento, se usará dicho argumento como parámetro para ejecutar la funcion de texto plano: `texto_plano('argumento')`.

## CUARTA ETAPA.
`nueva_oportunidad()`

A partir de un archivo abierto en modo interactivo se repite el proceso de las funciones anteriores.
Al llegar al final, si la cantidad de palabras registradas en el contador es 0 el programa termina.
De lo contrario nos da la opcion de realizar una acción sobre cada palabra.
Iteramos sobre cada palabra contenida en la lista de palabras no encontradas.

**Entonces podemos**: Agreagarla al diccionario abriendo el archivo `.lst` en modo **'a'** (append), o reemplazando la palabra en el archivo original.
Para esta parte deberemos abrir el archivo original en modo escritura, y uno nuevo a modo de back up en modo escritura. Tambien abrimos el diccionario para buscar la nueva palabra.
Luego de elegir la nueva palabra a reemplazar debemos 'limpiarla' de acentos, signos especiales etc. para poder compararla con el diccionario.
Luego reemplazamos esa palabra por la otra en el archivo original y lo guardamos todo en una variable.
esa variable la escribimos en el archivo nuevo.
cerramos ambos archivos.
Ahora abrimos ambos archivos pero: el archivo original en modo escritura, y el archivo nuevo (con la palabra nueva ya reemplazada) en modo lectura.
directamente escribimos todo el archivo nuevo en el archivo original.
Esto permite que los cambios se guarden por cada palabra, así en cada iteración podremos modificar cada palabra que querramos.
cerramos los archivos usados.

En caso de quedar alguna palabra fuera del diccionario el programa nos lo informa mediante el contador, que se ha ido modificando segun las comprobaciones pertinentes.

![programacion](https://cryptoshitcompra.com/wp-content/uploads/2022/01/Como-calcular-la-diferencia-horaria-en-Python.jpg)
