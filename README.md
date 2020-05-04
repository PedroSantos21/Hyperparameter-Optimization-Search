# Project-4

4o Exercício de casa
Jacques Wainer

Pode ser feito individualmente ou em duplas.

data para entrega: até meia note de 7/5 (5a feira)

## Objetivo
Vamos fazer a busca dos melhores hiperparametros para uma SVM para Regressão num banco de dados em particular.

Xtreino.npy e Xteste5.npy são os dados de treino e teste, e ytreino5.npy e yteste5.npy as saidas correspondentes do dados.

## SVM Regressor
O sklearn.svm.SVR do sklearn implementa o regressor SVM e tem vários hiperparametros. Vamos usar o kernel “rbf”. Neste caso há 3 hiperparametros que se considera como os mais importantes, : C, gamma, e epsilon

Vamos fazer a busca no range:

C entre 2^{-5}2 
−5
  e 2^{15}2 
15
  (uniforme nos expoentes)
gamma entre 2^{-15}2 
−15
  e 2^{3}2 
3
  (uniforme nos expoentes)
epsilon entre 0.05 a 1.0 (uniforme neste intervalo)
Medida de erro
Para cada conjunto de hiperparametros, treine o SVM no conjunto de treino ( Xtreino e ytreino), e meça o erro absoluto médio (MAE) no conjunto de teste (Xteste e yteste).

## Algoritmos de otimização
- random search

- grid search

- Bayesian optimization

- PSO

- simulated aneeling

- CMA-ES

# Random search
Use um random search de 125 combinações dos hiperparametros. Voce pode usar o sklearn.modelselection.RandomizedSearchCV do sklearn, ou o random search do hyperopt (ver abaixo a otimização bayesiana), ou voce pode implementar a busca voce mesmo

Reporte os melhores valores dos hiperparametros e o MAE para esses valores.

# Grid seach
Faça um grid search de 5 x 5 x 5 em cada uma dos atributos acima. Note que os hiperparametros C e gamma são um grid linear no expoente.

Vc pode usar o GridSearchCV do sklearn ou implementar o seu proprio código.

Reporte os melhores valores dos hiperparametros e o MAE para esses valores.

# Otimização bayesiana
Voce pode utilizar o pacote hyperopt para fazer a otimização bayesiana dos hiperparametros. Essa implementação usa um regressor (TPE) para modelar a distribuição de probabilidades que é muito mais rápido que a implementação padrão utilizando “processos gaussianos”. Ou utilize algum outro pacote de otimização bayesiana.

Use 125 chamadas para a função.

Reporte os melhores valores dos hiperparametros e o MAE para esses valores.

# PSO
Utilize o PSO para resolver a busca de hiperparametros. Voce pode utilizar implementações como pyswarm ou psopy ou qualquer outra.

Utilize 11 partículas por 11 interações (para ser justo com os outros algoritmos acima) . Utilizes os valores default (da sua implementação) para os hiperparametros do PSO.

Reporte os melhores valores dos hiperparametros e o MAE para esses valores

# Simulated annealing
Utilize um pacote como simannel para fazer a busca usando simulated annealing. Utilize 125 passos na simulação. Voce pode usar o valor default para o cooling schedule.

Reporte os melhores valores dos hiperparametros e o MAE para esses valores.

# CMA-ES
Utilize o pacote pycma ou alguma outra implementação do CMA-ES. Utilize 125 chamadas da função. Reporte os melhores valores dos hiperparametros e o MAE para esses valores.

# Optunity
Parece que o pacote Optunity implementa todos os algoritmos acima menos o SA. O pacote parece que esta parado desde 2016 e portanto isso pode ser um problema. Use este pacote ou use os pacotes específicos para cada algoritmo.
