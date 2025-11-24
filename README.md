# Adventure-Works-Cycles-(AWC)

# 💻 Proyecto Integrador: Análisis Financiero y Comercial de Adventure Works Cycles (AWC)

---

## 💡 Introducción

Este proyecto final del bootcamp de Data Analytics de Henry tiene como objetivo principal aplicar el ciclo completo de Business Intelligence (BI), que incluye ETL (Extracción, Transformación y Carga) y Visualización de Datos, utilizando la base de datos AdventureWorksDW2019.

El análisis se centra en evaluar el desempeño financiero y comercial de Adventure Works Cycles (AWC), proporcionando una visión integral sobre:

Ingresos, costos (COGS), utilidades y márgenes.

Demografía de clientes y segmentación por producto y territorio de ventas.

---

## 🛠️ Tecnologías y Herramientas

- ETL & Modelado: Power Query (M Language), DAX (Data Analysis Expressions)

- Visualización & Reporting: Microsoft Power BI

- Base de Datos: AdventureWorksDW2019 (SQL Server)

---

## 📈 Desarrollo del Proyecto

### 1. Extracción y Transformación (ETL en Power Query)

Se cargaron y analizaron tablas clave como DimProduct, FactInternetSales, DimCustomer, DimDate, y DimSalesTerritory.

Las transformaciones más importantes incluyeron:

- Promoción de Encabezados: Utilización de la primera fila como encabezado en tablas con columnas numeradas.

- Limpieza de Datos: Eliminación de columnas irrelevantes (ej. idiomas no utilizados, columnas nulas) y filas nulas.

- Creación de Columnas: Generación de una columna personalizada para la abreviatura del mes.

- Combinación de Tablas: Consolidación de información clave (ej. DimCustomer + DimGeography; tablas de producto).

### 2. Modelado de Datos y Medidas (DAX)

Se definieron las relaciones entre las tablas y se crearon medidas fundamentales utilizando DAX para el análisis financiero:

**Medidas Financieras:**

- Ingresos, COGS, UtilidadBruta, UtilidadNeta, Impuestos, y Envíos (usando SUM y restas).

- Ratios: Margen Bruto %, Margen Neto %, y Ratio Costos (usando DIVIDE).

**Medidas de Variación Temporal:** 

Cálculo de Variación Nominal y márgenes del período anterior para análisis interanual.

**Otras Medidas:** 

Clientes Únicos y Artículos Vendidos.

**Columna DAX:** 

Creación de la columna "Trimestre" en la tabla DimDate para el análisis temporal.

---

## 📊 Análisis y Visualización (Power BI Dashboards)

Se diseñaron dos tableros principales:

### Tablero 1: Reporte Financiero 

* **KPI Cards:** Muestran métricas clave (Ingresos, COGS, Utilidad Bruta, Utilidad Neta). Incluyen indicadores de **variación respecto al período anterior**, junto con el porcentaje de variación, facilitando la detección rápida de crecimiento o decrecimiento.
* **Medidores (Tacómetros):** Visualizan los **márgenes** (bruto y neto), ratios de costos y porcentaje COGS, ayudando a comprender qué tan cerca se encuentra la empresa de valores óptimos de rentabilidad.
* **Gráfico Temporal:** Un gráfico combinado de columnas y línea (Ingresos, COGS y Utilidad Bruta) para analizar la evolución mensual y detectar patrones de estacionalidad.
* **Mapa Geográfico:** Muestra la **cantidad de clientes por país**, lo que permite tomar decisiones estratégicas sobre expansión geográfica y priorización de territorios.

### Tablero 2: Análisis Estados Unidos 

* **Matriz Detallada:** Presenta Ingresos, COGS, Utilidad Bruta y Utilidad Neta para cada categoría de producto y región geográfica, incluyendo las **variaciones interanuales**. Esta visualización es clave para detectar áreas de oportunidad o productos menos rentables.
* **Gráfico de Líneas:** Permite comparar la evolución de los **Ingresos acumulados** a lo largo de los años, contrastando el período actual con el anterior.
* **Segmentadores:** Filtros interactivos por **Año** y **Categoría** para otorgar flexibilidad en el análisis y responder preguntas específicas del negocio.

---

## 🔍 Resultados y Conclusiones Principales

El análisis del desempeño de AWC arrojó los siguientes hallazgos:

* **Rentabilidad Saludable:** El **margen bruto se mantiene en niveles saludables, superando el 41%**, indicando un control eficiente de los costos de producción. La **utilidad neta alcanzó un margen cercano al 30%**, lo que refleja eficiencia operativa.
* **Foco Geográfico:** Los países con mayor número de clientes y concentración de ingresos son **Estados Unidos, Reino Unido y Canadá**.
* **Anomalía Detectada:** El análisis revela un **incremento muy significativo de los ingresos en el período 2013-2014**, con una variación superior al **4050%** respecto al año anterior, lo cual debe ser investigado por un posible error en el cálculo o en los datos manejados.

---

## 🚀 Líneas Futuras de Análisis

Para enriquecer aún más este proyecto y el valor para el negocio, se propone:

* **Predicción de Ventas:** Incorporar modelos de **Machine Learning** para la proyección de ventas.
* **Análisis de Estacionalidad:** Profundizar en los patrones estacionales para realizar proyecciones de ventas más ajustadas y planificar inventarios de manera más eficiente.
