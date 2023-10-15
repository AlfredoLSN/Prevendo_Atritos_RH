# Previsão de Atrito de Funcionários

Este README fornece uma visão detalhada do código e de sua funcionalidade para prever o atrito de funcionários usando um conjunto de dados e diferentes algoritmos de aprendizado de máquina. O código usa Python com bibliotecas como Pandas, Seaborn, Matplotlib, Scikit-Learn e TensorFlow. O README está estruturado para ajudar os usuários a entender o código, seu propósito e como executá-lo de forma eficaz.

## Tabela de Conteúdo
1. [Introdução](#1.introdução)
2. [Requisitos](#2-requisitos)
3. [Estrutura do Código](#3-estrutura-do-código)
4. [Pré-processamento de Dados](#4-pré-processamento-de-dados)
5. [Análise Exploratória de Dados](#5-análise-exploratória-de-dados)
6. [Modelos de Aprendizado de Máquina](#6-modelos-de-aprendizado-de-máquina)
   - [Regressão Logística](#regressão-logística)
   - [Random Forest](#random-forest)
   - [Rede Neural](#rede-neural)
7. [Avaliação do Modelo](#7-avaliação-do-modelo)
8. [Salvando o Modelo](#8-salvando-o-modelo)
9. [Usando o Modelo Salvo](#9-usando-o-modelo-salvo)
10. [Conclusão](#10-conclusão)

---

## 1. Introdução

Este código é projetado para prever o atrito de funcionários usando um conjunto de dados fornecido. Ele inclui pré-processamento de dados, análise exploratória de dados e a implementação de três modelos de aprendizado de máquina: Regressão Logística, Random Forest e uma Rede Neural. O código também avalia os modelos e fornece a opção de salvar o modelo de melhor desempenho para previsões futuras.

## 2. Requisitos

Antes de executar o código, certifique-se de ter as seguintes bibliotecas Python instaladas:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- tensorflow (para a rede neural)
- pickle (para salvar o modelo)

Você pode instalar essas bibliotecas usando o seguinte comando:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn tensorflow pickle
```
## 3. Estrutura do Código

   O código está organizado da seguinte forma:

   - Importação das bibliotecas necessárias.
   - Leitura do conjunto de dados de funcionários de um arquivo CSV.
   - Pré-processamento de dados para lidar com variáveis categóricas e escalar características numéricas.
   - Análise exploratória de dados, incluindo visualizações.
   - Implementação de três modelos de aprendizado de máquina: Regressão Logística, Random Forest e uma Rede Neural.
   - Avaliação do modelo usando métricas como acurácia, precisão, recall, pontuação F1 e matriz de confusão.
   - Salvando o melhor modelo para uso futuro.

## 4. Pré-processamento de Dados

   O código pré-processa os dados convertendo variáveis categóricas em formato codificado one-hot e escalando características numéricas usando escalonamento Min-Max. Isso garante que os dados estejam em um formato adequado para algoritmos de aprendizado de máquina.

## 5. Análise Exploratória de Dados

   A análise exploratória de dados (EDA) é realizada para obter insights sobre o conjunto de dados. Diversas visualizações são usadas, incluindo histogramas, mapas de calor e gráficos de caixa, para entender a distribuição e as relações entre diferentes atributos no conjunto de dados.

## 6. Modelos de Aprendizado de Máquina

   **Regressão Logística**
   - Um modelo de Regressão Logística é treinado para prever o atrito de funcionários.
   - O modelo é treinado com os dados pré-processados.
   - Métricas de desempenho do modelo são calculadas.

   **Random Forest**
   - Um Classificador Random Forest é treinado para prever o atrito de funcionários.
   - O modelo é treinado com os dados pré-processados.
   - Métricas de desempenho do modelo são calculadas.

   **Rede Neural**
   - Uma Rede Neural com três camadas ocultas é treinada para prever o atrito de funcionários.
   - O modelo é treinado usando TensorFlow.
   - Métricas de desempenho do modelo são calculadas.

## 7. **Avaliação do Modelo**

   Para avaliar o desempenho dos modelos de aprendizado de máquina, foram calculadas as métricas de precisão, recall e pontuação F1 para cada um deles. Abaixo estão as estatísticas para cada modelo:

   **Regressão Logística:**
       |              | precision | recall | f1-score | support |
|--------------|-----------|--------|----------|---------|
| 0            | 0.90      | 0.97   | 0.93     | 306     |
| 1            | 0.74      | 0.45   | 0.56     | 62      |
|              |           |        |          |         |
| accuracy     |           |        | 0.88     | 368     |
| macro avg    | 0.82      | 0.71   | 0.75     | 368     |
| weighted avg | 0.87      | 0.88   | 0.87     | 368     |

   **Random Forest::**
       |              | precision | recall | f1-score | support |
|--------------|-----------|--------|----------|---------|
| 0            | 0.86      | 0.99   | 0.92     | 306     |
| 1            | 0.80      | 0.19   | 0.31     | 62      |
|              |           |        |          |         |
| accuracy     |           |        | 0.86     | 368     |
| macro avg    | 0.83      | 0.59   | 0.62     | 368     |
| weighted avg | 0.85      | 0.86   | 0.82     | 368     |

   **Redes Neurais:**
       |              | precision | recall | f1-score | support |
|--------------|-----------|--------|----------|---------|
| 0            | 0.88      | 0.88   | 0.88     | 306     |
| 1            | 0.42      | 0.42   | 0.42     | 62      |
|              |           |        |          |         |
| accuracy     |           |        | 0.80     | 368     |
| macro avg    | 0.65      | 0.65   | 0.65     | 368     |
| weighted avg | 0.80      | 0.80   | 0.80     | 368     |


## 8. Salvando o Modelo

   O código fornece uma opção para salvar o modelo de melhor desempenho (neste caso, a Rede Neural) usando a biblioteca pickle. Isso permite que você use o modelo treinado para previsões futuras sem a necessidade de reentrená-lo.

## 9. Usando o Modelo Salvo

   O código demonstra como carregar o modelo salvo e fazer previsões em novos dados. Ele inclui as etapas de pré-processamento necessárias e a previsão do modelo.

## 10. Conclusão

   Este código serve como um exemplo abrangente de um projeto de ciência de dados que inclui pré-processamento de dados, análise exploratória de dados e a implementação de modelos de aprendizado de máquina para um problema do mundo real: prever o atrito de funcionários. Os usuários podem aprender com o código e adaptá-lo para seus próprios projetos.

   Sinta-se à vontade para modificar e estender este código para diferentes conjuntos de dados e casos de uso. Se você tiver alguma dúvida ou precisar de assistência adicional, não hesite em entrar em contato.
