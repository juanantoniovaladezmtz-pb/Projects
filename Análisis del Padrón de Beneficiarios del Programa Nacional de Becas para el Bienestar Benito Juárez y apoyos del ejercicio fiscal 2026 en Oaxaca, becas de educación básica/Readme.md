# Padrón de Becas de Educación Básica — Oaxaca 2026

## Distribución territorial y composición de los registros del padrón

Análisis exploratorio desarrollado en **Power BI** sobre los registros del Padrón de Beneficiarios del Programa Nacional de Becas para el Bienestar Benito Juárez y apoyos correspondientes al ejercicio fiscal 2026 para educación básica en el estado de Oaxaca.

El proyecto busca comprender la dimensión del padrón, la composición de los registros según el monto de beca y su distribución territorial a nivel municipal y local.

---

## 📊 Dashboard

<img width="1137" height="637" alt="image" src="https://github.com/user-attachments/assets/4290d92a-5ab8-47d2-9ebc-e6337f6cdec5" />


> **Herramienta:** Microsoft Power BI  
> **Periodo analizado:** 2.º trimestre · Ejercicio fiscal 2026  
> **Entidad:** Oaxaca, México

---

## 🎯 Objetivo

Analizar la distribución de los registros y montos de beca contenidos en el padrón de educación básica de Oaxaca, identificando patrones relacionados con:

- La dimensión general del padrón.
- Los registros con y sin monto de beca.
- La distribución de los diferentes montos registrados.
- La concentración territorial de los montos.
- La distribución de los registros entre municipios.
- El alcance territorial a través de las localidades.
- La antigüedad de los registros que integran el padrón.

El propósito principal es transformar un conjunto de datos de gran volumen en información visual que facilite su interpretación.

---

# 🔎 Pregunta principal

> **¿Cómo se distribuyen territorialmente los registros y montos de beca del padrón de educación básica en Oaxaca?**

A partir de esta pregunta se plantearon las siguientes preguntas de análisis.

### 1. Dimensión del padrón

**¿Cuál es la magnitud del padrón analizado?**

Se busca conocer el volumen total de registros y su alcance territorial.

### 2. Composición de los apoyos

**¿Qué montos de beca concentran la mayor cantidad de registros?**

Esta pregunta permite identificar si los registros se encuentran distribuidos entre diferentes niveles de apoyo o si existe una concentración importante en determinados montos.

### 3. Distribución territorial

**¿Cómo se distribuye el monto acumulado entre los municipios de Oaxaca?**

El análisis territorial permite identificar los municipios que concentran los mayores montos registrados.

### 4. Concentración

**¿Qué proporción del monto acumulado se concentra en los municipios con mayor participación?**

Esta perspectiva permite distinguir entre una distribución ampliamente dispersa y una distribución concentrada en un grupo reducido de municipios.

### 5. Alcance territorial

**¿Existe una relación entre el monto acumulado y la cantidad de localidades asociadas a cada municipio?**

La pregunta busca observar si un mayor monto registrado necesariamente implica una mayor extensión territorial.

### 6. Antigüedad de los registros

**¿Qué antigüedad presentan los registros que conforman el padrón?**

La variable `fecha_alta` permite observar la composición temporal de los registros incluidos en el conjunto de datos.

---

# 📌 Indicadores principales

| Indicador | Resultado |
|---|---:|
| Registros del padrón | **811,031** |
| Registros con monto positivo | **353,796** |
| Registros con monto igual a $0 | **457,235** |
| Monto acumulado registrado | **$2,146,573,900** |
| Registros con monto positivo | **43.62%** |
| Municipios identificados | **568** |
| Localidades identificadas | **3,586** |

---

# 📈 Principales hallazgos

## 1. El padrón presenta una escala considerable

El conjunto analizado contiene **811,031 registros**, con presencia territorial en cientos de municipios y miles de localidades de Oaxaca.

