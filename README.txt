# Flight ETA & Risk Monitoring

Pipeline em Python + MySQL para monitoramento de voos, cálculo de ETA real, análise de condições climáticas e geração de alertas operacionais.  
Dashboard final consumindo dados do banco via Power BI (link abaixo).

---

## ✅ Objetivo
Transformar dados de radar (com limitações e inconsistências) em informações confiáveis para:
- estimar **ETA real de chegada**
- avaliar **risco climático** para pouso
- detectar **comportamentos anormais** (possível emergência)

---

## 🧰 Tecnologias
- Python
- SQL (MySQL)
- Power BI (online)

---

## 🔎 Como resolvemos o problema
- A API de radar original apresentou inconsistências e foi substituída
- A API gratuita não informava **aeroporto de origem**
- Utilizamos direção/trajetória e altitude para estimar **aeroporto de destino**
- Criamos um **ETA real** (porque “no horário” não refletia o cenário real)
- Integramos **Open-Meteo** para condições climáticas da pista
- Criamos regra de alerta por mudança brusca de **velocidade/altitude**

---

## 📊 Dashboard (Power BI)
Link do relatório online:  
https://app.powerbi.com/links/8YTSg-iCKJ?ctid=bd697c1b-c481-479c-841e-c618542675c3&pbi_source=linkShare

---

## 📁 Arquivos principais
- `main_fixed.py` → pipeline principal (coleta, tratamento, regras e carga no banco)
- `schema.sql` → criação das tabelas no MySQL

---

## ▶️ Como executar (resumo)
1. Crie as tabelas no MySQL usando `schema.sql`
2. Configure as variáveis de ambiente (host, user, password, database)
3. Execute o pipeline:
   ```bash
   python main_fixed.py

# Flight ETA & Risk Monitoring

Pipeline em Python + MySQL para monitoramento de voos, cálculo de ETA real, análise de condições climáticas e geração de alertas operacionais.  
Dashboard final consumindo dados do banco via Power BI (link abaixo).

---

## ✅ Objetivo
Transformar dados de radar (com limitações e inconsistências) em informações confiáveis para:
- estimar **ETA real de chegada**
- avaliar **risco climático** para pouso
- detectar **comportamentos anormais** (possível emergência)

---

## 🧰 Tecnologias
- Python
- SQL (MySQL)
- Power BI (online)

---

## 🔎 Como resolvemos o problema
- A API de radar original apresentou inconsistências e foi substituída
- A API gratuita não informava **aeroporto de origem**
- Utilizamos direção/trajetória e altitude para estimar **aeroporto de destino**
- Criamos um **ETA real** (porque “no horário” não refletia o cenário real)
- Integramos **Open-Meteo** para condições climáticas da pista
- Criamos regra de alerta por mudança brusca de **velocidade/altitude**

---

## 📊 Dashboard (Power BI)
Link do relatório online:  
https://app.powerbi.com/links/8YTSg-iCKJ?ctid=bd697c1b-c481-479c-841e-c618542675c3&pbi_source=linkShare

---

## 📁 Arquivos principais
- `main_fixed.py` → pipeline principal (coleta, tratamento, regras e carga no banco)
- `schema.sql` → criação das tabelas no MySQL

---

## ▶️ Como executar (resumo)
1. Crie as tabelas no MySQL usando `schema.sql`
2. Configure as variáveis de ambiente (host, user, password, database)
3. Execute o pipeline:
   ```bash
   python main_fixed.py

