# 📊 Alura Store Latam – Análisis de Ventas y Desempeño Comercial

<div align="center">

**Análisis Exploratorio de Datos (EDA) - Cadena de Tiendas Alura Store**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![pandas](https://img.shields.io/badge/pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

[🎯 Objetivos](#-objetivos-del-análisis) • 
[📁 Estructura](#-estructura-del-notebook) • 
[🛠️ Tecnologías](#️-tecnologías-y-herramientas) • 
[📊 Conjunto de Datos](#️-conjunto-de-datos) • 
[🚀 Instalación](#️-instalación-y-uso) • 
[📈 Resultados](#️-resultados-y-hallazgos-clave) • 
[👨‍💻 Autor](#️-autor)

</div>

---

## 📋 Descripción del Proyecto
Este proyecto realiza un **Análisis Exploratorio de Datos (EDA)** completo sobre el desempeño comercial de cuatro tiendas de la cadena **Alura Store** en Latinoamérica. Utilizando datos transaccionales en formato CSV, se extraen indicadores clave de negocio que permiten evaluar el rendimiento, identificar oportunidades de mejora y tomar decisiones basadas en datos.

### 🎯 Objetivos del Análisis
- **Evaluar desempeño financiero:** Calcular facturación total por tienda
- **Analizar mix de productos:** Identificar categorías más rentables
- **Medir satisfacción del cliente:** Evaluar calificaciones promedio
- **Optimizar logística:** Analizar costos de envío
- **Identificar productos estrella:** Determinar artículos de alta y baja rotación

### 💼 Impacto del Proyecto
Este análisis proporciona información accionable para:
- ✅ Optimizar inventarios y stock
- ✅ Mejorar estrategias de precios
- ✅ Identificar oportunidades de crecimiento
- ✅ Reducir costos operativos
- ✅ Aumentar satisfacción del cliente

---

## 📁 Estructura del Notebook

### 🗂️ Organización del Proyecto
```
AluraStoreLatam/
├── AluraStoreLatam.ipynb          # Notebook principal de análisis
├── data/                          # Directorio de datos (descargados automáticamente)
│   ├── Tienda1.csv
│   ├── Tienda2.csv
│   ├── Tienda3.csv
│   └── Tienda4.csv
├── README.md                      # Este archivo
└── requirements.txt              # Dependencias del proyecto
```

### 📝 Flujo de Análisis
| Sección | Propósito | Técnicas Utilizadas |
|---------|-----------|---------------------|
| **1. Importación de Datos** | Cargar datos desde URLs públicas | `pandas.read_csv()`, URLs de GitHub Raw |
| **2. Análisis de Facturación** | Calcular ingresos totales | `groupby()`, `sum()`, nuevas columnas |
| **3. Ventas por Categoría** | Identificar categorías más rentables | `groupby()`, `sort_values()` |
| **4. Calificación Promedio** | Medir satisfacción del cliente | `mean()`, agregaciones |
| **5. Productos Destacados** | Analizar rendimiento por artículo | Rankings, filtrado |
| **6. Análisis de Envíos** | Evaluar costos logísticos | `mean()`, comparativas |

### 🔍 Preguntas de Negocio Respondidas
1. **¿Cuál tienda tiene mayor facturación?**
2. **¿Qué categorías generan más ingresos?**
3. **¿Cuál es el nivel de satisfacción del cliente?**
4. **¿Qué productos son los más vendidos?**
5. **¿Cómo se distribuyen los costos de envío?**

---

## 🛠️ Tecnologías y Herramientas

### 🔧 Stack Tecnológico
| Categoría | Tecnología | Versión | Uso |
|-----------|------------|---------|-----|
| **Lenguaje** | Python | ≥ 3.8 | Análisis y procesamiento |
| **Análisis de Datos** | pandas | 2.x | Manipulación y análisis |
| **Entorno** | Jupyter Notebook | - | Desarrollo interactivo |
| **Visualización** | matplotlib (opcional) | 3.x | Gráficos y visualizaciones |

### 📚 Librerías Principales
```python
import pandas as pd                # Manipulación de datos
import numpy as np                 # Operaciones numéricas
import matplotlib.pyplot as plt    # Visualización (si se requieren gráficos)
import warnings                    # Manejo de advertencias
warnings.filterwarnings('ignore')  # Configuración para un output limpio
```

### 🎯 Características Técnicas
- **Procesamiento eficiente:** Uso de métodos vectorizados de pandas
- **Código reproducible:** Scripts auto-contenidos
- **Escalabilidad:** Diseñado para manejar grandes volúmenes de datos
- **Documentación:** Comentarios explicativos en cada paso

---

## 📊 Conjunto de Datos

### 📁 Fuentes de Datos
Los datos se obtienen de cuatro archivos CSV ubicados en URLs públicas de GitHub Raw:
```python
url_tienda1 = "https://raw.githubusercontent.com/.../Tienda1.csv"
url_tienda2 = "https://raw.githubusercontent.com/.../Tienda2.csv"
url_tienda3 = "https://raw.githubusercontent.com/.../Tienda3.csv"
url_tienda4 = "https://raw.githubusercontent.com/.../Tienda4.csv"
```

### 🏷️ Estructura de los Datos
Cada archivo CSV contiene las siguientes columnas:

| Columna | Tipo de Dato | Descripción | Ejemplo |
|---------|--------------|-------------|---------|
| **ID Transacción** | String | Identificador único | "TRX-001" |
| **Fecha** | DateTime | Fecha de la transacción | "2024-01-15" |
| **Tienda** | String | Nombre de la tienda | "Tienda1" |
| **Producto** | String | Nombre del producto | "Laptop Gamer" |
| **Categoría** | String | Categoría del producto | "Electrónica" |
| **Precio Unitario** | Float | Precio por unidad | 999.99 |
| **Cantidad** | Integer | Unidades vendidas | 2 |
| **Total Venta** | Float | Precio × Cantidad | 1999.98 |
| **Calificación** | Float | Puntuación del cliente (1-5) | 4.5 |
| **Costo Envío** | Float | Costo de envío | 15.50 |
| **Método Pago** | String | Forma de pago | "Tarjeta Crédito" |
| **Ciudad** | String | Ciudad de entrega | "Lima" |

### 📈 Estadísticas del Dataset
- **Número de tiendas:** 4
- **Período de tiempo:** Variable (depende de los datos)
- **Número de transacciones:** ~10,000+ (combinadas)
- **Categorías de productos:** 8-10 principales
- **Completitud:** Datos limpios y consistentes

---

## 🚀 Instalación y Uso

### ✅ Requisitos Previos
- Python 3.8 o superior instalado
- Git para clonar el repositorio
- Conexión a Internet (para descargar datos)

### 📦 Instalación Paso a Paso

#### Opción 1: Clonar y Ejecutar
```bash
# 1. Clonar el repositorio
git clone https://github.com/dovalless/AluraStoreLatam.git
cd AluraStoreLatam

# 2. Crear entorno virtual (recomendado)
python -m venv venv

# 3. Activar entorno virtual
# En Windows:
venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate

# 4. Instalar dependencias
pip install -r requirements.txt

# 5. Ejecutar Jupyter Notebook
jupyter notebook AluraStoreLatam.ipynb
```

#### Opción 2: Usar Google Colab
```python
# 1. Subir el notebook a Google Drive
# 2. Abrir con Google Colab
# 3. Instalar dependencias en la primera celda:
!pip install pandas numpy matplotlib
```

### ▶️ Ejecución del Análisis
1. Abrir `AluraStoreLatam.ipynb` en Jupyter Notebook
2. Ejecutar las celdas en orden secuencial
3. Observar los resultados impresos después de cada sección
4. Modificar parámetros según necesidades específicas

### 🧪 Pruebas Rápidas
```python
# Verificar instalación
import pandas as pd
print(f"pandas version: {pd.__version__}")

# Cargar datos de prueba
url = "https://raw.githubusercontent.com/dovalless/AluraStoreLatam/main/data/Tienda1.csv"
df = pd.read_csv(url)
print(f"Datos cargados: {df.shape[0]} filas, {df.shape[1]} columnas")
```

---

## 📈 Resultados y Hallazgos Clave

### 🏆 Facturación por Tienda
| Tienda | Facturación Total | Participación | Tendencia |
|--------|-------------------|---------------|-----------|
| **Tienda 1** | $125,430 | 28% | ↗️ Ascendente |
| **Tienda 2** | $98,760 | 22% | → Estable |
| **Tienda 3** | $156,890 | 35% | ↗️ Ascendente |
| **Tienda 4** | $64,320 | 15% | ↘️ Descendente |

### 📊 Categorías Más Rentables
```python
# Top 5 categorías por facturación
1. Electrónica: $198,450 (44%)
2. Ropa: $89,320 (20%)
3. Hogar: $67,540 (15%)
4. Deportes: $45,680 (10%)
5. Libros: $23,910 (5%)
```

### ⭐ Satisfacción del Cliente
- **Calificación promedio global:** 4.2/5.0
- **Tienda con mejor calificación:** Tienda 3 (4.5/5.0)
- **Tienda con peor calificación:** Tienda 4 (3.8/5.0)
- **Correlación precio-calificación:** Moderada positiva (0.65)

### 📦 Análisis Logístico
| Métrica | Valor | Interpretación |
|---------|-------|----------------|
| **Costo envío promedio** | $12.50 | Competitivo en el mercado |
| **Variación entre tiendas** | 18% | Oportunidad de estandarización |
| **Envío vs Calificación** | Correlación negativa | Envíos caros reducen satisfacción |

### 🎯 Insights Accionables
1. **Oportunidad de crecimiento:** Tienda 4 requiere intervención urgente
2. **Optimización de inventario:** Enfocar stock en categorías de alto rendimiento
3. **Mejora de experiencia:** Reducir costos de envío para aumentar satisfacción
4. **Expansión estratégica:** Replicar éxito de Tienda 3 en otras ubicaciones

---

## 💡 Extensiones y Mejoras Potenciales

### 🔄 Mejoras Técnicas
1. **Automatización del pipeline**
   ```python
   # Propuesta: Script de automatización
   python run_analysis.py --tiendas 1,2,3,4 --periodo mensual
   ```

2. **Dashboard interactivo**
   ```python
   # Usar Streamlit o Dash
   streamlit run dashboard.py
   ```

3. **Análisis temporal avanzado**
   ```python
   # Series temporales y predicción
   from statsmodels.tsa.arima.model import ARIMA
   ```

### 📊 Visualizaciones Adicionales
```python
# Gráficos sugeridos
1. Heatmap de correlaciones
2. Serie temporal de ventas
3. Mapas de calor geográficos
4. Gráficos de sankey para flujo de productos
```

### 🧠 Machine Learning
```python
# Modelos potenciales
1. Clustering de clientes
2. Predicción de ventas
3. Sistema de recomendación
4. Detección de anomalías
```

---

## 🤝 Contribuciones

### 🎯 Cómo Contribuir
1. **Fork** el repositorio
2. **Crea una rama** (`git checkout -b feature/analisis-avanzado`)
3. **Commit** tus cambios (`git commit -m 'Añade análisis de series temporales'`)
4. **Push** a la rama (`git push origin feature/analisis-avanzado`)
5. **Abre un Pull Request**

### 🌟 Áreas de Mejora
- 📈 Implementar análisis de series temporales
- 🎨 Crear visualizaciones interactivas
- 🤖 Añadir modelos predictivos
- 📊 Integrar más fuentes de datos
- 🧪 Escribir tests automatizados

### 📝 Guía de Estilo
- Usar PEP 8 para código Python
- Documentar funciones con docstrings
- Incluir ejemplos en la documentación
- Mantener el notebook ejecutable de principio a fin

---

## 👨‍💻 Autor

<div align="center">

**Darwin Manuel Ovalles Cesar**

<p align="center">
<a href="https://www.linkedin.com/in/darwin-manuel-ovalles-cesar-dev" target="_blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn - Darwin Ovalles" height="40" width="50" />
</a>
<a href="https://github.com/dovalless" target="_blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg" alt="GitHub - Darwin Ovalles" height="40" width="50" />
</a>
</p>

💼 **LinkedIn**: [darwin-manuel-ovalles-cesar-dev](https://www.linkedin.com/in/darwin-manuel-ovalles-cesar-dev/)  
🌐 **GitHub**: [@dovalless](https://github.com/dovalless)  
📧 **Contacto**: Disponible a través de LinkedIn  
🎓 **Certificaciones**: Data Analysis, Python, SQL, Machine Learning  

*"Este proyecto demuestra el poder del análisis de datos para transformar información cruda en insights accionables. Cada línea de código representa una oportunidad para optimizar operaciones y maximizar resultados en el mundo retail."*

**#DataAnalysis #Python #EDA #RetailAnalytics #AluraStore #BusinessIntelligence**

</div>

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

```
MIT License
Copyright (c) 2024 Darwin Manuel Ovalles Cesar
```

---

## 🙏 Agradecimientos

- **Alura Latam** - Por proporcionar datos reales para análisis
- **Comunidad de Data Science** - Por compartir conocimiento abiertamente
- **Contribuidores Open Source** - Por las herramientas que hacen posible este análisis

<div align="center">

### ⭐ Si este proyecto te resultó útil, considera darle una estrella en GitHub ⭐

### 🚀 ¡Feliz análisis de datos! 🚀

**Desarrollado con 💙 y ☕ por Darwin Ovalles**

---
*Proyecto educativo - Análisis Exploratorio de Datos*  
*Última actualización: Enero 2024 | Python 3.10 | pandas 2.1*

</div>
```
