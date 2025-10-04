<img src="https://universidaddelaciudad.bue.edu.ar/pluginfile.php/1/theme_universidadelaciudad/logo/1756916448/Udelaciudad-logo-preferencial_de%20Bs%20As.png" alt="Logo Udelaciudad" width="300">

# Dashboard de Facturación de Hospitales

**Programación Avanzada en Ciencia de Datos**

**Pablo Ciociano**

## Descripción

Este proyecto consiste en un **dashboard interactivo** que permite visualizar la facturación de hospitales públicos en Argentina.  
El dashboard muestra información clave como:

- Importe total aprobado por **provincia**.
- Ranking de los **10 hospitales** con mayor importe aprobado.
- Evolución mensual del importe aprobado.

El objetivo es ofrecer una **herramienta de análisis visual** para tomar decisiones basadas en datos de facturación hospitalaria.

## Dataset Seleccionado

Facturación de Hospitales Públicos de Gestión descentralizada

Facturas pagas por prestaciones brindadas a Beneficiarios de Obras Sociales, del 5/1/2018 al 6/12/2018

Ministerio de Salud. Superintendencia de Servicios de Salud.

[https://datos.gob.ar/dataset/salud-facturacion-hospitales-publicos-gestion-descentralizada](https://datos.gob.ar/dataset/salud-facturacion-hospitales-publicos-gestion-descentralizada/archivo/salud_148185dd-d9ae-4b0c-ae79-4f8e7f0fc2d5)

## Motor de base de datos 

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

## Ejecución

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
- Se generará automáticamente el archivo HTML del dashboard completo en html/dashboard_facturacion.html
- Abrir el archivo HTML en cualquier navegador web para la visualización interactiva

---

## Funcionalidades del Dashboard

- **Importe por provincia:** gráfico de barras interactivo mostrando el total aprobado por provincia.
- **Ranking de hospitales:** gráfico de barras horizontales con los 10 hospitales que más facturaron.
- **Evolución mensual:** gráfico de línea mostrando la evolución temporal de los importes aprobados.
- **Interactividad:** menús desplegables, hover con información detallada, y posibilidad de filtrar por provincia (si se dispone de la columna).

---

## Autor

**Pablo Ciociano**  
[Universidad de la Ciudad de Buenos Aires](https://universidaddelaciudad.bue.edu.ar)

---

