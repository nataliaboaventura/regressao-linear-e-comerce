# Construindo um modelo de Regressão para marketing

Este projeto foi desenvolvido como parte do curso de Análise de Dados da escola DNC. O objetivo é construir um modelo de regressão linear para prever o retorno de vendas com base em investimentos em plataformas de publicidade online, como YouTube, Facebook e jornal.

## Contexto do Projeto

Uma empresa está investindo mensalmente em plataformas de publicidade online, como YouTube, Facebook e jornal, para a prospecção de leads (pessoas interessadas em seus produtos). Para acompanhar o desempenho desses investimentos, a empresa registra todos os gastos com publicidade e os retornos de vendas gerados a partir desses investimentos.

O objetivo deste projeto é:
1. Analisar a relação entre os investimentos em publicidade e as vendas.
2. Identificar os fatores que mais impactam na geração de leads.
3. Criar um modelo de predição para estimar o retorno de vendas com base nos investimentos.

## Sobre os Dados

O conjunto de dados foi importado diretamente de um link do Google Sheets e contém informações sobre os investimentos feitos em:
- **YouTube**
- **Facebook**
- **Newspaper (Jornal)**

Além disso, o dataset inclui a quantidade de vendas geradas a partir desses investimentos.

---

## Análise Descritiva e Exploratória

### Histogramas
- **YouTube**: A distribuição é relativamente simétrica, com alguns investimentos mais altos.
- **Facebook**: A distribuição é um pouco assimétrica, com alguns investimentos mais baixos.
- **Newspaper**: A distribuição tem uma cauda longa à direita, indicando alguns investimentos altos.
- **Sales**: A distribuição é relativamente simétrica, com alguns valores mais altos.

### Boxplots
- **YouTube**: A distribuição é relativamente simétrica, sem outliers significativos.
- **Facebook**: A distribuição é assimétrica, com alguns investimentos mais baixos.
- **Newspaper**: A distribuição tem uma cauda longa à direita, indicando alguns investimentos altos.
- **Sales**: A distribuição é relativamente simétrica, sem outliers significativos.

### Matriz de Correlação
- **YouTube** tem uma correlação forte com **sales** (0.78), indicando que investimentos no YouTube têm um impacto significativo nas vendas.
- **Facebook** tem uma correlação moderada com **sales** (0.60).
- **Newspaper** tem uma correlação fraca com **sales** (0.25), sugerindo que investimentos em jornal têm um impacto menor nas vendas.

### Pairplot
O pairplot mostra as relações entre todas as variáveis. A relação linear entre **YouTube** e **sales** é claramente visível, enquanto **Facebook** e **Newspaper** têm relações menos evidentes.

---

## Modelagem

### Separação dos Dados
- **Variáveis independentes (x)**: YouTube, Facebook, Newspaper.
- **Variável dependente (y)**: Sales.
- Os dados foram divididos em conjuntos de treino (70%) e teste (30%).

### Treinamento do Modelo
Um modelo de regressão linear foi treinado usando `LinearRegression()` do `sklearn`.

### Previsões
O modelo foi usado para prever as vendas (`y_pred`) no conjunto de teste.

---

## Avaliação do Modelo

### Métricas de Avaliação
- **Erro Quadrático Médio (MSE)**: 4.70  
  O MSE mede a média dos erros ao quadrado entre os valores reais e previstos. Um valor de 4.70 indica que o modelo tem um erro médio relativamente baixo.
- **Coeficiente de Determinação (R²)**: 0.86  
  O R² de 0.86 indica que o modelo explica 86% da variância nas vendas. Isso é um bom resultado, mostrando que o modelo se ajusta bem aos dados.

### Coeficientes do Modelo
Os coeficientes do modelo de regressão linear são:
- **YouTube**: 0.045
- **Facebook**: 0.188
- **Newspaper**: 0.002

Isso significa:
- Para cada unidade de investimento no YouTube, as vendas aumentam em 0.045 unidades.
- Para cada unidade de investimento no Facebook, as vendas aumentam em 0.188 unidades.
- Para cada unidade de investimento em jornal, as vendas aumentam em 0.002 unidades.

---

## Visualizações Adicionais

### Gráfico de Regressão (regplot)
O gráfico de regressão entre **YouTube** e **sales** mostra uma relação linear clara, confirmando a forte correlação observada na matriz de correlação.

### Vendas Reais vs. Vendas Previstas
O gráfico de dispersão compara as vendas reais com as vendas previstas pelo modelo, mostrando uma boa aderência dos dados à linha de referência.

---

## Conclusões e Recomendações

### Conclusões
- O modelo de regressão linear se ajustou bem aos dados, com um R² de 0.86 e um MSE de 4.70.
- A visualização de "Vendas Reais vs. Vendas Previstas" confirma que o modelo tem uma boa capacidade de previsão.
- **YouTube** e **Facebook** são os canais de marketing que mais impactam as vendas, enquanto **Newspaper** tem um impacto mínimo.

### Recomendações
- A empresa pode priorizar investimentos no **YouTube** e no **Facebook** para maximizar o retorno das vendas.
- Investimentos em **Newspaper** podem ser reduzidos ou reavaliados, já que têm um impacto menor nas vendas.

---

## Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/regressao-linear-e-comerce.git
