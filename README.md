# Ciencia de datos - Trabajo Final de Máster sobre la contaminación acústica

Autor: Álvaro López Cabello

Este repositorio contiene los datos y el código correspondiente al desarrollo del trabajo final del máster en Ciencia de Datos de la UOC con título **"Análisis de datos espacio-temporales sobre la contaminación acústica de Madrid"**. El proyecto consiste en la creación de mapas de ruido de los distritos del municipio Madrid a lo largo del 2022 a partir del tráfico viario y del análisis de la población expuesta al ruido. La información extraída permite identificar los lugares expestos a niveles de ruido que superan los Objetivos de Calidad Acústica definidos en el Real Decreto 1367/2007 para tomar medidas según el distrito, el mes y el periodo del día.

La mayor parte de la captura, procesamiento y análisis exploratorio de los datos se ha llevado a cabo de Python, aunque QGIS ha sido de ayuda para la unión de algunas capas vectoriales. A partir de los conjuntos de datos generados, se ha creado un [dashboard interactivo](https://public.tableau.com/app/profile/.lvaro.l.pez7412/viz/Contaminacinacstica/Dashboard2) en Tableau con los mapas de ruido y otras visualizaciones de interés.

El repositorio contiene el directorio *Código* con los siguientes notebooks creados durante el trabajo:

- [Código/Tráfico_mensual_y_calles.ipynb](Código/Trafico_mensual_y_calles.ipynb): carga, limpieza y análisis de los datos con la intensidad del tráfico y los puntos de medida y de la asignación del tráfico a los ejes viarios. Se obtienen doce ficheros shapefiles para cargarlos en NoiseModelling.
- [Código/Edificios.ipynb](Código/Edificios.ipynb): carga, limpieza y análisis de los datos del Catastro sobre los edificios. Se obtiene un fichero sobre los edificios para QGIS y otro para cargarlo en NoiseModelling.
- [Código/Temperatura_HR.ipynb](Código/Temperatura_HR.ipynb): obtención de la media de temperatura y humedad relativa de las estaciones meteorológicas de Madrid por cada mes. Cada par de valores se añade en NoiseModelling para la creación de los mapas de ruido.
- [Código/Tráfico_diario.ipynb](Código/Tráfico_diario.ipynb): carga, limpieza y análisis sobre las medidas del tráfico diario.
- [Código/Exposición_ruido.ipynb](Código/Exposición_ruido.ipynb): transformación de los datos de expisición al ruido, tanto de la población como de los centros sociosanitarios y docentes, después de obtener las tablas de salida de NoiseModelling y de asignar a los edificios los receptores más cercanos con los niveles de ruido.
- [Código/Centros_sociosanitarios_docentes.ipynb](Código/Centros_sociosanitarios_docentes.ipynb): carga, limpieza del dataset inicial de los centros sociosanitarios y docentes antes de QGIS.
- [Código/Unir_datos_mapas_para_Tableau.ipynb](Código/Unir_datos_mapas_para_Tableau.ipynb): se unen los conjuntos de datos con los contornos de ruido de los cuatro índices y doce meses, con el objetivo de cargarlo todo junto en Tableau.

Los conjuntos de datos abiertos utilizados para el proyecto y los conjuntos de datos resultantes se pueden encontrar en el directorio de [Google Drive](https://drive.google.com/drive/folders/1wBgVF3ykTYgC7f8M-y8d0pvqTzPFPK5S?usp=drive_link).
