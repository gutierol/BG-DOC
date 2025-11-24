<!-- title: BASE Gráfico -->
# BASE Gráfico &reg;

[![BASE Gráfico](https://basegrafico.com/img/logo-image.png)](https://basegrafico.com/)

## Índice de Ayuda para Asesores<!-- omit from toc -->

---

- [BASE Gráfico ®](#base-gráfico-)
  - [Funciones Globales:](#funciones-globales)
    - [FN%acum: Acumula un campo númerico de un archivo](#fnacum-acumula-un-campo-númerico-de-un-archivo)
    - [FN%fecha$: Formatea una fecha](#fnfecha-formatea-una-fecha)
    - [FN%fecha\_letras$: Fecha en letras](#fnfecha_letras-fecha-en-letras)
    - [FN%fecinv$: Invierte una fecha](#fnfecinv-invierte-una-fecha)
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
    - [RP\_CATAL: Manejo del catálogo](#rp_catal-manejo-del-catálogo)
      - [RP\_CATAL;APLICACIONES: Leer tabla de aplicaciones](#rp_catalaplicaciones-leer-tabla-de-aplicaciones)
      - [RP\_CATAL;CATALOGO: Leer catálogo de una aplicación](#rp_catalcatalogo-leer-catálogo-de-una-aplicación)
    - [RP\_FECHA: Manejo de Fechas](#rp_fecha-manejo-de-fechas)
      - [RP\_FECHA;AJUSTAR: Ajustar una fecha](#rp_fechaajustar-ajustar-una-fecha)
      - [RP\_FECHA;CALENDARIO: Días entre dos fechas](#rp_fechacalendario-días-entre-dos-fechas)
      - [RP\_FECHA;DIASEM: Día de la semana](#rp_fechadiasem-día-de-la-semana)
      - [RP\_FECHA;EDAD: Diferencia entre dos fechas](#rp_fechaedad-diferencia-entre-dos-fechas)
      - [RP\_FECHA;EDITAR: Validar y editar una fecha](#rp_fechaeditar-validar-y-editar-una-fecha)
      - [RP\_FECHA;JULIANO: Cálculo del día en juliano](#rp_fechajuliano-cálculo-del-día-en-juliano)
      - [RP\_FECHA;LETRAS: Fecha en letras](#rp_fechaletras-fecha-en-letras)
      - [RP\_FECHA;VALIDATOR: Validar una fecha](#rp_fechavalidator-validar-una-fecha)
      - [RP\_FECHA;VALIDATOR\_MES: Validar un mes](#rp_fechavalidator_mes-validar-un-mes)
    - [RP\_FILE: Operaciones sobre archivos](#rp_file-operaciones-sobre-archivos)
      - [RP\_FILE;ABRIR\_ARCHIVOS\_DATOS: Abrir archivos de una aplicación](#rp_fileabrir_archivos_datos-abrir-archivos-de-una-aplicación)
      - [RP\_FILE;ABRIR\_ARCHIVOS\_DATOS\_BLANCO: Abrir los archivos de una aplicación y llenar campos](#rp_fileabrir_archivos_datos_blanco-abrir-los-archivos-de-una-aplicación-y-llenar-campos)
      - [RP\_FILE;CERRAR\_ARCHIVOS\_DATOS: Cerrar los archivos de una aplicación](#rp_filecerrar_archivos_datos-cerrar-los-archivos-de-una-aplicación)
      - [RP\_FILE;COPIAR: Copia de registros](#rp_filecopiar-copia-de-registros)
      - [RP\_FILE;COPIAR\_ARCHIVO: Copiar un archivo completo](#rp_filecopiar_archivo-copiar-un-archivo-completo)
      - [RP\_FILE;EXPORTAR\_REGISTRO: Exportar registros](#rp_fileexportar_registro-exportar-registros)
      - [RP\_FILE;IMPORTAR\_REGISTRO: Importar registros](#rp_fileimportar_registro-importar-registros)
      - [RP\_FILE;OPEN: Apertura de archivos](#rp_fileopen-apertura-de-archivos)
      - [RP\_FILE;PGM\_STR: Grabar un programa en un archivo tipo SERIAL](#rp_filepgm_str-grabar-un-programa-en-un-archivo-tipo-serial)
      - [RP\_FILE;REMOVE: Eliminación de registros](#rp_fileremove-eliminación-de-registros)
      - [RP\_FILE;WORK: Genera nombre de archivo de trabajo](#rp_filework-genera-nombre-de-archivo-de-trabajo)
    - [RP\_FORMA: Impresión de Formatos](#rp_forma-impresión-de-formatos)
      - [RP\_FORMA;ENCABEZADO: Preparación de datos del encabezado](#rp_formaencabezado-preparación-de-datos-del-encabezado)
      - [RP\_FORMA;DETALLE: Preparación de datos del detalle](#rp_formadetalle-preparación-de-datos-del-detalle)
      - [RP\_FORMA;FIN: Finalizar e imprimir la forma](#rp_formafin-finalizar-e-imprimir-la-forma)
      - [RP\_FORMA;FIN\_MULTIPLE: Finalizar la impresión múltiple](#rp_formafin_multiple-finalizar-la-impresión-múltiple)
    - [RP\_GRID: Utilidades para objetos tipo GRID](#rp_grid-utilidades-para-objetos-tipo-grid)
      - [RP\_GRID;ACT\_BOTONES: Activar botones del GRID](#rp_gridact_botones-activar-botones-del-grid)
      - [RP\_GRID;ACT\_CHECKMARK: Activar botones de chequeo en el GRID](#rp_gridact_checkmark-activar-botones-de-chequeo-en-el-grid)
      - [RP\_GRID;ACT\_COLUMNAS: Activar columnas en el GRID](#rp_gridact_columnas-activar-columnas-en-el-grid)
      - [RP\_GRID;AD\_LINEA: Agregar una línea al GRID](#rp_gridad_linea-agregar-una-línea-al-grid)
      - [RP\_GRID;COLUMNAS: Prepara plantilla con variables de columnas](#rp_gridcolumnas-prepara-plantilla-con-variables-de-columnas)
      - [RP\_GRID;DEL\_LINEA: Elimina una línea del GRID renumerando la columna descriptiva (0)](#rp_griddel_linea-elimina-una-línea-del-grid-renumerando-la-columna-descriptiva-0)
      - [RP\_GRID;DES\_BOTONES: Desactivar botones en el GRID](#rp_griddes_botones-desactivar-botones-en-el-grid)
      - [RP\_GRID;DES\_COLUMNAS: Desactivar columnas en el GRID](#rp_griddes_columnas-desactivar-columnas-en-el-grid)
      - [RP\_GRID;GRABAR\_GRID: Grabar valores en una línea indicada](#rp_gridgrabar_grid-grabar-valores-en-una-línea-indicada)
      - [RP\_GRID;LEER\_LINEA: Leer valores de una línea dada](#rp_gridleer_linea-leer-valores-de-una-línea-dada)
      - [RP\_GRID;INS\_LINEA: Insertar una línea al GRID renumerando la columna descriptiva (0)](#rp_gridins_linea-insertar-una-línea-al-grid-renumerando-la-columna-descriptiva-0)
      - [RP\_GRID;LEER\_LINEA\_ACTUAL: Leer línea actual](#rp_gridleer_linea_actual-leer-línea-actual)
      - [RP\_GRID;ORDENAR: Ordenar el GRID](#rp_gridordenar-ordenar-el-grid)
      - [RP\_GRID;PREPARAR: Preparar inicialmente el GRID](#rp_gridpreparar-preparar-inicialmente-el-grid)
    - [RP\_GUI: Utilidades para Entorno  Gráfico](#rp_gui-utilidades-para-entorno--gráfico)
      - [RP\_GUI;CAMBIO\_FOLDER: Cambiar pestaña (FOLDER) activa](#rp_guicambio_folder-cambiar-pestaña-folder-activa)
      - [RP\_GUI;COMIENZO\_PROCESO: Ventana de proceso (Comienzo)](#rp_guicomienzo_proceso-ventana-de-proceso-comienzo)
      - [RP\_GUI;CONTINUAR\_PROCESO: Ventana de proceso (Continuar)](#rp_guicontinuar_proceso-ventana-de-proceso-continuar)
      - [RP\_GUI;FIN\_PROCESO: Ventana de proceso (Finalización)](#rp_guifin_proceso-ventana-de-proceso-finalización)
      - [RP\_GUI;DIALOGUE: Crear ventana de diálogo](#rp_guidialogue-crear-ventana-de-diálogo)
      - [RP\_GUI;INPUT: Lectura (INPUT) en entorno gráfico (No aplica para NOMADS)](#rp_guiinput-lectura-input-en-entorno-gráfico-no-aplica-para-nomads)
      - [RP\_GUI;MENU\_DISABLE: Deshabilitar opciones del MENU](#rp_guimenu_disable-deshabilitar-opciones-del-menu)
      - [RP\_GUI;MENU\_ENABLE: Habilitar opciones del MENU](#rp_guimenu_enable-habilitar-opciones-del-menu)
      - [RP\_GUI;PREPARA\_SELECT: Leer LIST\_BOX y preparación valores](#rp_guiprepara_select-leer-list_box-y-preparación-valores)
      - [RP\_GUI;SEL\_LIST: Selecciona una valor de una lista](#rp_guisel_list-selecciona-una-valor-de-una-lista)
      - [RP\_GUI;SIZE: Tomar el tamaño de la ventana](#rp_guisize-tomar-el-tamaño-de-la-ventana)
      - [RP\_GUI;UNT\_OBJETO: Tomar próximo número de objeto disponible](#rp_guiunt_objeto-tomar-próximo-número-de-objeto-disponible)
    - [RP\_LISTV: Utilidades para objetos tipo LIST\_VIEW](#rp_listv-utilidades-para-objetos-tipo-list_view)
      - [RP\_LISTV;COLUMNAS: Prepara TEMPLATE con variables de columnas](#rp_listvcolumnas-prepara-template-con-variables-de-columnas)
      - [RP\_LISTV;GRABAR\_LISTV: Grabar valores en una línea indicada](#rp_listvgrabar_listv-grabar-valores-en-una-línea-indicada)
      - [RP\_LISTV;LEER\_LINEA: Leer línea actual](#rp_listvleer_linea-leer-línea-actual)
      - [RP\_LISTV;LEER\_LINEA\_IND: Leer valores de una línea indicada](#rp_listvleer_linea_ind-leer-valores-de-una-línea-indicada)
      - [RP\_LISTV;PREPARAR: Preparar inicialmente el LIST\_VIEW](#rp_listvpreparar-preparar-inicialmente-el-list_view)
    - [RP\_PARAM: Lectura de parámetros y control de la aplicación](#rp_param-lectura-de-parámetros-y-control-de-la-aplicación)
      - [RP\_PARAM: Genera un TEMPLATE con los parámetros y controles](#rp_param-genera-un-template-con-los-parámetros-y-controles)
    - [RP\_QUERY: Despliegue o consulta de valores para seleccionar](#rp_query-despliegue-o-consulta-de-valores-para-seleccionar)
    - [RP\_REP: Manejo de Reportes](#rp_rep-manejo-de-reportes)
      - [RP\_REP;FORMATO: Preparar columnas y datos del reporte](#rp_repformato-preparar-columnas-y-datos-del-reporte)
  - [Rutinas Utilitarias (RU\_XXXXX):](#rutinas-utilitarias-ru_xxxxx)
    - [RU\_COPY](#ru_copy)

## [Funciones Globales:](#funciones-globales)

Funciones de usuario definidas de forma global para mejorar la codificación en los programas.

[Volver arriba](#top)

### FN%acum: Acumula un campo númerico de un archivo

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
  |""|Sin opciones|
  |KNO\[número_de_llave\]|Llave o índice del archivo a usar|
  |CND\[Condición\]|Condición que deben cumplir los registros|

- Ejemplo:

~~~text
-> PRINT FN%acum("FACENCAB","MONTO","HLS"+"200001","KNO[0] CND[REC.TIPO$=""FA""]")
8752336.98
~~~

[Volver arriba](#funciones-globales)

### FN%fecha$: Formatea una fecha

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
-> PRINT FN%fecha$("24102025")
24/10/2025
~~~

[Volver arriba](#funciones-globales)

### FN%fecha_letras$: Fecha en letras

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
-> PRINT FN%fecha_letras$("24102025")
24 de Octubre de 2025
~~~

[Volver arriba](#funciones-globales)

### FN%fecinv$: Invierte una fecha

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
-> PRINT FN%fecinv$("24102025")
20251024
~~~

[Volver arriba](#funciones-globales)

### FN%find$: Busca un valor de un campo en un archivo

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
-> PRINT FN%find$("CTLCIAS","CIA_NOM","HLS")
H.L. Sistemas S.R.L.
-> PRINT FN%find$("NOMDESCR","NOMBRE","HLS"+"0003/002  ")
MONICA GUADALUPE
~~~

[Volver arriba](#funciones-globales)

### FN%mes$: Nombre de un mes

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
-> PRINT FN%mes$("10")
Octubre
~~~

[Volver arriba](#funciones-globales)

### FN%mescrito$: Monto escrito

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
-> PRINT FN%mescrito$(24528.12)
VEINTICUATRO MIL QUINIENTOS VEINTIOCHO CON 12 CENTIMOS
~~~

[Volver arriba](#funciones-globales)

### FN%no_todo: Que la explique JL

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

### FN%ope_valido: Operador válido para una función específica

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
-> PRINT FN%ope_valido("VER_SALDOS")
1
~~~

[Volver arriba](#funciones-globales)

### FN%pos: Busca un texto en otro texto

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
-> PRINT fn%pos("ÁéÍóÚ","aeIOu")
1
~~~

[Volver arriba](#funciones-globales)

### FN%precision: Ajustar precisión a un monto

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
-> PRINT FN%precision(249.02193822,3)
249.022
~~~

[Volver arriba](#funciones-globales)

### FN%tabla: Busca un valor en una variable

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
-> tabla$="01020304"
-> PRINT FN%tabla$("10",tabla$,2)
0
-> PRINT FN%tabla$("02",tabla$,2)
1
~~~

[Volver arriba](#funciones-globales)

### FN%tbl$: Traduce acentos en un texto

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
-> OPEN(unt)"*windev*"
-> PRINT (lfo)fn%tbl$(lfo,"ÁéÍóÚ")
-> PRINT fn%tbl$(lfo,"ÁéÍóÚ")
 ‚¡¢£
-> CLOSE(lfo)
~~~

[Volver arriba](#funciones-globales)

## [Rutinas Públicas (RP_XXXXX):](#rutinas-públicas-rp_xxxxx)

Definición de lo que son las rutinas públicas.

[Volver arriba](#top)

### RP_CATAL: Manejo del catálogo

Para realizar operaciones relacionadas al catálogo de funciones. Típicamente usada en programas de control de procesos (Mantenimiento y Listado del Catálogo, Permisos de Grupos y/o Operadores, etc.)

#### RP_CATAL;APLICACIONES: Leer tabla de aplicaciones

Leer tabla de aplicaciones

~~~text
CALL "RP_CATAL;APLICACIONES",TAB_APL$
~~~

- Parámetros:

  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |TAB_APL$|S|Tabla con las aplicaciones (Separadas con \$09\$)|

~~~text
CALL "RP_CATAL;APLICACIONES",TAB_APL$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_CATAL;CATALOGO: Leer catálogo de una aplicación

Leer catálogo de una aplicación.

~~~text
CALL "RP_CATAL;CATALOGO",CIA$, APLIC, CATAL, LCAT${ALL}, IND_CAT, OPC$
~~~

- Parámetros:
  
  | Parámetro | E/S | Descripción |
  |:----------|:---:|-------------|
  |CIA$|E|Código de Compañía (Normalmente %BASE_CIA_CATA$)|
  |APLIC|E|Objeto (List_Box o Drop_Box) donde está seleccionada la Aplicación|
  |CATAL|E|Objeto (Tree_View) donde se va a generar el catálogo|
  |LCAT$\{ALL\}|S|Líneas del Catálogo (Clave en el archivo CTLCATAL)|
  |IND_CAT|S|Total de Líneas del Catálogo|
  |OPC$|E|Opciones Adicionales (Separadas con Espacio)|

  - Opciones:
  
    |Opción|Descripción|
    |:-----|-----------|
    |""|Sin opciones|
    |SOLO_MENU|No Incluir Procesos, solo sub_menus|
    |AGREGAR_FIN|Agregar línea <Fin del Catálogo> por sub_menu|
    |NO_OBJ_CATAL|No hay Objeto (Tree_view) con catálogo|

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FECHA: Manejo de Fechas

Permite realizar las operaciones asociadas al cálculo, edición, validación, etc. de una o varias fechas.

#### RP_FECHA;AJUSTAR: Ajustar una fecha

Ajuste algebraico de una fecha en días, meses y años.

~~~text
CALL “RP_FECHA;AJUSTAR”,FECHA_ORIGEN$,DIAS,MESES,AÑOS,FECHA_RESULTADO$,OPCIONES$
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
    |""|Sin opciones|
    |-U|Ajustar hasta el ultimo dia del mes|
    |-H|Ajustar días basado en los días hábiles (Archivo CTLCALEN)|

- Ejemplos:

~~~text
-> CALL "RP_FECHA;AJUSTAR","01/10/2025",10,0,0,FECHA_RESULTADO$,""
-> PRINT FECHA_RESULTADO$
11102025
-> CALL "RP_FECHA;AJUSTAR","01/10/2025",0,0,0,FECHA_RESULTADO$,"-U"
-> PRINT FECHA_RESULTADO$
31102025
-> CALL "RP_FECHA;AJUSTAR","01/10/2025",0,1,0,FECHA_RESULTADO$,"-H"
-> PRINT FECHA_RESULTADO$
01112025
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;CALENDARIO: Días entre dos fechas

Calcula los días hábiles, calendario y feriados entre dos fechas

~~~text
CALL “RP_FECHA;CALENDARIO”,DESDE$,HASTA$,CAL{ALL},HAB{ALL},FER{ALL},TIPO$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |DESDE$|E|Fecha de Comienzo (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |HASTA$|E|Fecha de Finalización (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |CAL\{ALL\}|S|Matriz de 7 posiciones con los días calendario (0=domingos, 1=lunes, ..., 6=sábados, 7=total)|
  |HAB\{ALL\}|S|Matriz de 7 posiciones con los días hábiles (0=domingos, 1=lunes, ..., 6=sábados, 7=total)|
  |FER\{ALL\}|S|Matriz de 7 posiciones con los días feriados (0=domingos, 1=lunes, ..., 6=sábados, 7=total). Se basa en el archivo CTLCALEN|
  |TIPO$|E|Tipo de Feriado a tomar|

  - Tipo: Tipo de Feriado

    |TIPO$|Descripción|
    |:--:|-|
    |N|Nacional|
    |B|Bancario|
    |F|Compañía|
    |""|Cualquiera|

- Ejemplos:

~~~text
-> CALL "RP_FECHA;CALENDARIO","20071969","20081969",CAL[ALL],HAB[ALL],FER[ALL],""
-> PRINT CAL[ALL]
5 5 5 5 4 4 4 32 ! 32 días en total, 5 domingos, 4 sábados

-> PRINT HAB[ALL]
0 5 5 5 4 4 0 23 ! 23 días hábiles total, 5 lunes, 4 jueves

-> PRINT FER[ALL]
0 0 0 0 0 0 0 ! No hubo días feriados en el periodo
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;DIASEM: Día de la semana

Día de la semana de una fecha.

~~~text
CALL "RP_FECHA;DIASEM",FECHA_ORIGEN$,DSEM,DIA$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha de Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |DSEM|S|Día de la semana en número (0 = domingo, 6 = sábado)|
  |DIA$|S|Día de la semana en letras (Dom,Lun,....,Sab)|

- Ejemplo:

~~~text
-> CALL "RP_FECHA;DIASEM","20071969",DIA,DIA$
-> PRINT DIA
0
-> PRINT DIA$
Dom
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;EDAD: Diferencia entre dos fechas

Cálculo de la edad o diferencia entre dos fechas.

~~~text
CALL "RP_FECHA;EDAD",DESDE$,HASTA$,AÑOS,MESES,DIAS
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
-> CALL "RP_FECHA;EDAD","20071969","01082001",AÑOS,MESES,DIAS
-> PRINT AÑOS,MESES,DIAS
32 0 12
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;EDITAR: Validar y editar una fecha

Validar y editar fecha.

~~~text
CALL "RP_FECHA;EDITAR",FECHA_ORIGEN$,FECHA_SIN_FMT$,FECHA_CON_FMT$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha Origen (ddmmaaaa, dd/mm/aaaa, ddmmaa o dd/mm/aa)|
  |FECHA_SIN_FMT$|S|Fecha en formato ddmmaaaa (""=no es válida)|
  |FECHA_CON_FMT$|S|Fecha en formato dd/mm/aaaa (""=no es válida)|

- Ejemplo:

~~~text
-> CALL "RP_FECHA;EDITAR","200769",FECHA1$,FECHA2$
-> PRINT FECHA1$
20071969

-> PRINT FECHA2$
20/07/1969
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;JULIANO: Cálculo del día en juliano

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
-> CALL "RP_FECHA;JULIANO","20071969",JULIANO,AÑO
-> PRINT JULIANO
718997
-> PRINT AÑO
201
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;LETRAS: Fecha en letras

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
-> CALL "RP_FECHA;LETRAS","20071969",DIA$
-> PRINT DIA$
20 de Julio de 1969
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;VALIDATOR: Validar una fecha

Validar una fecha desde NOMADS.

~~~text
CALL "RP_FECHA;VALIDATOR",FECHA_ORIGEN$,ERR$,TAG$,OLD$,EOM$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha a validar (ddmmaaaa)|
  |ERR$|S|Mensaje de error (""=No hubo error)|
  |TAG$|E|Tag de usuario para el objeto|
  |OLD$|E|Valor anterior del campo|
  |EOM$|E|Valor de EOM (Forma de Input)|

- Ejemplo:
La llamada la hace NOMADS automáticamente cuando tiene RP_FECHA;VALIDATOR en el campo "VALIDATOR" del objeto.

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FECHA;VALIDATOR_MES: Validar un mes

~~~text
CALL "RP_FECHA;VALIDATOR_MES", FECHA_ORIGEN$,ERR$,TAG$,OLD$,EOM$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |FECHA_ORIGEN$|E|Fecha a validar (mmaaaa)|
  |ERR$|S|Mensaje de error (""=No hubo error)|
  |TAG$|E|Tag de usuario para el objeto|
  |OLD$|E|Valor anterior del campo|
  |EOM$|E|Valor de EOM (Forma de Input)|

- Ejemplo:
La llamada la hace NOMADS automáticamente cuando tiene RP_FECHA;VALIDATOR_MES en el campo "VALIDATOR" del objeto.

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FILE: Operaciones sobre archivos

Permite realizar las operaciones rutinarias relacionadas a archivos. Aunque algunas de ellas básicamente reemplazan verbos de <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a>, deben ser utilizados para mantener un estándar y ampliar las posibilidades (ODBC, ORACLE, etc.)

#### RP_FILE;ABRIR_ARCHIVOS_DATOS: Abrir archivos de una aplicación

Abrir todos los archivos de una aplicación, según se especifica en CTLFORAR, serán abiertos y los canales correspondientes así como su "IOLIST" serán identificados con su nombre.

~~~text
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS"
~~~

- Variables a definir antes de la ejecución:

  |Variable|E/S|Descripción|
  |:--------|:-:|-----------|
  |KAPL$|E|Código de la aplicación. (""=activa)|

- Ejemplo:

~~~text
KPAL$="10" ! Aplicación de Nómina
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS"

->? NOMDPTOS
15

->? LST(IOL(NOMDPTOS$))
IOLIST CIA$,CODIGO$,DESCRIP$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;ABRIR_ARCHIVOS_DATOS_BLANCO: Abrir los archivos de una aplicación y llenar campos

Abrir todos los archivos de una aplicación, según se especifica en CTLFORAR, para imprimir los modelos de los formatos.

~~~text
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS_BLANCOS"
~~~

- Variables a definir antes de la ejecución:

  |Variable|E/S|Descripción|
  |:--------|:-:|-----------|
  |KAPL$|E|Código de la aplicación. (""=activa)|

- Ejemplo:

~~~text
KPAL$="10" ! Aplicación de Nómina
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS_BLANCOS"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;CERRAR_ARCHIVOS_DATOS: Cerrar los archivos de una aplicación

Cerrar todos los archivos de una aplicación, según se especifica en CTLFORAR.

~~~text
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS_BLANCOS"
~~~

- Variables a definir antes de la ejecución:

  |Variable|E/S|Descripción|
  |:--------|:-:|-----------|
  |TAB_CAN$|E|Tabla de canales abiertos por "RP_FILE;ABRIR_ARCHIVOS_DATOS"|

- Ejemplo:

~~~text
KPAL$="10" ! Aplicación de Nómina
PERFORM "RP_FILE;ABRIR_ARCHIVOS_DATOS_BLANCOS"
...
PERFORM "RP_FILE;CERRAR_ARCHIVOS_DATOS"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;COPIAR: Copia de registros

Copiar registros de un archivo origen a un archivo destino.

~~~text
CALL “RP_FILE;COPIAR”, CANAL1,CANAL2,KNUM,POSIC$,EXEC$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |CANAL1|E|Canal donde está abierto el archivo de origen|
  |CANAL2|E|Canal donde está abierto el archivo de destino|
  |KNUM|E|Número de clave de ordenación (0=principal)|
  |POSIC$|E|Prefijo de posicionamiento (clave de copia)|
  |EXEC$|E|Comando a ejecutar antes del <a href="https://manual.pvxplus.com/PXPLUS/directives/write.htm" target="_blank">WRITE()</a> de la copia|

- Ejemplo:

Copia todas las cuentas de la compañía "HLS" a la compañía "LAT":

~~~text
> CALL "RP_FILE;OPEN","MGADESCR",CANDES1
> CALL "RP_FILE;OPEN","MGADESCR",CANDES2
> CALL "RP_FILE;COPIAR",CANDES1,CANDES2,0,"HLS","REC.CIA$="+QUO+"LAT"+QUO
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;COPIAR_ARCHIVO: Copiar un archivo completo

Copiar un archivo completo, de forma física.

~~~text
CALL "RP_FILE;COPIAR_ARCHIVO",ORIGEN$,DESTINO$,OK
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |ORIGEN$|E|Nombre del archivo original|
  |DESTINO$|E|Nombre del archivo copia|
  |OK|S|Resultado de la copia (OK=1, No OK=0)|

- Ejemplo:

Copiar un archivo a través de la red vía Windx:

~~~text
CALL "RP_FILE;COPIAR_ARCHIVO","FOTO.BMP",%BASE_WDX$+"FOTO.BMP",OK
-> ? OK
1
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;EXPORTAR_REGISTRO: Exportar registros

Permite la exportación de registros de BASE Gráfico &reg; a archivo plano con extensión .BGR

~~~text
CALL "RP_FILE;EXPORTAR_REGISTRO",CAN_SER,CAN_ORI,KPOS$,TOTAL
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |CAN_SER|E|Canal donde está abierto el archivo serial (con extensión .BGR)|
  |CAN_ORI|E|Canal donde está abierto el archivo origen (<a href="https://manual.pvxplus.com/PXPLUS/PxPlus%20User%20Guide/File%20Handling/Data%20Files/Keyed%20Files.htm" target="_blank">Keyed Files</a>)|
  |KPOS$|E|Clave de Posicionamiento|
  |TOTAL|S|Total de registros exportados|

- Ejemplos:

Crear un archivo serial que contenga todos los registros de la compañía para 2 archivos.

~~~text
CALL "RP_FILE;EXPORTAR_REGISTRO",TXT,NOMDESCR,%BASE_CIA$,T
CALL "RP_FILE;EXPORTAR_REGISTRO",TXT,NOMHISNO,%BASE_CIA$,T
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;IMPORTAR_REGISTRO: Importar registros

Permite la importación de registros desde un archivo plano con extensión .BGR a un archivo de BASE Grafico &reg;.

~~~text
CALL "RP_FILE;IMPORTAR_REGISTRO",CAN_SER,TAB_FILE$,CANALES$,OK,OPC$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |CAN_SER|E|Canal donde está abierto el archivo serial (con extensión .BGR)|
  |TAB_FILE$|E|Tabla de archivos válidos para la importación|
  |CANALES$|E|Template: Canales donde quedan abiertos los archivos MEMORY de trabajo|
  |OK|S|Resultado de la importación|
  |OPC$|E|Opciones adicionales|

  - Opciones:

    |Opciones|Descripción|
    |:-------|-----------|
    |""|Sin opción| 
    |NO_CIA|No usar la compañía|

- Ejemplo:

~~~text
CALL "RP_FILE;IMPORTAR_REGISTROS",TXT,"NOMDESCR,NOMHISNO",CANAL$,OK,""
SELECT *,REC=DES$ FROM CANAL.NOMDESCR BEGIN "" END $FF$
LIST_BOX LOAD EMP.CTL,0,DES.CODIGO$+SEP+ES.NOMBRE$
NEXT RECORD
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;OPEN: Apertura de archivos

Apertura de archivos, incluido su diccionario de datos. Puede remplazar la directiva <a href="https://manual.pvxplus.com/PXPLUS/directives/open.htm" target="_blank">OPEN()</a>.

~~~text
CALL "RP_FILE;OPEN",NOMBRE$,CANAL[,OPC$]
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |NOMBRE$|E|Nombre del Archivo a abrir. El archivo será abierto de la forma (IOL=*) para tomar el diccionario de datos interno. Ver directiva <a href="https://manual.pvxplus.com/PXPLUS/directives/open.htm" target="_blank">OPEN()</a> de <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a>|
  |CANAL|E/S|Canal en el que se abrió el archivo (0=No se pudo abrir). Como entrada sí se acompaña de la opción USAR_CANAL|
  |OPC$|E|Opciones|

  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |""|Sin opciones|
    |NO_IOL|Abrir el archivo sin usar el diccionario de datos interno (IOL=*)|
    |NO_ERROR|No mostrar ventana de error si no se puede abrir|
    |USAR_CANAL|Abrir archivo en CANAL especificado|

- Ejemplos:

Abrir un archivo:

~~~text
-> CALL "RP_FILE;OPEN","MGADESCR",CANDES
-> PRINT LST(IOL(CANDES))
IOLIST  CIA$,CUENTA$,DESC_CTA$,TITULO$,CENTRO$,AUXIL$,OTROS1$,OTROS2$,OTROS3$
~~~

Abrir un directorio: 

~~~text
-> CALL "RP_FILE;OPEN","C:\MIS DOCUMENTOS",DISCO_C,"NO_IOL NO_ERROR" 
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;PGM_STR: Grabar un programa en un archivo tipo SERIAL

Graba un programa a un archivo plano.

~~~text
CALL "RP_FILE;PGM_STR",IN$,OUT$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |IN$|E|Nombre del programa a convertir|
  |OUT$|E|Nombre del archivo SERIAL resultante (no debe existir)|

- Ejemplo:
  
~~~text
ARCH$="NOMCTL40.TXT"
ERASE ARCH$,ERR=*NEXT
CALL "RP_FILE;PGM_STR","NOMCTL40",ARCH$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;REMOVE: Eliminación de registros

Elimina registros de un archivo.

~~~text
CALL "RP_FILE;REMOVE",CANAL,KNUM,POSIC$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |CANAL|E|Canal donde está abierto el archivo|
  |KNUM|E|Número de clave de ordenación (0=principal)|
  |POSIC$|E|Prefijo de posicionamiento (clave de eliminación)|

- Ejemplo:

Eliminar todas las cuentas de la compañía HLS

~~~text
-> CALL "RP_FILE;OPEN","MGADESCR",CANDES
-> CALL "RP_FILE;REMOVE",CANDES,0,"HLS" 
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FILE;WORK: Genera nombre de archivo de trabajo

Genera un nombre de archivo de trabajo en el directorio temporal del sistema operativo.

~~~text
CALL "RP_FILE;WORK",ARCHIVO$
~~~

- Parámetros:

  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |ARCHIVO$|S|Nombre del archivo de trabajo a crear|

- Ejemplo:

~~~text
-> CALL “RP_FILE;WORK”,ARCHIVO$
-> ? ARCHIVO$
C:\WINDOWS\TEMP\WRK1717.JL
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_FORMA: Impresión de Formatos

Perimite preparar e imprimir un formato de impresión definido.

Debe ser llamado con el verbo <a href="https://manual.pvxplus.com/PXPLUS/directives/perform.htm" target="_blank">PERFORM</a> de <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a> para compartir todas las variables del programa.

Esta rutina se basa en la definición de formatos (CTLSYS80) que contempla cada aplicación.

Con %SEL_MULTIPLE=1 antes de la llamada a la rutina le estamos indicando que se pueden imprimir múltiples documentos antes de cerrar la impresión, por ejemplo al imprimir los recibos de pago de nómina.

#### RP_FORMA;ENCABEZADO: Preparación de datos del encabezado

Debe ser llamado de primero.

~~~text
PERFORM "RP_FORMA;ENCABEZADO"
~~~

- Variables a definir antes de la ejecución:

  |Variable|E/S|Descripción|
  |:--------|:-:|-----------|
  |F_APLIC$|E|Código de la aplicación (01=Control de Procesos, 02=Contabilidad,etc.)|
  |F_FORMA$|E|Código de la forma a utilizar (Normalmente se relaciona con un tipo de documento y se define como un campo en la tabla de tipos de operación o tipos de documento o tipos de cálculos)|

- Ejemplo: Preparar datos de la factura (programa VTAFAC75)

~~~text
¡ APLICACIÓN: VENTAS
LET  F_APLIC$="05" 
! CODIGO DEL FORMATO DE IMPRESION SEGUN OPERACION
LET  F_FORMA$=FACTBOPE.FORMATO$ 
PEFORM "RP_FORMA;ENCABEZADO"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FORMA;DETALLE: Preparación de datos del detalle

Debe ser llamado por cada línea del detalle.

~~~text
PERFORM "RP_FORMA;DETALLE"
~~~

- Ejemplo:

Enviar datos del detalle de Factura (programa VTAFAC75)

~~~text
! CICLO FACDETAL
SELECT *,REC=FACDETAL$ FROM CANDET BEGIN KENC$ END KENC$+$FF$
LET FACTBLIN$=""; FIND (FACTBLIN,,REC=FACTBLIN$,KEY=%BASE_CIA$+FACDETAL.TIP_LIN$,KNO=0,DOM=*NEXT)
LET INVDESCR$=""; FIND (INVDESCR,REC=INVDESCR$,KEY=%BASE_CIA$+FACDETAL.PROD$,KNO=0,DOM=*NEXT)
LET INVGRUPO$=""; FIND (INVGRUPO,REC=INVGRUPO$,KEY=%BASE_CIA$+INVDESCR.GRUPO$,,KNO=0,DOM=*NEXT)
LET MONTO=(FACDETAL.CANT*FACDETAL.PRC_UNIT)
LET MONTO=MONTO-MONTO*FACDETAL.PCTDSC/100
LET MONTO=MONTO-MONTO*DNETO/100
PERFORM "RP_FORMA;DETALLE"
NEXT RECORD
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FORMA;FIN: Finalizar e imprimir la forma

Debe ser llamado al final de la emisión del formato.

~~~text
PERFORM "RP_FORMA;FIN"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_FORMA;FIN_MULTIPLE: Finalizar la impresión múltiple

Debe ser llamado al final de una impresión múltiple (ver %SEL_MULTIPLE). 

~~~text
CALL "RP_FORMA;FIN_MULTIPLE"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_GRID: Utilidades para objetos tipo GRID

Permite simplificar algunas funciones típicas asociadas a los objetos tipo <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a> (rejilla).

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;ACT_BOTONES: Activar botones del GRID

~~~text
CALL "RP_GRID;ACT_BOTONES",OBJETO,VAL$,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas a activar separadas con coma|
  |LINEA|E|Número de línea|

- Ejemplo:

~~~text
VAL$="BCTA,BCCO,BAUX,"
LINEA=1
CALL "RP_GRID;ACT_BOTONES",GRID_DAT.CTL,VAL$,LINEA
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;ACT_CHECKMARK: Activar botones de chequeo en el GRID

~~~text
CALL "RP_GRID;ACT_CHECKMARK",OBJETO,VAL$,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas a activar separadas con coma|
  |LINEA|E|Número de línea|

- Ejemplo:

~~~text
VAL$="CONCIL,NO_NONCIL,"
LINEA=1
CALL "RP_GRID;ACT_BOTONES",GRID_DAT.CTL,LINEA
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;ACT_COLUMNAS: Activar columnas en el GRID

~~~text
CALL "RP_GRID;ACT_COLUMNAS",OBJETO,VAL$,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas a activar separadas con coma|
  |LINEA|E|Número de línea|

- Ejemplo:

~~~text
VAL$="CTA,CCO,AUX"
LINEA=1
CALL "RP_GRID;ACT_COLUMNAS",GRID_DAT.CTL,VAL$,LINEA
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;AD_LINEA: Agregar una línea al GRID

~~~text
CALL "RP_GRID;AD_LINEA",OBJETO,ULT_COLACT,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |ULT_COLACT|E|Número de la última columna activa (visible)|
  |LINEA|E|Número de línea a insertar|

- Ejemplo:

~~~text
LIN=2
CALL "RP_GRID;AD_LINEA",GRID_DAT.CTL,8,LIN
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;COLUMNAS: Prepara plantilla con variables de columnas

~~~text
CALL "RP_GRID;COLUMNAS",OBJETO,VAL$,CL$,NCOL
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas separadas con coma|
  |CL$|S|plantilla con los nombres de las columnas como campos|
  |NCOL|S|Número total de columnas|

- Ejemplo:

~~~text
VAL$="CTA,BCTA,CCO,BCCO,AUX,BAUX,REF,DEB,CRE,"
CALL "RP_GRID;COLUMNAS",GRID_DAT.CTL,VAL$,CL$,NCOL
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;DEL_LINEA: Elimina una línea del GRID renumerando la columna descriptiva (0)

~~~text
CALL "RP_GRID;DEL_LINEA",OBJETO,TNLIN,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |TNLIN|E|Total de líneas en el GRID|
  |LINEA|E|Número de línea a eliminar|
  
- Ejemplo:

~~~text
TNLIN=GRID_DAT.CTL'ROWSHIGH
LIN=3
CALL "RP_GRID;DEL_LINEA",GRID_DAT.CTL,TNLIN,LIN
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;DES_BOTONES: Desactivar botones en el GRID

~~~text
CALL "RP_GRID;DES_BOTONES",OBJETO,VAL$,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas a desactivar separadas con coma|
  |LINEA|E|Número de línea|

- Ejemplo:

~~~text
VAL$="BCTA,BCCO,BAUX"
LINEA=1
CALL "RP_GRID;DES_BOTONES",GRID_DAT.CTL,VAL$,LINEA
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;DES_COLUMNAS: Desactivar columnas en el GRID

~~~text
CALL "RP_GRID;DES_COLUMNAS",OBJETO,VAL$,LINEA
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |VAL$|E|Nombre de las columnas a desactivar separadas con coma|
  |LINEA|E|Número de línea|

- Ejemplo:

~~~text
VAL$="CTA,CCO,AUX"
LINEA=1
CALL "RP_GRID;DES_COLUMNAS",GRID_DAT.CTL,VAL$,LINEA
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;GRABAR_GRID: Grabar valores en una línea indicada

~~~text
CALL "RP_GRID;GRABAR_GRID",OBJETO,LINEA,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |LINEA|E|Línea a grabar|
  |LINEA$\{all\}|E|Valores de las celdas de la línea indicada|

- Ejemplo:

~~~text
LINEA=1
CALL "RP_GRID;GRABAR_LINEA",GRID_DAT.CTL,LINEA,VAL_GRID${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;LEER_LINEA: Leer valores de una línea dada

~~~text
CALL "RP_GRID;LEER_LINEA",OBJETO,LINEA,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |LINEA|E|Línea a leer|
  |LINEA$\{all\}|S|Valores de las celdas de la línea solicitada|

- Ejemplo:

~~~text
LINEA=1
CALL "RP_GRID;LEER_LINEA",GRID_DAT.CTL,LINEA,VAL_GRID${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;INS_LINEA: Insertar una línea al GRID renumerando la columna descriptiva (0)

~~~text
CALL "RP_GRID;INS_LINEA",OBJETO,TNLIN,LINEA,ULT_COLACT
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |TNLIN|E|Total de líneas en el GRID|
  |LINEA|E|Número de línea a insertar|
  |ULT_COLACT|E|Número de la última columna activa (visible)|

- Ejemplo:

~~~text
TNLIN=GRID_DAT.CTL'ROWSHIGH
LIN=3
CALL "RP_GRID;INS_LINEA",GRID_DAT.CTL,TNLIN,LIN,8
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;LEER_LINEA_ACTUAL: Leer línea actual

~~~text
CALL "RP_GRID;LEER_LINEA_ACTUAL",OBJETO,COLUM,LINEA,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |COLUM|S|Columna actual|
  |LINEA|S|Línea actual|
  |LINEA$\{all\}|S|Valores de las celdas de la línea actual|

- Ejemplo:

~~~text
CALL "RP_GRID;LEER_LINEA_ACTUAL",GRID_DAT.CTL,COLUM,LINEA,VAL_GRID${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;ORDENAR: Ordenar el GRID

~~~text
CALL "RP_GRID;ORDENAR",OBJETO,LSTORDE$,TIPORDE$,OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |LSTORDE$|E|Lista de columnas separadas con coma por donde se va a ordenar el GRID. x,x,xF (xF = columna de fecha) 
Forma de ordenamiento (A= Ascendente, D = Descendente)|
  |TIPORDE$|E|Forma de ordenamiento (A= Ascendente, D = Descendente)|
  |OPC$|E|Opciones adicionales (Para uso futuro)|

- Ejemplo:

~~~text
CALL "RP_GRID;ORDENAR",GRID_DAT.CTL,"4,2,1F","A",""
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GRID;PREPARAR: Preparar inicialmente el GRID

~~~text
CALL "RP_GRID;PREPARAR",OBJETO,TITULO$,VAL_IN$,ULT_COLACT,NUCOL
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>|
  |TITULO$|E|Descripción título que se colocará en la columna 0 (Ej. Línea)|
  |VAL_IN$|E|Valor inicial para la primera línea en la columna 0 (Ej. 001)|
  |ULT_COLACT|E|Número de la última columna activa (visible)|
  |NUCOL|E|Número de columnas invisibles a agregar al final del GRID|

- Ejemplo:

~~~text
CALL "RP_GRID;PREPARAR",GRID_DAT.CTL,"Linea","001",8,NCOL-8
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_GUI: Utilidades para Entorno  Gráfico

Permite simplificar algunas funciones típicas asociadas a los objetos y el entorno gráfico en general.

[Volver arriba](#rutinas-públicas-rp_xxxxx)


#### RP_GUI;CAMBIO_FOLDER: Cambiar pestaña (FOLDER) activa

Cambiar la pestaña activa en un objeto <a href="https://manual.pvxplus.com/PXPLUS/NOMADS%20Graphical%20Application/Creating%20Panel%20Controls/Folder%20Controls/Overview.htm" target="_blank">FOLDER</a> de <a href="https://manual.pvxplus.com/PXPLUS/NOMADS%20Graphical%20Application/NOMADS%20Development/Getting%20Started.htm" target="_blank">NOMADS</a>.

~~~text
PERFORM "RP_GUI;CAMBIO_FOLDER"
~~~

- Variables a definir antes de la ejecución:

  |Variable|E/S|Descripción|
  |:--------|:-:|-----------|
  |NEXT_FOLDER|E|Número de control asociado a la pestaña. <a href="https://manual.pvxplus.com/PXPLUS/NOMADS%20Graphical%20Application/NOMADS%20Development/Getting%20Started.htm" target="_blank">NOMADS</a> lo asigna a FLDR.<nombre_de_la_pestaña>.CTL. La pestaña debe estar activa para poder tomar los valores de los objetos que están dentro de ella|

- Ejemplo:

~~~text
LET NEXT_FOLDER=FLDR.SEL_COSTOS.CTL
PERFORM "RP_GUI;CAMBIO_FOLDER"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;COMIENZO_PROCESO: Ventana de proceso (Comienzo)

~~~text
CALL "RP_GUI;COMIENZO_PROCESO",TIT$,PROC$
~~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |TIT$|E|Título de la ventana de proceso|
  |PROC$|S|TEMPLATE con valores propios de la rutina (reservado)|

- Ejemplo:

~~~text
CALL "RP_GUI;COMIENZO_PROCESO", "Grabando Reporte",PR$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;CONTINUAR_PROCESO: Ventana de proceso (Continuar)

~~~text
CALL "RP_GUI;CONTINUAR_PROCESO",VALOR$,PROC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |VALOR$|E|Valor STRING a ser desplegado en la ventana de proceso|
  |PROC$|E/S|TEMPLATE con valores propios de la rutina (reservado)|

- Ejemplo:

~~~text
CALL "RP_GUI;CONTINUAR_PROCESO","Línea: "+STR(LIN),PR$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;FIN_PROCESO: Ventana de proceso (Finalización)

~~~text
CALL "RP_GUI;FIN_PROCESO",PROC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |PROC$|S|TEMPLATE con valores propios de la rutina (reservado)|

- Ejemplo:

~~~text
CALL "RP_GUI;FIN_PROCESO",PR$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;DIALOGUE: Crear ventana de diálogo

~~~text
CALL "RP_GUI;DIALOGUE",NUM_WIN,COL,FIL,ANCHO,ALTO,TITULO$,OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |NUM_WIN|S|Número de ventana (CTL) asignado|
  |COL|E|Columna inicial (posición)|
  |FIL|E|Fila inicial (posición)|
  |ANCHO|E|Ancho de la ventana|
  |ALTO|E|Alto de la ventana|
  |TITULO$|E|Título de la ventana|
  |OPC$|E|Opciones adicionales separadas por un espacio|

  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |""|Sin opciones|
    |CEN|centrar ventana en la pantalla|
    |IZQ|pegar a la izquierda de la pantalla|
    |DER|pegar a la derecha de la pantalla|
    |SUP|pegar al borde superior de la pantalla|
    |INF|pegar al borde inferior de la pantalla|
    |WINDOW|Venta normal (no de diálogo)|
    |PVX|opciones propias del mnemónico 'DIALOGUE' de <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a>|

- Ejemplo:

~~~text
CALL "RP_GUI;DIALOGUE",WIN,0,0,20,30,"Selección de Operadores", "CEN  PVX=X*c"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;INPUT: Lectura (INPUT) en entorno gráfico (No aplica para NOMADS)

~~~text
CALL "RP_GUI;INPUT",NUM_CTL,NUM:WIN,CTL_SYS,OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |NUM_CTL|S|Número de control donde se generó el evento|
  |NUM_WIN|S|Número de ventana donde se generó el evento|
  |CTL_SYS|S|Valor de control de BASE (no de <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a>). 9=Cerrar ventana|
  |OPC$|E|Opciones|

  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |""|Sin opciones|
    |TAB|Interpreta tabulador como enter|
    |CAPTION|Muestra en la barra de título el número de objeto que tiene el foco|

- Ejemplo:

~~~text
salir=0
REPEAT
CALL "RP_GUI;INPUT",CTL_ULT,NUM_WIN,CTL_SYS,""
IF CTL_SYS=9 THEN salir=1
.
.
UNTIL salir

~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;MENU_DISABLE: Deshabilitar opciones del MENU

~~~text
CALL "RP_GUI;MENU_DISABLE",OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OPC$|E|Opciones a deshabilitar separadas con coma. En <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a> las opciones del MENU están identificadas por su tecla de acceso rápido (la que está subrayada).|

- Ejemplo:

~~~text
CALL "RP_GUI;MENU_DISABLE","DA,DC,DM,E"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;MENU_ENABLE: Habilitar opciones del MENU

~~~text
CALL "RP_GUI;MENU_ENABLE",OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OPC$|E|Opciones a habilitar separadas con coma. En <a href="https://home.pvxplus.com/" target="_blank">PxPlus</a> las opciones del MENU están identificadas por su tecla de acceso rápido (la que está subrayada).|

- Ejemplo:

~~~text
CALL "RP_GUI;MENU_ENABLE","DA,DC,DM,E"
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;PREPARA_SELECT: Leer LIST_BOX y preparación valores

Leer un <a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a> y preparación valores para condicionar un <a href="https://manual.pvxplus.com/PXPLUS/directives/select.htm" target="_blank">SELECT</a>

~~~text
CALL "RP_GUI;PREPARA_SELECT",PREF$,LISTBOX,LONGITUD,COMIENZO$,FIN$,TABLA$,OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |PREF$|E|Prefijo se posicionamiento (Normalmente %BASE_CIA$)|
  |LISTBOX|E|Número de objeto del <a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a>|
  |LONGITUD|E|Largo de la clave de selección sin prefijo (Ej. 12 en MGADESCR)|
  |COMIENZO$|S|Clave de comienzo|
  |FIN$|S|Clave de finalización|
  |TABLA$|S|Tabla con los códigos válidos|
  |OPC$|S|Opciones Adicionales (Para uso futuro)|

- Ejemplo:

~~~text
CALL "RP_GUI;PREPARA_SELECT",%BASE_CIA$,SEL_CTAS.CTL,12,DESDE$,HASTA$,TABLA_DES$,""
SELECT *,REC=DES$ FROM "MGADESCR" BEGIN DESDE$ END HASTA$ WHERE POS(DES.CUENTA$=TABLA_DES$,12)
.
.
.
NEXT RECORD
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;SEL_LIST: Selecciona una valor de una lista

Selecciona una valor de una lista (<a href="https://manual.pvxplus.com/PXPLUS/directives/drop_box.htm" target="_blank">DROP_BOX</a>, 
<a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a>, etc)

~~~text
CALL "RP_GUI;SEL_LIST",OBJETO,VALOR$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/directives/drop_box.htm" target="_blank">DROP_BOX</a>, <a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a>, etc|
  |VALOR$|E|Valor a seleccionar (por comienzo de la línea). Si no existe en la lista se seleccionará el primero.|

- Ejemplo:

Seleccionar el estado civil en un <a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a>

~~~text
CALL "RP_GUI;SEL_LIST",EDO_CIVIL.CTL,DES.CIVIL$
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;SIZE: Tomar el tamaño de la ventana

~~~text
CALL "RP_GUI;SIZE",ANCHO_CAR,ALTO_CAR,ANCHO_VENP,ALTO_VENP,ANCHO_VENC,ALTO_VENC
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |ANCHO_CAR|S|Ancho del caracter en pixels|
  |ALTO_CAR|S|Alto del caracter en pixels|
  |ANCHO_VENP|S|Ancho de la ventana en pixels|
  |ALTO_VENP|S|Alto de la ventana en pixels|
  |ANCHO_VENC|S|Ancho de la ventana en caracteres|
  |ALTO_VENC|S|Alto de la ventana en carcateres|

- Ejemplo:

~~~text
->CALL "RP_GUI;SIZE",C1,C2,C3,C4,C5,C6
->PRINT C1,C2,C3,C4,C5,C6
 8 15 800 553 100 36
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_GUI;UNT_OBJETO: Tomar próximo número de objeto disponible

~~~text
CALL "RP_GUI;UNT_OBJETO",OBJETO
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|S|Número de objeto disponible|

- Ejemplo:

~~~text
CALL "RP_GUI;UNT_OBJETO",ACEPTAR
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_LISTV: Utilidades para objetos tipo LIST_VIEW

Permite simplificar algunas funciones típicas asociadas a los objetos tipo <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a> (Lista estilo reporte).

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_LISTV;COLUMNAS: Prepara TEMPLATE con variables de columnas

~~~text
CALL "RP_LISTV;COLUMNAS",VAL$,CL$,NCOL
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |VAL$|E|Nombre de las columnas separadas con coma|
  |CL$|S|TEMPLATE con los nombres de las columnas como campos|
  |NCOL|S|Número de columnas|

- Ejemplo:

~~~text
VAL$="CTA,BCTA,CCO,BCCO,AUX,BAUX,REF,DEB,CRE,"
CALL "RP_LISTV;COLUMNAS",VAL$,CL$,NCOL
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_LISTV;GRABAR_LISTV: Grabar valores en una línea indicada

~~~text
CALL "RP_LISTV;GRABAR_LISTV",OBJETO,LINEA,NCOL,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>|
  |LINEA|E|Línea a grabar|
  |NCOL|E|Número de columnas|
  |LINEA$\{all\}|E|Valores de las columnas de la línea indicada|

- Ejemplo:

~~~text
CALL "RP_LISTV;LEER_LINEA_IND",LIST_DAT.CTL,3,5,VAL_LIST${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_LISTV;LEER_LINEA: Leer línea actual

~~~text
CALL "RP_LISTV;LEER_LINEA",OBJETO,LINEA,NCOL,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>|
  |LINEA|S|Línea actual|
  |NCOL|E|Número de columnas|
  |LINEA$\{all\}|S|Valores de las columnas de la línea actual|

- Ejemplo:

~~~text
CALL "RP_LISTV;LEER_LINEA",LIST_DAT.CTL,LINEA,5,VAL_LIST${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_LISTV;LEER_LINEA_IND: Leer valores de una línea indicada

~~~text
CALL "RP_LISTV;LEER_LINEA_IND",OBJETO,LINEA,NCOL,LINEA${all}
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>|
  |LINEA|E|Línea a leer|
  |NCOL|E|Número de columnas|
  |LINEA$\{all\}|E|Valores de las columnas de la línea indicada|

- Ejemplo:

~~~text
CALL "RP_LISTV;LEER_LINEA_IND",LIST_DAT.CTL,3,5,VAL_LIST${all}
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_LISTV;PREPARAR: Preparar inicialmente el LIST_VIEW

~~~text
CALL "RP_LISTV;PREPARAR",OBJETO,ULT_COLACT,NUCOL
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |OBJETO|E|Número de control de objeto asociado al <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>|
  |ULT_COLACT|E|Número de la última columna activa (visible)|
  |NUCOL|E|Número de columnas invisibles a agregar al final del <a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>|

- Ejemplo:

~~~text
CALL "RP_LISTV;PREPARAR",LIST_DAT.CTL,8,NCOL-8
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_PARAM: Lectura de parámetros y control de la aplicación

Carga los valores de los parámetros (por ejemplo: Estructura del comprobante, cuenta de resultado) y controles (por ejemplo: último cierre, último pre-cierre) de la compañía para una aplicación dada.

#### RP_PARAM: Genera un TEMPLATE con los parámetros y controles

~~~text
CALL "RP_PARAM",APL$,PAR$,CTR$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |APL$|E|Aplicación (MGA,INV,CTA,FAC,COM,PRV,BAN,AFI,NOM)|
  |PAR$|S|Parámetros (Template)|
  |CTR$|S|Controles (Template)|

- Ejemplo:

~~~text
-> CALL "RP_PARAM",MGA,PAR$,CTR$

-> PRINT LST(IOL(PAR$))
iolist CIA$,FISCAL$,ESTR_COMP$,CTAS_NOM$,CTA_RESULT$,CTA_PERD_DIFC$, 
CTA_INGR_DIFC$,CBA_DIF$

-> PRINT PAR.ESTR_COMP$
AAMMNNNN

-> PRINT LST(IOL(CTR$))
iolist CIA$,CIERRE$,PRECIERRE$

-> PRINT CTR.CIERRE$
31012000
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_QUERY: Despliegue o consulta de valores para seleccionar

Permite mostrar la lista de valores posibles para un campo específico.

Esta lista puede ser tomada de un archivo o de una tabla predefinida.

[Volver arriba](#rutinas-públicas-rp_xxxxx)

### RP_REP: Manejo de Reportes

Para realizar todas al operaciones relacionadas a la emisión de reportes.

[Volver arriba](#rutinas-públicas-rp_xxxxx)

#### RP_REP;FORMATO: Preparar columnas y datos del reporte

~~~text
CALL "RP_REP; FORMATO",LP,REP$,FMT$,OPC$
~~~

- Parámetros:
  
  |Parámetro|E/S|Descripción|
  |:--------|:-:|-----------|
  |LP|S|Canal donde queda abierta la impresora (0 = no está abierta)|
  |REP$|S|TEMPLATE con la información y controles del reporte
  |FMT$|E|Formato para definir las columnas (\[\<DESCRIPCIÓN\>\]\<ANCHO\> )|
  |OPC$|E|Opciones Adicionales (Separadas con Espacio)|

  - TEMPLATE REP$:
    |Variable|Valor|
    |:-------|-----|
    |REP.CLIN|Contador de líneas|
    |REP.CPAG|Contador de páginas|
    |REP.TLIN|Total de líneas por página|
    |REP.ANCH|Ancho del reporte|
    |REP.*|Columnas (Ej. REP.CIA,REP.NOM,REP.SALDO)|


  - Opciones:

    |Opción|Descripción|
    |:-----|-----------|
    |""|Sin opciones|
    |COL\[xx\]|Ancho del reporte (default=132)|
    |CIA\[xx\]|Nombre de la Compañía (default = activa)|
    |TIT\[xx\]|Título del reporte (default = función activa del catálogo)|
    |REP\[xx\]|Nombre del programa (default = proceso activo del catálogo)|
    |SUB\[xx\]|Sub_titulo|
    |SU2\[xx\]|Sub_titulo (segunda línea)|
    |COR\[xx\]|Correspondiente, etc.|
    |LI2\[xx\]|Segunda línea, datos adicionales|
    |SEP\[xx\]|Separación entre columnas (default = 1)|
    |ADI\[xx\]|Líneas adicionales antes del encabezado de columnas (Separadas por \\)|
    |FLG\[xx\]|Flags o banderas adicionales|
    |MAR\[xx\]|Margen izquierdo para las columnas|

- Ejemplo:

~~~text
~~~

[Volver arriba](#rutinas-públicas-rp_xxxxx)

## [Rutinas Utilitarias (RU_XXXXX):](#rutinas-utilitarias-ru_xxxxx)

Definición de lo que son las rutinas utilitarias.

[Volver arriba](#top)

### RU_COPY

Copia de registros.

>Anteriormente: `HLCOPY`

~~~text
CALL "RU_COPY"
~~~

[Volver arriba](#rutinas-utilitarias-ru_xxxxx)

[
<a href="https://home.pvxplus.com/" target="_blank">PxPlus</a>
<a href="https://manual.pvxplus.com/PXPLUS/directives/perform.htm" target="_blank">PERFORM</a>
<a href="https://manual.pvxplus.com/PXPLUS/directives/grid.htm" target="_blank">GRID</a>
<a href="https://manual.pvxplus.com/PXPLUS/control_object_properties/listview_properties.htm" target="_blank">LIST_VIEW</a>
<a href="https://manual.pvxplus.com/PXPLUS/directives/drop_box.htm" target="_blank">DROP_BOX</a>
<a href="https://manual.pvxplus.com/PXPLUS/directives/list_box.htm" target="_blank">LIST_BOX</a>
<a href="https://manual.pvxplus.com/PXPLUS/NOMADS%20Graphical%20Application/Creating%20Panel%20Controls/Folder%20Controls/Overview.htm" target="_blank">FOLDER</a>
<a href="https://manual.pvxplus.com/PXPLUS/NOMADS%20Graphical%20Application/NOMADS%20Development/Getting%20Started.htm" target="_blank">NOMADS</a>
<a href="https://manual.pvxplus.com/PXPLUS/directives/select.htm" target="_blank">SELECT</a>
<a href="" target="_blank"></a>

]: #
