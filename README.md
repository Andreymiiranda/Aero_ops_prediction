# 📦 Projeto SkyCargo – Aero Ops Predictor

## 🏢 Contexto do Projeto

A **SkyCargo** atua no transporte de **órgãos para transplante** e **peças urgentes de maquinário**.  
Atualmente, a operação depende de painéis externos para confirmar a chegada dos voos, que são **atualizados manualmente** e muitas vezes indicam **“No horário”**, mesmo quando a aeronave enfrenta **tempestades a quilômetros do destino**.

---

## ❗ O Problema

Ambulâncias e caminhões aguardam na pista **sem informações reais e confiáveis**, desperdiçando **tempo crítico** em operações onde **cada minuto é vital** para:
- o sucesso de um transplante
- a continuidade de uma operação logística nacional

---

## 🎯 O Desafio

Criar uma **“Torre de Controle Própria”**:  
um sistema capaz de calcular o **ETA (Estimated Time of Arrival) real**, cruzando:

- a **posição física da aeronave**
- as **condições climáticas exatas do aeroporto de destino**

---

## 🧠 A Solução

Foi desenvolvido um sistema de **inteligência operacional aérea**, capaz de:
- Monitorar aeronaves em tempo real
- Identificar voos em aproximação real
- Ajustar automaticamente o ETA com base em clima e perfil de voo
- Gerar alertas operacionais e de emergência
- Persistir dados para análise histórica e tomada de decisão

---

## 🔹 Python – Motor de Dados e Inteligência

O Python foi utilizado como **núcleo do sistema**, responsável por:

- Consumo de APIs de tráfego aéreo (**ADS-B**) e meteorologia (**OpenMeteo**)
- **Cálculo Geodésico** utilizando a biblioteca `geopy`, considerando a curvatura da Terra para garantir **precisão matemática** na distância real até o destino
- Aplicação de **regras de negócio**, incluindo:
  - Ajuste automático de ETA com base em **Vento de Proa**
  - Penalização por **Pista Molhada**
  - Geração de **alertas de emergência** para quedas bruscas de altitude longe do aeroporto

---

## 🔹 SQL – Persistência e Histórico

Os dados processados são persistidos em um banco **MySQL**, garantindo:

- Integridade da telemetria dos voos
- Histórico completo para auditoria
- Base confiável para análises operacionais

Essa base de dados é utilizada como **fonte oficial** para consumo no Power BI.

---

## 🔹 Power BI – Visibilidade Operacional

O Power BI é utilizado para fornecer **visibilidade estratégica**, com dashboards focados em:

- 🗺️ **Mapa de Rastreio**  
  Trajetória real percorrida pela aeronave

- 📈 **Análise de Performance**  
  Monitoramento de velocidade e altitude ao longo do tempo

- ⚠️ **Matriz de Risco**  
  Visão clara das condições de pouso por aeroporto, considerando clima e status operacional

---

## 🚀 Visão de Futuro

Como evolução do projeto, estão previstos:

- Integração com **provedores de dados premium**
- Aplicação de **Machine Learning** (modelos de regressão)
- Identificação de padrões de órbita e desvios de rota
- Transformar o ETA de **reativo** para **preditivo**

O objetivo é tornar o sistema ainda mais inteligente e antecipar riscos antes que impactem a operação.

---

## 👤 Autor

**Andrey Miranda**  
Projeto desenvolvido para fins de estudo, portfólio e demonstração de competências em **engenharia de dados, análise operacional e suporte à decisão**.
