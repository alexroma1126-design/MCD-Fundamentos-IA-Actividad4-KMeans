# Actividad 4 — Segmentación de clientes con K-Means

**Universidad:** Yachay Tech
**Programa:** Maestría en Ciencia de Datos
**Asignatura:** Fundamentos de Inteligencia Artificial
**Periodo:** IISEM2026
**Docente:** Manuel Eugenio Morocho Cayamcela
**Estudiante:** Héctor Alexander Román Potosí

## 1. Descripción del proyecto

Este proyecto implementa el algoritmo de aprendizaje no supervisado
K-Means para segmentar clientes de un centro comercial según sus
ingresos anuales y su comportamiento de gasto.

Se desarrolla la Opción 1 de la Actividad 4, utilizando el conjunto
de datos Mall Customers y el notebook proporcionado en clase.

## 2. Objetivos

- Explorar y comprender las características de los datos.
- Implementar el algoritmo de agrupamiento K-Means.
- Seleccionar el número de grupos mediante el método del codo.
- Evaluar los agrupamientos mediante el índice de silueta.
- Interpretar los perfiles de los clientes.
- Proponer una estrategia comercial fundamentada.
- Predecir el segmento de nuevos clientes.

## 3. Base de datos

El archivo mall_customers.csv contiene 200 observaciones y cinco
variables originales:

| Variable | Descripción |
|---|---|
| CustomerID | Identificador único del cliente |
| Gender | Género |
| Age | Edad |
| Annual Income (k$) | Ingreso anual en miles de dólares |
| Spending Score (1-100) | Puntuación de gasto |

Para el agrupamiento se utilizan exclusivamente dos variables:

- Annual Income (k$).
- Spending Score (1-100).

El identificador no participa en el modelado. Las variables se
mantienen en sus escalas originales, siguiendo el ejercicio de clase.

## 4. Metodología

El procedimiento comprende las siguientes etapas:

1. Carga y exploración de datos con Pandas.
2. Selección de las características de agrupamiento.
3. Evaluación de K entre 1 y 10 mediante la inercia.
4. Visualización de la curva del método del codo.
5. Selección de cinco grupos.
6. Evaluación complementaria mediante el índice de silueta.
7. Interpretación de los segmentos comerciales.
8. Predicción de nuevos clientes.

Configuración del modelo final:

- Algoritmo: KMeans.
- n_clusters: 5.
- n_init: 20.
- random_state: 42.
- Biblioteca: Scikit-learn.

## 5. Resultados

| Indicador | Resultado |
|---|---:|
| Clientes analizados | 200 |
| Número de grupos | 5 |
| Inercia | 44448.46 |
| Índice de silueta | 0.5539 |
| Errores de ejecución | 0 |

### Segmentación obtenida

| Cluster | Clientes | Ingreso medio (kUSD) | Gasto medio |
|---|---:|---:|---:|
| 0 | 81 | 55.30 | 49.52 |
| 1 | 39 | 86.54 | 82.13 |
| 2 | 22 | 25.73 | 79.36 |
| 3 | 35 | 88.20 | 17.11 |
| 4 | 23 | 26.30 | 20.91 |

El agrupamiento distingue perfiles de clientes con diferentes
niveles de ingreso y puntuaciones de gasto.

Los identificadores de los clusters son etiquetas numéricas,
no categorías jerárquicas.

## 6. Recomendación comercial

Se selecciona el cluster 3 como grupo prioritario.

Este segmento contiene 35 clientes con ingresos anuales promedio
de 88.20 miles de dólares y una puntuación media de gasto de 17.11.

La combinación de ingresos elevados y gasto reducido representa
una oportunidad potencial para desarrollar acciones comerciales.

Se propone implementar una campaña piloto de productos premium,
ofertas personalizadas y beneficios de fidelización.

Para evaluar su efectividad, se recomienda realizar un experimento
A/B y medir cambios en conversión, frecuencia de compra y ventas.

## 7. Predicción de nuevos clientes

Se evalúa un nuevo cliente con las siguientes características:

- Ingreso anual: 110 miles de dólares.
- Spending Score: 21/100.

Resultado del modelo: cluster 3.

Esto permite asignar nuevos clientes a segmentos previamente
identificados por el algoritmo.

## 8. Reproducción del proyecto

Entorno utilizado:

- Python 3.13.14.
- NumPy.
- Pandas.
- Matplotlib.
- Seaborn.
- Scikit-learn.
- Jupyter.

Instalar las dependencias ejecutando en la terminal:

    python -m pip install -r requirements.txt

Abrir el archivo:

    Actividad_4_KMeans_Entrega_Final.ipynb

Seleccionar el kernel de Python y ejecutar todas las celdas.

El archivo mall_customers.csv debe encontrarse en la misma
carpeta que el notebook.

La generación del reporte con ydata-profiling es opcional.

## 9. Limitaciones

- El análisis es descriptivo y no permite establecer causalidad.
- El Spending Score no equivale directamente al monto gastado.
- No se aplicó estandarización de características.
- La selección de K se fundamenta en métricas internas.
- Los resultados corresponden a esta base de datos específica.

Como extensión futura, puede compararse el comportamiento del
modelo con variables estandarizadas y diferentes inicializaciones.

## 10. Archivos del proyecto

- Actividad_4_KMeans_Entrega_Final.ipynb:
  notebook con código, visualizaciones y resultados.
- mall_customers.csv:
  base de datos original.
- requirements.txt:
  dependencias del entorno.
- README.md:
  documentación académica del proyecto.

## 11. Referencia académica

Morocho Cayamcela, M. E. (2026).
Fundamentos de Inteligencia Artificial.
Maestría en Ciencia de Datos, Yachay Tech.

Notebook base y actividad proporcionados por el docente.

Desarrollo, reproducción y análisis de la Actividad 4.
