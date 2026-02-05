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

O dashboard foi estruturado em três visões principais, permitindo análises detalhadas e também uma visão geral do projeto.

### 1️⃣ Visão por voo (filtro por número do voo)
Permite selecionar um voo específico e acompanhar:
- Status atual do voo (no horário, atrasado ou emergência)
- ETA esperado x ETA real
- Velocidade e altitude ao longo do tempo
- Aeroporto de destino
- Condições da pista e impacto climático

Essa visão é voltada para análise operacional individual de cada aeronave.

### 2️⃣ Visão geral do projeto
Apresenta os dados consolidados coletados ao longo do projeto, incluindo:
- Quantidade total de aeronaves monitoradas
- Classificação de risco dos voos
- Distribuição de voos por aeroporto
- Impacto de condições meteorológicas
- Indicadores de pontualidade

Essa visão permite entender padrões, volumes e riscos de forma macro.

### 3️⃣ Visão geográfica (mapa)
Exibe a trajetória dos voos em mapa interativo, com:
- Visualização da rota percorrida
- Distribuição espacial das aeronaves
- Filtros por voo e aeroporto

Essa camada facilita a análise espacial do tráfego aéreo e o acompanhamento visual das rotas.


