# Clasificación de Tipos de Psoriasis mediante Redes Neuronales Convolucionales

## 📖 Resumen del Proyecto

Este repositorio contiene el código y los resultados del Trabajo de Fin de Grado (TFG) para la **clasificación automática de cinco tipos de psoriasis** a partir de imágenes dermatológicas. El objetivo principal es desarrollar y validar un modelo de aprendizaje profundo (Deep Learning) que sirva como herramienta de apoyo al diagnóstico en el campo de la teledermatología.

El modelo implementado utiliza una arquitectura de Red Neuronal Convolucional (CNN) moderna, `EfficientNetB0`, aplicando la técnica de **Aprendizaje por Transferencia** (Transfer Learning) para lograr un alto rendimiento con un conjunto de datos de tamaño moderado.


## 🌟 Características Principales

- **Clasificación Multiclase:** El modelo es capaz de distinguir entre 5 tipos de psoriasis:
  - Psoriasis Vulgar (en Placas)
  - Psoriasis Guttata (en Gotas)
  - Psoriasis Inversa
  - Psoriasis Pustulosa
  - Psoriasis Eritrodérmica
    
- **Alta Precisión:** Se alcanzó una **precisión del 87.50%** en el conjunto de prueba final no visto, validando la robustez del enfoque.
- **Metodología Rigurosa:** El rendimiento del modelo se validó exhaustivamente mediante técnicas de **Validación Cruzada Estratificada K-Fold** y **Leave-One-Out Cross-Validation (LOOCV)**.
- **Aumento de Datos:** Se implementó una estrategia avanzada de aumento de datos para balancear el dataset y mejorar la capacidad de generalización del modelo.
  
## 🛠️ Metodología en Resumen

1.  **Conjunto de Datos:** Se utilizó un dataset de **798 imágenes** recopiladas de fuentes dermatológicas de referencia como DermNet y Roboflow Universe.
2.  **Preprocesamiento:**
    - Redimensionamiento de imágenes a 224x224 píxeles.
    - Normalización específica para el modelo `EfficientNetB0`.
    - **Aumento de Datos:** Aplicación de transformaciones geométricas (rotación, zoom, volteo, etc.) para balancear las clases y prevenir el sobreajuste.
3.  **Arquitectura del Modelo:**
    - **Base:** `EfficientNetB0` pre-entrenado en ImageNet, utilizado como extractor de características (base congelada).
    - **Clasificador Personalizado:** Se añadieron capas densas con `BatchNormalization` y `Dropout` para adaptar el modelo al problema específico de la psoriasis.
4.  **Validación y Evaluación:**
    - **División de Datos:** El dataset se dividió en un 85% para entrenamiento/validación y un 15% para un conjunto de prueba final.
    - **Validación Cruzada K-Fold (K=5):** Se utilizó para obtener una estimación robusta del rendimiento del modelo, alcanzando una precisión promedio del **91.59%**.
    - **Validación Cruzada Leave One Out:** Se utilizó para obtener una estimación más robusta del rendimiento del modelo, alcanzando una precisión del **89.10%**.
    - **Evaluación Final:** El modelo final, entrenado con el 85% de los datos, se evaluó en el 15% de prueba, obteniendo una precisión del **86.67%**.


## 🚀 Cómo Empezar

Para replicar este proyecto, puedes seguir los siguientes pasos:

1.  **Clonar el Repositorio:**
    ```bash
    git clone [https://github.com/Josmanr3/TFG_Psoriasis.git](https://github.com/Josmanr3/TFG_Psoriasis.git)
    cd TFG_Psoriasis
    ```
2.  **Entorno de Ejecución:** Se recomienda utilizar un entorno como Kaggle o Google Colab con acceso a una GPU para acelerar el entrenamiento.
3.  **Dataset:** Descarga el conjunto de datos utilizado desde [este enlace de Kaggle]([https://www.kaggle.com/datasets/josemlearning/psoriasis-ds/data?select=dataset_v8]) y ajústalo a la ruta `DATASET_PATH` en los notebooks.
4.  **Ejecutar los Notebooks:** Abre y ejecuta los cuadernos para ver el proceso de entrenamiento y evaluación.

---

## 👨‍💻 Autor

- **José Manuel Rosado Ríos** - [Josmanr3](https://github.com/Josmanr3)

## 🎓 Tutor

- **José Antonio Pérez Carrasco** - Departamento de Teoría de la Señal y Comunicaciones, Universidad de Sevilla.
