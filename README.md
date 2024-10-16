# Análise de Preços de Imóveis na Califórnia

## Visão Geral do Projeto

Este projeto envolve a análise dos preços de imóveis na Califórnia usando um dataset do Kaggle. O objetivo é ajudar um empresário do setor imobiliário a determinar qual bairro na Califórnia oferece a maior margem de lucro para construção de residências, considerando um investimento inicial fixo de $200.000.

**Fonte do Dataset**: [California Housing Prices Dataset on Kaggle](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

## Objetivo

O principal objetivo deste projeto é avaliar diferentes bairros na Califórnia e determinar o melhor lugar para um investidor imobiliário construir residências. A análise considera vários fatores, como preços de imóveis, renda média, número de cômodos e dados sobre famílias para tomar decisões baseadas em dados.

A pergunta central a ser respondida é: **Em qual bairro o investidor deve construir para maximizar o lucro?**

## Ferramentas e Bibliotecas

As seguintes bibliotecas Python foram utilizadas para realizar a análise de dados, visualização e modelagem de machine learning:

- **pandas**: Manipulação e análise de dados.
- **numpy**: Operações matemáticas.
- **seaborn**: Visualização de dados.
- **matplotlib**: Criação de gráficos e visualizações.
- **sklearn (scikit-learn)**: Para construção e avaliação de modelos, incluindo:
  - `LinearRegression`: Regressão linear simples.
  - `DecisionTreeRegressor`: Árvores de decisão para problemas de regressão.
  - `RandomForestRegressor`: Aprendizado em conjunto usando múltiplas árvores de decisão.
  - `KNeighborsRegressor`: K-vizinhos mais próximos para regressão.
  - `SVR`: Support Vector Regressor para encontrar o melhor hiperplano de separação.
  - `GridSearchCV`: Ajuste de hiperparâmetros para otimização do desempenho do modelo.
  - `StandardScaler`: Normalização dos dados para melhor desempenho em machine learning.
  - `train_test_split`: Divisão dos dados em conjuntos de treinamento e teste.
  - `cross_val_score`: Validação cruzada para avaliar a precisão do modelo.

## Fluxo do Projeto

### 1. Carregamento dos Dados
O dataset é carregado usando `pandas`. Ele contém características importantes como:
- `households`: Número de famílias no bairro.
- `median_income`: Renda média das famílias.
- `total_rooms`: Total de cômodos disponíveis em cada bairro.

### 2. Exploração e Pré-processamento dos Dados
- **Estatísticas Descritivas**: Um resumo do dataset é gerado usando `.describe()` para entender a distribuição de variáveis-chave, como preços de casas, tamanho das famílias, etc.
- **Limpeza de Dados**: Valores ausentes e outliers são tratados adequadamente para garantir uma análise robusta.
  
### 3. Visualização dos Dados
- Diversos gráficos são criados para explorar as relações entre as variáveis. Por exemplo, a relação entre `median_income` e `median_house_value` é analisada para identificar tendências que possam orientar decisões de investimento.
- Mapas de correlação e gráficos de dispersão são usados para visualizar padrões potenciais entre as variáveis.

### 4. Construção de Modelos
Vários modelos de machine learning são treinados e avaliados para prever preços de imóveis e orientar a tomada de decisões para maximizar os retornos:
- **Regressão Linear**: Estabelece uma linha de base para a previsão dos preços de imóveis com base nas variáveis.
- **Árvores de Decisão e Florestas Aleatórias**: Modelos mais avançados para capturar relações complexas nos dados.
- **K-Nearest Neighbors**: Agrupamento de casas por similaridade e uso dos vizinhos para prever preços.
- **Support Vector Machines (SVR)**: Encontra a melhor fronteira de decisão em um espaço de alta dimensão para fazer previsões.

### 5. Ajuste de Modelos
- **Validação Cruzada**: Cada modelo passa por validação cruzada para estimar seu desempenho em dados não vistos.
- **GridSearchCV**: Ajuste de hiperparâmetros é realizado em modelos como Árvores de Decisão e Florestas Aleatórias para encontrar a melhor configuração para precisão e generalização.

### 6. Métricas de Avaliação
Os modelos são avaliados com base em:
- **Erro Quadrático Médio (MSE)**: Mede a diferença média quadrática entre os valores previstos e reais.
- **Validação Cruzada**: Avalia a robustez dos modelos em diferentes divisões do dataset.

### 7. Insights e Recomendações
- Com base na análise, certos bairros são identificados como mais rentáveis para construção, considerando fatores como `median_income` e `median_house_value`.
- Resultados visuais e quantitativos fornecem insights acionáveis sobre onde o empresário imobiliário deve investir para maximizar os retornos.

## Resultados e Conclusão

O projeto identifica com sucesso bairros potenciais na Califórnia onde um investimento fixo pode gerar os maiores retornos. Vários modelos são usados para prever os preços das casas, e a análise oferece recomendações claras, embasadas por visualizações e modelos de ciência de dados.

Este projeto demonstra habilidades em:
- Limpeza e pré-processamento de dados.
- Análise Exploratória de Dados (EDA) com visualizações.
- Construção e ajuste de modelos de machine learning.
- Extração de insights práticos de dados.
