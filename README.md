# Proyecto DataScience - Ingenias: Producción de Gas Natural en Argentina
# **Introducción al Proyecto**
Este proyecto tiene como objetivo realizar un análisis exploratorio y desarrollar un modelo predictivo de la producción de gas natural en Argentina, aprovechando dos fuentes de datos complementarias:

*  Dataset1: Serie histórica agregada de producción de gas natural por cuenca geológica y subtipo de recurso (convencional vs no convencional), con mediciones mensuales a nivel nacional.
*   Dataset2: Detalle de producción mensual a nivel de pozo no convencional, con información de empresa operadora, ubicación geográfica y volumen extraído de gas y petróleo.

Al combinar la visión macro (Dataset1) con el detalle micro (Dataset2), se podrá identificar patrones globales y específicos que expliquen el crecimiento de los recursos no convencionales y permitan proyectar tendencias futuras.

---

**Objetivo general**

Realizar un análisis exploratorio y desarrollar un modelo predictivo de la producción de gas natural en Argentina, utilizando datos históricos agregados y datos de pozos no convencionales, para identificar patrones temporales y proyectar la evolución futura de la producción a nivel nacional y por cuenca.

**Objetivos específicos**


1.   Análisis histórico: Describir la evolución anual de la producción total de gas natural y su desglose por cuenca (Neuquina, Austral, Golfo San Jorge, Noroeste, Cuyana) y tipo de recurso (convencional vs no convencional) utilizando el Dataset1.
2.   Exploración de pozos: Analizar la producción de gas a nivel de pozo no convencional según tipo de recurso (shale, tight),  cuenca y coordenadas geográficas con el Dataset2.
3. Evolución de recursos no convencionales: Investigar el peso relativo y la tasa de crecimiento del gas shale y tight sobre la producción nacional total (Dataset1).
4. Modelo predictivo: Desarrollar modelos que estimen la producción futura de gas natural, tanto agregada como por cuencas, a partir de las variables temporales, geográficas y técnicas disponibles en ambos datasets.

---
**Integrantes: Equipo 5**

Mansilla, Fabiana Yamila

Perea, Daniela

---
**Hipótesis de trabajo**

La producción de gas natural en Argentina puede modelarse y predecirse con precisión a partir de patrones temporales y geográficos presentes en los datos. En particular, se espera que el desarrollo de los recursos no convencionales (shale y tight), concentrado principalmente en la cuenca Neuquina, sea el principal motor del aumento sostenido de la producción nacional.

---

**Descripción de los datasets**

**Dataset1: Serie histórica de producción de Gas Natural (CapítuloIV)**

*   Fecha: Año, Mes, (índice de tiempo mensual).
*   Producción de gas: Por cuenca y tipo de recurso (convencional vs no convencional).
*   Totales: Volumen mensual nacional y promedio diario.

Útil para analizar evolución histórica, comparar convencional vs no convencional y proyectar tendencias.

**Dataset2: Producción de Pozos de Gas y Petróleo No Convencional**

*  Identificadores: idempresa, idpozo.

*  Producción: Petróleo (m³), gas (Miles de m³), agua (m³).

*  Volúmenes inyectados: iny_agua, iny_gas, iny_co2 (todos ceros en este caso).

*  Geografía: Cuenca, provincia, latitud, longitud, proyecto, tipo_recurso, clasificación y subclasificación.

Permite análisis detallado por pozo, comparación entre empresas y estudio de factores operativos.

---

**Fuente de datos**

*  Dataset1: Serie histórica de producción de Gas Natural por cuenca y subtipo de recurso (CapítuloIV). Disponible en la sección “Serie histórica de producción de Gas Natural por cuenca y subtipo de recurso (CapítuloIV)” del portal de datos energía de Argentina.

  Enlace: http://datos.energia.gob.ar/dataset/serie-historica-de-produccion-de-gas-natural-por-cuenca-y-sub-tipo-de-recurso-captulo-iv

*  Dataset2: Producción de Pozos de Gas y Petróleo No Convencional. Disponible en la sección “Producción de petróleo y gas por pozo” (no convencional) del portal de datos energía de Argentina.

  Enlace: http://datos.energia.gob.ar/dataset/produccion-de-petroleo-y-gas-por-pozo
  
---

**Estructura del Repositorio**

El repositorio está organizado en carpetas, cada una correspondiente a una etapa del proyecto:

📁 Pre-Entrega 1: Contiene las notebooks individuales 5 y 7, realizadas por cada integrante como entregas previas al trabajo grupal.

📁 Pre-Entrega 2: En esta carpeta comienza el desarrollo del proyecto grupal. Se incluye la notebook con el proceso de limpieza de datos y el análisis exploratorio, que ya toma como base el problema específico de la producción de gas natural en Argentina. 

📁 Pre-Entrega 3:

📁 Pre-Entrega 4:

📄 README.md: Este archivo contiene la documentación general del proyecto.

---

**Metodología**

1. Limpieza de datos: Se llevó a cabo el tratamiento de valores nulos, la normalización de formatos de fecha, la estandarización de variables categóricas y la unificación de criterios entre ambos conjuntos de datos para permitir su análisis conjunto.
2. Análisis exploratorio: Se trabajó con ambos datasets desde dos perspectivas temporales: la serie histórica completa y un recorte de los últimos 10 años, para captar tanto la evolución general como las tendencias más recientes.
Los análisis se realizaron con agregación anual, lo que permitió visualizar mejor los patrones y reducir la variabilidad propia de los datos mensuales.
   * En el Dataset 1, se examinó la evolución anual de la producción total de gas natural, desagregando por cuenca y tipo de recurso (convencional vs no convencional).
   *  En el Dataset 2, se analizaron las producciones de pozos no convencionales según sub tipo de recurso (shale, tight), tipo de pozo (Gasífero), tipo de estado y por cuenca.
   *  Se investigó especialmente el crecimiento de los recursos no convencionales dentro del total nacional.


---

**Herramientas utilizadas**

* Python (v3.10)
* Pandas, Numpy, Matplotlib, Seaborn (análisis y visualización)
* Scipy: para análisis estadístico y funciones científicas complementarias.
