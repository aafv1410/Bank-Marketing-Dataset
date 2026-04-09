# 🚀 Predicción de Contratación de Depósitos Bancarios

## 📋 Descripción del Proyecto
[cite_start]Este proyecto desarrolla un modelo de Inteligencia Artificial diseñado para **predecir la contratación de un depósito a plazo** por parte de clientes bancarios, basándose en el análisis del dataset `bank.csv`[cite: 3]. [cite_start]A diferencia de predecir el monto del depósito, el sistema se enfoca exclusivamente en la probabilidad de que la acción de contratación ocurra[cite: 7].

[cite_start]El sistema se implementa bajo una **Arquitectura de Datos Híbrida (Pipeline)**, lo que permite un flujo automatizado y controlado desde la ingesta de datos brutos hasta la generación de predicciones[cite: 55].

---

## ⚙️ Componentes y Herramientas (Stack Tecnológico)
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

## 🏗️ Arquitectura del Sistema
El proyecto sigue una arquitectura de pipeline que garantiza la interoperabilidad:
1. [cite_start]**Ingesta:** Captura de datos desde `bank.csv`[cite: 55].
2. [cite_start]**Procesamiento:** Limpieza y transformación de datos usando Python dentro de Docker[cite: 8].
3. [cite_start]**Almacenamiento:** Carga de datos limpios en **MongoDB**[cite: 55].
4. [cite_start]**Modelado:** Entrenamiento y evaluación de la IA para la predicción de contratación[cite: 33, 34].

### 🚫 Límites del Proyecto
* [cite_start]El proyecto no contempla la predicción del monto del depósito, solo si se contrata o no[cite: 9].
* [cite_start]No contempla integración con sistemas bancarios reales en producción[cite: 9].

---

## 📁 Estructura del Repositorio
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

