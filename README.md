# Combinação de modelos - Parte 2 - Random Forest

Ao longo desta atividade tentei desenvolver um algoritmo de Random Forest capaz de ser aplicado para modelos de `classificação` e `regressão`. As seguintes características compõem o algoritmo:

- Seleção do modelo de decisão: Regressão (regressor) ou classificação (classifier)
- Separação dos dados a serem preenchidos/sugeridos pelo modelo
- Criação de amostras (amostragem com repetição)
- Avaliação da quantidade de dados repetidos
- Seleção de colunas aleatórias para compor as amostras (feature selection)
- Avaliação de colunas por amostra
- Geração de modelos de árvore de decisão para cada amostra criada:
  - Separação em dados de treino e teste
  - Criação e treino da árvore de decisão
  - Pós-poda utilizando ccp_alphas para selecionar a *melhor árvore* com o melhor "score"
  - Seguido pela obtenção dos dados antes faltantes (separados no segundo item)  agora sugeridos pela *melhor árvore* 
- Agregação de acordo com o modelo de decisão (classificação ou regressão)
  
A função retorna as melhores previsões geradas por cada modelo gerado para cada amostragem e também, por meio da agregação, os valores mais adequados, filtrados a partir da saída dos modelos de aprendizado (de acordo com a premissa da Random Forest), para substituir os dados faltantes.

Uma segunda função para anexar os dados obtidos pelo **Random Forest** (agregação *bagging*) ao banco de dados também está presente.




## Bibliotecas
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Scikit-learn](https://scikit-learn.org/stable/)
- [Random](https://docs.python.org/pt-br/3.13/library/random.html)
- [Collections](https://docs.python.org/3/library/collections.html)
