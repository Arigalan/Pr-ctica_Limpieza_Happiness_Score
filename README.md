# Practica Limpieza Happiness Score
Este notebook documenta el proceso de limpieza y análisis exploratorio del dataset World Happiness Report, abarcando registros desde 2005 hasta 2025. El objetivo principal es preparar los datos para su uso en análisis posteriores, aplicando buenas prácticas de transformación, imputación de valores nulos y selección de variables.

📊 Descripción del Dataset
El archivo original contiene 2116 filas y 13 columnas, con información sobre:

Año (year)

Ranking por año (rank_in_year)

País (country)

Puntaje de felicidad (happiness_score)

Intervalos de confianza (lower_whisker, upper_whisker)

Variables explicativas como:

Logaritmo del PIB per cápita

Apoyo social

Expectativa de vida saludable

Libertad para tomar decisiones

Generosidad

Percepción de corrupción

Residual del modelo (dystopia_plus_residual)

🧹 Proceso de Limpieza
1. Exploración inicial
Se identificaron las 13 columnas del dataset.

Se detectaron múltiples columnas con valores nulos, especialmente aquellas relacionadas con las variables explicativas y los whiskers.

2. Tratamiento de valores nulos
Se analizaron las columnas con valores faltantes.

Se compararon estrategias de imputación:

Media: 5.4656

Mediana: 5.48

Se concluyó que la media es el método más representativo debido a la distribución simétrica de los datos y la ausencia de outliers significativos.

3. Limpieza de texto en nombres de países
Se eliminaron espacios en blanco al inicio y final de los nombres.

Se aplicó formato capitalización para estandarizar la escritura (ej. sierra leone → Sierra Leone).

Justificación: Evitar errores en filtros y agrupaciones, y mejorar la legibilidad.

4. Selección de variables
Para simplificar el análisis, se creó un subconjunto con las columnas:

country

year

happiness_score

5. Comparación de métodos de imputación
Se compararon media y mediana, encontrando diferencias mínimas.

Se utilizó df.describe() para verificar la presencia de outliers.

Se confirmó que la media es adecuada por la estabilidad de los datos.

6. Reflexión sobre la calidad de los datos
Se respondieron preguntas clave:

¿Los valores nulos afectan el análisis? Sí, si no se imputan correctamente.

¿La limpieza de texto influye en los resultados? Sí, mejora la organización y fiabilidad de los filtros.

¿Qué método de imputación elegir? La media, por ser representativa y robusta.
