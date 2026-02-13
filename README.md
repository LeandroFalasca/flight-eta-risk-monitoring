# ✈️ Flight ETA & Risk Monitoring

Pipeline desenvolvido em **Python + MySQL** para monitoramento de voos, cálculo de **ETA real**, análise de risco climático e geração de alertas operacionais.

O dashboard final consome os dados estruturados via **Power BI Online**.

---

## 🎯 Objetivo

Transformar dados de radar (com limitações e inconsistências) em informações confiáveis para:

- Estimar **ETA real de chegada**
- Avaliar **risco climático para pouso**
- Detectar **comportamentos anormais** (possível emergência)

---

## 🧠 Desafios Técnicos Resolvidos

- Substituição de API de radar devido a inconsistências
- API gratuita não informava aeroporto de origem
- Estimativa de destino usando **trajetória, direção e altitude**
- Criação de cálculo próprio de **ETA real** (corrigindo status "no horário")
- Integração com **Open-Meteo** para análise de condições da pista
- Regra de alerta para variações bruscas de **velocidade e altitude**

---

## 🛠️ Stack Tecnológica

- Python (tratamento e regras de negócio)
- MySQL (armazenamento estruturado)
- Power BI Online (visualização)
- APIs: Radar + Open-Meteo

---

## 📊 Dashboard (Power BI)

🔗 Link do relatório online:  
https://app.powerbi.com/links/8YTSg-iCKJ?ctid=bd697c1b-c481-479c-841e-c618542675c3&pbi_source=linkShare

O dashboard foi estruturado em três visões principais:

### 1️⃣ Visão por voo
- ETA esperado vs ETA real
- Status operacional
- Velocidade e altitude ao longo do tempo
- Condições da pista

### 2️⃣ Visão geral
- Total de aeronaves monitoradas
- Classificação de risco
- Pontualidade
- Impacto meteorológico

### 3️⃣ Visão geográfica
- Mapa interativo com trajetórias
- Distribuição espacial
- Filtros por voo e aeroporto

---

## 📁 Arquivos Principais

- `main_fixed.py` → Pipeline completo (coleta, tratamento, regras e carga no banco)
- `schema.sql` → Estrutura das tabelas MySQL

---

## ▶️ Como Executar

1. Criar as tabelas usando `schema.sql`
2. Configurar variáveis de ambiente (host, user, password, database)
3. Executar:

```bash
python main_fixed.py


