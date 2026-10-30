---
name: wellness-icp-prospecting
description: Pesquisa recorrente e qualificação B2B pelo ICP Score do Wellness Protocol, com evidências, deduplicação e saída pronta para CRM/Direct. Sem envio automático de mensagens.
version: 1.1.0
---

# Skill: Wellness ICP Prospecting

## Missão e contexto
Localizar e qualificar empresas brasileiras de **recovery e wellness operacional** para a oferta B2B do Wellness Protocol. Transformar pesquisa pública em uma fila enxuta de prospects para discovery, proposta e eventual conexão à automação do Instagram Direct. Não executar contato externo, anúncio ou disparo a partir desta skill.

**Produto vendido:** implantação operacional inteligente com processos, checklists, agendamento e automações delimitadas; Kit Operação como oferta de entrada. Não vender como SaaS genérico nem assumir que todo centro de fisioterapia ou estética atende ao ICP.

**ICP prioritário:** centro de recovery/wellness especializado, independente ou pequena rede, em operação, com serviços presenciais e múltiplas rotinas/equipamentos. ICP secundário: centro em abertura/expansão, clínica de fisioterapia esportiva premium com recovery e spa especializado. Brasil; começar por Curitiba/RMC, São Paulo, Rio de Janeiro, Brasília e outras regiões com sinais reais, sem excluir bons prospects de outras cidades.

## Entradas
- data da execução e região preferida (default: Brasil);
- número-alvo de novos leads (default: 30; máximo: 30 por execução);
- histórico de leads e bloqueios, se acessível; não afirmar deduplicação entre dias sem consultar fonte persistente;
- evidências públicas disponíveis, data de verificação e regras de exclusão.

## Rotina de execução
1. Pesquisar empresas reais em fontes recentes: site oficial, Instagram público da empresa, diretórios empresariais, Google Maps e notícias verificáveis. Buscar por recovery, crioterapia, sauna, banho de gelo, contraste térmico, fisioterapia esportiva, centros de longevidade e termos adjacentes.
2. Comprovar que o estabelecimento existe e que ao menos uma fonte atual sustenta atividade, cidade e vínculo com recovery. Preferir links específicos do estabelecimento, não resultados genéricos da plataforma. Não usar conteúdo gerado por IA como única evidência.
3. Normalizar a identidade: CNPJ, quando oficial e pertinente; senão domínio + nome + cidade, identificando filiais separadamente sem duplicar rede/unidade. Consultar registro de leads anterior, se disponível. Nunca fingir que houve comparação com histórico se não houve.
4. Classificar aderência com os quatro critérios públicos (0–65), conforme rubrica a seguir. Dar zero e registrar 'não comprovado' quando faltar evidência; zero não equivale à inexistência do atributo.
5. Registrar 2–3 fatos observáveis com URLs e data de acesso; classificar momento comercial e oportunidade de abordagem como hipóteses, não como fatos internos. NÃO presumir orçamento, dor, receita, tamanho da equipe nem disponibilidade do decisor.
6. Ordenar por pré-score, relevância da evidência, capacidade de acesso comercial e preferência por organizações independentes com ciclos decisórios curtos; grandes redes podem ser P2 mesmo com pré-score alto.
7. Separar informações publicamente verificadas de campos que exigem conversa e preparar próxima ação humana. Não criar leads fictícios só para preencher a meta.
8. Para cada empresa, pesquisar os três canais: Instagram público oficial, e-mail empresarial e WhatsApp empresarial. Quando houver apenas telefone publicado, anotar como telefone (sem presumir que seja WhatsApp). Nunca inventar endereço, número ou perfil; campos não verificados permanecem vazios. Guardar fonte de cada contato.
9. Entregar relatório diário conciso, uma relação de até 30 registros e os respectivos canais de contato, conforme references/LEAD_SCHEMA.md; indicar sem novos leads se necessário.
10. Preparar uma fila de pré-aprovação para Telegram apenas quando houver integração autorizada com a instância ativa, com revisão humana individual antes de qualquer DM. Não afirmar que enviou ao Telegram sem confirmação do serviço.

