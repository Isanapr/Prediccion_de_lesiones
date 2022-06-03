# Predicción de lesiones
Las lesiones sin contacto en el fútbol resultan en la ausencia de los jugadores lo cual conlleva a la afectación de la salud, el desempeño y resultados deportivos, así como en pérdidas financieras a los Clubs y a los mismos jugadores. El próposito de este proyecto es construir un modelo de predicción mediante el empleo de técnicas de aprendizaje automático para alertar a los jugadores con alto riesgo de lesión.

## Miembros del Equipo
#### Fernanda Bueso Medina
#### Isabel Navarro

## Install
Download and install the following libraries:
```
pip install pandas
pip install imblearn
```

## Workflow

#### 1. Análisis y Limpieza de Datos
De la primera tabla original de GPS se realiza un análisis de todas las variables. Se eliminan los outliers y se reemplazan con la media. Asimismo, se acotan las fechas a únicamente la temporada de interés que va de Julio 2021 - Noviembre 2021. 

#### 1.1 Calendario
En este código se muestra una gráfica de calendario que indica la frecuencia en la cual los jugadores asisten a sus entrenamientos. 

#### 2. Imputación y Feauture Engineering
En este codigo se termina de realizar la imputación de datos. Luego se realiza la ingeniería de características para obtener los valores de Exponential Weighted Moving Average (EWMA), Acute-Chronic Workload Ratio (ACWR) y Monotony (MSWR) para cada una de las variables del GPS. Después de esto se añaden las características personales de los jugadores a la tabla (peso, talla, edad, rol). 


#### 3. Previous Injury + EMWA
En este codigo se extrae un excel GPS_extra del codigo de Imputación y Feauture Engineering, donde manualmente se agregan las lesiones y el "previous injury". Ese excel se pasa por el código 3_Completando PI para agregarle el feauture EMWA.

#### 4. Balanceo de datos y Modelado
Finalmente, en este codigo se realiza el balanceo de datos y el entrenamiento de los modelos. Al finalizar el entrenamiento de los modelos, se evalua su rendimiento.


## Referencias
[1] Rossi A, Pappalardo L, Cintia P, Iaia FM, Fernàndez J, Medina D (2018) Effective injury forecasting in soccer with GPS training data and machine learning. PLoS ONE 13(7): e0201264. https://doi.org/10.1371/journal.pone.0201264
