# Examen Práctico

**01-3900 | Ciencia de datos | 2025**

**Grupo**: Puta Data

## Integrantes
| DNI | Apellido/s | Nombre/s |
|--|--|--|
| 40.955.907 | Costanzo | Marcos Ezequiel |
| 43.875.244 | Fernández | Rocío Belén |
| 36.360.020 | Quelali Amistoy | Marcos Emir |
| 41.548.235 | Sandoval Vasquez | Juan Leandro |
| 39.213.320 | Siculin | Luciano Nahuel |

## Objetivos
* Desarrollar hipótesis sobre conjunto de datos utilizando técnicas de análisis exploratorio.
* Comprender los algoritmos utilizados en Machine Learning para problemas de clasificación.
* Desarrollar modelos predictivos para resolver problemas en el ámbito de la ciencia de datos.
* Comunicar los resultados del análisis de datos, a través de técnicas de visualización de información adecuadas e interpretables.

## Enunciado
La empresa "Business Prop SRL" contrata nuestros servicios para que le desarrollemos un modelo que permita predecir si los departamentos vendidos pagan o no comisión, cuando su precio de venta sea superior a un determinado valor.  

Para ello, nos comparten un dataset llamado dptos_entrenamiento.csv, que contiene información de departamentos vendidos en distintos lugares de Argentina y el exterior. Este dataset será el que utilicemos para el entrenamiento del modelo construido.  

El dataset de predicción a utilizar es dptos_predecir.csv, el cual no contiene la etiqueta de la variable clase (por defecto viene indicada como “no paga”). Cada uno de estos datasets pueden descargarlos desde:

* [Departamentos Entrenamiento](https://raw.githubusercontent.com/pokengineer/DataScience/refs/heads/main/assessment/dptos_entrenamiento.csv)
* [Departamentos Predicción](https://raw.githubusercontent.com/pokengineer/DataScience/refs/heads/main/assessment/dptos_predecir.csv)

### a. Función de ganancia y criterio de aprobación
Por cada predicción que el modelo acierte, la empresa les pagará USD 100 en concepto de comisión, pero si fallan y cobran una comisión que no deberían, deben darle a Business Prop SRL una compensación de USD 50.

La evaluación de aprendizaje se considerará aprobada si la ganancia obtenida por el modelo sobre los datos desconocidos supera los USD 300.000. Como referencia, la ganancia que calculará el modelo construido es sobre el porcentaje de los datos usados para testing (muestra del 30%), con lo que ese valor puede ser alrededor de USD 120.000.

### b. Entregable
Generar y enviar un archivo de salida dptos_entrega.csv con los casos donde la medición realizada infiera que se pagará comisión. Para ello, deberá utilizar el dataset que se usó para predecir dptos_predecir.csv. Enviar también el notebook construido con el trabajo desarrollado.

### c. Sugerencias
- Algunas variables pueden generar alta dimensionalidad en el dataset, como ser los campos "title", "start_date", "end_date", "created_on", "l3", "l4" y "l5". Sugerimos comenzar con un modelo que no incluya estos campos o bien analizar qué información interesante de los mismos podría contribuir a la mejorar de la predicción. Por otro lado, sugerimos que el campo "id" lo usen como índice, con el comando set_index("id").
- Probar diferentes modelos. El objetivo del trabajo es lograr mejorar su modelo original.
