# MÓDULO 21 - Projeto de Credit Score - Árvore de Decisão

## Descrição

Este projeto tem como objetivo aplicar o algoritmo de **Árvore de Decisão** para prever o **score de crédito** de clientes, avaliando o desempenho do modelo com diferentes conjuntos de variáveis e comparando com o modelo de **Naive Bayes** desenvolvido no Módulo 20.

## Etapas do Projeto

1. **Carregamento e Verificação dos Dados**
   - Leitura das bases de treino (`X_train`, `y_train`) e teste (`X_test`, `y_test`).
   - Verificação da consistência entre o número de linhas nas bases.
   - Confirmação de que `y` contém apenas a variável `score`.
   - Checagem do balanceamento da variável `score` na base de teste.

2. **Aplicação do Algoritmo de Árvore de Decisão**
   - O algoritmo da árvore de decisão funciona dividindo os dados em ramos baseados nos valores das variáveis preditoras. A cada divisão, o algoritmo escolhe a variável e o ponto de corte que melhor separa os dados de acordo com um critério (neste caso, Gini).
   - Após o treinamento, o modelo é avaliado por meio de métricas como **acurácia** e **matriz de confusão**.

3. **Treinamento do Modelo**
   - Treinamento do modelo com `DecisionTreeClassifier(criterion='gini', random_state=0)`.
   - Cálculo da **acurácia** do modelo na base de treino.

4. **Avaliação na Base de Teste**
   - Aplicação do modelo aos dados de teste.
   - Avaliação por meio da acurácia e comparação com os resultados da base de treino.

5. **Visualização da Árvore de Decisão**
   - Plotagem gráfica da estrutura da árvore gerada pelo modelo.

6. **Identificação das Principais Variáveis**
   - Identificação das **duas principais features** com maior importância no modelo treinado.

7. **Modelo Reduzido com 2 Variáveis**
   - Recriação do modelo utilizando apenas as 2 variáveis mais importantes.
   - Avaliação da performance e comparação com o modelo completo.
   - Obteve-se uma acurácia levemente inferior, mas, ainda sim muito alta = 0,95

8. **Comparação com o Modelo de Naive Bayes (Módulo 20)**
- Ambos os modelos (Naive Bayes e Árvore de Decisão) obtiveram **acurácia de 0,9756** na base de teste.
- Cada um cometeu apenas **um erro de classificação**, o que demonstra uma **excelente capacidade de generalização**.
- Considerando a performance equivalente, pode-se afirmar que **ambos os modelos se adequaram muito bem aos dados**, sendo alternativas viáveis para a classificação de score de crédito.
- A escolha entre um ou outro pode depender de fatores como **interpretabilidade** (onde a árvore de decisão pode se destacar) ou **simplicidade computacional** (vantagem do Naive Bayes).

## Conclusão

O modelo de Árvore de Decisão apresentou desempenho equivalente ao Naive Bayes, com **alta acurácia e baixo número de erros**. Ambos os modelos demonstraram boa capacidade de generalização, sendo adequados para a tarefa de classificação de score de crédito.
