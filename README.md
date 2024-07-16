# Proyecto de Análisis del Consumo de Electricidad de una Vivienda
## Desarrollado por Juan Sebastian Moncada Aguilar
*Todo el proceso fue desarrollado en Kaggle (TPU VM v3-8)

Este proyecto tiene como objetivo analizar el consumo de electricidad de una vivienda utilizando registros con una periodicidad de un minuto. A lo largo del proyecto, se realizaron diversas etapas de análisis y modelado, culminando en la implementación de un sencillo modelo ARIMA para pronosticar los niveles de consumo para los siguientes 60 minutos.

## Variables del Dataset

- `Global_active_power` (float): Potencia activa global en kilovatios (kW).
- `Global_reactive_power` (float): Potencia reactiva global en kilovatios (kW).
- `Voltage` (float): Voltaje medio por minuto.
- `Global_intensity` (float): Intensidad de corriente global en amperios (A).
- `Sub_metering_1` (float): Energía submedida en la cocina (en vatios-hora).
- `Sub_metering_2` (float): Energía submedida en la lavandería (en vatios-hora).
- `Sub_metering_3` (float): Energía submedida en el sistema de calefacción y aire acondicionado (en vatios-hora).
- `Datetime` (datetime): Marca temporal de cada observación.

## Análisis Exploratorio de Datos (EDA)

Se realizó un análisis exploratorio exhaustivo que incluyó:

- **Medidas de Tendencia Central**: Cálculo de la media, mediana y moda para comprender la distribución central de las variables.
- **Medidas de Posición**: Cálculo de percentiles y cuartiles para entender la dispersión y distribución de los datos.
- **Correlación**: Análisis de la correlación entre las variables para identificar relaciones lineales.
- **Valores Duplicados**: Detección y eliminación de registros duplicados.
- **Valores Nulos**: Identificación y tratamiento de valores nulos.
- **Outliers**: Detección y tratamiento de valores atípicos utilizando el método del rango intercuartílico (IQR).

## Modelado

### Modelo ARIMA

Se implementó un modelo ARIMA (AutoRegressive Integrated Moving Average) básico, conocido también como modelo Naivy, para pronosticar los niveles de consumo de electricidad de los siguientes 60 minutos. Sin embargo, este modelo debe pasar por un proceso de selección de orden utilizando criterios de información como AIC (Akaike Information Criterion) o BIC (Bayesian Information Criterion) mediante un procedimiento stepwise para determinar el mejor orden del modelo.

### Mejoras Futuras

- **Modelos Alternativos**: Considerar el uso de otros modelos más robustos, como Random Forest, para mejorar las predicciones.
- **Evaluaciones Adicionales**: Realizar evaluaciones adicionales en términos de la distribución del error (autocorrelación), multicolinealidad y heterocedasticidad para garantizar la validez y robustez del modelo.

## Instrucciones de Uso

1. **Carga de Datos**: Asegúrate de que los datos estén en un archivo CSV con las variables definidas anteriormente.
2. **Preprocesamiento**: Ejecuta las etapas de preprocesamiento para manejar valores nulos, duplicados y outliers.
3. **Análisis Exploratorio**: Realiza el análisis exploratorio de datos para obtener una comprensión profunda de la distribución y relaciones entre las variables.
4. **Modelado ARIMA**: Implementa el modelo ARIMA y realiza las predicciones para los próximos 60 minutos.
5. **Evaluación del Modelo**: Calcula métricas como el MAE (Mean Absolute Error) para evaluar la precisión del modelo.
6. **Visualización**: Utiliza `plotly express` para visualizar las observaciones y las predicciones de manera interactiva.

## Conclusiones

Este proyecto proporciona una base sólida para el análisis del consumo de electricidad en una vivienda. Sin embargo, se recomienda seguir mejorando el modelo mediante técnicas de selección de modelos más avanzadas y la consideración de modelos alternativos para obtener mejores predicciones. La evaluación adicional en términos de la distribución del error y otras métricas estadísticas es esencial para garantizar la precisión y robustez del modelo.
