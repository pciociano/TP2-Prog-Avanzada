<img src="https://universidaddelaciudad.bue.edu.ar/pluginfile.php/1/theme_universidadelaciudad/logo/1756916448/Udelaciudad-logo-preferencial_de%20Bs%20As.png" alt="Logo Udelaciudad" width="300">

# Dashboard de Facturación de Hospitales

**Programación Avanzada en Ciencia de Datos**

Trabajo Práctico - Módulo 2

**Pablo Ciociano**

## Descripción

Este proyecto consiste en un **dashboard interactivo** que permite visualizar la facturación de hospitales públicos en Argentina.  
El dashboard muestra información clave como:

- Importe total aprobado por **provincia**.
- Ranking de los **10 hospitales** con mayor importe aprobado.
- Evolución mensual del importe aprobado.

El objetivo es ofrecer una **herramienta de análisis visual** para tomar decisiones basadas en datos de facturación hospitalaria.

El proyecto se encuentra disponible en la siguiente URL de Git: https://github.com/pciociano/TP2-Prog-Avanzada.

## Dataset Seleccionado

El dataset utilizado en este proyecto corresponde al conjunto de datos públicos denominado  
**“Facturación de hospitales públicos de gestión descentralizada”**, publicado por el  
**Ministerio de Salud de la República Argentina** en el portal oficial [datos.gob.ar](https://datos.gob.ar/dataset/salud-facturacion-hospitales-publicos-gestion-descentralizada).

### Descripción general

Este dataset recopila información sobre la **facturación aprobada por el Ministerio de Salud** a distintos hospitales y centros de salud públicos de gestión descentralizada de todo el país.  
Cada registro representa una transacción o expediente de pago asociado a un hospital, indicando el monto aprobado, la fecha del depósito y la provincia correspondiente.

Facturas pagas por prestaciones brindadas a Beneficiarios de Obras Sociales, del 5/1/2018 al 6/12/2018

Ministerio de Salud. Superintendencia de Servicios de Salud.

[https://datos.gob.ar/dataset/salud-facturacion-hospitales-publicos-gestion-descentralizada](https://datos.gob.ar/dataset/salud-facturacion-hospitales-publicos-gestion-descentralizada/archivo/salud_148185dd-d9ae-4b0c-ae79-4f8e7f0fc2d5)

### Formato y procesamiento

- El dataset fue descargado en formato **CSV** desde el portal.
- Durante el procesamiento, se realizaron tareas de **limpieza, normalización y transformación**:
  - Conversión de fechas al formato `YYYY-MM-DD`.
  - Corrección de valores nulos o mal formados.
  - Generación de un campo derivado `periodo` en formato `AAAAMM` para análisis mensual.
- Finalmente, los datos fueron cargados en una base **SQLite** para facilitar las consultas y análisis mediante SQL y Pandas.

## Motor de Base de Datos

El proyecto utiliza **SQLite** como motor de base de datos relacional.

SQLite es un motor **ligero, embebido y sin servidor**, que permite gestionar datos mediante el lenguaje **SQL** sin requerir una instalación o configuración adicional.  
Su estructura basada en archivos `.db` facilita la portabilidad y reproducibilidad del proyecto, ya que toda la información se almacena en un único archivo dentro del entorno de trabajo.

### Características principales

- **Motor local y autónomo:** no necesita un servidor de base de datos.
- **Compatibilidad total con SQL estándar.**
- **Excelente integración con Python**, a través de los módulos nativos `sqlite3` y `pandas`.
- **Alto rendimiento** para volúmenes medios de datos (ideal para datasets analíticos).

### Implementación en el proyecto

En este proyecto, SQLite se utiliza para:

1. **Crear y estructurar** la base de datos a partir del archivo CSV original (`facturacion.csv`).
2. **Definir y ejecutar consultas SQL** para agrupar, filtrar y consolidar los datos.
3. **Servir como fuente de datos** para los gráficos generados en Python mediante la librería Plotly.

---

## Pasos para ejecutar el dashboard

**1. Clonar el repositorio:**

```bash
git clone https://github.com/pciociano/TP2-Prog-Avanzada.git
```

**2. Abrir la notebook principal:**

   Abrir en Jupyter Notebook o Google Colab
```bash
notebook/TP2_Prog_Avanzada.ipynb
```

**3. Ejecutar todas las celdas:**

- Ejecutar las celdas en orden secuencial
- La notebook descargará automáticamente los datasets
- Procesará y limpiará los datos
- Generará los gráficos interactivos

**4. Visualizar el dashboard:**

- Los gráficos se mostrarán directamente en la notebook
- Se generará automáticamente el archivo HTML del dashboard completo en
  ```bash
  html/dashboard_facturacion.html
  ```
- Abrir el archivo HTML en cualquier navegador web para la visualización interactiva

---

## Funcionalidades del Dashboard

- **Importe por provincia:** gráfico de barras interactivo mostrando el total aprobado por provincia.
- **Ranking de hospitales:** gráfico de barras horizontales con los 10 hospitales que más facturaron.
- **Evolución mensual:** gráfico de línea mostrando la evolución temporal de los importes aprobados.
- **Interactividad:** menús desplegables, hover con información detallada, y posibilidad de filtrar por provincia (si se dispone de la columna).

---
## Estructura del proyecto

```
dashboard_facturacion/
│
├── data/
│   └── facturacion.csv           # Dataset descargado de datos.gob.ar
│
├── database/
│   └── hospitales.db           # Base de datos SQLite
│
├── html/
│   └── dashboard_facturacion.html       # Dashboard final exportado a HTML
│
├── notebook/
│   └── TP2_Prog_Avanzada.ipynb          # Notebook principal
│
└── README.md             
```

---

## Tecnologías y herramientas

- **Python 3.x**
- **Pandas**: manipulación y limpieza de datos
- **SQLite**: almacenamiento de datos estructurados
- **Plotly / Plotly Express**: visualizaciones interactivas
- **HTML + CSS**: presentación del dashboard

---

## Autor

**Pablo Ciociano**  
[Universidad de la Ciudad de Buenos Aires](https://universidaddelaciudad.bue.edu.ar)

---