Esto proporciona una visión de gran escala sobre la composición territorial del padrón.

---

## 2. Menos de la mitad de los registros presentan un monto positivo

De los 811,031 registros analizados:

- **353,796** presentan un monto de beca mayor a cero.
- **457,235** presentan un valor de `beca = 0`.

Los registros con monto positivo representan aproximadamente **43.62%** del total.

> En este análisis, los registros con `beca = 0` se consideran registros sin monto registrado. No se interpretan automáticamente como personas que no recibieron el apoyo.

---

## 3. Los montos de $5,700 y $7,800 concentran la mayoría de los registros con apoyo

La distribución de los registros con monto positivo muestra una concentración particularmente marcada:

| Monto de beca | Registros | Participación |
|---:|---:|---:|
| $5,700 | 295,127 | 83.42% |
| $7,800 | 54,510 | 15.41% |
| $9,900 | 3,459 | 0.98% |
| $7,100 | 408 | 0.12% |
| Otros montos | 292 | 0.08% |

En conjunto, los montos de **$5,700 y $7,800 representan aproximadamente el 98.83% de los registros con monto positivo**.

Este comportamiento constituye uno de los principales patrones identificados durante el análisis.

---

## 4. Oaxaca de Juárez concentra el mayor monto acumulado

Los municipios con mayores montos acumulados registrados son:

| Municipio | Monto acumulado |
|---|---:|
| Oaxaca de Juárez | $70.94 M |
| Juchitán de Zaragoza | $63.86 M |
| San Juan Bautista Tuxtepec | $59.02 M |
| Santiago Pinotepa Nacional | $32.76 M |
| Heroica Ciudad de Huajuapan de León | $32.30 M |

Los diez municipios con mayor monto acumulado representan aproximadamente **18.67% del monto total registrado**.

---

## 5. La concentración territorial aumenta conforme se amplía el grupo de municipios

La participación acumulada del monto muestra el siguiente comportamiento:

| Grupo de municipios | Participación acumulada |
|---|---:|
| Top 10 | 18.67% |
| Top 20 | 29.87% |
| Top 50 | 49.51% |
| Top 100 | 65.92% |

Este resultado permite observar que el monto no se concentra exclusivamente en unos cuantos municipios, sino que se distribuye entre un número amplio de unidades territoriales.

---

## 6. El monto acumulado y la amplitud territorial representan dimensiones diferentes

La cantidad de localidades asociadas a un municipio presenta diferencias importantes.

Por ejemplo:

- **San Juan Bautista Tuxtepec:** 86 localidades.
- **Santiago Juxtlahuaca:** 61 localidades.
- **Acatlán de Pérez Figueroa:** 54 localidades.
- **Villa de Tututepec:** 48 localidades.
- **Oaxaca de Juárez:** 3 localidades.

Esto muestra que un municipio con un monto acumulado elevado no necesariamente presenta la misma amplitud territorial en términos de localidades.

---

# 🗺️ Dashboard

El dashboard fue diseñado para presentar el análisis de forma progresiva, comenzando con una visión general y profundizando posteriormente en la composición y distribución territorial.

### Componentes principales

#### Indicadores KPI

Permiten conocer rápidamente:

- Total de registros.
- Registros con beca.
- Registros sin monto.
- Monto acumulado.
- Porcentaje de registros con monto.
- Municipios identificados.

#### Distribución de montos

Gráfico de barras que muestra la cantidad de registros asociados a cada monto de beca.

#### Mapa territorial

Visualización geográfica de Oaxaca que permite observar la distribución municipal del padrón y explorar las diferencias territoriales.

#### Ranking municipal

Permite identificar los municipios con mayor participación dentro del padrón.

#### Localidades

Permite comparar la cantidad de localidades asociadas a los municipios.

#### Antigüedad del registro

Control temporal basado en `fecha_alta`, utilizado para explorar la composición temporal de los registros.

---

