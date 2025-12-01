Trabajo Final Laboratorio de Implementación I | Final submit

Descripción

En este repositorio se encuentra el notebook con el Modelo.v8 utilizado para la competencia Kaggle de predicción de bajas bancarias.

Características

Semilla primigenia: 228311

N° Experimento: KA9661

Optimización Bayesiana: 50 iteraciones guardadas en el repositorio

Mejor score público: 8.997M (envios 1900)

AUC validación: 0.932305869

Se seleccionó este experimento debido a ser el de mayor ganancia promedio por envio. Logre obtener ganancias myaores en otros exprimentos con otra cantidad de envios pero el promedio por envio fue menor. 

Hiperparámetros Óptimos

num_leaves: 151

min_data_in_leaf: 3974

feature_fraction: 0.677877662

learning_rate: 0.011219122

num_iterations: 1015

lambda_l1:0.1605

lambda_l2:3.6176

min_gain_to_split:0.0706

Modificaciones Implementadas

Para optimizar el código nos basamos en buenas prácticas y experimentos colaborativos, en particular:

Catastrophe Analysis con método del VAGO para imputación de variables corruptas

Data Drifting con metodo dolar_blue para ajustar variables monetarias

FE agregue variables denominadas bestias con ratios y EMAs.

Feature Engineering Histórico creando lags y deltas de orden 1 y 2 para todas las variables (~800 variables nuevas) + Lag3 y delta 3 para variablem_comisiones. En los primeros experimentos vi que era la que mejor respondia al lag 3. 

AUmente parametros del Random Forest ya que vi que me genreaba las mejores variables.

Exclusión de numero_de_cliente y foto_mes para el modelado

Tomar AUC como métrica y GBDT como método de boosting

Implemente canritos con el objetivo de ir a 100 interaciones en la bayesiana (cosa que no logre)

training_pct = 0.4 

Resultados

Corte	Ganancia (M)

ENVIO:1800	1900	2000	2100	2200	2300	2400

GANAN:18446	8997	8647	8306	8436	8597	8236

Autor

Juan Ignacio Ton Vanerio Materia: Laboratorio de Implementación I 2025 Maestría en Ciencias de Datos, Universidad Austral
