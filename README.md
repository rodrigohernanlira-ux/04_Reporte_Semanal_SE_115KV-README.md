# SE 115kV - Arquitectura de Datos y Simulación Estocástica 

Este repositorio contiene el núcleo técnico de la gobernanza de datos para la Subestación 115kV. El enfoque se centra en la transición de datos planos (CSV) hacia un modelo dimensional robusto y simulaciones de alto impacto.

## 📂 Componentes del Sistema
* `data_proyecto.csv`: Fuente primaria de datos con métricas EVM.
* `project_data.db`: Base de datos SQLite que implementa el modelo dimensional para analítica.
* `Informe_SE115kv_Sem_20.ipynb`: Script maestro en Python que integra el procesamiento, la carga a DB, el análisis de Montecarlo (10k iteraciones) y la generación automatizada de informes.

## 🛠️ Flujo de Trabajo (Pipeline)
1. **Ingesta:** Procesamiento del dataset simulado mediante Pandas.
2. **Persistencia:** Creación y población de tablas en SQLite (`create_and_populate_sqlite_db`).
3. **Analítica:** Cálculo de indicadores (CPI/SPI) por capítulo y globales.
4. **Simulación:** Ejecución de Montecarlo para determinar percentiles de costo y tiempo (P10, P50, P90).

## 🎯 Estándar Aplicado
Desarrollado bajo los dominios de **Planificación e Incertidumbre del PMBOK® 8.ª edición**, priorizando la transparencia de datos y la gestión de riesgos probabilísticos.

## ⚠️ Descargo de Responsabilidad (Disclaimer)
Este repositorio y el "Modelo de Informe para PMO 4.0" se comparten con fines estrictamente educativos y demostrativos. 
* **Uso bajo propio riesgo:** El autor no se hace responsable por decisiones financieras, contractuales o de planificación tomadas basadas en el uso de estos scripts o modelos.
* **Validación requerida:** Los modelos estocásticos (Monte Carlo) dependen de la calidad de los datos de entrada; es responsabilidad del usuario validar sus propias distribuciones y parámetros.
* **Sin garantías:** El software se proporciona "tal cual", sin garantía de ningún tipo, expresa o implícita.
