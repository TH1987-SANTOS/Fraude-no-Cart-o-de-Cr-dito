# 🧠 Detecção de Fraudes em Transações Financeiras

### 📊 Projeto de Machine Learning com Python & Power BI

Este projeto apresenta o desenvolvimento completo de um sistema de **detecção de fraudes em transações financeiras**, combinando **análise exploratória de dados (EDA)**, **balanceamento de classes (SMOTE)**, **treinamento de modelos supervisionados** e **visualização em Power BI**.

O objetivo é demonstrar, em um fluxo reprodutível e didático, como técnicas de Ciência de Dados podem ser aplicadas em problemas reais de classificação com dados desbalanceados.

---

## 🚀 Estrutura do Projeto

| Etapa | Descrição | Ferramentas |
|-------|------------|-------------|
| 1️⃣ | Coleta e limpeza de dados | `pandas`, `numpy` |
| 2️⃣ | Análise exploratória (EDA) | `matplotlib`, `seaborn` |
| 3️⃣ | Balanceamento de classes | `imblearn.SMOTE` |
| 4️⃣ | Treinamento de modelos (LR, RF, KNN, DT) | `scikit-learn` |
| 5️⃣ | Calibração de probabilidades | `CalibratedClassifierCV` |
| 6️⃣ | Exportação para Power BI | `pandas.to_csv()` |

---

## 📂 Estrutura de Arquivos

```
├── data/
│   ├── transactions_synthetic_simple.csv    # Dataset base
│
├── notebooks/
│   ├── Fraude_cartao_credito.ipynb          # Notebook principal
│
├── export_powerbi/
│   ├── test_predictions_with_probs.csv      # Previsões e probabilidades para Power BI
│
├── requirements.txt                         # Dependências do projeto
└── README.md                                # Documentação principal
```

---

## 🧩 Modelos Avaliados

- **Logistic Regression** — modelo base interpretável.  
- **Decision Tree** — simples e visual.  
- **Random Forest** — melhor performance geral (AUC e Recall).  
- **K-Nearest Neighbors (KNN)** — comparativo de vizinhança.

📈 **Métricas consideradas:**
- Acurácia  
- Precisão  
- Recall (sensibilidade às fraudes)  
- F1-Score  
- AUC-ROC  
- Brier Score (para calibração)

---

## 🔍 Principais Insights

- A base de dados é **altamente desbalanceada**: menos de 1% das transações são fraudes.  
- O **Random Forest** obteve melhor **AUC-ROC**, sendo mais robusto e equilibrado.  
- Após calibração de probabilidades, as predições tornaram-se mais confiáveis para uso operacional.  
- Com ajuste de *threshold*, é possível aumentar o **recall** (captura de fraudes) conforme o risco tolerado pelo negócio.

---

## 💡 Conclusões

- Modelos de aprendizado supervisionado são eficazes para **identificação automática de fraudes financeiras**, desde que os dados sejam bem balanceados.  
- O **uso de SMOTE e calibração de probabilidades** melhora significativamente o desempenho prático.  
- Dashboards em **Power BI** permitem o monitoramento contínuo e suporte à decisão em tempo real.  
- Para aplicações corporativas, recomenda-se **deploy em nuvem** (AWS, Azure, GCP) e uso de pipelines automatizados.

---

## ⚙️ Como Reproduzir

```bash
# 1. Criar ambiente virtual
python -m venv venv
source venv/bin/activate  # (Windows: venv\Scripts\activate)

# 2. Instalar dependências
pip install -r requirements.txt

# 3. Rodar o notebook
jupyter notebook notebooks/Fraude_cartao_credito.ipynb
```

---

## 📈 Integração com Power BI

O arquivo `test_predictions_with_probs.csv` contém:
- ID da transação  
- Probabilidade de fraude  
- Classe predita  
Esses dados podem ser integrados ao Power BI para gerar:
- Painéis de monitoramento de risco  
- Curvas ROC e F1 Score interativas  
- Indicadores de alerta operacional  

---

## 👩‍💻 Sobre o Projeto

Este projeto integra conhecimentos de:
- **Ciência de Dados**  
- **Machine Learning**  
- **Estatística Aplicada**  
- **Business Intelligence (BI)**  

e foi desenvolvido com o objetivo de compor o portfólio profissional da autora, destacando aplicações práticas em **fraudes financeiras** e **modelagem preditiva**.

---

## 🧰 Tecnologias Utilizadas

| Categoria | Ferramentas |
|------------|-------------|
| Linguagem | Python |
| Análise de Dados | Pandas, NumPy |
| Modelagem | scikit-learn, imbalanced-learn |
| Visualização | Seaborn, Matplotlib, Power BI |
| Versão e Portfólio | GitHub |

---

## 🏁 Próximos Passos

- Implementar **XGBoost / LightGBM** para otimização de performance.  
- Criar **pipeline automatizado** com deploy em nuvem (AWS ou Azure).  
- Adicionar dashboard interativo com **dados em tempo real**.  
