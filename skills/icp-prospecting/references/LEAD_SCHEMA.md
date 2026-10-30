# Registro canônico de prospect — Wellness Protocol B2B

## Tabela de campos
| Campo | Uso |
| --- | --- |
| lead_id | ID estável gerado do identificador empresarial/canonical_key |
| canonical_key | CNPJ oficial se disponível; senão domínio normalizado + cidade + unidade |
| company_name | Razão/nome comercial verificável |
| parent_brand | Rede/marca, caso unidade |
| branch_name | Unidade ou bairro |
| city, state, country | Geografia |
| website_url, instagram_url, instagram_username | Contato corporativo público verificado |
| contact_url | Canal comercial público (site/WhatsApp empresarial/Instagram) |
| evidence_urls | URLs específicas com os fatos pontuados |
| source_checked_at | Data/hora da verificação |
| recovery_score, operations_score, growth_score, investment_score | Quatro critérios públicos |
| pre_score | Soma dos quatro critérios (0–65) |
| confirmed_pain_score, decision_maker_score | Critérios após discovery (0–35) |
| full_score | SOMENTE após qualificação (0–100); vazio antes |
| prospect_priority | P1/P2/P3 pela pesquisa; A/B/C após discovery |
| verified_facts | 1–3 frases curtas com link |
| assumptions_to_validate | Hipóteses de dor, capacidade e urgência |
| buyer_name, buyer_role | Apenas se profissional e público/confirmado |
| status | discovered/researching/reviewed/approved_for_outreach/contacted/replied/qualified/proposal/client/not_fit/opted_out |
| outreach_channel | Canal planejado; não enviado automaticamente |
| offer_id, landing_page_url, campaign_id | Roteamento para ofertas, LP e campanhas |
| opt_in_status | unknown/yes/no; não inferir consentimento |
| approval_status | pending/approved/rejected |
| dm_status | not_authorized/ready/queued/sent/replied/failed/opted_out |
| last_contact_at, next_action_at | Rotina comercial com controle de cadência |
| dedup_status | checked_against_registry/checked_against_prior_report/unverified |
| created_at, updated_at | Auditoria |

## Chave e política de deduplicação
- Mesmo CNPJ e mesma unidade => mesmo lead.
- Se faltar CNPJ: preferir hostname normalizado + cidade + unidade; não unir empresas distintas com nomes parecidos.
- Marca com múltiplas filiais: registrar a marca como parent_brand e cada unidade como lead com chave diferente; contar tanto unidades quanto marcas sem mistura.
- Se o cadastro histórico não estiver disponível, marcar dedup_status=unverified; não alegar leads 'novos' absolutos.
- Atualizar a mesma empresa quando surgir novo sinal; não reenviar diariamente como novo lead.

## Saída mínima interoperável
CSV/Sheets-ready ou JSON com campos principais: company_name, city, state, website_url, instagram_url, canonical_key, pre_score, prospect_priority, evidence_urls, source_checked_at, status, approval_status, dm_status. A publicação no chat deve conter links legíveis e evidências, não dados pessoais privados.

## Proteções para uma integração futura com DM
A pesquisa e a aprovação comercial são etapas separadas do envio. Nenhum campo calculado autoriza mensagem. A integração deve exigir aprovação explícita, política de plataforma atendida, verificação de contato permitido, idempotência por lead + campanha, logging de tentativa/resultado e opt-out.
