 Descripción del ProyectoEste proyecto desarrolla un modelo de Inteligencia Artificial diseñado para predecir la contratación de un depósito a plazo por parte de clientes bancarios, basándose en el análisis del dataset bank.csv. A diferencia de predecir el monto, el sistema se enfoca exclusivamente en la probabilidad de que la acción de contratación ocurra.El sistema se implementa bajo una Arquitectura de Datos Híbrida (Pipeline), lo que permite un flujo automatizado desde la ingesta de datos hasta la generación de predicciones.
 Componentes y Herramientas (Stack Tecnológico)Se ha seleccionado un stack moderno para garantizar la portabilidad y escalabilidad del sistema:CategoríaHerramientaJustificaciónLenguajePythonIdeal para procesamiento de datos y modelos de IA por su legibilidad.IDEVS CodeEntorno estándar para desarrollo eficiente con extensiones de Python.ContenedoresDockerAsegura que el pipeline funcione igual en cualquier computador.Base de DatosMongoDBAlmacenamiento flexible de documentos para los datos procesados.AutomatizaciónGitHub ActionsEjecuta pruebas y despliegues automáticos (CI/CD).CloudRenderPlataforma para desplegar la aplicación de forma sencilla.
 Arquitectura del Sistema
El proyecto sigue una arquitectura de pipeline que garantiza la interoperabilidad y seguridad:
Ingesta: Captura de datos desde bank.csv.
Procesamiento: Limpieza y transformación de datos usando Python dentro de Docker.
Almacenamiento: Carga de datos limpios en MongoDB.
Modelado: Entrenamiento y evaluación de la IA para la predicción de contratación.
├── .github/workflows/   # Automatización con GitHub Actions
├── data/                # Archivos CSV originales (bank.csv)
├── docs/                # Documentación técnica y planificación
├── src/                 # Código fuente (Scripts de Python)
│   ├── ingesta.py       # Conexión y carga inicial
│   ├── limpieza.py      # Transformación de datos
│   └── modelo.py        # Entrenamiento de la IA
├── Dockerfile           # Configuración de imagen Docker
├── docker-compose.yml   # Orquestación de servicios (App + MongoDB)
└── README.md            # Guía del proyecto
Instrucciones de Ejecución
Sigue estos pasos para configurar el entorno local:
Clonar el repositorio:
git clone https://github.com/usuario/proyecto-depositos.git
cd proyecto-depositos
Levantar el entorno con Docker:
Este comando instalará las dependencias y configurará la base de datos automáticamente:
docker-compose up --build
Ejecución de Scripts:
El pipeline se inicia automáticamente con el contenedor, pero puedes ejecutar procesos específicos:
python src/ingesta.py
Planificación e Hitos (2026)El proyecto se rige por el siguiente cronograma basado en la metodología PMBOK:
Hito 1: Entrega de Planificación (3 de marzo - 5 de abril) 
Hito 2: Diseño Técnico y README inicial (6 de abril - 19 de abril) 
Hito 3: Pipeline Ejecutado (IA entrenada) (20 de abril - 9 de junio) 
Hito 4: Entrega Final Completa (13 de junio - 30 de junio) 
Equipo y Documentación

Integrantes:
AGUSTIN FERNANDEZ VASQUEZ
NICOLAS CASANOVA PEREZ
JUANJOSE MARCOS MARDONES MORAGA
