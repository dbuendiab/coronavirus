# coronavirus

Gráficas y tablas sobre datos de COVID-19 de Open Data Europe (2020).

> **Nota**: Este notebook es un documento histórico que captura la evolución
> de la pandemia durante la primera mitad de 2020. El dataset original de la
> ECDC dejó de actualizarse a finales de ese año, cuando la responsabilidad
> de publicación se transfirió a la OMS. El notebook arranca pero la celda
> de importación de datos fallará, ya que el endpoint ya no está disponible.

## Lo que hace

* Importación de los datos de casos mundiales desde
  `https://opendata.ecdc.europa.eu/covid19/casedistribution/csv`
* Volcado del CSV a una tabla **SQLite** en memoria. Cálculo de datos acumulados.
* Presentación gráfica interactiva de la evolución de casos y muertes:
  * Consulta de casos y muertes por país.
  * Consulta de casos y media móvil de 7 días por país.
  * Listado de países que empeoran o mejoran según su media móvil.

## Estado actual

El `requirements.txt` ha sido simplificado para eliminar conflictos de
dependencias entre paquetes de 2020 y versiones más recientes. Las
dependencias reales del notebook son:
```txt
numpy
matplotlib
scipy
ipywidgets
jupyter
```

Si se desea restaurar la funcionalidad completa, habría que redirigir la
importación de datos a una fuente alternativa como
[Our World in Data](https://github.com/owid/covid-19-data) o el
[repositorio de la OMS](https://covid19.who.int/data).
