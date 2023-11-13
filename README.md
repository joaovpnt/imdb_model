# Machine Learning Models with IMDB - A Sentiment Analysis

## Resumo do Dataset IMDB

O conjunto de dados IMDB é uma coleção de informações sobre filmes, incluindo títulos, gêneros, diretores, elenco, sinopses e classificações. É comumente usado para treinar modelos de análise de sentimento, permitindo a classificação de opiniões de usuários como positivas, negativas ou neutras com base em críticas e avaliações.

## Distribuição dos Dados e Informações Técnicas

O conjunto de dados IMDB consiste em 50 mil resenhas de filmes, projetado para processamento de linguagem natural e análise de texto. Este conjunto de dados é usado para classificação de sentimento binário, onde os valores numéricos representam avaliações positivas e negativas, oferecendo uma quantidade substancialmente maior de dados em comparação com conjuntos de dados de referência anteriores. É composto por um conjunto de 25.000 resenhas de filmes altamente polarizadas para fins de treinamento e 25.000 para fins de teste. Dessa forma, os algoritmos de classificação ou aprendizado profundo são utilizados para prever o número de avaliações positivas e negativas.

## Processo de Limpeza da Base

Durante o processo de limpeza dos dados, várias etapas foram seguidas para preparar o texto para análise. Isso incluiu o uso das seguintes técnicas:

- **BeautifulSoup e a função `get_text()`:**
  - Utilização da biblioteca BeautifulSoup para remover marcações HTML e obter o texto principal das páginas da web.
  - A função `get_text()` é empregada para extrair somente o texto relevante, eliminando quaisquer elementos de formatação ou código HTML indesejados.

- **Expressões regulares (Regex):**
  - Emprego de expressões regulares para identificar e remover caracteres especiais, pontuações e outros elementos não essenciais para a análise de sentimentos.
  - As expressões regulares permitem a identificação de padrões específicos no texto, facilitando a limpeza e manipulação dos dados textuais.

- **Remoção de stopwords com NLTK:**
  - Utilização das stopwords da biblioteca NLTK (Natural Language Toolkit) para eliminar palavras comuns que não contribuem significativamente para a análise de sentimentos.
  - As stopwords são palavras frequentes, como artigos e preposições, que geralmente são removidas durante o pré-processamento para focar nas palavras-chave que transmitem sentimentos e significado.

Essas etapas de limpeza são fundamentais para garantir a eficácia da análise de sentimentos e para fornecer aos modelos de aprendizado de máquina dados textuais que sejam relevantes e representativos do conteúdo das avaliações e críticas de filmes no conjunto de dados IMDB.

## Modelos

A seguir, são apresentados os modelos utilizados no contexto da análise de sentimentos com o conjunto de dados IMDB:

- **Logistic Regression:**
  - A regressão logística é um modelo de classificação frequentemente utilizado para problemas de classificação binária. Neste contexto, pode ser aplicada para prever a polaridade dos sentimentos associados às críticas de filmes.

- **Ridge Classifier:**
  - O classificador Ridge é uma variação do modelo de regressão logística que incorpora regularização L2. Ele é frequentemente empregado em tarefas de classificação para melhorar a generalização do modelo.

- **Random Forest Classifier:**
  - O classificador de floresta aleatória é um modelo de aprendizado de máquina que utiliza múltiplas árvores de decisão para realizar tarefas de classificação. Este modelo é conhecido por lidar bem com dados de alta dimensionalidade e por sua capacidade de lidar com overfitting.

- **Decision Tree Classifier:**
  - O classificador de árvore de decisão é um modelo de aprendizado de máquina que utiliza uma estrutura de árvore para realizar tarefas de classificação. É um modelo interpretável e fácil de compreender, o que o torna uma escolha popular em muitas aplicações.

- **Ada Boost Classifier:**
  - O classificador AdaBoost é um algoritmo de aprendizado de máquina que combina vários classificadores fracos para formar um classificador forte. Esse modelo é conhecido por sua capacidade de lidar com dados complexos e é frequentemente utilizado em problemas de classificação.


## Resultados

| Métrica | Logistic Regression | Ridge Classifier | Random Forest Classifier | Decision Tree Classifier | Ada Boost Classifier |
|---------|---------------------|------------------|--------------------------|-------------------------|----------------------|
| Acurácia | 0.8623 | 0.8578 | 0.8286 | 0.7107 | 0.7989 |
| Precisão | 0.8625 | 0.8584 | 0.8286 | 0.7107 | 0.8014 |
| Recall | 0.8623 | 0.8578 | 0.8286 | 0.7107 | 0.7989 |
| F1 Score | 0.8622 | 0.8577 | 0.8286 | 0.7107 | 0.7984 |

## Imagens

![Distribuição 1](https://github.com/joaovpnt/imdb_model/blob/main/images/distrib.png)
![Wordcloud](https://github.com/joaovpnt/imdb_model/blob/main/images/wordcloud.png)

