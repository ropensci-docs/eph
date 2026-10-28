# Índice del paquete

## Descarga y recodificación

Funciones para descargar los datos de la encuesta y recodificar sus
variables.

- [`get_microdata()`](https://docs.ropensci.org/eph/reference/get_microdata.md)
  : Descarga de Bases de EPH
- [`organize_caes()`](https://docs.ropensci.org/eph/reference/organize_caes.md)
  : Clasificador de Actividades
- [`organize_cno()`](https://docs.ropensci.org/eph/reference/organize_cno.md)
  : Clasificador de Ocupaciones
- [`organize_labels()`](https://docs.ropensci.org/eph/reference/organize_labels.md)
  : Funcion para etiquetar las bases de la Encuesta Permanente de
  Hogares.
- [`organize_panels()`](https://docs.ropensci.org/eph/reference/organize_panels.md)
  : Pool de Datos en Panel - Base Individudal EPH continua
- [`get_total_urbano()`](https://docs.ropensci.org/eph/reference/get_total_urbano.md)
  : Descarga de Bases de EPH total urbano
- [`get_eahu()`](https://docs.ropensci.org/eph/reference/get_eahu.md) :
  Descarga de Bases de la Encuesta anual de hogares urbanos

## Tablas auxiliares

Tablas auxiliares para la recodificacion y otros calculos frecuentes.

- [`get_poverty_lines()`](https://docs.ropensci.org/eph/reference/get_poverty_lines.md)
  : Descarga de canasta basica alimentaria y canasta basica total
- [`adulto_equivalente`](https://docs.ropensci.org/eph/reference/adulto_equivalente.md)
  : Tabla de valores de adulto equivalente segun sexo y edad
- [`diccionario_aglomerados`](https://docs.ropensci.org/eph/reference/diccionario_aglomerados.md)
  : Diccionario de aglomerados segun diseno de registro de la EPH
- [`diccionario_regiones`](https://docs.ropensci.org/eph/reference/diccionario_regiones.md)
  : Diccionario de regiones segun diseno de registro de la EPH
- [`errores_muestrales`](https://docs.ropensci.org/eph/reference/errores_muestrales.md)
  : Tabla con los errores muestrales para estimaciones de poblacion
- [`CNO`](https://docs.ropensci.org/eph/reference/CNO.md) : Categorias
  de las 4 dimensiones del Clasificador Nacional de Ocupaciones 2001.
- [`caes`](https://docs.ropensci.org/eph/reference/caes.md) : Categorias
  del Clasificador de Actividades Economicas para encuestas
  Sociodemograficas
- [`centroides_aglomerados`](https://docs.ropensci.org/eph/reference/centroides_aglomerados.md)
  : Tabla de centroides de los aglomerados

## Procesamiento

Funciones para facilitar procesamientos básicos de la base de datos
(incluyendo mapeo)

- [`calculate_errors()`](https://docs.ropensci.org/eph/reference/calculate_errors.md)
  : Calculo del desvio estandar y el coeficiente de variacion
- [`calculate_poverty()`](https://docs.ropensci.org/eph/reference/calculate_poverty.md)
  : Calculo de Pobreza e Indigencia
- [`calculate_tabulates()`](https://docs.ropensci.org/eph/reference/calculate_tabulates.md)
  : Tabulado con ponderacion
- [`map_agglomerates()`](https://docs.ropensci.org/eph/reference/map_agglomerates.md)
  : Mapa de indicadores por aglomerado

## Ejemplos y bases de juguete

- [`toybase_hogar_2016_04`](https://docs.ropensci.org/eph/reference/toybase_hogar_2016_04.md)
  : Seleccion aleatoria de casos de la base 2016 trimestre 4 para la
  base hogar
- [`toybase_individual_2016_03`](https://docs.ropensci.org/eph/reference/toybase_individual_2016_03.md)
  : Seleccion aleatoria de casos de la base 2016 trimestre 3 para la
  base individual
- [`toybase_individual_2016_04`](https://docs.ropensci.org/eph/reference/toybase_individual_2016_04.md)
  : Seleccion aleatoria de casos de la base 2016 trimestre 4 para la
  base individual
- [`canastas_reg_example`](https://docs.ropensci.org/eph/reference/canastas_reg_example.md)
  : Canastas Basicas Alimentarias y Canastas Basicas Totales segun
  region y trimestre
