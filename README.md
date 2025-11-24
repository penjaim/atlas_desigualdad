---
title: "Atlas de Desigualdad Espacial de Penjamillo (2025–2027)"
subtitle: "Proyecto de Investigación para el Instituto Municipal de Planeación"
author: "Vidal Mendoza Tinoco"
date: "2025"
geometry: margin=1in
fontsize: 12pt
---

# Introducción

La desigualdad territorial constituye una de las dimensiones menos atendidas por los gobiernos locales en México, a pesar de su impacto directo en el bienestar de la población. Penjamillo no es la excepción. El municipio presenta disparidades notorias en acceso a servicios básicos, infraestructura, educación y salud, cuyas manifestaciones se concentran en patrones geográficos detectables mediante análisis espacial.

Con fundamento en las atribuciones otorgadas al Instituto Municipal de Planeación (IMPLAN) —como la generación de información geoestadística (Art. 6, B-III), la creación y dirección del Banco Municipal de Información (Art. 23, VI) y la elaboración de estudios para identificar zonas prioritarias de atención (Art. 23, VII) del Reglamento del IMPLAN publicado en el Periódico Oficial del Estado de Michoacán— el presente documento propone la construcción del **Atlas de Desigualdad Espacial de Penjamillo**.

Este proyecto corresponde al primer componente del *Plan de Innovación para el Desarrollo Municipal 2025–2027*, donde se define como prioridad medir la desigualdad intra-municipal mediante técnicas de análisis espacial como Moran’s I, LISA, SAR y SEM, utilizando exclusivamente datos públicos (INEGI, CONEVAL, SEP, Secretaría de Salud).  

Este documento se desarrolla como una tesina técnica y aplicada, con sustento teórico, metodológico y econométrico.

---

# Justificación

La desigualdad territorial opera como un obstáculo estructural para el desarrollo municipal. Cuando ciertos barrios, localidades o AGEB presentan rezagos significativos, dichos rezagos tienden a reproducirse en el tiempo. En ausencia de herramientas que permitan visualizar estas brechas con precisión geográfica, los gobiernos locales enfrentan dificultades para asignar recursos, justificar intervenciones o diseñar programas focalizados.

El **Atlas de Desigualdad Espacial** permitirá:

- Identificar clusters espaciales de pobreza y rezago.
- Localizar zonas críticas de atención prioritaria.
- Diagnosticar los determinantes territoriales de la desigualdad.
- Justificar ante Cabildo y ciudadanía la asignación de recursos.
- Focalizar intervenciones y obras públicas de manera estratégica.
- Crear una herramienta replicable que permanezca más allá de los ciclos de gobierno.

---

# Marco Teórico

## Desigualdad y territorio

La desigualdad no solo se expresa en ingresos, sino en distribución espacial de oportunidades (Sen, 1992). Según Kanbur y Venables (2005), las disparidades regionales reflejan fallas profundas en el desarrollo territorial. Storper (2013) destaca que la geografía condiciona el acceso diferencial a servicios e infraestructura, creando círculos de inequidad.

## Autocorrelación espacial

La estadística espacial permite identificar patrones donde zonas similares tienden a agruparse. Técnicas esenciales incluyen:

- **Moran’s I** (Moran, 1950): autocorrelación global.
- **LISA** (Anselin, 1995): clusters locales (High-High, Low-Low).

## Econometría espacial

Elhorst (2014) sistematiza tres modelos fundamentales:

- SAR (Spatial Autoregressive Model)
- SEM (Spatial Error Model)
- SDM (Spatial Durbin Model)

Estos permiten analizar la dependencia espacial entre unidades territoriales.

## GWR: Regresión Ponderada Geográficamente

Propuesta por Brunsdon et al. (1996), permite que las relaciones entre variables cambien según el territorio.

## Planeación Municipal y Marco Legal

El Reglamento del IMPLAN establece la obligación de:

- Generar información geoestadística (Art. 6).
- Crear y actualizar el Banco Municipal de Información (Art. 23).
- Identificar zonas prioritarias de atención (Art. 23, VII).  

---

# Preguntas de Investigación

1. ¿Cómo se distribuye espacialmente la desigualdad socioeconómica dentro de Penjamillo?
2. ¿Existen clusters geográficos significativos de pobreza o rezago (Low-Low)?
3. ¿Qué factores explican territorialmente la desigualdad?
4. ¿Qué zonas deben priorizarse para inversión pública?
5. ¿Cómo construir un sistema replicable de monitoreo territorial a largo plazo?

---

# Metodología

## Datos

