## Estructura de directorios y archivos
La estructura de directorios sigue una jerarquía organizada y modular para facilitar la reproducibilidad y la colaboración. Cada etapa del pipeline de datos está claramente separada según el principio de bronze-silver-gold para garantizar calidad y trazabilidad de los datos.

```plaintext
  analisis_comportamiento_del_consumidor/
  │
  ├── artifacts/                                      # Artefactos generados durante el procesamiento y modelado
  │   ├── .gitkeep
  │   ├── preprocessor.joblib
  │   └── top_columns.joblib
  │
  ├── data/                                           # Directorio principal de los datos
  │   ├── 1_bronze/                                   # Datos originales obtenidos de las fuentes
  │   │   ├── clients_behavior.csv
  │   │   ├── shopping_behavior_updated.csv
  │   │   └── shopping_trends.csv
  │   │
  │   ├── 2_silver/                                   # Datos transformados y preparados para el análisis
  │   │   └── df_encoded_scaled.csv
  │   │
  │   └── 3_gold/                                     # Datos finales para análisis y visualización
  │       └── df_processed.csv
  │
  ├── models/                                         # Modelos entrenados y recursos de visualización
  │   ├── arbol_decision_sin_reduccion.png
  │   └── subscription_status_decision_tree_base_model.pkl
  │
  ├── notebooks/                                      # Cuadernos y dashboard de las fases del proyecto
  │   ├── __pycache__/                                # Caché de Python
  │   │   └── transform_classes_and_functions.cpython-312.pyc
  │   │
  │   ├── 1_extract_comprehension.ipynb               # Extracción y comprensión inicial de los datos
  │   ├── 2_transform.ipynb (private)                 # Tratamiento y transformación de los datos
  │   ├── 3_exploratory_analysis.ipynb (private)      # Análisis exploratorio de los datos (EDA)
  │   ├── 4_dashboard.pbix                            # Dashboard interactivo de Power BI
  │   └── 5_machine_learning.ipynb                    # Modelado predictivo mediante Machine Learning
  │
  ├── reports/                                        # Informes y entregables del proyecto
  │   ├── .gitkeep
  │   └── c20_78-NO_COUNTRY.pbix
  │
  ├── src/                                            # Código fuente y funciones auxiliares de Python
  │   ├── __pycache__/                                # Caché de Python
  │   │   ├── average_cost.cpython-312.pyc
  │   │   ├── custom_standarization_classes_and_functions.cpython-312.pyc
  │   │   ├── eval_models.cpython-312.pyc
  │   │   ├── experiment_evaluator.cpython-312.pyc
  │   │   ├── experiment_factory.cpython-312.pyc
  │   │   ├── experiment_tracker.cpython-312.pyc
  │   │   └── model_optimizer.cpython-312.pyc
  │   │
  │   ├── .gitkeep
  │   ├── average_cost.py (private)
  │   ├── bins_estimator.py (private)
  │   ├── custom_standarization_classes_and_functions.py (private)
  │   ├── eval_models.py (private)
  │   ├── experiment_evaluator.py (private)
  │   ├── experiment_factory.py (private)
  │   ├── experiment_tracker.py (private)
  │   ├── feature_asosiation_with_target_column.py (private)
  │   ├── model_optimizer.py (private)
  │   └── tree_rules_to_table.py (private)
  │
  ├── .gitignore                                      # Reglas de exclusión de Git
  ├── bussines_objetives.md                           # Objetivos de negocio del proyecto
  ├── README.md                                       # Documentación principal del repositorio
  └── requirements.txt                                # Dependencias del proyecto Python
```

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

La metodologia de este proyecto se basa en CRISP-DM (Cross Industry Standard Process for Data Mining), y consiste en las siguientes fases:

1.	Comprensión del Negocio: Definir los objetivos y las preguntas clave para el análisis.
2.	Comprensión de los Datos: Recopilar y explorar los datos disponibles.
3.	Tratamiento de los Datos: Realizar la limpieza, transformación y preprocesamiento de los datos.
4.	Análisis Exploratorio de Datos: Realizar una exploración descriptiva.
5.	Modelado y Evaluación: Crear, evaluar, optimizar y seleccionar modelos de machine learning para predecir la probabilidad de suscripción a servicios personalizados.
6.	Visualización Ejecutiva: Presentar visualizaciones y recomendaciones ejecutivas con accionables para el negocio.

## Instalación y Configuración
Para ejecutar este proyecto localmente, sigue estos pasos:
1.	Clona este repositorio:
```bash
    git clone https://github.com/c20-78-t/analisis_comportamiento_del_consumidor.git

    cd analisis_comportamiento_del_consumidor
```
2. Instala las dependencias necesarias:
```bash
    pip install -r requirements.txt
```

3.	Ejecuta los notebooks en el orden establecido para replicar el análisis.

## Estado del proyecto:
- En proceso -> 80% completado (MVP completado)

## Equipo c20-78-t-data-bi:
- [Stassi, Nicolas](https://www.linkedin.com/in/nicol%C3%A1s-stassi/)
- [Yané, Ian Cristian](https://www.linkedin.com/in/iancristianyane/)
