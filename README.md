## Regressão Linear

Este repositório contém a resolução da atividade do módulo 18 do curso de Cientista de Dados da EBAC.

O objetivo do projeto é desenvolver um modelo de Regressão Linear Múltipla para prever o valor de aluguel de imóveis com base em suas características.

**Base de dados utilizada**: ALUGUEL_MOD12.csv (7.203 imóveis, com metragem, número de quartos/banheiros/suítes/vagas e valor de condomínio). Outliers de valor de aluguel, condomínio e metragem foram mantidos (representam imóveis de alto padrão, não erros); apenas 43 linhas com valor de condomínio maior que o do aluguel — inconsistência de dados — foram removidas.

**Etapas do projeto**:

* Análise exploratória dos dados (EDA) para extrair insights sobre as variáveis;

* Desenvolvimento e treinamento do modelo de regressão linear;

* Avaliação de desempenho utilizando a métrica R².

## Resultados

| Modelo | R² (treino) | R² (teste) |
|---|---|---|
| Regressão Linear Simples (apenas `Metragem`) | 0,54 | 0,58 |
| Regressão Linear Múltipla (todas as variáveis) | 0,62 | 0,65 |

A regressão múltipla superou a simples em ambos os conjuntos, confirmando que características além da metragem (número de quartos, vagas, valor de condomínio, etc.) agregam poder explicativo ao modelo. Em ambos os casos, o R² de teste ficou próximo (ou levemente acima) do R² de treino, indicando boa generalização, sem sinais de overfitting.

## Tecnologias

- Python, pandas, numpy
- scikit-learn (LinearRegression, train_test_split)
- matplotlib, seaborn, plotly

## Como executar

1. Instale as dependências: `pip install pandas numpy scikit-learn matplotlib seaborn plotly`.
2. Coloque `ALUGUEL_MOD12.csv` no mesmo diretório do notebook.
3. Execute `Profissao Cientista de Dados M18 Pratique.ipynb` em ordem.
