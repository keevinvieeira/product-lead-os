# 🚀 Product Lead OS (`product-lead-os`)
> **Copiloto Estratégico de Product Management, Go-To-Market e Diagnóstico de Produto para Founders, PMs e PMMs.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Framework: FoundersPM](https://img.shields.io/badge/Framework-FoundersPM%20%2F%20Monica%20Possel-orange.svg)](https://founderspm.com.br)
[![Author: Kevin Augusto Vieira](https://img.shields.io/badge/Author-Kevin%20Augusto%20Vieira-green.svg)](https://www.linkedin.com/in/kevin-augusto/)

O **Product Lead OS** é uma skill avançada de inteligência artificial desenhada para atuar como um **Head de Produto / Principal PM & PMM de bolso**. Ele foi concebido para ir além de relatórios retrospectivos e atuar **ativamente nas decisões do dia a dia**: orientando lançamentos do 0 ao 1, priorizando features em produtos já escalados e diagnosticando gargalos críticos de telemetria e funil com rigor analítico.

---

## 🎯 Por Que Esta Skill Existe?

Na rotina de Product Management e Product Marketing (PMM), os erros mais caros costumam ser:
1. **Construir antes de validar:** Gastar meses e dezenas de milhares de reais desenvolvendo softwares complexos ou apps nativos antes de comprovar o Product-Market Fit.
2. **A armadilha do "Feature Creep":** Empilhar novas funcionalidades no roadmap apenas porque clientes isolados pediram, poluindo a experiência do produto.
3. **Falta de honestidade intelectual com os dados:** Tentar resolver abandono de usuários adicionando mais recursos, em vez de diagnosticar a causa-raiz real (ex.: latência técnica, atrito de onboarding ou falta de liquidez local).

O **Product Lead OS** implementa a esteira metodológica de **Monica Possel (FoundersPM / PMAC)**, combinada aos princípios de **Teresa Torres (OST)** e **Marty Cagan (4 Riscos de Produto)**, transformando o assistente de IA em um copiloto de alto impacto.

---

## 🧭 Os 3 Modos de Operação

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        MODOS DE ATUAÇÃO DO PRODUCT LEAD OS                             │
├─────────────────────────┬──────────────────────────┬───────────────────────────────────┤
│ MODO 1: GTM 0→1         │ MODO 2: EXPANSÃO &       │ MODO 3: DIAGNÓSTICO               │
│ (Lançamento de Produto) │ FEATURES (Produto Ativo) │ & AUDITORIA (Análise de PM)       │
├─────────────────────────┼──────────────────────────┼───────────────────────────────────┤
│ Tirar a ideia do papel  │ Evitar a armadilha de    │ Olhar analítico sobre o produto:  │
│ com MVP enxuto,         │ empilhar features que    │ por que usuários abandonam? Onde  │
│ Discovery via OST,      │ ninguém usa, priorizar   │ está o gargalo de latência/UX?    │
│ priorização SCALE e     │ rollouts e desenhar o    │ Quando congelar o roadmap para    │
│ tração de lançamento.   │ GTM de adoção in-app.    │ consertar o atrito técnico?       │
└─────────────────────────┴──────────────────────────┴───────────────────────────────────┘
```

### 1. Modo 1: Lançamento 0→1 & Go-To-Market
*Ideal para novos negócios próprios, startups early-stage ou validação de novas verticais.*
- **Opportunity Solution Tree (OST):** Alinhamento de outcomes de negócio e mapeamento de dores de usuários e parceiros B2B.
- **Matriz SCALE:** Pontuação de soluções divergentes em *Solução Clara (S)*, *Conhecimento Gerado (C)*, *Agilidade (A)*, *Escala (L)* e *Efeito WOW (E)* para escolher o MVP mais leve.
- **Hypothesis Canvas (8 Blocos):** Formulação canônica do experimento com mitigação dos 4 riscos de Marty Cagan (Valor, Usabilidade, Viabilidade Técnica e Negócio).
- **Playbook de GTM Híbrido:** Conteúdo temático de nicho, mídia enxuta para reconhecimento e fechamento comercial B2B presencial.

### 2. Modo 2: Descoberta e Rollout de Novas Features
*Ideal para produtos já ativos e escalados que necessitam de expansão responsável.*
- **Triagem Anti-Feature Creep:** Definição explícita de *Escopo Negativo* (o que NÃO construir).
- **Validação Pré-Código:** Desenho de testes de intenção (*fake door testing*, prototipagem rápida, beta fechado).
- **Estratégia de Rollout & Adoção In-App:** Campanhas de ativação in-app (tooltips, onboarding contextual) e telemetria de retenção da feature (D1, D7, D30).

### 3. Modo 3: Diagnóstico Crítico de Funil & Telemetria
*Ideal para produtos no ar com métricas de retenção, conversão ou engajamento abaixo do esperado.*
- **Auditoria de Funil:** Mapeamento do ponto de maior vazamento de usuários.
- **Cascata de Latência & Telemetria:** Análise de causa-raiz técnica (tempo de resposta de webhooks, requisições de API, banco de dados).
- **Decisão Executiva de Trade-off:** Racional maduro de liderança de produto para **congelar o roadmap** de novidades e focar na estabilidade e tempo de resposta.

---

## 📂 Estrutura do Repositório

```bash
product-lead-os/
├── SKILL.md                          # Manual de instruções da skill para o agente de IA
├── README.md                         # Documentação completa do projeto
├── templates/
│   ├── input_router.md               # Roteador de intake inteligente (entrevista adaptativa)
│   ├── gtm_launch_template.md        # Template de PRD + GTM Brief + Hypothesis Canvas (Modo 1)
│   ├── feature_rollout_template.md   # Template de Descoberta & Adoção de Features (Modo 2)
│   ├── product_audit_template.md     # Template de Diagnóstico de Funil & Telemetria (Modo 3)
│   └── web_case_template.html        # Template web responsivo com Tailwind CSS e Mermaid.js
```

---

## 🛠️ Como Usar no Antigravity ou Agentes de IA

1. Copie esta pasta para o diretório de skills do seu agente (ex.: `~/.gemini/config/skills/product-lead-os/`).
2. No chat com seu agente, execute comandos como:
   - *"Quero usar o **product-lead-os** para o meu novo produto [Nome]"*
   - *"Ajude-me a planejar o GTM do [Nome]"*
   - *"Quero auditar o gargalo de conversão do [Nome] como PM"*
3. O agente ativará o **Roteador Inteligente**, fará apenas 4-5 perguntas específicas do seu momento e gerará tanto o documento de trabalho (PRD / Canvas / Auditoria) quanto uma página web interativa para publicação.

---

## 🌟 Caso de Referência Construído com Este Método

Este repositório e seus frameworks foram validados na prática no case da startup **Meu Barzin** (Curitiba - PR):
- **Página Live do Case:** [https://keevinvieeira.github.io/case-meu-barzin/](https://keevinvieeira.github.io/case-meu-barzin/)
- **Registro no PMRadar:** [PMRadar Case #cef86cff](https://pmradar.founderspm.com.br/case/cef86cff-658d-49aa-a955-facda01e601f)

---

## 👤 Autor

**Kevin Augusto Vieira**  
*Co-Founder, Product Manager & AI Solutions Builder*  
- 💼 **LinkedIn:** [https://www.linkedin.com/in/kevin-augusto/](https://www.linkedin.com/in/kevin-augusto/)  
- 🐙 **GitHub:** [https://github.com/keevinvieeira](https://github.com/keevinvieeira)  
- 📧 **Contato:** kevin.aug.vieira@gmail.com
