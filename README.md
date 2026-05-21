# Análise de Teste A/A/B: Mudança de Fonte no Aplicativo

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Statsmodels](https://img.shields.io/badge/Statsmodels-ADADAD?style=for-the-badge)

## 📌 Visão Geral do Projeto
Este projeto analisa os resultados de um experimento A/A/B em um aplicativo de comércio de produtos alimentares. O objetivo foi avaliar se a mudança nas fontes do aplicativo impactaria a conversão dos usuários ao longo do funil de vendas, utilizando dois grupos de controle (246 e 247) e um grupo de teste (248).

## 🎯 Objetivos de Negócio
* **Validação do Experimento (A/A):** Verificar se os dois grupos de controle são estatisticamente equivalentes, garantindo a integridade do mecanismo de divisão de tráfego.
* **Análise do Funil:** Identificar em qual etapa os usuários mais abandonam o aplicativo.
* **Teste A/B:** Avaliar se a nova fonte gera diferença significativa na conversão em cada etapa do funil.

## 🛠️ Stack Técnica
* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Estatística:** Statsmodels (Teste Z para proporções)

## 📉 Metodologia
1. **Preparação de Dados:** Conversão de timestamps, filtragem de dados incompletos (anteriores a 01/08/2019) e separação por grupo experimental.
2. **Análise do Funil:** Mapeamento da jornada `MainScreenAppear → OffersScreenAppear → CartScreenAppear → PaymentScreenSuccessful`, com cálculo de proporção por etapa.
3. **Teste A/A:** Comparação estatística entre os grupos de controle 246 e 247 para validar a divisão de tráfego.
4. **Teste A/B:** Comparação do grupo de teste (248) contra cada grupo de controle e contra os dois combinados, para todos os eventos do funil.

## 🏆 Resultados e Conclusões
* **Validação A/A aprovada:** Os grupos 246 e 247 não apresentaram diferença estatisticamente significativa em nenhum evento, confirmando a integridade do experimento.
* **Maior gargalo do funil:** A etapa `OffersScreenAppear` retém apenas ~62% dos usuários — maior perda do funil.
* **46.9% dos usuários** completam o caminho inteiro até o pagamento.
* **Nova fonte sem impacto:** Em todos os testes A/B, falhamos em rejeitar a hipótese nula. A mudança de fonte não gerou diferença significativa na conversão com alpha de 0.05.
* **Recomendação:** Manter a fonte atual do aplicativo, pois a mudança não trouxe ganho comprovado.

---

### 📂 Estrutura do Repositório
* `projeto11.ipynb`: Notebook Jupyter contendo toda a análise, testes e visualizações.
* `logs_exp_us.csv`: Dataset com logs de eventos dos usuários por grupo experimental.

---
**Enzo Bombassaro de Freitas** | *Data Analyst* | [LinkedIn](https://www.linkedin.com/in/enzo-bombassaro/) | [GitHub](https://github.com/ezodia1)
