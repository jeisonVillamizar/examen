# examen


La farmacia no quiere solo listar medicamentos que caducan antes de una fecha, sino identificar riesgo real de caducidad en función de su rotación de ventas, por lo cual se requiere de un módulo que combine fechas de expiración con el historial de ventas.

El comando debe:

Leer:
Medicamentos.json
Ventas.json
Configurar (ya sea en código o en un archivo JSON de configuración, por ejemplo config_caducidad.json) parámetros como:
horizonte_dias: Dentro de cuántos días se considera “próximo a caducar” (ej: 90 días).
umbral_baja_rotacion: Unidades vendidas promedio por mes por debajo del cual se considera que el medicamento rota poco.
Para cada medicamento:
Determinar:
Si su fecha de expiración está dentro del horizonte (por comparación con una fecha de corte definida).
Su rotación de ventas:
Calcular unidades totales vendidas en un periodo (por ejemplo, último año) y sacar un promedio mensual.
Clasificar:
"ALTO_RIESGO_CADUCIDAD": Está próximo a caducar y tiene baja rotación.
"MEDIO_RIESGO": Está próximo a caducar pero tiene rotación aceptable.
"BAJO_RIESGO": No está próximo a caducar o rota bien.
Generar reporte_riesgo_caducidad.json con:
Lista de medicamentos:
nombre
stock
fechaExpiracion
unidades_vendidas_periodo
promedio_mensual
categoria_riesgo
Resumen:
Número de medicamentos en cada categoría.
Lista de medicamentos en "ALTO_RIESGO_CADUCIDAD" para atención prioritaria.
Requisitos
Ejecutar desde el menú interactivo la funcionalidad:
reporte_riesgo_caducidad()
Definir claramente la fecha de corte (puede ser actual o fija para la simulación).
JSON de salida debe estar ordenado, por ejemplo, listando primero los de mayor riesgo.
Entrega
Módulo de análisis de riesgo de caducidad.
reporte_riesgo_caducidad.json de ejemplo (con datos del escenario dado).
Si usas config_caducidad.json, dejarlo en el repositorio con valores de ejemplo.
