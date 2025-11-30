# Desafío de Modelo Fundacional para Análisis de Imágenes de Ultrasonido (FMC-UIA) - Bitácora de Desarrollo

![Status](https://img.shields.io/badge/Status-Active-success)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-ee4c2c)
![Challenge](https://img.shields.io/badge/FMC__UIA-ISBI%202025-violet)

**Contexto del Desafío**

La ecografía es una herramienta diagnóstica vital, pero el análisis preciso de imágenes a través de diversos órganos y patologías sigue siendo un desafío significativo en la práctica clínica. Los métodos tradicionales a menudo se limitan a tareas específicas (como la clasificación de órganos o detección de tumores) y carecen de generalización.

Este repositorio documenta mi participación en el **Foundation Model Challenge for Ultrasound Image Analysis (FMC_UIA)**. El objetivo principal del reto es diseñar un **Modelo Fundacional generalizado** capaz de manejar múltiples tareas simultáneamente en el análisis de imágenes de ultrasonido, incluyendo:
* **Clasificación**
* **Segmentación**
* **Detección**
* **Regresión**

A través del aprendizaje multitarea (*Multi-task learning*), buscamos aprender representaciones compartidas para proporcionar resultados más fiables y consistentes en diversas aplicaciones médicas.

## Objetivos del Proyecto
Alineados con las metas del desafío organizado por `jared2408`:
1.  **Desarrollar un Modelo Fundacional:** Crear una arquitectura unificada que no dependa de modelos aislados para cada tarea.
2.  **Evaluación Clínica Real:** Evaluar el modelo en escenarios del mundo real utilizando métricas estandarizadas sobre un dataset diverso.
3.  **Reproducibilidad y Eficiencia:** Implementar pipelines de datos robustos y estrategias de entrenamiento eficientes (e.g., *Hard Parameter Sharing*).

## Estructura del Repositorio

El desarrollo se organiza cronológicamente por sprints semanales:

```bash
.
├── Week_1/                 # [Completado] Reproducibilidad, ETL y Validación Inicial
│   ├── src/               # Scripts de saneamiento (subset) y entrenamiento
│   ├── reports/           # Informe técnico, métricas y visualizaciones
│   └── README.md          # Documentación técnica de la semana
├── Week_2/                 # [Planeado] Optimización de Loss Functions & Augmentation
├── Week_3/                 # [Planeado] Refinamiento de Arquitectura y Dockerización
└── README.md              # Este archivo
```

## Bitácora de Avance

| Sprint   | Fechas          | Foco Principal                 | Estado       | Entregables Clave                                                                     |
| -------- | --------------- | ------------------------------ | ------------ | ------------------------------------------------------------------------------------- |
| Semana 1 | Dic 1 - Dic 5   | Ingeniería de Datos & Baseline | ✅ Completado | Pipeline verificado, Subset estratificado, Métricas baseline.                        |
| Semana 2 | Dic 9 - Dic 12  | Estrategias de Optimización    | ⏳ Pendiente  | Implementación de Focal Loss, SmoothL1 y aumentación geométrica.                      |
| Semana 3 | Dic 15 - Dic 19 | Despliegue & Contenerización   | ⏳ Pendiente  | Docker final basado en `tytll/isbi-evaluation:latest` y validación en CodaBench.      |

## Stack Tecnológico

- **Core:** PyTorch, Torchvision.
- **Arquitectura:** EfficientNet-B4 (Encoder) + FPN (Decoder) + Custom Heads.
- **Data Augmentation:** Albumentations.
- **Validación:** Scikit-learn, OpenCV.
- **Entorno de Evaluación:** Docker Image `tytll/isbi-evaluation:latest`.

## Información Oficial del Reto

- **Organizador:** jared2408
- **Contacto:** fuyc.isbi25@gmail.com
- **Plataforma:** CodaBench (Competitions v1.6)



