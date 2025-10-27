[BASE Gráfico](https://basegrafico.com/img/logo-image.png)
# BASE Gráfico - Índice de Ayuda para Asesores
---
- [BASE Gráfico - Índice de Ayuda para Asesores](#base-gráfico---índice-de-ayuda-para-asesores)
  - [Funciones Globales:](#funciones-globales)
    - [FN%acum: Acumula un campo númerico de un archivo](#fnacum-acumula-un-campo-númerico-de-un-archivo)
    - [fn%fecha$: Formatea una fecha](#fnfecha-formatea-una-fecha)
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
      - [- RP\_CATAL;CATALOGO](#--rp_catalcatalogo)
      - [- RP\_CATAL;APLICACIONES](#--rp_catalaplicaciones)
    - [RP\_FECHA](#rp_fecha)
      - [- RP\_FECHA;AJUSTAR: Ajustar una fecha](#--rp_fechaajustar-ajustar-una-fecha)
  - [Rutinas Utilitarias (RU\_XXXXX):](#rutinas-utilitarias-ru_xxxxx)
    - [RU\_COPY](#ru_copy)

## [Funciones Globales:](#funciones-globales)

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

Funciones de usuario definidas de forma global para mejorar la codificación en los programas.

### FN%acum: Acumula un campo númerico de un archivo

~~~
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
  |KNO[número_de_llave]|Llave o índice del archivo a usar|
  |CND[Condición]|Condición que deben cumplir los registros|

- Ejemplo:

~~~
PRINT FN%acum("FACENCAB","MONTO","HLS"+"200001","KNO[0] CND[REC.TIPO$=""FA""]")
> 8752336.98
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### fn%fecha$: Formatea una fecha

~~~
fn%fecha$(LOCAL fecha$)
~~~

- Descripción:

Retorna una variable que contiene una fecha válida end formato ddmmaaaa, formateada del modo dd/mm/aaaa.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha a formatear|
  
- Ejemplo:

~~~
PRINT FN%fecha$("24102025")
> 24/10/2025
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%fecinv$: Invierte una fecha

~~~
FN%fecinv$(LOCAL fecha$)
~~~

- Descripción:

Retorna el valor enviado (ddmmaaaa) de forma invertida: aaaammaa.

- Argumentos:
  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha ddmmaaaa a invertir|

- Ejemplo:

~~~
PRINT FN%fecinv$("24102025")
> 20251024
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%fecha_letras$: Fecha en letras

~~~
FN%fecha_letras$(LOCAL fecha$)
~~~

- Descripción:

Retorna la fecha enviada en letra, para ser usada por ejemplo en cartas.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |fecha$|Fecha ddmmaaaa a convertir en letras|

- Ejemplo:

~~~
PRINT FN%fecha_letras$("24102025")
> 24 de Octubre de 2025
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%find$: Busca un valor de un campo en un archivo

~~~
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

~~~
PRINT FN%find$("CTLCIAS","CIA_NOM","HLS")
> H.L. Sistemas S.R.L.
PRINT FN%find$("NOMDESCR","NOMBRE","HLS"+"0003/002  ")
> MONICA GUADALUPE
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%mes$: Nombre de un mes

~~~
FN%mes$(LOCAL mes$)
~~~

- Descripción:

Retorna el nombre en letras del *mes$* en números.

- Argumentos:

  |Argumento|Descripción|
  |:--------|-----------|
  |mes$|Número del mes|

- Ejemplo:

~~~
PRINT FN%mes$("10")
> Octubre
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%mescrito$: Monto escrito

~~~
FN%mescrito$(LOCAL monto)
~~~

- Descripción:

Retorna el número enviado en letras.

- Argumentos:
  |Argumento|Descripción|
  |:--------|-----------|
  |monto|Monto o cifra a convertir en letras

- Ejemplo:

~~~
PRINT FN%mescrito$(24528.12)
> VEINTICUATRO MIL QUINIENTOS VEINTIOCHO CON 12 CENTIMOS
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%no_todo: Que la explique JL

~~~
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

~~~
FN%no_todo(listbox.ctl, "","REC.TIPO=""75""","INVGRUPO","")
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%ope_valido: Operador válido para una función específica

~~~
FN%ope_valido(LOCAL funcion$)
~~~

- Descripción:

Retorna verdadero (1) sí el usuario actual (**%base_login$**), esta autorizado en la *funcion$* específica (**CTLFNOPE**), de lo contrario retorna falso (0)

- Argumentos:
  |Argumento|Descripción|
  |:--------|-----------|
  |funcion$|Nombre de la función específica|

- Ejemplo:

~~~
PRINT FN%ope_valido("VER_SALDOS")
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%pos: Busca un texto en otro texto

~~~
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

~~~
PRINT fn%pos("ÁéÍóÚ","aeIOu")
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%precision: Ajustar precisión a un monto

~~~
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
  
~~~
PRINT FN%precision(249.02193822,3)
> 249.022
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%tabla: Busca un valor en una variable

~~~
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

~~~
tabla$="01020304"
PRINT FN%tabla$("10",tabla$,2)
> 0
PRINT FN%tabla$("02",tabla$,2)
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%tbl$: Traduce acentos en un texto

~~~
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

~~~
OPEN(unt)"*windev*"
PRINT (lfo)fn%tbl$(lfo,"ÁéÍóÚ")
PRINT fn%tbl$(lfo,"ÁéÍóÚ")
>  ‚¡¢£
CLOSE(lfo)
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

## [Rutinas Públicas (RP_XXXXX):](#rp_xxxxx---rutinas-públicas)

Definición de lo que son las rutinas públicas.

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### RP_CATAL

#### - RP_CATAL;CATALOGO

Catálogo de la Aplicación

- Parámetros:
  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |CIA$|E||
  |APLIC|E||
  |CATAL|E|
  |LCAT$[ALL]|E|
  |IND_CAT|E|
  |OPC$|E|

~~~
CALL "RP_CATAL",%BASE_CIA$,...
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

#### - RP_CATAL;APLICACIONES

Tabla de Aplicaciones

- Parámetros:

  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |TAB_APL$|S|Contiene la lista de aplicaciones de BG|

~~~
CALL "RP_CATAL;APLICACIONES",TAB_APL$
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### RP_FECHA

#### - RP_FECHA;AJUSTAR: Ajustar una fecha

Ajusta una fecha, en días, meses y/o años, retornando la fecha resultante.

- Parámetros:
  
  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |FECHA_ORIGINAL$|E|Fecha inicial para el cálculo (DDMMAAAA, DD/MM/AAAA, DDMMAA o DD/MM/AA)|
  |DIAS|E|Ajuste algebraico del día|
  |MESES|E|Ajuste algebraico del mes|
  |AÑOS|E|Ajuste algebraico del año|
  |FECHA_RESULTADO$|S|Fecha resultante, sí la fecha resultante es nula es porque la fecha original es inválida|
  |OPCIONES$|E|Opciones de la rutina|

  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |-U|Ajustar hasta el ultimo dia del mes|
    |-H|Ajustar en dias habiles (DIAS)|

- Ejemplos:

~~~
CALL "RP_FECHA;AJUSTAR","01/10/2025",10,0,0,""
> 11102025
CALL "RP_FECHA;AJUSTAR","01/10/2025",0,0,0,"-U"
> 31102025
CALL "RP_FECHA;AJUSTAR","01/10/2025",0,1,0,"-H"
> 01112025
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

## [Rutinas Utilitarias (RU_XXXXX):](#ru_xxxxx---rutinas-utilitarias)

Definición de lo que son las rutinas utilitarias.

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### RU_COPY

Copia de registros.

>Anteriormente: `HLCOPY`

~~~
CALL "RU_COPY"
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)
