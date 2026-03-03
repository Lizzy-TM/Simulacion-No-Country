# 📊 DATAMARK - Plataforma de Automatización de Ventas e Inventarios

## 🚀 Descripción del Proyecto

**DATAMARK** es una solución SaaS B2B en etapa MVP diseñada para
pequeños negocios de ropa y calzado en provincias del Perú.

El objetivo es **automatizar la gestión de ventas, inventarios y
clientes**, centralizando datos que normalmente se manejan en Excel o de
forma manual, y transformarlos en dashboards claros para la toma de
decisiones.

------------------------------------------------------------------------

# 🎯 Problema que Resuelve

Muchos pequeños negocios:

-   Gestionan ventas en Excel
-   No controlan correctamente inventarios
-   No tienen métricas claras
-   Cometen errores manuales
-   Toman decisiones sin datos estructurados

DATAMARK busca:

✔ Centralizar datos\
✔ Automatizar limpieza y transformación\
✔ Visualizar KPIs en dashboards\
✔ Reducir errores operativos

------------------------------------------------------------------------

# 🏗 Arquitectura del Proyecto

El flujo actual del sistema sigue una arquitectura tipo Data Pipeline:

    Ingreso Manual / Excel
            ↓
    Schema RAW (Datos crudos)
            ↓
    Schema STAGING (Limpieza y validación)
            ↓
    Schema WAREHOUSE (Modelo final optimizado)
            ↓
    Dashboard

------------------------------------------------------------------------

# 🗂 Estructura del Proyecto

    Dashboard-Ventas/
    │
    ├── etl.py                # Script principal de transformación de datos
    ├── requirements.txt      # Dependencias del proyecto
    ├── data/
    │   └── ventas.csv        # Archivo de ejemplo de datos
    │
    ├── sql/
    │   ├── create_schemas.sql
    │   ├── raw_tables.sql
    │   ├── staging_tables.sql
    │   └── warehouse_tables.sql
    │
    ├── .github/
    │   └── workflows/
    │       └── ci.yml        # Configuración de GitHub Actions (CI)
    │
    └── README.md

------------------------------------------------------------------------

# 🛠 Tecnologías Utilizadas

### Backend / ETL

-   Python
-   Pandas
-   SQLAlchemy
-   PostgreSQL

### Base de Datos

-   PostgreSQL
-   DBeaver (gestión visual)

### Control de Versiones

-   Git
-   GitHub

### Automatización

-   GitHub Actions (CI/CD)

------------------------------------------------------------------------

# 🔄 Flujo ETL Implementado

El proceso ETL actual realiza:

### 1️⃣ Extract

-   Lectura de archivos CSV creados por el usuario.

### 2️⃣ Load (RAW)

-   Inserción directa al schema `raw`.

### 3️⃣ Transform (STAGING)

-   Limpieza de:
    -   Valores nulos
    -   Tipos de datos
    -   Registros inconsistentes

### 4️⃣ Load Final (WAREHOUSE)

-   Inserción en tablas optimizadas para análisis.

------------------------------------------------------------------------

# 📊 Estado Actual del Proyecto

✔ Conexión exitosa a PostgreSQL\
✔ Creación de schemas: raw, staging, warehouse\
✔ Inserción de datos desde CSV\
✔ Script ETL funcional\
✔ Visualización de cambios en DBeaver\
✔ Repositorio conectado a GitHub\
✔ Pipeline básico de integración continua

------------------------------------------------------------------------

# ▶️ Cómo Ejecutar el Proyecto

## 1️⃣ Clonar repositorio

``` bash
git clone https://github.com/TU-USUARIO/TU-REPO.git
cd Dashboard-Ventas
```

## 2️⃣ Crear entorno virtual

``` bash
python -m venv venv
venv\Scripts\activate   # Windows
```

## 3️⃣ Instalar dependencias

``` bash
pip install -r requirements.txt
```

## 4️⃣ Ejecutar ETL

``` bash
python etl.py
```

------------------------------------------------------------------------

# 🔐 Variables de Entorno

Se recomienda usar un archivo `.env` con:

    DB_HOST=
    DB_PORT=
    DB_NAME=
    DB_USER=
    DB_PASSWORD=

------------------------------------------------------------------------

# 🧪 Próximos Pasos

-   Integración con frontend (Streamlit o React)
-   Automatización completa desde botón "Ver Dashboard"
-   Implementación de pruebas automatizadas
-   Despliegue en la nube
-   Autenticación de usuarios

------------------------------------------------------------------------

# 📈 Impacto Esperado

-   Reducción de errores manuales
-   Mayor control de inventarios
-   Visualización clara de ventas
-   Mejores decisiones comerciales

------------------------------------------------------------------------

# 👩‍💻 Autora

Proyecto desarrollado como parte de un desafío técnico enfocado en
automatización y análisis de datos para pequeñas empresas.
