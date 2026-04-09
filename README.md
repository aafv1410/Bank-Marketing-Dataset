#  Predicción de Contratación de Depósitos Bancarios

##  Descripción del Proyecto
Este proyecto desarrolla un modelo de Inteligencia Artificial diseñado para **predecir la contratación de un depósito a plazo** por parte de clientes bancarios, basándose en el análisis del dataset `bank.csv`. A diferencia de predecir el monto del depósito, el sistema se enfoca exclusivamente en la probabilidad de que la acción de contratación ocurra.

El sistema se implementa bajo una **Arquitectura de Datos Híbrida (Pipeline)**, lo que permite un flujo automatizado y controlado desde la ingesta de datos brutos hasta la generación de predicciones.

---

##  Componentes y Herramientas (Stack Tecnológico)
Se ha seleccionado un stack moderno para garantizar la portabilidad, seguridad y escalabilidad del sistema:

| Categoría | Herramienta | Justificación Técnica |
| :--- | :--- | :--- |
| **Lenguaje** | **Python** | Ideal para procesamiento de datos y modelos de IA por su legibilidad y ecosistema. |
| **IDE** | **VS Code** | Entorno estándar para desarrollo eficiente con extensiones profesionales. |
| **Contenedores** | **Docker** | Garantiza que el pipeline funcione exactamente igual en cualquier computador. |
| **Base de Datos** | **MongoDB** | Almacenamiento NoSQL flexible para los datos procesados del pipeline. |
| **Automatización** | **GitHub Actions** | Ejecuta flujos de CI/CD (pruebas y despliegues) de forma automática. |
| **Cloud** | **Render** | Plataforma PaaS para desplegar la aplicación de forma sencilla. |

---

##  Arquitectura del Sistema
El proyecto sigue una arquitectura de pipeline que garantiza la interoperabilidad:
1. *Ingesta:** Captura de datos desde `bank.csv`.
2. **Procesamiento:** Limpieza y transformación de datos usando Python dentro de Docker.
3. **Almacenamiento:** Carga de datos limpios en **MongoDB**.
4. **Modelado:** Entrenamiento y evaluación de la IA para la predicción de contratación.

###  Límites del Proyecto
* El proyecto no contempla la predicción del monto del depósito, solo si se contrata o no.
* No contempla integración con sistemas bancarios reales en producción.

---

## Planificación e Hitos (2026)

El proyecto se rige por el siguiente cronograma basado en la metodología PMBOK:



 **Hito 1: Entrega de Planificación** (26 de marzo - 5 de abril).

  **Hito 2: Entrega de Diseño Técnico** (6 de abril - 19 de abril).

 **Hito 3: Pipeline Ejecutado e IA entrenada** (20 de abril - 9 de junio).

  **Hito 4: Entrega Final Completa** (13 de junio - 30 de junio).



---
##  Equipo 

* **Integrantes:**

    * NICOLAS CASANOVA PEREZ.
    * AGUSTIN FERNANDEZ VASQUEZ.
    * JUANJOSE MARCOS MARDONES MORAGA.
      
##  Estructura del Repositorio
```text
├── .github/workflows/   # Automatización con GitHub Actions
├── data/                # Archivo original (bank.csv)
├── docs/                # Planificación y Diseño técnico
├── src/                 # Código fuente (Scripts de Python)
│   ├── ingesta.py       # Carga de datos
│   ├── limpieza.py      # Transformación y limpieza
│   └── modelo.py        # Entrenamiento de la IA
├── Dockerfile           # Configuración de imagen Docker
├── docker-compose.yml   # Orquestación (App + MongoDB)
└── README.md            # Guía del proyecto
---
