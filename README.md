📊 Análisis de Funnel en App Móvil y Evaluación de Experimento A/A/B

--------------------------------------------------------------

📌 Descripción del Proyecto

Este proyecto analiza el comportamiento de los usuarios dentro del embudo (funnel) de una aplicación móvil y evalúa los resultados de un experimento A/A/B.

Los objetivos principales son:

* Analizar el recorrido de los usuarios a través de las etapas clave del funnel

* Validar la correcta aleatorización mediante un test A/A

* Evaluar el impacto de un cambio experimental en la conversión

--------------------------------------------------------------

📂 Dataset

El dataset contiene registros de eventos generados por usuarios dentro de la aplicación móvil, incluyendo:

* event_name — acción realizada dentro de la app

* user_id — identificador único del usuario

* event_ts — timestamp del evento

* exp_id — grupo experimental asignado

El experimento incluye tres grupos:

* 246 — Grupo de control A

* 247 — Grupo de control B

* 248 — Grupo experimental

--------------------------------------------------------------

🔎 Metodología

1️⃣ Preprocesamiento de Datos

* Estandarización y renombrado de columnas

* Conversión de timestamps a formato datetime

* Eliminación de duplicados

* Revisión general de calidad de datos

2️⃣ Construcción del Funnel

El embudo se compone de los siguientes eventos:

* MainScreenAppear

* OffersScreenAppear

* CartScreenAppear

* PaymentScreenSuccessful

* Tutorial

Para cada etapa se calcularon las tasas de conversión respecto al total de usuarios por grupo.

3️⃣ Validación del Test A/A

Se aplicó una prueba estadística de comparación de proporciones (z-test) entre los grupos 246 y 247 para cada evento del funnel.

Objetivo:
Verificar que no existan diferencias significativas entre los grupos de control y confirmar que la asignación aleatoria fue correcta.

Resultado:
No se encontraron diferencias estadísticamente significativas (α = 0.05), lo que valida la consistencia del experimento.

4️⃣ Evaluación del Test A/B

Posteriormente, se comparó el grupo experimental (248) contra los grupos de control mediante una prueba z de dos proporciones para cada etapa del funnel.

* Prueba utilizada: z-test para comparación de proporciones

* Nivel de significancia: α = 0.05

Las conclusiones se basaron en la interpretación de los valores p y en la magnitud de las diferencias observadas.

--------------------------------------------------------------

📈 Hallazgos Clave

* Se identificaron puntos de abandono relevantes dentro del funnel.

* El test A/A confirmó la correcta aleatorización del experimento.

* Las comparaciones estadísticas fueron realizadas de manera rigurosa y fundamentada.

* Las conclusiones se basan exclusivamente en evidencia estadística.

--------------------------------------------------------------

🛠 Herramientas Utilizadas

* Python

* pandas

* NumPy

* statsmodels

* Matplotlib

* JupyterNotebook