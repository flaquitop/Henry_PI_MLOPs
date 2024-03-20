<p align="center">
 <img src="data/mlops.jpg"  height=600>
</p>

# <h1 align=center> PROYECTO INDIVIDUAL Nº1
<h1 align=center> Machine Learning Operations (MLOps) </h1>



## Descripción del proyecto:

### Este proyecto individual tiene como objetivo poner en práctica los conocimientos adquiridos en la etapa de labs sobre Machine Learning Operations (MLOps). En el cual se me asignó el rol de un MLOps Engineer y deberé desarrollar un sistema de recomendación de videojuegos para la plataforma Steam.

### Contexto:

### Me he unido al equipo de Data Science de Steam y me encomendaron la tarea de crear un sistema de recomendación de videojuegos para mejorar la experiencia de usuarios.

### Tareas a realizar:

## Preparación de datos:

### Datos

Los datos empleados para este proyecto se encuentran en tres archivos JSON con una estructura anidada:

- australian_user_reviews.json: contiene las reseñas de los usuarios sobre los juegos que han jugado.
- australian_users_items.json: contiene la información de los usuarios, los juegos que poseen y las horas que han jugado.
- output_steam_games.json: contiene la información de los juegos disponibles en Steam, como el nombre, el género, el precio, etc.


Previamente a la realización del proyecto, procedí a limpiar y transformar los datos proporcionados en los archivos originales mencionados anteriormente y eliminé las filas y columnas innecesarias para la validación y creación de los DataFrame. Creé una nueva columna 'sentiment_analysis' para el análisis de sentimiento con NLP.



## Desarrollo de la API:

### Implementar la API usando el framework FastAPI.


**`PlayTimeGenre( genero : str ):`**  Debe devolver año con mas horas jugadas para dicho género.
Ejemplo de retorno: {"Año de lanzamiento con más horas jugadas para Género X" : 2013}

**`UserForGenre( genero : str ):`** Debe devolver el usuario que acumula más horas jugadas para el género dado y una lista de la acumulación de horas jugadas por año.
Ejemplo de retorno: {"Usuario con más horas jugadas para Género X" : us213ndjss09sdf, "Horas jugadas":[{Año: 2013, Horas: 203}, {Año: 2012, Horas: 100}, {Año: 2011, Horas: 23}]}

**`UsersRecommend( año : int ):`** Devuelve el top 3 de juegos MÁS recomendados por usuarios para el año dado. (reviews.recommend = True y comentarios positivos/neutrales)
Ejemplo de retorno: [{"Puesto 1" : X}, {"Puesto 2" : Y},{"Puesto 3" : Z}]

**`UsersNotRecommend( año : int ):`** Devuelve el top 3 de juegos MENOS recomendados por usuarios para el año dado. (reviews.recommend = False y comentarios negativos)
Ejemplo de retorno: [{"Puesto 1" : X}, {"Puesto 2" : Y},{"Puesto 3" : Z}]

**`sentiment_analysis( año : int ):`** Según el año de lanzamiento, se devuelve una lista con la cantidad de registros de reseñas de usuarios que se encuentren categorizados con un análisis de sentimiento.
Ejemplo de retorno: {Negative = 182, Neutral = 120, Positive = 278}



# Análisis exploratorio de datos (EDA):

### Investigar las relaciones entre las variables del dataset.

### Detectar outliers o anomalías.

### Identificar patrones interesantes.



# Modelo de aprendizaje automático:

Crearemos la columna 'sentiment_analysis' aplicando análisis de sentimiento con NLP, con lo que entrené el modelo de ML y definí las funciones recomendacion_juego(id_producto: int) y recomendacion_usuario(id_usuario: int) en la API.


## Video:

En mi proyecto se presentará un video explicativo, resumido, mostrando brevemente la estructura del proyecto, el funicionamiento de las consultas de la API y conteniendo una breve explicación del modelo de ML utilizado. 


## Recursos:
## Tecnologias y herramientas utilizadas

Para el desarrollo del EDA (*Exploratory Data Analysis*), se utilizaron las siguientes herramientas y tecnologias:


![VSCode](https://img.shields.io/badge/-VSCode-333333?style=flat&logo=visual-studio-code)
![Python](https://img.shields.io/badge/-Python-333333?style=flat&logo=python)
![Jupyter](https://img.shields.io/badge/-Jupyter-333333?style=flat&logo=jupyter)
![Pandas](https://img.shields.io/badge/-Pandas-333333?style=flat&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-333333?style=flat&logo=WordCloud)
![Seaborn](https://img.shields.io/badge/Seaborn-333333?style=flat&logo=Seaborn)

Para la realización de mi proyecto, se me facilitó: 

Dataset: Carpeta con los archivos a procesar.

Diccionario de datos: Diccionario con algunas descripciones de las columnas disponibles en el dataset.

