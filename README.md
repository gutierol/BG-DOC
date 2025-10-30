<!-- title: BASE Gráfico -->
# BASE Gráfico<!-- omit from toc -->

## Índice de Ayuda para Asesores<!-- omit from toc -->

[![BASE Gráfico](https://basegrafico.com/img/logo-image.png)](https://basegrafico.com/)

---

- [Funciones Globales:](#funciones-globales)
  - [FN%acum: Acumula un campo númerico de un archivo](#fnacum-acumula-un-campo-númerico-de-un-archivo)
  - [FN%fecha$: Formatea una fecha](#fnfecha-formatea-una-fecha)
  - [FN%fecinv$: Invierte una fecha](#fnfecinv-invierte-una-fecha)
  - [FN%fecha\_letras$: Fecha en letras](#fnfecha_letras-fecha-en-letras)
  - [FN%find$: Busca un valor de un campo en un archivo](#fnfind-busca-un-valor-de-un-campo-en-un-archivo)
  - [FN%mes$: Nombre de un mes](#fnmes-nombre-de-un-mes)
  - [FN%mescrito$: Monto escrito](#fnmescrito-monto-escrito)
  - [FN%no\_todo: Que la explique JL](#fnno_todo-que-la-explique-jl)
  - [FN%ope\_valido: Operador válido para una función específica](#fnope_valido-operador-válido-para-una-función-específica)
  - [FN%pos: Busca un texto en otro texto](#fnpos-busca-un-texto-en-otro-texto)
  - [FN%precision: Ajustar precisión a un monto](#fnprecision-ajustar-precisión-a-un-monto)
  - [FN%tabla: Busca un valor en una variable](#fntabla-busca-un-valor-en-una-variable)
  - [FN%tbl$: Traduce acentos en un texto](#fntbl-traduce-acentos-en-un-texto)
- [Rutinas Públicas (RP\_XXXXX):](#rutinas-públicas-rp_xxxxx)
  - [RP\_CATAL](#rp_catal)
    - [RP\_CATAL;CATALOGO](#rp_catalcatalogo)
    - [RP\_CATAL;APLICACIONES](#rp_catalaplicaciones)
  - [RP\_FECHA](#rp_fecha)
    - [RP\_FECHA;AJUSTAR: Ajustar una fecha](#rp_fechaajustar-ajustar-una-fecha)
    - [RP\_FECHA;JULIANO: Cálculo del día en juliano](#rp_fechajuliano-cálculo-del-día-en-juliano)
    - [RP\_FECHA;DIASEM: Día de la semana](#rp_fechadiasem-día-de-la-semana)
    - [RP\_FECHA;LETRAS: Fecha en letras](#rp_fechaletras-fecha-en-letras)
    - [RP\_FECHA;EDAD: Diferencia entre dos fechas](#rp_fechaedad-diferencia-entre-dos-fechas)
- [Rutinas Utilitarias (RU\_XXXXX):](#rutinas-utilitarias-ru_xxxxx)
  - [RU\_COPY](#ru_copy)

# [Funciones Globales:](#funciones-globales)

Funciones de usuario definidas de forma global para mejorar la codificación en los programas.

[Volver arriba](#top)

## FN%acum: Acumula un campo númerico de un archivo

~~~text
FN%acum(LOCAL archivo$, LOCAL campo$, LOCAL clave$, LOCAL opciones$)
~~~

- Descripción:

Retorna la acumulación de un *campo$* numérico en un *archivo$* de los registros con la *clave$* indicada, y con *opciones$*.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |archivo$|Nombre del archivo que contiene el campo|
  |campo$|Nombre del campo numérico a acumular|
  |clave$|Clave de posicionamiento en el archivo|
  |opciones$|Opciones de la función|
  
- Opciones:
  
  | Opción | Descripción |
  |:-------|-------------|
  |KNO\[número_de_llave\]|Llave o índice del archivo a usar|
  |CND\[Condición\]|Condición que deben cumplir los registros|

- Ejemplo:

~~~text
> PRINT FN%acum("FACENCAB","MONTO","HLS"+"200001","KNO[0] CND[REC.TIPO$=""FA""]")
8752336.98
~~~

[Volver arriba](#funciones-globales)

## FN%fecha$: Formatea una fecha

~~~text
fn%fecha$(LOCAL fecha$)
~~~

- Descripción:

Retorna una variable que contiene una fecha válida end formato ddmmaaaa, formateada del modo dd/mm/aaaa.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha a formatear|
  
- Ejemplo:

~~~text
> PRINT FN%fecha$("24102025")
24/10/2025
~~~

[Volver arriba](#funciones-globales)

## FN%fecinv$: Invierte una fecha

~~~text
FN%fecinv$(LOCAL fecha$)
~~~

- Descripción:

Retorna el valor enviado (ddmmaaaa) de forma invertida: aaaammaa.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha ddmmaaaa a invertir|

- Ejemplo:

~~~text
> PRINT FN%fecinv$("24102025")
20251024
~~~

[Volver arriba](#funciones-globales)

## FN%fecha_letras$: Fecha en letras

~~~text
FN%fecha_letras$(LOCAL fecha$)
~~~

- Descripción:

Retorna la fecha enviada en letra, para ser usada por ejemplo en cartas.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha ddmmaaaa a convertir en letras|

- Ejemplo:

~~~text
> PRINT FN%fecha_letras$("24102025")
24 de Octubre de 2025
~~~

[Volver arriba](#funciones-globales)

## FN%find$: Busca un valor de un campo en un archivo

~~~text
FN%find$(LOCAL archivo$, LOCAL campo$, LOCAL clave$)
~~~

- Descripción:

Retorna el valor del *campo$* contenido en el registro con llave primaria *clave$* del *archivo$, sí no consigue la *clave$* retorna un valor vacio.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |archivo$|Nombre del archivo a consultar|
  |campo$|Nombre del campo o columna en el archivo|
  |clave$|Clave de posicionamiento en el archivo|

- Ejemplo:

~~~text
> PRINT FN%find$("CTLCIAS","CIA_NOM","HLS")
H.L. Sistemas S.R.L.
> PRINT FN%find$("NOMDESCR","NOMBRE","HLS"+"0003/002  ")
MONICA GUADALUPE
~~~

[Volver arriba](#funciones-globales)

## FN%mes$: Nombre de un mes

~~~text
FN%mes$(LOCAL mes$)
~~~

- Descripción:

Retorna el nombre en letras del *mes$* en números.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |mes$|Número del mes|

- Ejemplo:

~~~text
> PRINT FN%mes$("10")
Octubre
~~~

[Volver arriba](#funciones-globales)

## FN%mescrito$: Monto escrito

~~~text
FN%mescrito$(LOCAL monto)
~~~

- Descripción:

Retorna el número enviado en letras.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |monto|Monto o cifra a convertir en letras|

- Ejemplo:

~~~text
> PRINT FN%mescrito$(24528.12)
VEINTICUATRO MIL QUINIENTOS VEINTIOCHO CON 12 CENTIMOS
~~~

[Volver arriba](#funciones-globales)

## FN%no_todo: Que la explique JL

~~~text
FN%no_todo(LOCAL num_ctl, LOCAL cond$, LOCAL botones$, LOCAL archivo$, LOCAL posic$)
~~~

- Descripción:

Que me la explique JL.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |num_ctl|ID (ctl) del objeto LIST_BOX|
  |cond$|Condición de los registros a retornar|
  |botones$||
  |archivo$|Nombre del archivo|
  |posic$|Clave de posicionamiento en el archivo|

- Ejemplo:

~~~text
FN%no_todo(listbox.ctl, "","REC.TIPO=""75""","INVGRUPO","")
~~~

[Volver arriba](#funciones-globales)

## FN%ope_valido: Operador válido para una función específica

~~~text
FN%ope_valido(LOCAL funcion$)
~~~

- Descripción:

Retorna verdadero (1) sí el usuario actual (**%base_login$**), esta autorizado en la *funcion$* específica (**CTLFNOPE**), de lo contrario retorna falso (0)

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |funcion$|Nombre de la función específica|

- Ejemplo:

~~~text
> PRINT FN%ope_valido("VER_SALDOS")
1
~~~

[Volver arriba](#funciones-globales)

## FN%pos: Busca un texto en otro texto

~~~text
FN%pos(LOCAL texto1$, LOCAL texto2$)
~~~

- Descripción:

Compara *texto1$* dentro de *texto2$* sin importar que contengan acentos, mayúsculas y/o minúsculas. Retorna verdadero (1) sí son iguales, falso (0) si son diferentes y -1 si *texto1$* esta vacío.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |texto1$|Patrón a buscar|
  |texto2$|Texto donde va a buscar el patrón|

- Ejemplo:

~~~text
> PRINT fn%pos("ÁéÍóÚ","aeIOu")
1
~~~

[Volver arriba](#funciones-globales)

## FN%precision: Ajustar precisión a un monto

~~~text
FN%precision(LOCAL valor, LOCAL decimales)
~~~

- Descripción:

Retorna el *valor* ajustado a la precision de *decimales*.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |valor|Monto a ajustar|
  |decimales|Cantida de decimales a ajustar|

- Ejemplo:
  
~~~text
> PRINT FN%precision(249.02193822,3)
249.022
~~~

[Volver arriba](#funciones-globales)

## FN%tabla: Busca un valor en una variable

~~~text
FN%tabla(LOCAL valor$, LOCAL tabla$, LOCAL longitud)
~~~

- Descripción:  

Retorna verdadero (1) sí el elemento *valor$* se encuentra contenido dentro de la variable *tabla$*, haciendo la busqueda del elemento con la *longitud* indicada, de lo contrario retorna falso (0) .

- Argumentos:

  |Argumento|Descripción|
  |valor$|Patrón a buscar|
  |tabla$|Texto donde va a buscar el patrón|
  |longitud|tamaño del patrón|

- Ejemplo:

~~~text
> tabla$="01020304"
> PRINT FN%tabla$("10",tabla$,2)
0
> PRINT FN%tabla$("02",tabla$,2)
1
~~~

[Volver arriba](#funciones-globales)

## FN%tbl$: Traduce acentos en un texto

~~~text
FN%tbl$(LOCAL lp, LOCAL lin$)
~~~

- Descripción:

Traduce acentos en una cadena *lin$* para la impresión directa por el canal *lp*.

- Argumentos:
  
  |Argumento|Descripción|
  |:--------|-----------|
  |lp|Canal de impresión|
  |lin$|Línea a imprimir|

- Ejemplo:

~~~text
> OPEN(unt)"*windev*"
> PRINT (lfo)fn%tbl$(lfo,"ÁéÍóÚ")
> PRINT fn%tbl$(lfo,"ÁéÍóÚ")
 ‚¡¢£
> CLOSE(lfo)
~~~

[Volver arriba](#funciones-globales)

# [Rutinas Públicas (RP_XXXXX):](#rutinas-públicas-rp_xxxxx)

Definición de lo que son las rutinas públicas.

[Volver arriba](#top)

## RP_CATAL

Para realizar operaciones relacionadas al catálogo de funciones. Típicamente usada en programas de control de procesos (Mantenimiento y Listado del Catálogo, Permisos de Grupos y/o Operadores, etc.)

### RP_CATAL;CATALOGO

Leer catálogo de una aplicación.

~~~text
CALL "RP_CATAL;CATALOGO", CIA$, APLIC, CATAL, LCAT${ALL}, IND_CAT, OPC$
~~~

- Parámetros:
  
  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |CIA$|E|Código de Compañía (Normalmente %BASE_CIA_CATA$)|
  |APLIC|E|Objeto (List_Box o Drop_Box) donde está seleccionada la Aplicación|
  |CATAL|E|Objeto (Tree_View) donde se va a generar el catálogo|
  |LCAT$\[ALL\]|S|Líneas del Catálogo (Clave en el archivo CTLCATAL)|
  |IND_CAT|S|Total de Líneas del Catálogo|
  |OPC$|E|Opciones Adicionales (Separadas con Espacio)|

  - Opciones:
  
    |Opción|Descripción|
    |:-----|-----------|
    |SOLO_MENU|No Incluir Procesos, solo sub_menus|
    |AGREGAR_FIN|Agregar línea <Fin del Catálogo> por sub_menu|
    |NO_OBJ_CATAL|No hay Objeto (Tree_view) con catálogo|

~~~text
CALL "RP_CATAL",%BASE_CIA$,...
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_CATAL;APLICACIONES

Leer tabla de aplicaciones

~~~text
CALL "RP_CATAL;APLICACIONES", TAB_APL$
~~~

- Parámetros:

  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |TAB_APL$|S|Tabla con las aplicaciones (Separadas con \$09\$)|

~~~text
CALL "RP_CATAL;APLICACIONES",TAB_APL$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

## RP_FECHA

Permite realizar las operaciones asociadas al cálculo, edición, validación, etc. de una o varias fechas.

### RP_FECHA;AJUSTAR: Ajustar una fecha

Ajuste algebraico de una fecha en días, meses y años.

~~~text
CALL “RP_FECHA;AJUSTAR”, FECHA_ORIGEN$,DIAS,MESES,AÑOS,FECHA_RESULTADO$,OPCIONES$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha de Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |DIAS|E|Ajuste en días (Positivo = adelante, negativo = atrás)|
  |MESES|E|Ajuste en meses (Positivo = adelante, negativo = atrás)|
  |AÑOS|E|Ajuste en años (Positivo = adelante, negativo = atrás)|
  |FECHA_RESULTADO$|S|Fecha Resultante (ddmmaaaa), sí la fecha resultante es nula es porque la fecha original es inválida|
  |OPCIONES$|E|Opciones Adicionales (Separadas con Espacio)|

  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |-U|Ajustar hasta el ultimo dia del mes|
    |-H|Ajustar días basado en los días hábiles (Archivo CTLCALEN)|

- Ejemplos:

~~~text
> CALL "RP_FECHA;AJUSTAR","01/10/2025",10,0,0,FECHA_RESULTADO$,""
> PRINT FECHA_RESULTADO$
11102025
> CALL "RP_FECHA;AJUSTAR","01/10/2025",0,0,0,FECHA_RESULTADO$,"-U"
> PRINT FECHA_RESULTADO$
31102025
> CALL "RP_FECHA;AJUSTAR","01/10/2025",0,1,0,FECHA_RESULTADO$,"-H"
> PRINT FECHA_RESULTADO$
01112025
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FECHA;JULIANO: Cálculo del día en juliano

Cálculo del dia juliano y del día dentro del año.

~~~text
CALL "RP_FECHA;JULIANO", FECHA_ORIGEN$, DJUL, DYEAR
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha de Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |DJUL|S|Día Juliano (Días desde el año 0000), típicamente se usa para calcular la diferencia de días que hay entre dos fechas|
  |DYEAR|S|Día dentro del año|

- Ejemplo:

~~~text
> CALL "RP_FECHA;JULIANO","20071969",JULIANO,AÑO
> PRINT JULIANO
718997
> PRINT AÑO
201
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FECHA;DIASEM: Día de la semana

Día de la semana de una fecha.

~~~text
CALL "RP_FECHA;DIASEM", FECHA_ORIGEN$, DSEM, DIA$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha de Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |DSEM|S|Día de la semana en número (0 = domingo, 6 = sábado)|
  |DIA$|S|Día de la semana en letras (Dom,Lun,....,Sab)|

- Ejemplo:

~~~text
> CALL "RP_FECHA;DIASEM","20071969",DIA,DIA$
> PRINT DIA
0
> PRINT DIA$
Dom
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FECHA;LETRAS: Fecha en letras

Fecha suministrada escrita en letras.

~~~text
CALL "RP_FECHA;LETRAS",FECHA_ORIGEN$,FECHA_LETRAS$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha de Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |FECHA_RESULTADO$|S|Fecha Resultante (ddmmaaaa), sí la fecha resultante es nula es porque la fecha original es inválida|

- Ejemplo:

~~~text
> CALL "RP_FECHA;LETRAS","20071969",DIA$
> PRINT DIA$
20 de Julio de 1969
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FECHA;EDAD: Diferencia entre dos fechas

Cálculo de la edad o diferencia entre dos fechas.

~~~text
CALL "RP_FECHA;EDAD", DESDE$, HASTA$, AÑOS, MESES, DIAS
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |DESDE$|E|Fecha de Comienzo (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |HASTA$|E|Fecha de Finalización (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |AÑOS|S|Años de edad o diferencia (Número entero)|
  |MESES|S|Fracción de meses de edad o diferencia|
  |DIAS|S|Fracción de días de edad o diferencia|

- Ejemplo:

~~~text
> CALL "RP_FECHA;EDAD","20071969","01082001",AÑOS,MESES,DIAS
> PRINT AÑOS,MESES,DIAS
32 0 12
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

# [Rutinas Utilitarias (RU_XXXXX):](#rutinas-utilitarias-ru_xxxxx)

Definición de lo que son las rutinas utilitarias.

[Volver arriba](#top)

## RU_COPY

Copia de registros.

>Anteriormente: `HLCOPY`

~~~text
CALL "RU_COPY"
~~~

[Volver arriba](#rutinas-utilitarias-ru_xxxxx)