Fuentes públicas según el Plan de Innovación:  

- INEGI: Censo 2020  
- CONEVAL: pobreza municipal  
- SEP (SIGED): ubicación de escuelas  
- Secretaría de Salud (RECS)  
- Marco Geoestadístico (INEGI)  
:contentReference[oaicite:5]{index=5}

## Indicadores de desigualdad

Se crearán índices normalizados:

- Rezago educativo
- Acceso a servicios básicos
- Accesibilidad a salud
- Índice multidimensional de pobreza local
- Acceso a infraestructura

## Análisis exploratorio espacial

### Moran’s I

$$
I = \frac{n}{\sum_{i \ne j} w_{ij}} 
\frac{\sum_{i}\sum_{j} w_{ij}(x_{i}-\bar{x})(x_{j}-\bar{x})}
{\sum (x_{i}-\bar{x})^{2}}
$$

### LISA

Identificación de:

- High-High  
- Low-Low  
- High-Low  
- Low-High  

## Modelos espaciales (SAR, SEM, SDM)

Ejemplo SAR:

$$
y = \rho Wy + X\beta + \epsilon
$$

## Regresiones GWR

$$
y_i = \beta_{0}(u_i, v_i) + \sum_k \beta_{k}(u_i, v_i) x_{ik} + \epsilon_i
$$

---

# Beneficios para el Ayuntamiento y la Gestión Pública Municipal

El Atlas generará beneficios directos para la administración municipal:

## 1. **Toma de decisiones basada en evidencia**
Permite justificar intervenciones como obras públicas, programas sociales y ampliación de servicios con argumentos técnicos verificables.

## 2. **Priorización estratégica del gasto**
Identifica zonas donde una misma inversión genera mayor impacto, optimizando recursos escasos.

## 3. **Cumplimiento normativo**
El proyecto responde a obligaciones del IMPLAN:  
- Art. 6 (información y geoestadística)  
- Art. 23 (banco de información y estudios técnicos)  
- Art. 24 (planeación territorial)  
:contentReference[oaicite:6]{index=6}

## 4. **Transparencia y rendición de cuentas**
El Atlas fortalece la credibilidad institucional al permitir comunicar diagnósticos técnicos a ciudadanía, Cabildo y entes fiscalizadores.

## 5. **Atracción de recursos federales y estatales**
Los programas de inversión (SEDATU, SEDESOL, Ramo 33, FAIS) priorizan proyectos con soporte geoestadístico.

## 6. **Continuidad administrativa**
Al ser un instrumento técnico, el Atlas se convierte en un legado institucional que trasciende ciclos políticos.

## 7. **Fortalecimiento del IMPLAN**
Incrementa su capacidad técnica y su papel estratégico como órgano rector de la planeación.

---

# Cronograma 2025–2027

| Etapa | Periodo | Actividades |
|-------|---------|-------------|
| Preparación institucional e integración de datos | Nov 2025 – Ene 2026 | Bases normativas y marco teórico; Descarga, depuración y normalización de datos|
| Análisis Espacial | Ene – Mar 2026 | Moran, LISA, SAR/SEM, GWR |
| Elaboración del Atlas | Mar – Jun 2026 | Mapas, capítulos, indicadores |
| Publicación | Jul 2026 – Sept 2027 | PDF, portal de datos |
| Implementación de políticas | Oct – Nov 2027 | Zonas prioritarias |
| Evaluación final | Dic 2027 | Informe técnico |

---

# Resultados Esperados

- Atlas físico y digital.  
- Mapa oficial de Zonas Prioritarias de Atención.  
- Base de datos geoespacial integrada al Banco Municipal.  
- Tablero interactivo.  
- Informe anual de monitoreo de desigualdad territorial.  

---

# Conclusiones

El **Atlas de Desigualdad Espacial de Penjamillo** constituye un pilar fundamental para la modernización de la gestión municipal, alineado al Reglamento del IMPLAN y al Plan de Innovación 2025–2027. Su implementación permitirá mejorar la focalización del gasto, transparentar la acción pública y fortalecer la planeación estratégica del Ayuntamiento.

---

# Bibliografía

- Anselin, L. (1995). Local Indicators of Spatial Association (LISA).  
- Elhorst, J. (2014). Spatial Econometrics. Springer.  
- Kanbur, R. & Venables, A. (2005). Spatial Inequality and Development.  
- Sen, A. (1992). Inequality Reexamined.  
- Storper, M. (2013). Keys to the City.  
- Brunsdon, C., Fotheringham, S., & Charlton, M. (1996). GWR.

