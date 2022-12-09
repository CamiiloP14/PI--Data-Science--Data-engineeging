<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>
# Proyecto I- Data engineering- Data Science Henry
[imagen](https://camo.githubusercontent.com/09bd9c8fd059de237050145eff2d484627bf3ffe6958205914d3af018357e998/68747470733a2f2f66696c65732e7265616c707974686f6e2e636f6d2f6d656469612f576861742d69732d446174612d456e67696e656572696e675f57617465726d61726b65642e3630376537363161336330652e6a7067)

Este primero proyecto es presentado para la finalizacion de la carrera Data Science en Henry, orientado a Data Engineering. Propone demostrar el uso de varias herramientas y habilidades.

## Habilidades:
- Analisis de datos, proceso de ETL.
- Trabajar con un ambiente Dockerizado para la disponibilidad de los datos en FasAPI

## Herramientas.
- Jupiter Notebook, DockerFile, FastAPI.

## Propuesta de trabajo.
El proyecto consiste en realizar una ingesta de datos desde diversas fuentes, posteriormente aplicar las transformaciones que consideren pertinentes, y luego disponibilizar los datos limpios para su consulta a través de una API. Esta API deberán construirla en un entorno virtual dockerizado.

# Procesos
En primera instancia, la idea es hacer la extracción de los 4 datasets que contienen registros de titulos de películas en algunas plataformas. Para esto se utilizará, la libreria pandas de Python. Posteriormente se realiza un EDA  de los datasets y se hace un proceso de limpieza y normalización para finalmente concatenar los datasets y poder disponibilizarlos para las consultas a realizar.

## Carga archivo a DockerFile

Luego de tener nuestro dataset limpio lo que hacemos es exportarlo a nuestro ámbiente Dockerizado en donde mediante la librería fastapi y uvicon creamos una FastAPI en la cual de manera interactiva podemos visualizar nuestras consultas.

## Consultas en FastAPI

Finalmente, hacemos las diferente consultas a nuestra FastAPI en el navegador, mediante la ruta localhost:8000/docs. Las consultas a realizar son:

- Máxima duración según tipo de film (película/serie), por plataforma y por año: El request debe ser: get_max_duration(año, plataforma, [min o season])
- Cantidad de películas y series (separado) por plataforma El request debe ser: get_count_plataform(plataforma)
- Cantidad de veces que se repite un género y plataforma con mayor frecuencia del mismo. El request debe ser: get_listedin('genero')
- Actor que más se repite según plataforma y año. El request debe ser: get_actor(plataforma, año)

# Diagrama de flujo
