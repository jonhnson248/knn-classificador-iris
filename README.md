# Classificador de Espécies Iris com KNN e Grid Search

Este projeto foi desenvolvido como parte da disciplina de Inteligência Artificial / Aprendizado de Máquina. O objetivo principal é construir, avaliar e otimizar um modelo de Machine Learning baseado no algoritmo **KNN (K-Nearest Neighbors)** para classificar três espécies de flores Iris (Setosa, Versicolor e Virginica) com base em suas medidas morfológicas.

## 🚀 Engenharia e Etapas do Projeto

O projeto foi construído seguindo rigorosamente as boas práticas de Ciência de Dados, dividindo-se em:

1. **Análise de Dimensões:** Exploração e preparação dos dados do dataset clássico `Iris` do Scikit-Learn.
2. **Isolamento de Dados (Validação Racional):** Divisão controlada da base em dados de Treino (80%) e Teste (20%) utilizando amostragem estratificada para evitar o vazamento de dados (*data leakage*).
3. **Avaliação Detalhada de Métricas:** Implementação e interpretação de:
   * Acurácia Geral
   * Matriz de Confusão (Mapeamento de erros e acertos cruzados)
   * Relatório de Classificação (Precision, Recall e F1-Score por espécie)
4. **Análise de Sensibilidade do Hiperparametro K:** Laço de repetição automático investigando o comportamento da acurácia com valores de $K$ variando de 1 a 10.
5. **Otimização Robusta (Grid Search):** Implementação do `GridSearchCV` configurado com **30 realizações (Cross-Validation com 30 folds)** para eliminar a interferência de cortes de dados puramente aleatórios e encontrar de forma justa o melhor valor de vizinhos ($K$).
6. **Análise de Estabilidade Estocástica:** Plotagem de um gráfico Box-plot avaliando a consistência e dispersão das notas de acurácia obtidas pelo modelo vencedor ao longo das 30 provas distintas, identificando inclusive a presença de cenários de maior dificuldade (*outliers*).

## 📊 Principais Resultados

* **Melhor Hiperparâmetro Encontrado:** O Grid Search apontou $K = 6$ como o ponto ideal de equilíbrio para o classificador.
* **Consistência:** O modelo demonstrou altíssima estabilidade, atingindo uma mediana de acurácia de 100% na maior parte das fatias de teste, com uma flutuação mínima (outlier) isolada na faixa de 80% em cenários de testes severos.

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Google Colab** (Ambiente de desenvolvimento)
* **Pandas** & **NumPy** (Manipulação de estruturas de dados)
* **Scikit-Learn** (Módulos de Machine Learning, Metrics e Model Selection)
* **Matplotlib** (Visualização gráfica e plotagem estatística)
