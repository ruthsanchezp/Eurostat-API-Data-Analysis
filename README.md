# Eurostat API Data Analysis

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar la satisfacción laboral entre los jóvenes de 25 a 34 años con educación terciaria en Europa utilizando datos de Eurostat. La consulta se enfoca en el nivel de satisfacción laboral (JOB) de este colectivo. Los datos se obtienen de la API de Eurostat y se procesan utilizando Python y Jupyter Notebook.

## Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

- `notebook.ipynb`: Contiene el código en Jupyter Notebook que realiza la consulta a la API de Eurostat, procesa los datos y genera gráficos.
- `README.md`: Este archivo, que describe el objetivo del proyecto, las instrucciones para ejecutar el código y las dependencias necesarias.

## Instrucciones para Ejecutar el Proyecto

1. **Instalar Dependencias**:
    Primero, asegúrate de tener instaladas las librerías necesarias. Puedes instalarlas ejecutando:
    ```bash
    !pip install eurostat
    !pip install pandas
    !pip install matplotlib
    ```

2. **Ejecutar el Notebook**:
    Abre y ejecuta el archivo `notebook.ipynb` en Jupyter Notebook. Este archivo contiene el siguiente flujo:

    - Crear una variable string con la URL de la llamada a la API de Eurostat.
    - Crear un diccionario con el objeto JSON obtenido de la API.
    - Imprimir el elemento "dimension" del diccionario.
    - Descargar los datos de satisfacción en Europa en formato pandas.
    - Filtrar los datos para el colectivo objetivo.
    - Construir un gráfico para el nivel de satisfacción en cada país en 2018 y determinar los países con mayor y menor satisfacción laboral.

## Detalles del Análisis

1. **Consulta a la API de Eurostat**:
    La URL de la consulta se genera de acuerdo con los parámetros especificados: 
    - Nivel de educación: Tertiary education ED5-8
    - Indicador: JOB
    - Género: Total (T)
    - Edad: 25-34 años (Y25-34)

2. **Procesamiento de Datos**:
    - Se descarga el dataset `ilc_pw01b` de la API de Eurostat.
    - Se filtran los datos para obtener únicamente la información relevante para el colectivo objetivo.
    - Se generan gráficos para visualizar el nivel de satisfacción en cada país en 2018.

3. **Resultados**:
    - El país con mayor satisfacción laboral en 2018 es identificado.
    - El país con menor satisfacción laboral en 2018 es identificado.
