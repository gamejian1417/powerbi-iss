# powerbi-iss
Ejercicio Power BI para proceso de selección en ISS


# 📊 Informe Power BI – Evaluación Técnica para ISS

Este repositorio contiene el ejercicio de Power BI desarrollado como parte del proceso de selección para la posición de **Analista de Datos (Power BI / SQL / Python)**.  
El objetivo del proyecto es demostrar competencias en modelado de datos, DAX, visualización, documentación técnica y buenas prácticas end‑to‑end.

---

## 🎯 Objetivo del Informe

El informe permite analizar el impacto de las estrategias del 2026 y evaluar su status y avance respecto al estimado.
El diseño está orientado a facilitar la toma de decisiones mediante una estructura clara: visión general → análisis detallado → documentación técnica.

---

## 🧱 Modelo de Datos

El modelo está construido bajo un **enfoque en estrella (Star Schema)** para asegurar rendimiento y claridad.

### **Estructura:**

- **Tabla de Hechos**
  - Registros operativos (iniciativas).
  - Incluye claves foráneas hacia las dimensiones.
  - Fechas normalizadas para su relación con la tabla calendario.

- **Tablas de Dimensión**
  - `DimFecha` → Tabla calendario marcada como *Date Table*.
  - `Dimidarea
  - `DimResponsable
  - `DimDG

### **Buenas prácticas aplicadas**
- Todas las relaciones son **1 → *many*** en una sola dirección.
- Sin relaciones bidireccionales.
- Columnas innecesarias ocultas para el usuario final.
- Todas las medidas se encuentran en la tabla `_Measures`.
- Tabla calendario generada por DAX para asegurar continuidad temporal.

---

## 📈 Contenido del Informe (Páginas)

### **1. Portada**
Presentación, título, fecha y autora.

### **2. Resumen ejecutivo**
Incluye:
- Métricas principales.
- Evolución temporal.
- Desglose por categorías, dgs.
- Filtros de usuario (slicers).

### **3. Página de Análisis**
- Gantt con drill para ver el detalle de cada iniciativa.
- Gráficos de barras y tendencia.

### **4. Página Técnica**
Incluye:
- Arquitectura del modelo de datos.
- Lógica DAX documentada.
- Transformaciones en Power Query.
- Consideraciones de rendimiento.
- Proceso de validación.
- Captura del modelo.

---

## 🧩 KPIs Principales
---

## 🗂 Estructura del Repositorio
/pbix/        → Archivo Power BI (.pbix)
├─ dataset/   → Archivos utilizados como origen de datos
├─ captures/  → Imágenes ilustrativas del informe
└─ README.md  → Este documento
---

## ▶️ Cómo abrir el informe

1. Descargar el archivo `.pbix`.
2. Abrir con **Power BI Desktop**.
3. Verificar las rutas del dataset si fuera necesario.
4. Refrescar el modelo (*Refresh*).

---

## 👩‍💻 Autora

**Gabriela Giselle Mejía Fernández**  
Sr. Analyst – Data Engineering  

Gracias por revisar este ejercicio.  
Estoy a disposición para ampliar cualquier explicación técnica o funcional.
