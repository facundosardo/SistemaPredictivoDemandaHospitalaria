# 🏥 Modelo Predictivo de Deterioro de Salud en Pacientes Hospitalizados  

**Equipo Nº76 – Vertical Data Science (HealthTech)**  
Proyecto desarrollado en **No Country**  
🎥 **Demo:** [YouTube – Presentación del proyecto](https://www.youtube.com/watch?v=6jqe4DEqTF8)

---

## 🧠 Descripción General  

Este proyecto tiene como objetivo **anticipar la demanda hospitalaria** en los establecimientos de salud de la Provincia de Buenos Aires mediante técnicas de *machine learning*.  

A partir del análisis de datos históricos (2005–2023), el sistema **predice la evolución mensual** de:  
- Consultas médicas  
- Cirugías  
- Urgencias  
- Porcentaje de ocupación hospitalaria  

El modelo busca **mejorar la planificación y gestión hospitalaria**, ayudando a anticipar picos de demanda, optimizar la disponibilidad de camas y personal, y prevenir situaciones de saturación.  

---

## 🎯 Objetivos del Proyecto  

- Analizar tendencias históricas del rendimiento hospitalario.  
- Entrenar modelos predictivos basados en *machine learning* (**XGBoost**, **Prophet**).  
- Desarrollar una **API REST** para exponer las predicciones dinámicamente.  
- Conectar la API con un **dashboard interactivo en Power BI** que visualiza la demanda proyectada (2023–2026).  

---

## ⚙️ Arquitectura del Sistema  

1. **Dataset original:** Ministerio de Salud de la Provincia de Buenos Aires.  
2. **Procesamiento y limpieza:** Python (Pandas / NumPy).  
3. **Entrenamiento de modelos:** XGBoost.  
4. **Proyecciones mensuales:** 2024–2026.  
5. **API Flask:** expone resultados en formato JSON.  
6. **Dashboard Power BI:** visualización interactiva y actualizable.  

---

## 🗂️ Fuente de Datos  

Datos públicos del **Ministerio de Salud de la Provincia de Buenos Aires**, disponibles en el portal de datos abiertos:  
🔗 [Rendimientos de Establecimientos de Salud](https://catalogo.datos.gba.gob.ar/dataset/rendimientos-establecimientos-salud/archivo/8c3130cb-61ad-4014-b829-503b214ba3c0)

El dataset contiene información sobre:  
- Ocupación de camas  
- Consultas médicas  
- Cirugías  
- Urgencias  
- Personal y servicios  
- Variables temporales  

---

## 🧩 Tecnologías Utilizadas  

| Componente              | Tecnología       |
| ----------------------- | ---------------- |
| Lenguaje principal      | Python 3.10      |
| Modelado predictivo     | XGBoost          |
| Procesamiento de datos  | Pandas, NumPy    |
| API REST                | Flask            |
| Visualización           | Power BI         |
| Almacenamiento temporal | CSV / JSON       |

---

## 📈 Modelos Implementados  

| Variable          | Modelo            | R²   | Descripción                           |
| ----------------- | ----------------- | ---- | ------------------------------------- |
| Consultas médicas | XGBoost Regressor | 0.96 | Alta precisión en patrones temporales |
| Cirugías          | XGBoost (log)     | 0.94 | Estacionalidad controlada             |
| Urgencias         | XGBoost           | 0.93 | Buena estabilidad ante variabilidad   |
| Ocupación (%)     | XGBoost           | 0.90 | Ajuste robusto ante valores extremos  |

---

## 🔗 API REST  

**Endpoint principal:** `/predictorio` *(POST)*  
Devuelve la **proyección esperada** para un hospital y mes determinados en formato JSON.  

---

## 📊 Dashboard Power BI  

El dashboard interactivo muestra la **evolución proyectada** y el **estado actual del sistema hospitalario**.  
Se conecta directamente a la API Flask, actualizando las predicciones automáticamente.  

**Secciones principales:**  
- **Visión general:** KPIs de consultas, cirugías, urgencias y ocupación.  
- **Evolución temporal:** análisis de tendencias y estacionalidad (2024–2026).  
- **Detalle por hospital:** nivel de alerta, recomendaciones y confianza del modelo.  

---

## 👥 Equipo de Desarrollo  

**Equipo Nº76 – Vertical Data Science / HealthTech**  
- Ramón Ramírez  
- Gastón Peló  
- Belén Urbaneja  
- Lourdes Núñez  
- Facundo Ariel Sardo  
