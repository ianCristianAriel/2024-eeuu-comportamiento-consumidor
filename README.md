## Estructura de directorios y archivos
La estructura de directorios sigue una jerarquía organizada y modular para facilitar la reproducibilidad y la colaboración. Cada etapa del pipeline de datos está claramente separada según el principio de bronze-silver-gold para garantizar calidad y trazabilidad de los datos.

    analisis_comportamiento_del_consumidor/
    │
    ├── data/                          # Directorio principal de los datos
    │   ├── 1_bronze/                  # Datos crudos (brutos) directamente obtenidos de las fuentes
    │   ├── 2_silver/                  # Datos procesados y transformados (listos para ML y EDA)
    │   └── 3_gold/                    # Datos finales, listos para la visualización o análisis avanzado
    │
    ├── models/                        # Modelos entrenados (mejores modelos para predecir la variable target)
    │
    ├── notebooks/                     # Cuadernos Jupyter de cada fase del proceso CRISP-DM
    │   ├── 1_extraccion_comprension.ipynb  # Extracción y comprensión inicial de los datos
    │   ├── 2_tratamiento.ipynb             # Tratamiento de datos: limpieza y preprocesamiento
    │   ├── 3_eda.ipynb                     # Análisis exploratorio de los datos (EDA)
    │   ├── 4_visualizacion.pbix            # Visualización interactiva de los resultados (Power BI)
    │   └── 5_ml.ipynb                      # Modelado predictivo usando Machine Learning
    │
    └── requirements.txt               # Dependencias del proyecto (Python)

## Tecnologías Utilizadas
- Python
  - Bibliotecas para análisis de datos:
    - NumPy
    - pandas
    - missingno
  -	Bibliotecas para visualización de datos:
    -	Seaborn
    - matplotlib
  -	Bibliotecas para aprendizaje automático:
    -	scikit-learn
    - joblib
  - Bibliotecas para gestion de directorios y archivos
    - os

## Metodología

Este proyecto se basa en la metodología CRISP-DM (Cross Industry Standard Process for Data Mining), que consiste en las siguientes fases:

1.	Comprensión del Negocio: Definir objetivos y preguntas clave para el análisis.
2.	Comprensión de los Datos: Recopilación y exploración de los datos disponibles.
3.	Tratamiento de los Datos: Limpieza, transformación y preprocesamiento.
4.  Analisis exploratorio de datos: Exploracion descriptiva.
5.	Modelado y Evaluación: Creacion y evaluacion de modelos de machine learning para predicción.
6.	Visualizacion ejecutiva: Visualizacion con presentacion ejecutiva para recomendar accionables de negocio.

## Instalación y Configuración
Para ejecutar este proyecto localmente, sigue estos pasos:
1.	Clona este repositorio:
    git clone https://github.com/c20-78-t/analisis_comportamiento_del_consumidor.git
    cd analisis_comportamiento_del_consumidor

2. Instala las dependencias necesarias:
    pip install -r requirements.txt

3.	Ejecuta los notebooks en el orden establecido para replicar el análisis.

## Colaboradores del equipo c20-78-t:
- [@ianCristianAriel](https://github.com/ianCristianAriel)
- (https://github.com/nicostassi04)
- Amalia Teresa Raimundo (www.linkedin.com/in/amalia-raimundo)
- Luis Fernando Sánchez Romero (www.linkedin.com/in/luis-romerosr)

## Estado del proyecto:
- En proceso -> 75% completado