
# Clasificación de Hongos con Machine Learning y Redes Neuronales MLP

Este proyecto implementa modelos de Machine Learning para clasificar hongos en venenosos o no venenosos. Se comparan dos enfoques: Regresión Logística y una Red Neuronal Perceptrón Multicapa (MLP). Se realiza análisis, visualización y evaluación de los modelos con el dataset limpio de hongos.

## Contenido del Proyecto

### Integrantes

- Juan Sebastián Caicedo Orobio
- Santiago Giraldo Gutierrez
- Brayan Alexis Medina
- Juan Hurtado

### Enlace al Dataset

El dataset utilizado se aloja en el siguiente enlace:  
[Dataset de Hongos Limpio](https://raw.githubusercontent.com/Skpow1234/Dataset_Repo/refs/heads/main/data/mushroom_cleaned.csv)

### Tecnologías y Librerías Utilizadas

- Python
- Numpy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Redes Neuronales (MLPClassifier)
- Métricas de Clasificación (confusion_matrix, accuracy_score, etc.)

## Pasos del Proyecto

1. **Carga y Procesamiento de Datos**
   - Se cargan los datos desde el enlace proporcionado.
   - Las columnas son renombradas para facilitar la interpretación (por ejemplo, `cap-diameter` -> `diámetro-sombrero`).
   - Se seleccionan características relevantes para la clasificación.

2. **División de Datos**
   - Se divide el dataset en un 75% para entrenamiento y un 25% para prueba.

3. **Normalización**
   - Los datos se escalan utilizando `StandardScaler` para mejorar el rendimiento del modelo.

4. **Implementación de Modelos**
   - **Regresión Logística:** Modelo inicial para clasificación.
   - **Red Neuronal MLP:** Modelo avanzado con una capa oculta y un máximo de 500 iteraciones.

5. **Evaluación de Modelos**
   - Se utilizan métricas como precisión, recall, F1-score y matriz de confusión.
   - Se evalúa el rendimiento general con la Curva ROC y AUC.

6. **Visualizaciones**
   - Gráficos de dispersión y fronteras de decisión.
   - Comparación de modelos mediante gráficos de barras, líneas y pastel.

7. **Predicción**
   - Predicción con nuevos valores para clasificar un hongo según sus características.

## Resultados

### Métricas Clave

- **Precisión General:**
  - Regresión Logística: ~63%
  - Red Neuronal MLP: Mejora ligera (~65%).
  
- **Rendimiento por Clase:**
  - MLP tiene un mejor rendimiento general comparado con la regresión logística.

### Análisis

- La MLP es más compleja y menos interpretable, pero ofrece un rendimiento superior.
- La Regresión Logística es más simple e interpretable, ideal para entender cómo afectan las características las predicciones.

## Conclusión

El modelo más adecuado depende de las prioridades del proyecto:

- Si se requiere precisión y no importa la interpretabilidad, **MLP** es mejor.
- Si se necesita simplicidad y comprensión, **Regresión Logística** es preferible.

## Ejecución del Proyecto

1. Clonar el repositorio con:

   ```bash
   git clone https://github.com/Skpow1234/Dataset_Repo.git
   ```

2. Instalar las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

3. Ejecutar el Jupyter Notebook:

   ```bash
   jupyter notebook Clasificacion_RegLog_Mushrums_Grupo3_MLP.ipynb
   ```
