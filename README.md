# Mlflow-Red-Neuronal-Fine-Tuning

## Descripción del problema
En tareas de clasificación supervisada, alcanzar un buen equilibrio entre precisión y recall
suele ser más relevante que maximizar únicamente la métrica de accuracy. Los modelos base
de redes neuronales pueden presentar valores aceptables de exactitud, pero fallar en su
capacidad de generalización entre clases, especialmente cuando la distribución de los datos
no es perfectamente balanceada.

Este proyecto aborda el problema de mejorar el desempeño de un modelo de clasificación
mediante un proceso sistemático de fine tuning, utilizando MLflow para el seguimiento de
experimentos, la comparación de configuraciones y la selección objetiva del mejor modelo.

---

## Stack tecnológico
- **Lenguaje de programación:** Python
- **Machine Learning:** Scikit-learn, TensorFlow / Keras
- **Gestión de experimentos:** MLflow
- **Procesamiento de datos:** Pandas, NumPy
- **Visualización:** Matplotlib
- **Entorno de trabajo:** Jupyter Notebook

---

## Arquitectura – Enfoque por fases

La solución se estructura mediante una arquitectura experimental basada en fases:

### Fase 1 – Modelo base
Se entrena y evalúa un modelo base de red neuronal para establecer un punto de referencia
en términos de desempeño.

### Fase 2 – Modelos optimizados
Se evalúan configuraciones previamente optimizadas y se comparan con el modelo base.

### Fase 3 – Fine tuning sistemático
Se definen múltiples configuraciones de fine tuning mediante el ajuste de hiperparámetros
como:
- Tasa de aprendizaje
- Configuración de la red neuronal
- Parámetros de entrenamiento

Cada configuración se registra como un experimento independiente dentro de MLflow.

### Fase 4 – Evaluación y comparación
Todos los modelos son evaluados utilizando múltiples métricas, permitiendo una comparación
integral del desempeño global.

---

## Evidencias
- Interfaz de seguimiento de experimentos en MLflow
- Comparación de métricas entre configuraciones
- Resúmenes de desempeño de los modelos

Las evidencias visuales se encuentran en:
- `SolanoAGuillenJ_MlflowFineTuningV1.html`
- `Resultados_SolanoAGuillenJ_MlflowFineTuningV1.pdf`

---

## Qué se logró
- Implementación de un flujo de trabajo reproducible para fine tuning de modelos
- Centralización del seguimiento de experimentos mediante MLflow
- Comparación objetiva de múltiples configuraciones de redes neuronales
- Identificación de un modelo ajustado con mejor equilibrio entre métricas de evaluación

---

## Código
La implementación completa se encuentra en los siguientes archivos:

- **`SolanoAGuillenJ_MlflowFineTuningV1.ipynb`**  
  Contiene todo el pipeline experimental: definición del modelo, entrenamiento,
  configuraciones de fine tuning, registro en MLflow y evaluación de resultados.

- **`SolanoAGuillenJ_MlflowFineTuningV1.html`**  
  Versión ejecutada y exportada del notebook para visualización directa.

---

## Resultados cuantificables
- Los valores de accuracy se mantienen relativamente estables entre configuraciones
  (aproximadamente entre 0.78 y 0.80), lo que indica una sensibilidad limitada al ajuste
  de hiperparámetros.
- El F1-score evidencia diferencias más claras entre los modelos evaluados.
- Una configuración de fine tuning sistemático alcanza el mayor valor de F1-score,
  superando al modelo base y a versiones optimizadas previas.
- El modelo seleccionado logra un mejor equilibrio entre precisión y recall, mejorando
  la confiabilidad global de la clasificación.


---

## Autores
Ariel Solano  
Juan Guillén  

Universidad Politécnica Salesiana  
Inteligencia Artificial – Práctica Integradora  
Diciembre 2025
