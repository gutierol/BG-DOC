# BASE Gráfico - Índice de Ayuda para Asesores
---
- [BASE Gráfico - Índice de Ayuda para Asesores](#base-gráfico---índice-de-ayuda-para-asesores)
  - [Funciones Globales:](#funciones-globales)
    - [FN%acum(LOCAL archivo$, LOCAL campo$, LOCAL clave$, LOCAL opciones$)](#fnacumlocal-archivo-local-campo-local-clave-local-opciones)
    - [fn%fecha$(LOCAL fecha$)](#fnfechalocal-fecha)
    - [FN%fecinv$(LOCAL fecha$)](#fnfecinvlocal-fecha)
    - [FN%fecha\_letras$(LOCAL fecha$)](#fnfecha_letraslocal-fecha)
    - [FN%find$(LOCAL archivo$, LOCAL campo$, LOCAL clave$)](#fnfindlocal-archivo-local-campo-local-clave)
    - [FN%mes$(LOCAL mes$)](#fnmeslocal-mes)
    - [FN%mescrito$(LOCAL monto)](#fnmescritolocal-monto)
    - [FN%no\_todo(LOCAL num\_ctl, LOCAL cond$, LOCAL botones$, LOCAL archivo$, LOCAL posic$)](#fnno_todolocal-num_ctl-local-cond-local-botones-local-archivo-local-posic)
    - [FN%ope\_valido(LOCAL funcion$)](#fnope_validolocal-funcion)
    - [FN%pos(LOCAL texto1$, LOCAL texto2$)](#fnposlocal-texto1-local-texto2)
    - [FN%precision(LOCAL valor, LOCAL decimales)](#fnprecisionlocal-valor-local-decimales)
    - [FN%tabla(LOCAL valor$, LOCAL tabla$, LOCAL longitud)](#fntablalocal-valor-local-tabla-local-longitud)
    - [FN%tbl$(LOCAL lp, LOCAL lin$)](#fntbllocal-lp-local-lin)
  - [Rutinas Públicas (RP\_XXXXX):](#rutinas-públicas-rp_xxxxx)
    - [RP\_CATAL](#rp_catal)
      - [RP\_CATAL;CATALOGO](#rp_catalcatalogo)
      - [RP\_CATAL;APLICACIONES](#rp_catalaplicaciones)
  - [Rutinas Utilitarias (RU\_XXXXX):](#rutinas-utilitarias-ru_xxxxx)

## [Funciones Globales:](#funciones-globales)

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

Funciones de usuario definidas de forma global para mejorar la codificación en los programas.

### FN%acum(LOCAL archivo$, LOCAL campo$, LOCAL clave$, LOCAL opciones$)

Retorna la acumulación de un *campo$* en un *archivo$* de los registros con la *clave$* indicada, y con *opciones$* que pueden ser:

    - KNO[numero_de_llave]: llave o índice del archivo
    - CND[Condición]: condición que deben cumplir los registros
~~~
PRINT FN%acum("FACENCAB","MONTO","HLS"+"200001","KNO[0] CND[REC.TIPO$=""FA""]")
> 8752336.98
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### fn%fecha$(LOCAL fecha$)

Retorna una variable que contiene una fecha válida end formato ddmmaaaa, formateada del modo dd/mm/aaaa.
~~~
PRINT FN%fecha$("24102025")
> 24/10/2025
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%fecinv$(LOCAL fecha$)

Retorna el valor enviado (ddmmaaaa) de forma invertida: aaaammaa.
~~~
PRINT FN%fecinv$("24102025")
> 20251024
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%fecha_letras$(LOCAL fecha$)

Retorna la fecha enviada en letra, para ser usada por ejemplo en cartas.
~~~
PRINT FN%fecha_letras$("24102025")
> 24 de Octubre de 2025
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%find$(LOCAL archivo$, LOCAL campo$, LOCAL clave$)

Retorna el valor del *campo$* contenido en el registro con llave primaria *clave$* del *archivo$, sí no consigue la *clave$* retorna un valor vacio.
~~~
PRINT FN%find$("CTLCIAS","CIA_NOM","HLS")
> H.L. Sistemas S.R.L.
PRINT FN%find$("NOMDESCR","NOMBRE","HLS"+"0003/002  ")
> MONICA GUADALUPE
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%mes$(LOCAL mes$)

Retorna el nombre en letras del *mes$* en números.
~~~
PRINT FN%mes$("10")
> Octubre
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%mescrito$(LOCAL monto)

Retorna el número enviado en letras.
~~~
PRINT FN%mescrito$(24528.12)
> VEINTICUATRO MIL QUINIENTOS VEINTIOCHO CON 12 CENTIMOS
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%no_todo(LOCAL num_ctl, LOCAL cond$, LOCAL botones$, LOCAL archivo$, LOCAL posic$)

Que me la explique JL.
~~~
FN%no_todo(listbox.ctl, "","REC.TIPO=""75""","INVGRUPO","")
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%ope_valido(LOCAL funcion$)

Retorna verdadero (1) sí el usuario actual (**%base_login$**), esta autorizado en la *funcion$* específica (**CTLFNOPE**), de lo contrario retorna falso (0)
~~~
PRINT FN%ope_valido("VER_SALDOS")
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%pos(LOCAL texto1$, LOCAL texto2$)

Compara *texto1$* dentro de *texto2$* sin importar que contengan acentos, mayúsculas y/o minúsculas. Retorna verdadero (1) sí son iguales, falso (0) si son diferentes y -1 si *texto1$* esta vacío. 
~~~
PRINT fn%pos("ÁéÍóÚ","aeIOu")
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%precision(LOCAL valor, LOCAL decimales)

Retorna el *valor* ajustado a la precision de *decimales*.
~~~
PRINT FN%precision(249.02193822,3)
> 249.022
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%tabla(LOCAL valor$, LOCAL tabla$, LOCAL longitud)

Retorna verdadero (1) o falso (0) sí el elemento *valor$* se encuentra contenido dentro de la variable *tabla$*, haciendo la busqueda del elemento con la *longitud* indicada.
~~~
tabla$="01020304"
PRINT FN%tabla$("10",tabla$,2)
> 0
PRINT FN%tabla$("02",tabla$,2)
> 1
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)

### FN%tbl$(LOCAL lp, LOCAL lin$)

Traduce acentos en una cadena *lin$* para la impresión directa por el canal *lp*.
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

#### RP_CATAL;CATALOGO
Catálogo de la Aplicación

Parámetros:
~~~
CIA$,APLIC,CATAL,LCAT$[ALL],IND_CAT,OPC$
~~~

#### RP_CATAL;APLICACIONES
Tabla de Aplicaciones

Parámetros
~~~
TAB_APL$
~~~

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)


## [Rutinas Utilitarias (RU_XXXXX):](#ru_xxxxx---rutinas-utilitarias)

Definición de lo que son las rutinas utilitarias.

[Volver arriba](#base-gráfico---índice-de-ayuda-para-asesores)
