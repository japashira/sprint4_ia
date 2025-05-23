# 🦷 DentalCare – Agendamento Inteligente com IA

Projeto final da disciplina **Disruptive Architectures: IOT, IOB & Generative IA**.

---

## 🧩 Visão Geral do Projeto

O **DentalCare** é uma solução baseada em IA para prever a necessidade de consultas odontológicas. Seu objetivo é reduzir consultas desnecessárias, minimizar cancelamentos e otimizar o uso da agenda de clínicas.

Desenvolvido como resposta ao desafio da **Odontoprev**, o projeto aplica modelos de machine learning a dados simulados de pacientes para recomendar, com base em histórico e perfil, se uma nova consulta deve ou não ser marcada.

---

## 🎯 Problema que Resolve

- Consultas agendadas sem necessidade real.
- Alto índice de cancelamentos de última hora.
- Retornos clínicos agendados por impulso.
- Dificuldade de prever o comportamento do paciente.

---

## 🧠 Como a IA Funciona

- **Base de dados sintética** com 2000 registros simulando:
  - Idade
  - Frequência de consultas
  - Histórico de cancelamentos
  - Valor gasto
  - Realização de procedimentos preventivos

- **Modelos utilizados:**
  - ✅ Random Forest Classifier (melhor desempenho)
  - Gradient Boosting (usado para comparação)

- **Validação cruzada** com 5 folds
- **GridSearchCV** para otimização dos hiperparâmetros

📊 **Resultado final:**  
Acurácia média de ~84% na detecção de consultas desnecessárias.

---

## 🖥️ Funcionalidades Demonstradas

- ✅ Geração e análise de dados sintéticos.
- ✅ Treinamento e comparação entre modelos.
- ✅ API Flask interna para simular previsões.
- ✅ Testes com pacientes simulados.
- ✅ Visualizações e métricas de desempenho.

---

## 🔧 Como Rodar o Projeto

1. Abra o notebook no Google Colab.
2. Execute todas as células na ordem.
3. A API Flask será iniciada internamente.
4. Use a célula de teste para simular uma requisição.

---

## 📉 Exemplo de Previsão

```json
Entrada do paciente:
{
  "idade": 40,
  "frequencia_consultas": 2,
  "procedimento_preventivo": 1,
  "historico_cancelamentos": 0,
  "valor_gasto": 120
}

Resultado da IA:
{
  "consulta_desnecessaria": 0
}
