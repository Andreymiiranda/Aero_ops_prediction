# ✈️ Aero Ops Predictor (Logistics Intelligence)

Este projeto foi desenvolvido como **trabalho de conclusão** no **Bootcamp da Generation Brasil**, com o apoio e patrocínio do **Grupo Cyrela** e **CashMe**.

O objetivo foi resolver um **desafio real de logística crítica** para a **SkyCargo Logistics**, empresa especializada no transporte de **órgãos para transplante** e **peças urgentes de maquinário**, onde **cada minuto é vital**.

---

## 📋 Problema de Negócio

A SkyCargo dependia de **painéis externos de aeroportos**, atualizados manualmente, que frequentemente exibiam o status *“No horário”* mesmo quando aeronaves enfrentavam **tempestades a quilômetros do destino**.

### ❗ Impacto
- Ambulâncias e caminhões aguardavam na pista sem informações confiáveis  
- Perda de tempo crítico em operações médicas e industriais  
- Falta de previsibilidade logística  

---

## 🎯 A Solução

Desenvolvemos uma **“Torre de Controle Própria”**, capaz de calcular o **ETA Real (Estimated Time of Arrival)** ao cruzar:

- **Telemetria real da aeronave (ADS-B)**
- **Condições meteorológicas exatas do aeroporto de destino**
- **Regras de negócio logísticas e operacionais**

---

## 🛠️ Tecnologias Utilizadas

### 🔹 Python
- Motor de coleta e processamento de dados
- Consumo de APIs:
  - **ADS-B** (telemetria aérea)
  - **OpenMeteo** (meteorologia)
- Cálculo geodésico preciso com **geopy**
- Implementação de regras de negócio e alertas

### 🔹 SQL (MySQL)
- Modelagem de dados
- Persistência da telemetria de voos
- Histórico para auditoria e análises
- Base de dados consumida pelo Power BI

### 🔹 Power BI
- Dashboards analíticos focados em decisão
- Visualização espacial, operacional e de risco

### 📦 Bibliotecas Principais
- `geopy` – Cálculo de distância considerando a curvatura da Terra  
- `requests` – Integração com APIs externas  
- `mysql-connector` – Persistência no MySQL  

---

## 🧠 Inteligência do Sistema & Regras de Negócio

- **Cálculo Geodésico**: distância real até o aeroporto considerando a curvatura da Terra  
- **Fator Clima**:
  - +10 minutos no ETA se vento > **30 km/h**
  - +15 minutos no ETA se precipitação > **0.5 mm**
- **Alerta de Emergência**:
  - Queda brusca de altitude (> **5000 pés**) longe do aeroporto
  - Geração de flag de desvio crítico

---

## 📊 Visualização de Dados

O dashboard responde a perguntas críticas do negócio:

- 🗺️ **Mapa de Rastreio** – Trajetória real da aeronave
- 📈 **Análise de Performance** – Velocidade e altitude ao longo do tempo
- ⚠️ **Matriz de Risco** – Pontualidade e condições de pista

### 👉 Acessar o Dashboard
[![Dashboard Power BI](docs/dashboard.png)](https://SEU_LINK_AQUI)

---

## 📂 Como Utilizar este Repositório

### 1️⃣ Banco de Dados
- Crie as tabelas:
  - `FACT_VOO_TELEMETRIA`
  - `FACT_CONDICOES_POUSO`

### 2️⃣ Configuração
- Insira suas credenciais no dicionário `DB_CONFIG`
- Arquivos:
  - `main.py`
  - `update_db.py`

## 3️⃣ Execução
-python main.py

## 👥 Agradecimentos
- **Equipe:** João Victor Ravazzi Ferretti, Andrey Alves Miranda, Carrie Jenniffer Alves Mota, Juliana Malheiros, Leandro Falasca.
- **Instrutores:** Luiz Chiavini e Samuel Reginatto
- **Apoiadores:** Generation Brasil,Grupo Cyrela e CashMe
