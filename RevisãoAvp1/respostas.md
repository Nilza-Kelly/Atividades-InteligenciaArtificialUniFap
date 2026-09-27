
# Lista de Exercícios: Lista de Revisão AVP1

## Enunciado
Questão 1. Uma empresa de entregas pretende utilizar Machine Learning em três situações

• prever o tempo de entrega de um pedido, em minutos;

• prever se uma entrega chegará dentro do prazo ou ficará atrasada;

• encontrar grupos de clientes com comportamentos semelhantes, sem possuir grupos previamente definidos.

Para cada situação, indique se o problema é de regressão, classificação ou aprendizado não supervisionado. Justifique sua resposta a partir do tipo de saída ou da existência de categorias previamente conhecidas.

**Resposta:**
1. Prever o tempo de entrega de um pedido, em minutos: Regressão

2. Prever se uma entrega chegará dentro do prazo ou ficará atrasada: Classificação

3. Encontrar grupos de clientes com comportamentos semelhantes, sem possuir grupos previamente definidos: Aprendizado não supervisionado

## Enunciado
Questão 2. Uma empresa de transporte possui dados sobre frequência de utilização, valor médio das viagens, horários utilizados e distância média percorrida pelos clientes. Entretanto, não existem rótulos ou categorias previamente definidas para esses clientes. Explique como você utilizaria aprendizado não supervisionado nesse cenário. O que o algoritmo estaria tentando descobrir nos dados? Por que não seria adequado afirmar que o objetivo é realizar uma classificação supervisionada?

**Resposta:**
O problema pode ser tratado com aprendizado não supervisionado, pois não existem rótulos ou categorias previamente definidas. O algoritmo pode analisar características como frequência de utilização, valor médio, horários e distância e identificar grupos de clientes com comportamentos semelhantes. Um exemplo de técnica que poderia ser utilizada é o K-Means. A classificação supervisionada não seria adequada porque ela necessita de exemplos previamente rotulados para aprender a separar as classes.

## Enunciado
Questão 3. Uma imobiliária utiliza o modelo de regressão linear:

yˆ = 40 + 0,10x,

em que x representa a área do imóvel, em metros quadrados, e yˆ representa o preço estimado, em milhares de reais. Calcule a previsão para um imóvel de 120 m2. Apresente o cálculo completo e interprete o resultado.

**Resposta:**
yˆ ​= 40 + 0,10(120)

yˆ ​= 40 + 12

yˆ ​= 52

A previsão é de 52 mil reais

## Enunciado
Questão 4. Considere novamente o modelo:

yˆ = 40 + 0,10x

a) O que representa o número 40 no modelo?

b) O que representa o coeficiente 0,10

c) Se a área aumentar em 50, de quanto aumenta a previsão de preço segundo o modelo?

d) Explique por que esse modelo é chamado de regressão linear.

**Resposta:**
a) O número 40 representa o intercepto do modelo, ou seja, o valor estimado de y quando x=0.

b) O 0,10 é o coeficiente angular (inclinação da reta). Ele mostra quanto a previsão aumenta quando x aumenta uma unidade.

c) 0,10 × 50 = 5. A previsão aumenta R$ 5.000.

d) O modelo é chamado de regressão linear porque relaciona a variável de entrada x com a variável de saída y por meio de uma equação linear, formando uma reta.

## Enunciado
Questão 5. Uma empresa avaliou um modelo de regressão em quatro entregas. Os valores reais e previstos foram:

| Entrega | Valor real | Valor previsto |
| --- | --- | --- |
| 1 | 10 | 12 |
| 2 | 20 | 18 | 
| 3 | 30 | 33 | 
| 4 | 40 | 35 | 

Considere: MSE = 1/n ∑n i=1 (yi − yˆi)²

Calcule o erro de cada previsão e, em seguida, calcule o MSE do modelo. Mostre todas as etapas do cálculo.

**Resposta:**
Entrega 1: 

10 − 12 = −2

(−2)² = 4

Entrega 2:

20 − 18 = 2

2² = 4

Entrega 3:

30 − 33 = −3

(−3)² = 9

Entrega 4:

40 − 35 = 5

5² = 25

Somando os erros² = 4 + 4 + 9 + 25 = 42

Temos 4 entregas: n = 4

