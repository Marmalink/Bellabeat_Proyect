# Bellabeat: análisis del uso de dispositivos inteligentes

Análisis descriptivo y prescriptivo de datos de dispositivos de seguimiento de actividad, para proponer ideas de mejora a la aplicación y a los productos de Bellabeat (caso práctico del Google Data Analytics Certificate).

**Herramientas:** Python, Pandas, NumPy, Sidetable, Matplotlib, Seaborn, Jupyter.

## Pregunta de negocio
¿Cómo usan sus dispositivos inteligentes las personas usuarias, y qué oportunidades hay para orientar la estrategia de la aplicación Bellabeat?

## Datos
- **FitBit Fitness Tracker Data** (Möbius, Kaggle): 33 usuarios, del 12/04/2016 al 12/05/2016 (aprox. 1 mes), 940 registros diarios de actividad. Datos de sueño de 24 usuarios.
- Se descartaron frecuencia cardíaca (14 usuarios) y peso (8 usuarios) por tener muy pocos participantes.
- **Stress-Lysis** (Laavanya Rachakonda, Kaggle): dataset independiente, usado solo de forma exploratoria. No corresponde a los mismos usuarios que los datos de FitBit.

## Proceso
1. **Limpieza y orden** (`LimpiezaYOrden.ipynb`): revisión de valores nulos, conversión de fechas, separación de fecha y hora, eliminación de columnas redundantes y exportación de tablas limpias a CSV.
2. **Análisis y visualización** (`AnalisisYVisualizacion.ipynb`): estadísticas descriptivas, frecuencias y gráficos de actividad, sueño, calorías y estrés.

## Hallazgos principales
- **Pasos diarios:** promedio de 7.638 (mediana 7.406).
- **Sedentarismo:** promedio de unos 991 minutos al día (casi 16,5 horas). Incluye días con 1.440 minutos sedentarios, probablemente sin uso del dispositivo.
- **Actividad:** promedio de 21 minutos diarios de actividad intensa, 14 de moderada y 193 de ligera.
- **Horas de mayor actividad:** entre las 11:00 y las 20:00.
- **Sueño:** promedio de 419 minutos (unas 7 horas) y mediana de 7,2 horas, pero un 25% de los registros duerme menos de unas 6 horas.
- **Calorías:** promedio diario de unas 2.300.

*Limitaciones: muestra pequeña (33 usuarios), un solo mes de 2016 y datos de sueño de solo 24 usuarios.*

## Recomendaciones para Bellabeat
- Alertas de inactividad tras largos períodos sedentarios, excluyendo las horas de sueño.
- Recordatorios para registrar el sueño y alerta ante registros de poco descanso.
- Rutinas y videos dentro de la aplicación, incluyendo opciones para interior en épocas de frío o lluvia.
- Detectar días sin registro y ofrecer seguir el monitoreo desde el celular.
- Ejercicios de relajación o meditación en la aplicación (a validar con datos de los mismos usuarios).

## Próximos pasos
- Excluir los días en que el dispositivo no se usó antes de calcular promedios.
- Analizar patrones por día de la semana.
- Explorar relaciones entre actividad, calorías y sueño.
- Armar un dashboard interactivo en Power BI.

---
**English summary:** Exploratory analysis of smart-device usage data (FitBit, 33 users, ~1 month) in Python (Pandas, Seaborn), with product recommendations for Bellabeat's app: inactivity alerts, sleep-tracking reminders and in-app routines.
