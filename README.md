Predicción Automatizada de Clics en Publicidad Usando Azure Machine Learning Studio

Autores: Anderson Mantuano, Camilo Granada, Alison Pino
Descripción

Este proyecto tiene como objetivo la creación y entrenamiento de un modelo de clasificación binaria para predecir si un usuario hará clic en un anuncio en línea. El modelo fue implementado utilizando Microsoft Azure Machine Learning Studio, un entorno de desarrollo basado en la nube que permite crear flujos de trabajo de aprendizaje automático. Se utilizó AutoML para automatizar el preprocesamiento de datos, la selección de algoritmos y la evaluación de métricas.

La práctica muestra cómo implementar un modelo de clasificación desde cero, utilizando únicamente las herramientas visuales de Azure Machine Learning Studio. Este enfoque permite a usuarios no expertos en programación aplicar el aprendizaje automático en contextos reales.
Índice de Términos

    Azure Machine Learning

    AutoML

    Clasificación

    Ciencia de Datos

    Inteligencia Artificial

    Microsoft Azure

Introducción

La publicidad digital está en constante crecimiento, y las empresas necesitan modelos predictivos que mejoren el rendimiento de sus campañas. El saber si un usuario hará clic en un anuncio es un problema clásico de clasificación binaria. Sin embargo, muchos profesionales no tienen los conocimientos técnicos necesarios para programar estos modelos desde cero.

Microsoft Azure Machine Learning Studio ofrece una solución accesible, permitiendo entrenar modelos automáticamente sin escribir código, mediante su herramienta AutoML. Este artículo documenta el proceso de implementación de un modelo de clasificación binaria para predecir los clics en anuncios, utilizando un conjunto de datos real obtenido desde Kaggle.
Descripción del Problema

El objetivo del proyecto es predecir la probabilidad de que un usuario haga clic en un anuncio en línea, en función de variables como:

    Edad del usuario (18 a 64 años)

    Género (Hombre, Mujer, No Binario)

    Tipo de dispositivo (Mobile, Desktop, Tablet)

    Posición del anuncio (Top, Side, Bottom)

    Historial de navegación

    Hora del día

El modelo se enmarca dentro de los problemas de clasificación binaria, donde la etiqueta a predecir es si el usuario hace clic o no en el anuncio (1 = clic, 0 = no clic).
Tecnologías Utilizadas

    Microsoft Azure Machine Learning Studio: Plataforma para entrenar y desplegar modelos ML sin código.

    AutoML: Servicio de automatización de aprendizaje automático que evalúa múltiples modelos y técnicas.

    Azure Compute Instance: Máquina virtual utilizada como recurso de cómputo.

    Dataset CSV: Archivo descargado desde Kaggle con información de usuarios.

    Visual Studio Code (opcional): Para gestión externa de notebooks si se desea ampliar el entorno.

Descripción de la Solución
1. Ingreso a Azure ML Studio

Accede a Azure Machine Learning Studio desde el portal de Azure y crea un recurso de ML. Luego, lanza el estudio para comenzar con el flujo de trabajo.
2. Carga del Dataset

El conjunto de datos fue descargado desde Kaggle y cargado en Azure ML Studio. La plataforma detecta automáticamente los tipos de columnas y realiza un análisis preliminar de los datos.
3. Configuración del Experimento AutoML

Inicia un nuevo experimento desde la pestaña Automated ML, selecciona el dataset previamente cargado y configura la tarea como clasificación binaria, usando la columna "click" como objetivo.
4. Uso de Terminal y Notebooks

Azure ML Studio permite acceder a la terminal integrada para verificar configuraciones y ejecutar comandos básicos. También se pueden usar notebooks para ampliar el entorno y realizar análisis adicionales.
Resultados

Azure AutoML dividió el dataset en conjuntos de entrenamiento y prueba, evaluando varios modelos como Logistic Regression, Random Forest, LightGBM y XGBoost. El modelo seleccionado fue LightGBM, con una precisión superior al 90%.

El modelo mostró un buen balance entre falsos positivos y verdaderos positivos. Las variables más influyentes fueron la edad, el tipo de dispositivo y la hora del día.
Conclusiones

Este proyecto demuestra cómo plataformas como Azure Machine Learning Studio facilitan el acceso al aprendizaje automático sin la necesidad de escribir código. Gracias a AutoML, fue posible crear un modelo preciso y funcional de manera rápida y eficiente. Este enfoque resulta ideal para prototipado rápido y análisis exploratorio de datos, especialmente para profesionales de áreas no técnicas interesados en aplicar inteligencia artificial a sus proyectos.
Guía Paso a Paso

Para obtener una guía detallada sobre cómo replicar este proyecto, por favor consulta el documento Guía Paso a Paso - Implementación de Modelo de Clasificación.
Referencias

    Microsoft, "Azure Machine Learning Documentation"

    Kaggle, "Ad Click Prediction Dataset"

    AutoML.org, "Automatic Machine Learning: Methods and Systems"

    Chen, T. and Guestrin, C., “XGBoost: A Scalable Tree Boosting System,” in Proc. of the 22nd ACM SIGKDD, 2016.

    Microsoft Azure, "What is AutoML in Azure Machine Learning?"