MSE = 42/4 = 10,5​


## Enunciado
Questão 6. Dois modelos foram utilizados para prever a demanda de um produto. Em quase todas as previsões, os erros dos dois modelos são semelhantes. 
Entretanto, o Modelo A comete uma previsão com erro muito maior que os demais erros. Considere:

MAE = 1/n ∑n i=1 |yi − yˆi|²

MSE = 1/n ∑n i=1 (yi − yˆi)²

**Resposta:**
O MSE é mais influenciado por um erro muito grande porque eleva cada erro ao quadrado. Assim, erros grandes recebem um peso muito maior na métrica. 
O MAE utiliza o valor absoluto do erro e, por isso, cresce de forma linear.

## Enunciado
Questão 7. Uma equipe possui um dataset com milhares de exemplos e decide utilizar todos os dados para treinar um modelo. Ao final, calcula o erro utilizando exatamente os mesmos exemplos que foram usados no treinamento. O erro obtido é extremamente baixo. Explique por que esse resultado não é suficiente para afirmar que o modelo terá bom desempenho em novos dados. Qual problema existe em avaliar o modelo nos mesmos dados utilizados para treiná-lo?

**Resposta:**
O modelo está sendo avaliado nos mesmos dados que utilizou para aprender. O modelo pode ter se ajustado excessivamente aos dados de treinamento e apresentar erro muito baixo sem conseguir generalizar para novos dados. Por isso, é necessário avaliar o modelo em dados diferentes daqueles usados para treiná-lo.

## Enunciado
Questão 8. Uma equipe decide dividir seus dados em três conjuntos: treinamento, validação e teste. Explique a finalidade de cada conjunto e descreva uma sequência adequada de utilização deles durante o desenvolvimento de um modelo. Em particular, explique por que o conjunto de teste deve permanecer separado das decisões tomadas durante o desenvolvimento.

**Resposta:**
O conjunto de treinamento é utilizado para ensinar o modelo e ajustar seus parâmetros. O conjunto de validação é utilizado durante o desenvolvimento para comparar modelos e tomar decisões sobre configurações. O conjunto de teste deve ser mantido separado para realizar a avaliação final do modelo. O teste deve permanecer separado porque utilizá-lo repetidamente durante o desenvolvimento pode fazer com que as decisões sejam adaptadas aos seus resultados.

## Enunciado
Questão 9. Três modelos apresentaram os seguintes resultados:

| Modelo | Erro no treino | Erro na validação |
| --- | --- | --- |
| A | 20 | 22 | 
| B | 5 | 7 | 
| C | 1 | 30 | 

a) Qual modelo apresenta indícios de underfitting? Justifique.

b) Qual modelo apresenta overfitting? Justifique.

c) Qual modelo apresenta o melhor equilíbrio entre treinamento e validação? Explique.


**Resposta:**
a) O modelo A pois os dois erros são relativamente altos.

b) O modelo C pois ele praticamente "decorou" o treinamento, mas foi mal na validação.

c) O modelo B pois os dois erros são relativamente baixos e próximos. Isso indica que o modelo consegue aprender os dados sem apresentar uma diferença muito grande entre treinamento e validação.

## Enunciado
Questão 10. Explique, com suas próprias palavras, a diferença entre underfitting e overfitting. Relacione sua resposta aos erros de treinamento e de validação.
Em seguida, explique por que um modelo com erro de treinamento muito baixo pode, ainda assim, ser pior para fazer previsões em novos dados.

**Resposta:**
Underfitting ocorre quando o modelo é simples demais e não consegue aprender adequadamente os padrões dos dados, apresentando erros altos no treinamento e na validação. Overfitting ocorre quando o modelo se ajusta excessivamente aos dados de treinamento, apresentando erro muito baixo no treinamento, mas erro elevado em dados de validação. Um erro de treinamento muito baixo não garante bom desempenho em novos dados porque o modelo pode não ter aprendido padrões gerais, mas apenas características específicas dos dados utilizados no treinamento.

