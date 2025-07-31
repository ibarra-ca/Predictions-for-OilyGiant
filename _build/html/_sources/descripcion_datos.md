# Descripción de datos

Los datos de exploración geológica de las tres regiones se almacenan en archivos:

- [/datasets/geo_data_0.csv](/datasets/geo_data_0.csv)
- [/datasets/geo_data_1.csv](/datasets/geo_data_1.csv)
- [/datasets/geo_data_2.csv](/datasets/geo_data_2.csv)
<br>

- *id* — identificador único de pozo de petróleo
- *f0, f1, f2* — tres características de los puntos (su significado específico no es importante, pero las características en sí son significativas)
- *product* — volumen de reservas en el pozo de petróleo (miles de barriles). 
</br>

### Instrucciones del proyecto

1. Descarga y prepara los datos. Explica el procedimiento.
2. Entrena y prueba el modelo para cada región en geo_data_0.csv:
    - 2.1. Divide los datos en un conjunto de entrenamiento y un conjunto de validación en una proporción de 75:25
    - 2.2. Entrena el modelo y haz predicciones para el conjunto de validación.
    - 2.3. Guarda las predicciones y las respuestas correctas para el conjunto de validación.
    - 2.4. Muestra el volumen medio de reservas predicho y RMSE del modelo.
    - 2.5. Analiza los resultados.
    - 2.6. Coloca todos los pasos previos en funciones, realiza y ejecuta los pasos 2.1-2.5 para los archivos 'geo_data_1.csv' y 'geo_data_2.csv'.
3. Prepárate para el cálculo de ganancias:
    - 3.1.Almacena todos los valores necesarios para los cálculos en variables separadas.
    - 3.2.Dada la inversión de 100 millones por 200 pozos petrolíferos, de media un pozo petrolífero debe producir al menos un valor de 500,000 dólares en unidades para evitar pérdidas (esto es equivalente a 111.1 unidades). Compara esta cantidad con la cantidad media de reservas en cada región.
    - 3.3.Presenta conclusiones sobre cómo preparar el paso para calcular el beneficio.
4. Escribe una función para calcular la ganancia de un conjunto de pozos de petróleo seleccionados y modela las predicciones:
    - 4.1. Elige los 200 pozos con los valores de predicción más altos de cada una de las 3 regiones (es decir, archivos 'csv').
    - 4.2.Resume el volumen objetivo de reservas según dichas predicciones. Almacena las predicciones para los 200 pozos para cada una de las 3 regiones.
    - 4.3. Calcula la ganancia potencial de los 200 pozos principales por región. Presenta tus conclusiones: propón una región para el desarrollo de pozos petrolíferos y justifica tu elección.
5. Calcula riesgos y ganancias para cada región:
    - 5.1. Utilizando las predicciones que almacenaste en el paso 4.2, emplea la técnica del bootstrapping con 1000 muestras para hallar la distribución de los beneficios.
    - 5.2. Encuentra el beneficio promedio, el intervalo de confianza del 95% y el riesgo de pérdidas. La pérdida es una ganancia negativa, calcúlala como una probabilidad y luego exprésala como un porcentaje.
    - 5.3. Presenta tus conclusiones: propón una región para el desarrollo de pozos petrolíferos y justifica tu elección. ¿Coincide tu elección con la elección anterior en el punto 4.3?