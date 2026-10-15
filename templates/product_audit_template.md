# 🔬 Product Health Check & Bottleneck Audit: [Nome do Produto]
> **Produto Auditado:** [Nome do Produto] | **Data da Auditoria:** [Data]
> **PM Lead:** Kevin Augusto Vieira | **Foco:** Diagnóstico de Telemetria, Funil & Trade-offs

---

## 1. O Diagnóstico Frio do Funil (Onde o Usuário Está Caindo)

```
[ Topo do Funil / Aquisição ] ─────────── 100% (X usuários)
         │
         ▼  (Taxa de Perda Crítica: [%] de Drop)
[ Etapa 2 / Primeiro Valor Percebido ] ── [%] (Y usuários)
         │
         ▼  (Engajamento Recorrente)
[ Usuários Retidos / Convertidos ] ────── [%] (Z usuários)
```

- **Métrica Alarmante Identificada:** [Ex: 43.9% de abandono imediato na 1ª mensagem / 60% de churn no onboarding]
- **Sintoma Observado:** [O que o usuário faz quando o atrito ocorre]

---

## 2. Auditoria de Causa-Raiz (Telemetria vs Instinto da Equipe)

### O Instinto Natural (Armadilha de Produto)
> *"A equipe ou os sócios queriam resolver o problema adicionando [novas funcionalidades / dar descontos agressivos / mudar layout visual]."*

### O Diagnóstico Analítico Baseado em Dados
- **Cascata de Telemetria / Latência:**
  - [Etapa A da infraestrutura/fluxo]: [Tempo em segundos ou atrito de cliques]
  - [Etapa B]: [Tempo em segundos ou falha de feedback visual]
  - [Etapa C]: [Tempo total acumulado]
- **Causa-Raiz Real:** [Ex: Latência de API que quebra a síncronia do canal / Falha de concorrência no banco / Falta de densidade de oferta local]

---

## 3. A Decisão Executiva de Trade-off (Rigor de Liderança de PM)
- **O que foi CONGELADO no roadmap:** [Quais entregas de vaidade ou novas features foram pausadas]
- **Onde o foco foi colocado:** [Ação prioritária de engenharia de produto / performance / liquidez]
- **Racional de Liderança:** Por que dizer "não" para ideias boas foi a decisão correta para salvar a retenção do produto.

---

## 4. Plano de Intervenção & Lições Estratégicas
1. **Ação Imediata (Semana 1):** [Correção de UX / Feedback síncrono em < 1s / Cache Redis / Redução de cliques]
2. **Ação Estrutural (Semanas 2-3):** [Otimização de backend / Refatoração de concorrência / Estratégia Supply-First]
3. **Lição de Longo Prazo:** [O que esse diagnóstico ensina sobre o modelo de negócio ou dinâmica do produto]
