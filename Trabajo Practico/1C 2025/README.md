# Examen Práctico

**01-3900 | Ciencia de datos | 2025**

**Grupo**: DataMinds

## Integrantes
| DNI | Apellido/s | Nombre/s |
|--|--|--|
| 43.630.151 | Antonioli | Ivan Oscar |
| 43.664.669 | Di Nicco | Luis Demetrio |
| 34.519.918 | Gramajo | Hector Marcelo |
| 35.634.266 | Miranda | Sergio Javier |
| 41.548.235 | Sandoval Vasquez | Juan Leandro |

## Enunciado
Se tienen un dataset con datos de pacientes internados en un hospital (TP_Virus_Alumnos.csv). La clase de interes (1) refiere a la presencia de un virus. El virus tiene normalmente una gravedad leve/baja y el tratamiento suele ser invasivo. Datos como nombre y apellido han sido eliminados y los valores tanto en sangre (BLD), hormonales u otros análisis sobre reactivos han sido alterados en sus valores para preservar la privacidad. Se aclara que no se ha modificado su capacidad predictiva (Si es que la tienen).

Para su conocimiento: Datos generales de Edad, Peso, Altura y condición laboral (Activo, Pasivo etc). Datos medidos en hospital:

* BLD: Sangre
* LVL: Hormonales
* REC: Otros análisis

Se pide obtener con los datos disponibles el mejor modelo posible que prediga la presencia o ausencia del virus. Dado que el tratamiento es invasivo y la grevedad es moderada se requiere "atrapar" tantos "1" como sea posible y minimizar los falsos positivos para evitar que reciban un tratamiento de estas caracteristicas personas que no presentan el virus. Intente obtener el mejor modelo que maximice la métrica que considere correspondiente.

## Como desarrollar el exámen
A partir del dataset realice todas las acciones para poder llegar al mejor modelo, explique brevemente en los fundamentos de sus transformaciones o acciones en general.

La nota derivará de:

1. La calidad de la clasificación realizada
2. La fundamentación de los pasos realizados
3. Lo sencillo de llevar a producción el desarrollo

Los docentes evaluaran su clasificador utilizando un conjunto de datos del dataset "fuera de la caja" (out of the box, al que usted no tiene acceso). Para minimizar la posible diferencia entre su medición y la medición del docente recuerde y aplique conceptos de test, validación cruzada y evite los errores comunes de sesgo de selección y fuga de datos ([Sklearn "10. Common pitfalls and recommended practices"](https://scikit-learn.org/stable/common_pitfalls.html))

Al final del notebook encontrará un bloque de código que lee la muestra adicional (a la que usted no tiene acceso) si `PRODUCCION == True`, en caso contrario solo lee una submuestra del conjunto original para validar que el código funciona. Desarrolle el notebook como considere para finalmente asignar el mejor clasificador o pipeline que usted haya obtenido remplazando en `f_clf = None`, None por su clasificador o pipeline. Si no utiliza un pipeline, implemente todas las transformaciones entre esa línea y la predicción final.

Persista modelos si realiza procesos que demoren (Mas de 10 minutos es mucho), alternativamente si quiere realizar búsquedas exhaustivas de hiperparametros o variables explicite el procedimiento y luego utilice los valores obtenidos para ajustar un clasificador/regresor y que los tiempos sean posibles en la corrección. Todas las herramientas vistas en clase están disponibles. Verifique que los docentes pueden ejecutar su clasificador / regresor usando el código adjunto y los datos "fuera de la caja" para validar la calidad su modelo.

En materiales del MIEL/GIT se adjuntan un notebooks con algunas ideas para automatizar el proceso (Pipelines/Transformadores customizados).