## ICP Score com rubricas obrigatórias (0–100)
**Pré-score público (máximo 65):**
- Especialização em recovery **0/5/10/15/20**: 0 sem comprovação; 5 wellness adjacente; 10 recovery complementar; 15 recovery central declarado; 20 recovery central com 2+ modalidades evidenciadas.
- Complexidade operacional **0/5/10/15/20**: 0 não verificada; 5 serviço único; 10 duas rotinas/modalidades; 15 operação com diferentes equipamentos/serviços e agendamento; 20 estrutura multiunidade OU evidência inequívoca de equipe + modalidades + processos.
- Momento de compra **0/5/10/15**: 0 nenhum sinal verificado; 5 lançamento de serviço/renovação recente; 10 expansão, contratação ou nova unidade anunciada; 15 inauguração recente (até 18 meses) ou unidade em expansão com data/fonte. Registrar a data; não tratar ausência de sinal como ausência de oportunidade.
- Estrutura de investimento **0/5/10**: 0 sem evidência; 5 localização fixa e equipamentos/estrutura visíveis; 10 múltiplos equipamentos relevantes, unidade premium com evidência concreta ou mais de uma unidade. Não inferir faturamento ou orçamento.

**Qualificação posterior em discovery (máximo 35):**
- Dor operacional **0/5/10/15/20**: 0 não investigada/sem confirmação; 5 indício relatado; 10 problema identificado com exemplo; 15 impacto/urgência confirmado; 20 impacto quantificado e iniciativa ativa de solução.
- Decisor e acesso **0/5/10/15**: 0 desconhecido; 5 nome/cargo por fonte pública; 10 canal profissional validado; 15 responsável por compra confirmado na conversa.
- **Score completo = pré-score + dor + decisor**. Não produzir score completo como se validado antes do contato.

## Priorização
- Pesquisa: P1 = pré-score 50–65; P2 = 35–49; P3 = 0–34.
- Comercial pós-discovery: A >=75/100 **com** confirmação de dor e contato do decisor; B 55–74; C <55. O limiar A nunca é aplicável automaticamente a pré-score.
- Classificar urgência separadamente: confirmada, provável ou desconhecida.
- Preferir evidência ao score quando houver conflito; explicar exceções.

## Saída: relatório diário
Título com data; contagem de pesquisados, encontrados, novos verificados, possíveis duplicatas e rejeitados. Apresentar até 30 novos leads verificados em tabela (não preencher lacunas artificialmente). Priorizar os 10 melhores na síntese e manter os demais no registro estruturado:
Empresa | Cidade/UF | Pré-score /65 | Modalidades e sinais verificados | Instagram público | E-mail empresarial | WhatsApp confirmado ou telefone comum | Por que abordar | Informação pendente | Prioridade.
Depois, no máximo 3 observações de mercado e 1 abordagem consultiva sugerida (sem mensagem enviada).
Incluir link para a própria skill e declarar se a deduplicação foi comprovada contra um cadastro persistente, só comparada com histórico da conversa ou não verificada. Apresentar também o lote apto a ser submetido a aprovação individual no Telegram, explicitando que preparação não é envio efetivo.
Nunca inventar dados, números ou contatos. Informar claramente quando não houver empresas novas suficientes.

## Regras de privacidade e automação
- Coletar dados corporativos públicos relevantes. Evitar dados pessoais sensíveis e extração em massa de contatos pessoais.
- Manter as URLs e a data de coleta para auditoria e revisão.
- Marcar lead como **discovered** e **dm_status=not_authorized** por padrão. Nenhuma mensagem automática, nenhuma campanha e nenhum bulk outreach sem autorização posterior e verificação das regras do Instagram/Meta.
- Para futura integração com a automação do Direct, usar a chave canônica do lead, channel, instagram_username, offer_id, campaign_id, opt_in_status, dm_status, last_contact_at, next_action_at e approval_status. O motor deve evitar duplicatas, respeitar opt-out, limites da API e revisão humana da primeira abordagem.
- Não alterar o Content OS nem publicar conteúdo sem aprovação humana. Nunca expor tokens, cookies ou credenciais em relatórios.

## Critérios de pronto
A execução só é bem sucedida se cada lead entregue tiver nome real, localização, link público específico, evidência recuperável e pontuação reproduzível. Score sem fonte é informação pendente. Nenhum contato externo deve ser enviado.
