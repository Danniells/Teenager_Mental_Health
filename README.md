# Impact of Social Media on Teenagers' Mental Health

## 📌 About the Project
This repository contains a detailed analysis of the impact of social media use on teenagers' mental health, employing supervised and unsupervised Machine Learning techniques. The project's goal is to understand behavioral patterns — such as sleep hours, screen time, and physical activity — and their relationship with stress levels, anxiety, and the risk of depression. 

## 📊 Dataset
The dataset used (`Teen_Mental_Health_Dataset.csv`) was obtained via Kaggle (`algozee/teenager-menthal-healy`). It includes data from 1,200 students, covering:
- Daily social media time and usage of specific platforms (Instagram, TikTok, or both).
- Hours of sleep and screen time before bed.
- Academic performance, physical activity levels, and social interaction.
- Psychological indicators: stress levels, anxiety, addiction, and depression diagnosis (`depression_label`).

## 📂 Repository Structure
The investigation was divided into two analytical fronts, documented in the following Jupyter Notebooks:

### 1. `k_means.ipynb` (Unsupervised Learning)
The focus of this script is to discover hidden behavioral profiles within the database.
- **Feature Engineering:** Creation of crucial new health metrics, such as `sleep_deficit`, `screen_sleep_ratio`, and `mental_load_score`.
- **Preprocessing:** Mathematical standardization of numerical variables using `StandardScaler`.
- **Dimensionality Reduction:** Application of PCA (*Principal Component Analysis*) to optimize the vector space and eliminate redundancies, visually evaluating the explained variance.
- **Clustering:** Utilization of the K-Means algorithm to segment teenagers into similarity groups (Clusters) and map the depression rate within each profile.

### 2. `random_forest.ipynb` (Supervised Learning)
This script focuses on modeling and predicting the target variable (`depression_label`).
- **Exploratory Data Analysis (EDA):** Evaluation using interactive correlation matrices to identify the strength of the linear relationship between social media use and mental health variables.
- **Class Balancing:** Implementation of spatial oversampling techniques (SMOTE) to handle the strong minority of positive depression cases.
- **Predictive Modeling:** Training a `RandomForestClassifier`, applying penalization hyperparameters (`class_weight='balanced'`) and depth restriction (`max_depth=5`) to mitigate overfitting.
- **Performance Evaluation:** Analysis of the Confusion Matrix, AUC-ROC score, Average Precision, and Precision-Recall curve Threshold.

## 💡 Key Insights and Conclusions
- Feature engineering proved to be essential: understanding composite proportions (such as the screen-to-sleep ratio) offered cleaner paths for clustering users compared to isolated data.
- **Data Anomaly Alert:** The trained Random Forest model achieved perfectly anomalous evaluation metrics (AUC-ROC of 0.9936). In the context of human health and psychiatry, behavior naturally possesses a high level of noise and uncontrollable variables, making this result statistically impossible. Since tree-based algorithms are excellent at mapping exact mathematical formulas, we strongly conclude that this dataset is synthetically generated. In the real world of Data Science, any model with an AUC greater than 0.80 on clinical mental health data inherently demands strong suspicion and revalidation.

## 🛠️ Technologies Used
- **Language:** Python
- **Core Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn (PCA, KMeans, RandomForestClassifier), and Imbalanced-learn (SMOTE).

---

# Impacto das Redes Sociais na Saúde Mental de Adolescentes

## 📌 Sobre o Projeto
Este repositório contém uma análise detalhada sobre o impacto do uso de redes sociais na saúde mental de adolescentes, utilizando técnicas de Machine Learning supervisionado e não supervisionado. O objetivo do projeto é entender os padrões de comportamento — como horas de sono, tempo de tela e atividade física — e sua relação com níveis de estresse, ansiedade e risco de depressão.

## 📊 Conjunto de Dados
O dataset utilizado (`Teen_Mental_Health_Dataset.csv`) foi obtido através do Kaggle (`algozee/teenager-menthal-healy`). Ele inclui dados de 1200 estudantes, abordando:
- Tempo diário de redes sociais e uso de plataformas específicas (Instagram, TikTok ou ambos).
- Horas de sono e tempo de tela antes de dormir.
- Desempenho acadêmico, nível de atividade física e interação social.
- Indicadores psicológicos: níveis de estresse, ansiedade, vício e diagnóstico de depressão (`depression_label`).

## 📂 Estrutura do Repositório
A investigação foi dividida em duas frentes analíticas, documentadas nos seguintes Jupyter Notebooks:

### 1. `k_means.ipynb` (Aprendizado Não Supervisionado)
O foco deste script é descobrir perfis de comportamento ocultos na base de dados.
- **Engenharia de Atributos (Feature Engineering):** Criação de novas métricas cruciais de saúde, como o `deficit_sono`, a `relacao_tela_sono` e a `pontuacao_carga_mental`.
- **Pré-processamento:** Padronização matemática das variáveis numéricas utilizando o `StandardScaler`.
- **Redução de Dimensionalidade:** Aplicação de PCA (*Principal Component Analysis*) para otimizar o espaço vetorial e eliminar redundâncias, avaliando visualmente a variância explicada.
- **Clusterização:** Uso do algoritmo K-Means para segmentar os adolescentes em grupos de similaridade (Clusters) e mapear a taxa de depressão dentro de cada perfil.

### 2. `random_forest.ipynb` (Aprendizado Supervisionado)
Este script foca na modelagem e previsão da variável alvo (`depression_label`).
- **Análise Exploratória (EDA):** Avaliação com matrizes de correlação interativas para identificar a força da relação linear entre o uso de mídias sociais e as variáveis de saúde mental.
- **Balanceamento de Classes:** Implementação de técnicas de *oversampling* espacial (SMOTE) para lidar com a forte minoria de casos positivos de depressão.
- **Modelagem Preditiva:** Treinamento de um `RandomForestClassifier`, aplicando hiperparâmetros de penalização (`class_weight='balanced'`) e restrição de profundidade (`max_depth=5`) para mitigar overfitting.
- **Avaliação de Performance:** Análise da Matriz de Confusão, pontuação AUC-ROC, *Average Precision* e Threshold da curva Precision-Recall.

## 💡 Principais Insights e Conclusões
- A feature engineering demonstrou ser essencial: entender proporções compostas (como a relação tela/sono) ofereceu caminhos mais limpos para a clusterização dos usuários do que os dados isolados.
- **Alerta de Anomalia nos Dados:** O modelo Random Forest treinado atingiu métricas de avaliação perfeitamente anômalas (AUC-ROC de 0.9936). No contexto de saúde humana e psiquiatria, o comportamento possui naturalmente um alto nível de ruídos e variáveis incontroláveis, tornando esse resultado estatisticamente impossível. Como algoritmos baseados em árvores são excelentes em mapear fórmulas matemáticas exatas, concluímos de forma contundente que este dataset é gerado sinteticamente. No mundo real de Data Science, qualquer modelo com uma AUC superior a 0.80 em dados de saúde mental clínica já exige forte suspeita e revalidação.

## 🛠️ Tecnologias Utilizadas
- **Linguagem:** Python
- **Bibliotecas Principais:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn (PCA, KMeans, RandomForestClassifier) e Imbalanced-learn (SMOTE).
