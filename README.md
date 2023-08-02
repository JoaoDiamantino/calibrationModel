<h1 align="center">🌧️: Modelo de Calibração de Sensor de Chuva</h1>

## :memo: Descrição
O desafio técnico proposto pela FieldPRO envolve a construção de um modelo de 
calibração de um sensor de chuva com base em impactos mecânicos. O sistema de 
medição de chuva utiliza um piezoelétrico, um acumulador de carga e um sensor 
de temperatura para medir o impacto das gotas de chuva e gerar uma queda na carga
do acumulador, que é medida e transmitida de hora em hora como a variável "piezo_charge".
Além disso, outras variáveis relevantes, como a temperatura da placa ("piezo_temperature"), 
o número total de resets da placa ("num_of_resets") e as condições atmosféricas externas,
como a temperatura do ar ("air_temperature_100"), umidade relativa do ar ("air_humidity_100")
e pressão atmosférica ("atm_pressure_main"), também estão disponíveis para a modelagem.

Para resolver esse desafio, foi utilizado um modelo de regressão com o algoritmo Random Forest. 
A escolha do modelo de regressão se deve ao fato de que queremos prever um valor contínuo, a 
quantidade de chuva, com base nas variáveis de entrada disponíveis. O Random Forest é um algoritmo
de aprendizado de máquina baseado em árvores de decisão que é eficiente e eficaz em problemas de 
regressão.

Para construir o modelo de Random Forest, foram utilizadas as medidas do sensor de chuva e 
as variáveis atmosféricas externas como features  para o modelo, como as perdas de carga do
acumulador ("piezo_charge_diff")e as medidas de chuva captadas por uma Estação próxima, como 
dados de saída. O conjunto de dados foi dividido em dados de treinamento e teste para avaliar
o desempenho do modelo. Foram utilizadas métricas de desempenho, como o Mean Squared Error (MSE),
Mean Absolute Error (MAE) ou R-squared (R²), para avaliar quão bem o modelo se ajusta aos dados de 
teste.

Ainda foi possivel fezer um tunning no modelo com GridSearch.

## :wrench: Tecnologias utilizadas
* Linguagem Python no Google Colab

## :rocket: Rodando o projeto
Para rodar o repositório é necessário clonar o mesmo e rodar em notebook no GoogleColab ou Jupyter

