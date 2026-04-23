# Statistic_Analysis_ConectaTel

# Segmentación de Clientes - ConnectaTel

## Descripción del proyecto
Este proyecto tiene como objetivo analizar el comportamiento de los clientes de ConnectaTel mediante técnicas de análisis de datos, con el fin de identificar patrones de uso, segmentar usuarios y generar recomendaciones de negocio.

## Objetivos
- Analizar la calidad de los datos y realizar limpieza
- Identificar patrones de uso en clientes
- Segmentar usuarios por nivel de uso y edad
- Detectar outliers y evaluar su impacto
- Generar insights y recomendaciones estratégicas

## Dataset
El análisis se basa en tres tablas principales:
- users: información demográfica de los clientes  
- usage: registros de actividad (mensajes, llamadas, duración)  
- plans: información de planes (opcional)

## Problemas detectados en los datos
- Valores nulos en:
  - city (~11%)
  - churn_date (~88%) (esperado)
  - duration (~55%) y length (~44%)  
- Valores sentinela (-999) en age  
- Posibles duplicados en variables de uso  
- Presencia de outliers en métricas de consumo  

## Limpieza y preparación de datos
- Reemplazo de valores sentinela por NaN
- Reconocimiento de outliers
- Conservación de nulos estructurales 
- Validación de consistencia de datos

## Segmentaciones
Se generaron variables clave para el análisis:

- uso_total = mensajes + llamadas + minutos  
- grupo_uso:
  - Bajo uso  
  - Uso medio  
  - Alto uso  

- Segmentación por edad:
  - Joven  
  - Adulto  
  - Adulto mayor  

## Análisis y visualización
Se utilizaron librerías como:
- pandas
- matplotlib
- seaborn

Principales visualizaciones:
- Distribución de clientes por nivel de uso (countplot)
- Segmentación por edad
- Análisis de dispersión y outliers

## Insights principales
- La mayoría de los clientes se concentra en el segmento de uso medio
- El grupo de alto uso es reducido pero potencialmente más valioso
- Existe un segmento relevante de bajo uso, con posible riesgo de baja retención
- La base de clientes está dominada por adultos, con menor presencia de usuarios jóvenes
- Los outliers representan usuarios intensivos reales, no errores

## Recomendaciones
- Diseñar planes premium para usuarios de alto consumo  
- Implementar estrategias de retención para clientes valiosos  
- Desarrollar ofertas específicas para el segmento joven  
- Enfocar estrategias comerciales en el segmento adulto  
- Monitorear usuarios extremos para optimizar operación y servicio  

## Tecnologías utilizadas
- Python  
- Pandas   
- Matplotlib  
- Seaborn  

