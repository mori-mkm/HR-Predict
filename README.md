# Análise de Rotatividade de Funcionários

Este projeto visa prever a probabilidade de demissão de funcionários com base em dados históricos, utilizando aprendizado de máquina. O objetivo é identificar os principais fatores que contribuem para a rotatividade e fornecer insights acionáveis para melhorar a retenção de talentos.

## Etapas do Projeto

### 1. Preparação dos Dados
- Realizada seleção e codificação de variáveis categóricas e contínuas.
- Divisão dos dados em conjuntos de treino e teste (80/20).

### 2. Construção do Modelo Inicial
- Utilizado um modelo de regressão logística para prever a probabilidade de demissão.
- Avaliação inicial com métricas de desempenho: Acurácia, F1-Score, Precisão e Recall.

### 3. Balanceamento de Classes
- Aplicado **SMOTE** (Synthetic Minority Oversampling Technique) para lidar com o desbalanceamento das classes.
- Re-treinamento do modelo com os dados balanceados.

### 4. Ajuste de Threshold
- Ajustado o threshold de decisão para melhorar o recall (identificação de funcionários propensos à saída).

### 5. Identificação de Variáveis Relevantes
- Coeficientes da regressão logística foram analisados para identificar as variáveis com maior impacto na probabilidade de demissão.
- Gráficos foram gerados para visualização das 10 variáveis mais relevantes.

### 6. Validação do Modelo
- Validação cruzada (5-fold) realizada para verificar a robustez do modelo.
- Avaliação final no conjunto de teste com métricas de desempenho (Acurácia e F1-Score).

## Resultados

### Métricas do Modelo Balanceado e Threshold Ajustado
- **Acurácia**: 0.73
- **F1-Score**: 0.36
- **Recall**: Melhorado para 0.74, indicando maior capacidade de identificar funcionários propensos à demissão.

### Variáveis Mais Relevantes
1. `OverTime_Yes`
2. `Department_Research & Development`
3. `Department_Sales`
4. `MaritalStatus_Married`
5. `YearsInCurrentRole`

### Validação Cruzada
- **F1-Score Médio**: 0.32
- **Desvio Padrão do F1-Score**: 0.03

## Tecnologias Utilizadas
- **Python**
  - `pandas`, `numpy`: Manipulação e análise de dados.
  - `scikit-learn`: Modelagem e métricas de aprendizado de máquina.
  - `imblearn`: Balanceamento de classes com SMOTE.
  - `matplotlib`, `seaborn`: Visualização de dados.

## Próximos Passos
1. Testar modelos mais avançados, como **Random Forest** ou **Gradient Boosting**.
2. Explorar novas variáveis por meio de engenharia de features.
3. Refinar o balanceamento de classes com técnicas adicionais.

## Como Utilizar
1. Clone este repositório: 
   ```bash
   git clone https://github.com/seu-usuario/employee-attrition-analysis.git
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o script principal:
   ```bash
   python employee_attrition_analysis.py
   ```

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença
Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais informações.

