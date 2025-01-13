O IPCA (Índice Nacional de Preços ao Consumidor Amplo) é influenciado por muitas variáveis, como taxas de juros, políticas fiscais, variações cambiais dentre outros. Neste estudo, explorei uma abordagem simplificada, utilizando apenas a tendência histórica da série temporal desde 2004. Com o uso de redes neurais do tipo LSTM (Long Short Term Memory)



Em dez/2023, o boletim Focus projetava 3,9% de IPCA para 2024. Atualmente, as projeções indicam 4,7% (+∆ 0,8 p.p.). O modelo apresentado neste estudo projetou 5,3% para 2024 (+∆ 0,6 p.p. vs atual) e 5,2% para o ano atual. 

Inicialmente, tentei projetar o IPCA utilizando o modelo SARIMA. Mas os resultados foram tão simples que quase me convenci a abrir o Excel e resolver tudo por lá! Decidi explorar uma abordagem mais robusta com redes neurais LSTM, para capturar padrões temporais complexos na série histórica. A LSTM é uma arquitetura de rede neural recorrente (RNN), muito utilizada atualmente na literatura científica:



Rusho et al. (2024) mostraram que redes LSTM melhoram previsões sísmicas, superando modelos estatísticos tradicionais. 

Mamdouh et al. (2024) desenvolveram uma LSTM bidirecional para prever atrasos de voos, alcançando mais de 93% de precisão e beneficiando o setor aéreo. 

Wang et al. (2024) destacaram LSTMs na previsão de ações, superando limitações de RNNs.

Histórico de IPCA disponível em: https://www.ibge.gov.br/estatisticas/economicas/precos-e-custos/9256-indice-nacional-de-precos-ao-consumidor-amplo.html?=&t=series-historicas. Após realizar o download da base, organizei os períodos no excel e importei a base para o google colab.

Embora o modelo tenha mostrado um bom desempenho no treino, com erros controlados, observa-se maior variabilidade na validação e teste, o que é esperado devido às flutuações do IPCA. Durante o processo, foram aplicadas técnicas avançadas de regularização, como o dropout e L2 regularization, para evitar overfitting e melhorar a generalização do modelo, além da normalização e o early stopping. Destaca-se  a possibilidade de aprimorar o modelo com a inclusão de variáveis externas e ajustes nos hiperparâmetros.