## Enunciado
Questão 11. Uma equipe observa que a relação entre duas variáveis não pode ser representada adequadamente por uma reta. Foram testados modelos polinomiais de graus 1, 3 e 30. O modelo de grau 1 apresenta erro elevado no treinamento e na validação. O modelo de grau 3 apresenta erros baixos e próximos nos dois conjuntos. O modelo de grau 30 apresenta erro quase zero no treinamento, mas erro muito elevado na validação. Explique o comportamento de cada modelo e indique qual deles você escolheria para utilização em novos dados. Justifique.

**Resposta:**
O modelo de grau 1 apresenta comportamento de underfitting, pois apresenta erros elevados tanto no treinamento quanto na validação. O modelo de grau 30 apresenta overfitting, pois possui erro quase zero no treinamento, mas erro muito elevado na validação. O modelo mais indicado para utilizar em novos dados é o modelo de grau 3 pois ele apresenta um equilíbrio melhor, apresentando erros baixos tanto no treinamento quanto na validação.6

## Enunciado
Questão 12. Explique por que aumentar o grau de um polinômio pode inicialmente melhorar o ajuste aos dados, mas, a partir de determinado ponto, pode prejudicar a capacidade de generalização do modelo. Em sua resposta, explique o que acontece com um modelo muito complexo e relacione esse comportamento ao overfitting.

**Resposta:**
Aumentar o grau do polinômio pode inicialmente melhorar o ajuste porque o modelo ganha maior capacidade de representar relações mais complexas entre as variáveis. Porém, se o grau for aumentado excessivamente, o modelo pode começar a se ajustar aos ruídos e detalhes específicos dos dados de treinamento, prejudicando sua capacidade de generalização e causando overfitting.

## Enunciado
Questão 13. Um modelo de regressão polinomial possui muitos parâmetros e está apresentando overfitting. A equipe decide utilizar regularização.
Explique o objetivo da regularização e como a inclusão de uma penalização na função de custo pode ajudar a evitar que o modelo se ajuste excessivamente aos ruídos dos dados de treinamento.

**Resposta:**
A regularização adiciona uma penalização à função de custo para diminuir valores excessivamente grandes dos parâmetros ou modelos muito complexos. Isso pode reduzir o overfitting porque o modelo é incentivado a encontrar uma solução mais simples e capaz de generalizar melhor para novos dados.

## Enunciado
Questão 14. Considere um modelo com vários pesos θ1, θ2, . . . , θn. A equipe deseja reduzir o tamanho dos pesos para diminuir a complexidade do modelo.
Explique conceitualmente o que acontece quando se aumenta o parâmetro α em uma regularização Ridge. Por que pesos menores podem contribuir para reduzir o overfitting?

**Resposta:**
Na regularização Ridge, aumentar o parâmetro α aumenta a intensidade da penalização aplicada aos pesos do modelo. Como consequência, os pesos tendem a ficar menores. Isso pode reduzir a complexidade do modelo e ajudar a diminuir o overfitting, melhorando sua capacidade de generalização.

## Enunciado
Questão 15. Uma empresa possui um modelo com 20 variáveis de entrada, mas acredita que apenas algumas são realmente relevantes. A equipe gostaria que algumas variáveis tivessem peso exatamente igual a zero. Entre Ridge e Lasso, qual técnica é mais adequada para esse objetivo? Explique sua resposta relacionando-a à penalização utilizada pela técnica escolhida.

**Resposta:**
A técnica mais adequada é o Lasso, pois utiliza regularização L1. Uma característica da penalização L1 é que ela pode fazer alguns coeficientes ficarem exatamente iguais a zero, permitindo reduzir a quantidade de variáveis efetivamente utilizadas pelo modelo.

## Enunciado
Questão 16. Compare Ridge e Lasso considerando seus efeitos sobre os pesos do modelo.

a) Qual delas utiliza penalização L2?

b) Qual utiliza penalização L1?

c) Qual delas pode produzir pesos exatamente iguais a zero?

d) Em que situação a característica de produzir pesos zero pode ser útil?

**Resposta:**
a) Ridge

b) Lasso

c) Lasso

d) Quando temos muitas variáveis e acreditamos que algumas são pouco relevantes.

## Enunciado
Questão 17. Um banco utiliza Regressão Logística para decidir se uma transação é “legítima” ou “fraudulenta”. O modelo produz uma probabilidade de fraude para cada transação. Explique por que a Regressão Logística pode ser utilizada em um problema de classificação binária, mesmo que inicialmente o modelo produza uma combinação linear das variáveis de entrada. Em seguida, explique a função da função sigmoide nesse processo e indique qual intervalo de valores ela produz.

