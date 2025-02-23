# Cálculo de Métricas de Avaliação de Aprendizado

# Avaliação de Métricas de Classificação com CNN no MNIST

Este projeto tem como objetivo calcular e analisar as principais métricas de avaliação de modelos de classificação, como **acurácia**, **sensibilidade (recall)**, **especificidade**, **precisão** e **F-score**, utilizando uma rede neural convolucional (CNN) treinada no dataset MNIST. O código foi desenvolvido para rodar no **Google Colab**.

## Descrição do Projeto

O código implementa uma CNN para classificar imagens do dataset MNIST, que contém dígitos manuscritos de 0 a 9. Após o treinamento, o modelo é avaliado utilizando uma matriz de confusão e as seguintes métricas:

1. **Sensibilidade (Recall)**: Proporção de verdadeiros positivos identificados corretamente.
2. **Especificidade**: Proporção de verdadeiros negativos identificados corretamente.
3. **Acurácia**: Proporção de previsões corretas em relação ao total de previsões.
4. **Precisão**: Proporção de verdadeiros positivos em relação a todos os positivos previstos.
5. **F-score**: Média harmônica entre precisão e sensibilidade.

Além disso, o código gera visualizações, como gráficos de acurácia ao longo das épocas e uma matriz de confusão normalizada.

## Como Executar o Código no Google Colab

1. **Acesse o Google Colab**:
   - Abra o [Google Colab](https://colab.research.google.com/).

2. **Copie o Código**:
   - Crie um novo notebook no Colab.
   - Copie e cole o código fornecido no notebook.

3. **Execute o Código**:
   - Execute cada célula do notebook sequencialmente.
   - O código carrega o dataset MNIST, treina a CNN e calcula as métricas de avaliação.

4. **Resultados**:
   - Gráfico de acurácia do treino e validação.
   - Matriz de confusão normalizada.
   - Métricas de avaliação impressas no console.

## Estrutura do Código

- **Carregamento e Pré-processamento dos Dados**:
  - O dataset MNIST é carregado e normalizado.
  - As imagens são redimensionadas para incluir a dimensão do canal.

- **Construção do Modelo**:
  - Uma CNN é construída com camadas convolucionais, de pooling e densas.
  - O modelo é compilado com o otimizador Adam e a função de perda `sparse_categorical_crossentropy`.

- **Treinamento**:
  - O modelo é treinado por 5 épocas.
  - A acurácia do treino e validação é monitorada.

- **Avaliação**:
  - A matriz de confusão é gerada a partir das previsões do modelo.
  - As métricas de avaliação são calculadas e exibidas.

## Resultados Esperados

- Gráfico de acurácia mostrando o desempenho do modelo ao longo das épocas.
- Matriz de confusão normalizada para análise do desempenho por classe.
- Métricas de avaliação impressas no console para cada classe.

## Exemplo de Saída

```plaintext
Sensibilidade (Recall): [0.98, 0.99, 0.97, ...]
-----------------------
Especificidade: [0.99, 0.99, 0.98, ...]
-----------------------
Acurácia: 0.985
-----------------------
Precisão: [0.98, 0.99, 0.97, ...]
-----------------------
F-score: [0.98, 0.99, 0.97, ...]
