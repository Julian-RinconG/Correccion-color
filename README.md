# Sistema de detección de color en flores a través de imágenes de cultivos de papa

Este proyecto desarrolla un sistema capaz de calibrar colores en imágenes de flores de cultivos de papa utilizando matrices de corrección 3x3 y 4x3 tanto con el modelo de openCV como de forma manual. El objetivo es minimizar la pérdida de color empleando métodos avanzados de inicialización y linealización. Se utiliza el estándar CIE2000 para evaluar la precisión de los colores corregidos.

Este trabajo fue desarrollado por estudiantes de ingeniería electrónica de la Pontificia Universidad Javeriana de Bogotá , como parte del enfásis de Procesamiento de Imágenes y Video.

# Características

- Procesamiento de imágenes con OpenCV
- Corrección de color mediante los modelos 3x3 y 4x3
- Evaluación de precisión utilizando la distancia CIE2000
- Métodos de inicialización (Balance de blancos y mínimos cuadrados)
- Métodos de linealización (LINEARIZATION_IDENTITY, LINEARIZATION_GAMMA, LINEARIZATION_COLORPOLYFIT, LINEARIZATION_COLORLOGPOLYFIT, LINEARIZATION_GRAYPOLYFIT, LINEARIZATION_GRAYLOGPOLYFIT)

# Conclusiones

Del presente proyecto se concluye que se logró cumplir parcialmente con el objetivo principal, puesto que se encontró que las combinaciones con menor pérdida, en el caso de la implementación por funciones de CCM de openCV tanto para modelos 3x3 y 4x3, son aquellas que utilicen la linelización de tipo Gamma, sin importar la inicialización; teniendo pérdidas propias del modelo de 3.1945 y 3.0913, respectivamente. Sin embargo, estas pérdidas no fueron medidas respecto al estándar CIE2000. Sin embargo, con la implementación manual, si se midió la pérdida a partir de este, obteniendo que la mejor combinación para el modelo 3x3 es la inicialización por balance de blancos, y nuevamente la linealización de tipo Gamma, obteniendo una distancia de 0.3508. Este resultado confirma la efectividad de estos métodos para garantizar una correspondencia cromática confiable entre la imagen corregida y los valores de referencia.
\vspace{3mm}

Por otra parte, debido a las limitaciones de la versión de OpenCV utilizada, fue necesario implementar un modelo manual para calcular la matriz de corrección y aplicar los métodos de inicialización y linealización. Aunque este enfoque incrementó la complejidad del desarrollo, permitió alcanzar resultados precisos y efectivos, destacando la importancia de comprender los fundamentos matemáticos de las transformaciones de color. Adicionalmente la calidad visual de las imágenes corregidas mostraron mejoras notables con ambos métodos de corrección, especialmente en los tonos de las flores y el follaje, proporcionando un equilibrio cromático más natural. Esto demuestra que la correcta selección de métodos de inicialización y linealización es fundamental para aplicaciones que requieren alta fidelidad en la representación de colores.

Del mismo modo, se tiene que se cumplió con los dos objetivos específicos, pues se identificó que los parámetros más críticos a la hora de la detección y corrección de una imagen son tanto la iluminación, la tonalidad de la luz aplicada, y la distribución de colores presentes en la misma. En cuanto al otro objetivo específico, se deduce que la matriz de corrección con mejor desempeño sería la matriz de 4x3, pues al incluir un parámetro adicional, puede adaptarse mejor a la calibración requerida, lo que deriva en una menor pérdida de color.



# Créditos
Este proyecto fue desarrollado por:

- Nasly Verónica Novoa Lozano
- Luna Sofía Corrales Sierra
- Julián David Rincón Garzón

  Profesor de la materia:

  Francisco Carlos Calderon Bocanegra

Pontificia Universidad Javeriana, Facultad de Ingeniería. Bogotá, Colombia.
