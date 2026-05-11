# Cálculo de Zona de Daño de Fallas - Incidencia Estructural (IZPR)
Este repositorio contiene una herramienta automatizada para el cálculo de la incidencia estructural dentro del modelo de Índice de Zonas Potenciales de Recarga (IZPR). El procedimiento se basa estrictamente en los lineamientos de la Guía Metodológica para la Identificación de Zonas de Recarga y de Acuíferos del Ministerio de Ambiente y Desarrollo Sostenible de Colombia.
## Descripción 
El código permite cuantificar la influencia de las estructuras geológicas (fallas) en la permeabilidad secundaria del terreno. Para ello, se determina la Zona de Daño (ZD) de cada segmento de falla, la cual define el área de influencia donde la fracturación aumenta la capacidad de infiltración y recarga de agua subterránea.
## Metodología
El flujo de procesamiento implementado sigue estos pasos secuenciales:
Cálculo de Longitud: Se determina la longitud geométrica de cada segmento de falla individual presente en el conjunto de datos vectoriales.
Cálculo de la Zona de Daño: Se aplica la constante empírica sugerida por la normativa técnica colombiana. La zona de daño se define mediante la siguiente expresión: ZD= (L*0.3)/100
Generación de Buffer: Utilizando el valor resultante de ZD como radio, se genera un área de influencia (buffer) para cada segmento. Este polígono resultante representa la extensión espacial de la incidencia estructural para el cálculo del IZPR.
## Ejemplo de aplicacion
A modo de ejemplificación y validación de los resultados, el script se ejecutó utilizando la capa de Fallas de Colombia (basada en la información oficial del igac https://www.colombiaenmapas.gov.co/#).
Este ejercicio permite visualizar cómo la metodología se adapta a la complejidad tectónica del territorio nacional, calculando áreas de influencia diferenciadas según la escala y longitud de los trazos de falla presentes en las diversas provincias geológicas del país. El resultado es un producto cartográfico listo para ser integrado como el parámetro de "Incidencia Estructural" en el modelamiento multivariado del IZPR.
