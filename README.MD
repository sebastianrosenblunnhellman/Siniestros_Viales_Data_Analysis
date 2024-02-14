# Observatorio de Movilidad y Seguridad Vial (OMSV) 🚦🚔

El Observatorio de Movilidad y Seguridad Vial (OMSV), un centro de estudios bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, ha encargado la realización de un proyecto de análisis de datos. El objetivo principal de este proyecto es generar información que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en siniestros viales.

## Descripción del Proyecto 📝🚗

El proyecto se enfoca en el análisis de un conjunto de datos sobre homicidios en siniestros viales ocurridos en la Ciudad de Buenos Aires durante el periodo 2016-2021. El dataset se encuentra en formato xlsx y consta de dos hojas principales: "hechos" y "víctimas". Además, se proporcionan dos hojas adicionales que contienen diccionarios de datos para facilitar la comprensión de la información compartida.

## Estructura del Proyecto 🏗️📊

El trabajo se organiza en tres secciones principales:

### 1. Data Cleaning 🧹🔍

En esta fase inicial del proyecto, se llevarán a cabo las siguientes tareas:

- Importación de los datos desde el archivo xlsx.
- Realización de transformaciones necesarias, como:
  - Imputación de valores nulos utilizando criterios pertinentes.
  - Eliminación de columnas redundantes.
  - Eliminación de duplicados.
  - Estandarización del formato de la fecha para su posterior uso en Power BI.

### 2. Análisis Exploratorio de Datos (EDA) 📈🔎

En esta sección, se lleva a cabo un análisis exploratorio detallado de los conjuntos de datos `df_victimas` y `df_hechos`. Se han identificado los siguientes niveles de medición para las variables de cada conjunto de datos:

#### Niveles de medición de `df_victimas`

- Nominal: id_hecho, ROL, VICTIMA, SEXO.
- Intervalo: FECHA, FECHA_FALLECIMIENTO.
- Razón: EDAD.

#### Niveles de medición de `df_hechos`

- Nominal: id_hecho, TIPO_DE_CALLE, Dirección Normalizada, COMUNA, VICTIMA, ACUSADO.
- Intervalo: FECHA, HORA.
- Razón: N_VICTIMAS, pos x, pos y.

#### Conclusiones del Análisis Univariado

**Para `df_victimas` y `df_hechos`:**

* **Rol de las víctimas:**
    * La mayoría de las víctimas son conductores (341), seguidos por peatones (267) y pasajeros (80).
* **Tipo de víctima:**
    * La mayoría de las víctimas son motociclistas (312), seguidos por peatones (267) y automovilistas (94).
* **Edad de las víctimas:**
    * La edad promedio de las víctimas es de 41 años y la mediana es de 35.
    * La edad mínima de una víctima es de 1 año y la máxima de 95 años, con una desviación estándar de 19 años, lo que indica una alta variabilidad.
    * La distribución de la edad de las víctimas está sesgada a la derecha, con más víctimas mayores que menores.
* **Sexo de las víctimas:** La mayoría de las víctimas son de sexo masculino, con una proporción de 3 a 1.
* **Tipo de calle:**
    * La mayoría de los accidentes ocurren en avenidas (429), seguidas por calles (136) y autopistas (66).
* **Comuna:**
    * La comuna con mayor número de accidentes es la 1 (90), seguida por la 4 (76) y la 9 (73).
* **Víctimas y Acusados:**
    * La mayoría de las víctimas son motociclistas (304), y los principales acusados son automovilistas (227).
    * También hay un número considerable de peatones tanto como víctimas (264) como acusados (173).
* **Número de víctimas:**
    * Casi todos los accidentes tienen una sola víctima (676).

#### Análisis Bivariado

Se realizó un análisis bivariado, principalmente utilizando las fechas, para observar la distribución de los hechos a lo largo del tiempo. Se analizó y visualizó la frecuencia de los hechos por año, mes, día de la semana y hora del día, con el objetivo de identificar patrones temporales en la incidencia de siniestros viales.

Además, se llevó a cabo una visualización geográfica de la distribución de los hechos para comprender mejor su ubicación en la Ciudad de Buenos Aires.

Continuaré con la siguiente sección una vez que me la proporciones.

### 3. Desarrollo en Power BI 📊🔍

Después del análisis exploratorio de datos, se procedió a estructurar el dashboard en Power BI siguiendo las siguientes pestañas:

#### Portada 🏠📊

En esta sección se presenta el uso del dashboard, utilizando el logotipo del Gobierno de la Ciudad y una paleta de colores similar para mantener la coherencia visual.

#### KPI's 📈🎯

Esta pestaña muestra los KPIs propuestos:

1. **Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.**
   - Se define la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. La fórmula utilizada es: (Número de homicidios en siniestros viales / Población total) * 100,000.

2. **Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.**
   - Se define la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado período temporal. La fórmula utilizada para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100.

#### Perfil Demográfico de las Víctimas 👤📊

Esta sección presenta:

- Distribución de víctimas por sexo (masculino/femenino).
- Distribución de víctimas por rango etario.
- Total de víctimas por año.
- Víctimas agrupadas por tipo de desplazamiento.

#### Distribución Temporal de Siniestros 🕒📈

En esta pestaña se muestra la cantidad de víctimas en función de:

- Año.
- Mes del año.
- Día del mes.
- Hora del día.

#### Distribución Geográfica de Siniestros 🌍🚨

Esta sección presenta:

- Mapa de burbujas por siniestros.
- Distribución de víctimas por comuna.
- Siniestros por año según el tipo de calle.

### Cierre y Conclusiones 🏁📝

El proyecto realizado para el Observatorio de Movilidad y Seguridad Vial (OMSV) ha sido un esfuerzo integral para analizar y comprender los datos relacionados con los siniestros viales en la Ciudad de Buenos Aires. A lo largo del proceso, se ha llevado a cabo un exhaustivo análisis exploratorio de datos (EDA), seguido de la creación de un dashboard interactivo en Power BI.

Durante el EDA, se identificaron varios hallazgos significativos sobre los siniestros viales y sus víctimas. Se observó una alta incidencia de accidentes en avenidas y una concentración de víctimas masculinas, siendo los conductores y motociclistas los grupos más afectados. Además, se analizó la distribución temporal y geográfica de los siniestros, lo que permitió identificar patrones y áreas de mayor riesgo.

El dashboard desarrollado en Power BI proporciona una herramienta visual y dinámica para monitorear y analizar la situación de los siniestros viales en la Ciudad de Buenos Aires. Los KPIs definidos permiten establecer metas específicas para la reducción de la tasa de homicidios y la cantidad de accidentes mortales de motociclistas, brindando así un marco para la toma de decisiones y la evaluación del progreso en la implementación de medidas preventivas.

En resumen, este proyecto ha demostrado la importancia del análisis de datos en la formulación de políticas y estrategias para mejorar la seguridad vial. Al comprender mejor los factores que contribuyen a los siniestros viales y sus consecuencias, las autoridades locales pueden tomar medidas más efectivas para proteger a los ciudadanos y reducir el número de víctimas en las calles. 🚗🛣️