**Resposta:**
A Regressão Logística é utilizada em problemas de classificação porque transforma uma combinação linear das variáveis em uma probabilidade por meio da função sigmoide. A sigmoide produz valores entre 0 e 1. Em seguida, utiliza-se um limiar, como 0,5, para transformar a probabilidade em uma classe. Com o limiar de 0,5, probabilidades abaixo de 0,5 podem ser classificadas como legítimas e probabilidades iguais ou superiores a 0,5 como fraudulentas.

## Enunciado                                                                                   
Questão 18. Um modelo de Regressão Logística utiliza um limiar de decisão igual a 0,5 para classificar transações. Considere as seguintes probabilidades de fraude:

| Transação | Probabilidade de fraude |
| --- | --- |
| A | 0,20 |  
| B | 0,47 | 
| C | 0,50 | 
| D | 0,68 | 
| E | 0,91 | 

Classifique cada transação como “legítima” ou “fraudulenta” de acordo com o limiar adotado. Explique especificamente o que acontece com uma probabilidade exatamente igual a 0,5.

**Resposta:**
| Transação	| Probabilidade	| Classificação | 
| --- | --- | --- |
| A	| 0,20	| Legítima | 
| B	| 0,47	| Legítima | 
| C	| 0,50	| Fraudulenta | 
| D	| 0,68	| Fraudulenta | 
| E	| 0,91	| Fraudulenta | 

## Enunciado
Questão 19. Considere um modelo de Regressão Logística utilizado para classificar transações como legítimas ou fraudulentas. O modelo utiliza 0,5 como limiar.
Em um gráfico, os pontos A, B e C possuem probabilidades de fraude abaixo de 0,5, enquanto os pontos D, E e F possuem probabilidades acima de 0,5.

a) Qual é a classificação dos pontos A, B e C?

b) Qual é a classificação dos pontos D, E e F?

c) Explique como a linha correspondente ao limiar 0,5 separa as duas classes.

d) Se o limiar fosse alterado para 0,7, quais pontos poderiam mudar de classificação?

**Resposta:**
a) Legítimos

b) Fraudulentos

c) Existe uma linha representando o P = 0,5. De um lado ficam os pontos P < 0,5  que são classificados como legítimos. Do outro ficam os pontos P >= 0,5 que são classificados como fraudulentos.

d) Agora a regra passa a ser P < 0,7 = legítima e P >= 0,7 = fraudulenta. Isso significa que alguns pontos que antes eram considerados fraudulentos podem passar a ser legítimos.

## Enunciado
Questão 20. Uma equipe está analisando um modelo de Machine Learning e observa os seguintes comportamentos:

• um modelo de regressão apresenta erro muito baixo no treinamento e muito alto na validação;

• outro modelo apresenta erros de treinamento e validação próximos e relativamente baixos;

• um modelo de classificação produz probabilidades entre 0 e 1 e utiliza 0,5 como limiar para definir as classes.

Explique, relacionando os três casos aos conceitos estudados:

a) como identificar overfitting a partir dos erros de treinamento e validação;

b) por que a validação é importante na escolha do modelo;

c) como a Regressão Logística transforma a saída do modelo em uma decisão de classificação.

**Resposta:**
a) O overfitting pode ser identificado quando o erro no treinamento é muito baixo, mas o erro na validação é muito alto. Isso indica que o modelo se ajustou excessivamente aos dados de treinamento e apresenta dificuldade para generalizar para dados novos.

b) A validação é importante porque permite avaliar o comportamento do modelo em dados diferentes daqueles utilizados no treinamento. Ela ajuda a identificar overfitting e a comparar diferentes modelos ou configurações antes da avaliação final no conjunto de teste.

c) A Regressão Logística inicialmente calcula uma combinação linear das variáveis de entrada. Essa saída é passada pela função sigmoide, que transforma o resultado em uma probabilidade entre 0 e 1. Depois, um limiar, como 0,5, é utilizado para transformar essa probabilidade em uma classe. Com limiar de 0,5, valores abaixo de 0,5 pertencem a uma classe e valores iguais ou superiores a 0,5 pertencem à outra.








