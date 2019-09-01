# Aprendizado de Máquina com Python
Adriano Sanick Padilha e José Carlos Bins Filho



<a href='https://www.ime.unicamp.br/~dias/Intoduction%20to%20Statistical%20Learning.pdf'>  <img src='ML_MEDIUM.jpeg' /></a>

# Métricas
### **MAE e RMSE - Qual métrica é melhor?**
Erro Absoluto Médio versus Raiz do Erro Quadrático Médio

**Definições**

- *Erro Absoluto Médio* (MAE): o MAE mede a magnitude média dos erros em um conjunto de previsões, sem considerar o seu sinal (positivo ou negativo). É a média na amostra de teste das diferenças absolutas entre a previsão e a observação real, onde todas as diferenças individuais têm peso igual.

$$\frac 1n\sum_{i=1}^n|y_i-\hat{y}_i|$$ 

- *Raiz do Erro Médio Quadrático* (RMSE): RMSE é uma regra de pontuação quadrática que também mede a magnitude média do erro. É a raiz quadrada da média das diferenças quadráticas entre previsão e observação real.

$$\sqrt{\frac 1n\sum_{i=1}^n(y_i-\hat{y}_i)^2}$$

**Comparação**

- **Semelhanças:** O MAE e o RMSE expressam erro médio de previsão do modelo em unidades da variável de interesse. Ambas as métricas podem variar de 0 a +∞ e são indiferentes à direção dos erros. São pontuações negativamente orientadas, o que significa que valores mais baixos são melhores.


- **Diferenças:** Obter a raiz quadrada dos erros quadráticos médios tem algumas implicações interessantes para o RMSE. Como os erros são elevados ao quadrado antes da média, o RMSE atribui um peso relativamente alto a erros grandes. Isso significa que o RMSE deve ser mais útil quando erros grandes são particularmente indesejáveis. 

**Discussão**

Há casos em que o MAE é constante e o RMSE aumenta à medida que a variação associada à distribuição de frequência das magnitudes de erro também aumenta. O RMSE não aumenta necessariamente com a variação dos erros. **O RMSE aumenta com a variação da distribuição de frequência das magnitudes de erro.** É importante ter em mente que poderá haver casos em que esta da variação da distribuição de frequência das magnitudes dos erros seja de interesse, mas na maioria dos casos a variação dos erros é de maior interesse.

Outra implicação da fórmula RMSE que não é discutida frequentemente tem a ver com o **tamanho da amostra**. Usando o MAE, podemos colocar um limite inferior e superior no RMSE.

- **[ MAE ]  ≤  [ RMSE ]:** O resultado do RMSE sempre será maior ou igual ao MAE. Se todos os erros tiverem a mesma magnitude, então RMSE = MAE.

- **[ RMSE ]  ≤  [ MAE * sqrt (n) ]:**  Sabendo que **n** é o número de amostras de teste. A diferença entre o RMSE e o MAE é maior quando todo o erro de previsão vem de uma única amostra de teste.

Focalizando o limite superior, isso significa que o RMSE tem uma tendência a ser cada vez maior que o MAE à medida que o tamanho da amostra de teste aumenta.
Isso pode ser problemático ao comparar os resultados do RMSE calculados em diferentes amostras de teste, o que é frequentemente o caso na modelagem do mundo real.

O RMSE tem o benefício de penalizar erros grandes, por isso pode ser mais apropriado em alguns casos, por exemplo, se a penalização dada devido a um erro igual a 10 é mais do que o dobro do que a penalização dada por um erro igual a 5.

Do ponto de vista da interpretação, o MAE é claramente o vencedor. O RMSE não descreve o erro médio sozinho e tem outras implicações mais difíceis de entender. Por outro lado, uma vantagem distinta do RMSE sobre o MAE é que o RMSE evita o uso do valor absoluto, o que é indesejável em muitos cálculos matemáticos.


## 3 - Regressão Linear
### 31_RegressaoLinear.ipynb

- Apresenta um passo a passo para contrução de um modelo de regressão linear utilizando como exemplo o *Dataset* **"USA_Housing.csv"** extraído do site www.kaggle.com. Também é discutido as métricas de avaliação para este modelo.

### 32_ExercicioRegressaoLinear.ipynb
- O exercício proposto utiliza o *dataset* retirado do site www.kaggle.com. Este dataset é referente uma empresa de comércio eletrônico com sede na cidade de Nova York que vende roupas on-line.

### 33_SolucaoRegressaoLinear.ipynb
- Solução para o exercício proposto.
