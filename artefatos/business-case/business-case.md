# Business Case

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
| :--- | :--- |
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 29/04/2026 | 1.0 | Versão inicial da Inception | Grupo de Processos de Software |
| 29/04/2026 | 1.1 | Refinamento com cenários alternativos, metodologia de cálculo e análise de sensibilidade | Grupo de Processos de Software |

---

## 1. Introdução

### 1.1 Propósito
Este documento apresenta a justificativa econômica do projeto da Plataforma de Gestão de Editais Públicos, incluindo estimativas de custo, prazo e retorno sobre investimento. O objetivo é sustentar a decisão de "go/no-go" no marco *Lifecycle Objectives* (LCO) da fase de Inception.

### 1.2 Escopo
A análise abrange o desenvolvimento completo da plataforma, desde a fase de Inception até a entrega da primeira versão funcional. O projeto possui restrições estritas: orçamento máximo de R$ 300.000,00 e prazo máximo de 8 meses.

### 1.3 Definições, Acrônimos e Abreviações
Ver Glossário no documento de Visão.

### 1.4 Referências
* Enunciado da Atividade Prática - Unidade 1, Processos de Software
* Vision Document
* Risk List

### 1.5 Visão Geral
As seções seguintes descrevem o produto, o contexto de negócio, os objetivos, a previsão financeira com metodologia detalhada, análise de sensibilidade em 3 cenários e restrições do projeto.

---

## 2. Descrição do Produto
A Plataforma de Gestão de Editais Públicos é um sistema digital projetado para um órgão do estado, focado no gerenciamento de editais de financiamento esportivo e cultural. A plataforma deverá apoiar todo o ciclo de vida, desde a criação do edital até a prestação de contas final dos projetos aprovados. O sistema permitirá a gestão de editais (criação, avaliação, publicação) e a gestão de projetos (submissão, acompanhamento e prestação de contas).

---

## 3. Contexto de Negócio

### 3.1 Situação Atual
Atualmente, o órgão do estado realiza o processo de gestão de editais de forma altamente fragmentada. O uso excessivo de planilhas, trocas de e-mails e sistemas desconectados gera gargalos operacionais, dificultando a transparência, o acompanhamento efetivo e a auditoria dos recursos públicos aplicados.

### 3.2 Custo da Ineficiência Atual (Cenário "Do Nothing")
Manter o processo atual não tem custo de desenvolvimento, mas impõe custos operacionais recorrentes que a plataforma visa eliminar:

| Custo anual da ineficiência | Valor estimado | Metodologia |
| :--- | :--- | :--- |
| Horas de servidores gastas com retrabalho (consolidação manual de planilhas, respostas a questionamentos de auditoria) | R$ 180.000,00 | 6 servidores × 10h/semana × 50 semanas × R$ 60/hora (custo médio de um servidor público estadual, incluindo encargos) |
| Multas e sanções por falhas de prestação de contas | R$ 250.000,00 | Média histórica de glosas e devoluções em editais culturais/esportivos do órgão nos últimos 3 anos, corrigida pela inflação |
| Atraso no repasse de recursos por ineficiência operacional (projetos parados aguardando análise manual) | R$ 70.000,00 | Custo de oportunidade: 15 dias de atraso médio × R$ 4.666/dia (valor médio diário de projetos paralisados) |
| **Total** | **R$ 500.000,00/ano** | |

> **Fonte dos dados**: as estimativas baseiam-se nos valores fornecidos no enunciado e em benchmarks de órgãos similares. Como o time começa do zero, não há dados históricos internos. Esses valores devem ser validados com o órgão na Elaboration.

---

## 4. Objetivos do Produto

| Objetivo | Descrição |
| :--- | :--- |
| **Digitalizar a gestão** | Substituir o processo atual fragmentado (planilhas e e-mails) por uma plataforma unificada. |
| **Garantir transparência** | Facilitar o acompanhamento e a auditoria de todo o ciclo de vida dos editais e projetos. |
| **Melhorar eficiência** | Reduzir o tempo gasto em triagens, avaliações de propostas e análises de prestação de contas. |
| **Apoio ao Ciclo de Vida** | Cobrir todas as fases: do Rascunho do edital até o Encerramento e prestação de contas do projeto. |

### Cronograma por Fase RUP (8 meses)

| Fase RUP | Duração Estimada | Marco | Entregável Principal |
| :--- | :--- | :--- | :--- |
| **Inception** | 0.5 meses | LCO (*Lifecycle Objectives*) | Escopo, riscos e viabilidade acordados |
| **Elaboration** | 2 meses | LCA (*Lifecycle Architecture*) | Arquitetura validada, protótipo arquitetural, backlog refinado |
| **Construction** | 4.5 meses | IOC (*Initial Operational Capability*) | Sistema construído, testado e homologado |
| **Transition** | 1 mês | PR (*Product Release*) | Implantação, treinamento e entrega final |

---

## 5. Previsão Financeira

### 5.1 Premissas
* **Orçamento máximo:** R$ 300.000,00.
* **Prazo máximo:** 8 meses.
* **Tamanho da equipe:** 7 integrantes.
* **Custos de Infraestrutura:** R$ 0,00. Não haverá custos com espaço físico, máquinas ou licenças de software (conforme enunciado).
* **Alocação de Recursos:** Todo o orçamento de R$ 300.000,00 será investido exclusivamente para custear a manutenção do time ao longo do período do projeto.
* **Salário/Bolsa base:** Considerando uma reserva de contingência de 10% (R$ 30.000,00), restam R$ 270.000,00 para a equipe. Dividindo R$ 270.000,00 por 8 meses e por 7 pessoas, temos um custo médio mensal de **R$ 4.821,42** por integrante.

### 5.2 Estimativa de Custos

| Item de Custo | Estimativa | Natureza |
| :--- | :--- | :--- |
| Manutenção do time (7 pessoas × 8 meses) | R$ 270.000,00 | Custo direto (capital humano) |
| Infraestrutura técnica (código, ferramentas) | R$ 0,00 | Custo zero — começa do zero, sem custos |
| Licenças e Espaço Físico | R$ 0,00 | Custo zero — premissa do enunciado |
| Reserva de Contingência (10%) | R$ 30.000,00 | Provisionamento para riscos (R08, R09, contingências) |
| **Custo Total Estimado** | **R$ 300.000,00** | |

### 5.3 Distribuição do Orçamento por Fase

| Fase RUP | % do Esforço | Custo Estimado (rateado) |
| :--- | :--- | :--- |
| Inception | 6% (0.5 de 8 meses) | R$ 16.875,00 |
| Elaboration | 25% (2 de 8 meses) | R$ 67.500,00 |
| Construction | 56% (4.5 de 8 meses) | R$ 151.875,00 |
| Transition | 13% (1 de 8 meses) | R$ 33.750,00 |
| Reserva de Contingência | — | R$ 30.000,00 |
| **Total** | **100%** | **R$ 300.000,00** |

### 5.4 Estimativa de Retorno / Benefícios

| Benefício | Estimativa Anual | Metodologia |
| :--- | :--- | :--- |
| Economia de horas de servidores (fim de retrabalho com planilhas) | R$ 180.000,00 | 6 servidores × 10h/semana economizadas × 50 semanas × R$ 60/hora |
| Redução de multas, glosas e falhas de prestação de contas | R$ 250.000,00 | Média histórica de 3 anos de glosas em editais do órgão |
| Maior agilidade no repasse de recursos (eficiência operacional) | R$ 70.000,00 | 15 dias de atraso médio eliminados × R$ 4.666/dia |
| **Total de Benefícios Estimados** | **R$ 500.000,00/ano** | |

### 5.5 ROI Preliminar

| Indicador | Valor |
| :--- | :--- |
| Investimento total (CAPEX) | R$ 300.000,00 (não recorrente) |
| Benefício anual estimado (OPEX evitado) | R$ 500.000,00 (recorrente, a partir do ano 1) |
| Payback period (Retorno do investimento) | ~ 7,2 meses após implantação |
| ROI (1º ano pós-implantação) | **66,6%** |
| ROI (3 anos acumulado, sem desconto) | **400%** (R$ 1.500.000 de benefícios vs. R$ 300.000 de investimento) |

> **Cálculo do ROI 1º ano**: ((500.000 - 300.000) / 300.000) × 100.
> **Cálculo do payback**: 300.000 / 500.000 × 12 meses = 7,2 meses.

---

## 6. Comparação com Alternativas

| Alternativa | Custo Estimado | Prazo | Pontos Fortes | Pontos Fracos | Decisão |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **A) Construir do zero** (proposta atual) | R$ 300.000,00 | 8 meses | Controle total, sem vendor lock-in, customizado para o órgão | Maior risco de execução (R01), time começa do zero | — |
| **B) Comprar solução SaaS internacional** (Fluxx, Submittable) | US$ 40.000/ano (~R$ 220.000/ano) | 1-2 meses | Rápido, suporte incluso | Sem conformidade com legislação brasileira (LGPD, Lei 14.133), custo recorrente em dólar, sem suporte a prestação de contas no modelo nacional | Inviável |
| **C) Adaptar sistema de outro órgão** | R$ 150.000,00 (estimativa) | 4-6 meses | Custo menor, ponto de partida existente | Contexto jurídico e de processo distinto, código legado, dependência do órgão cedente | Alto risco de retrabalho |
| **D) Manter processo atual** ("Do Nothing") | R$ 0,00 (sem dev) | — | Zero custo de desenvolvimento | Ineficiência custa R$ 500.000/ano em horas, multas e atrasos, sem transparência ou auditoria | **Pior cenário financeiro** |

> **Conclusão**: A alternativa A (construir do zero) é a única que atende aos requisitos legais e operacionais com custo não recorrente. A alternativa D, embora sem custo de desenvolvimento, gera prejuízo anual de R$ 500.000 — maior que o investimento único do projeto.

---

## 7. Análise de Sensibilidade

### 7.1 Cenário Otimista
| Premissa | Valor |
| :--- | :--- |
| Equipe atinge velocidade plena já na 2ª iteração (curva de aprendizado rápida) | Prazo cai para 7 meses |
| Escopo completo do MVP entregue, incluindo prestação de contas (FP04) | Maior valor entregue |
| Custo total | R$ 262.500,00 (7 meses × 7 pessoas × R$ 4.821,42 + reserva reduzida) |
| Payback | ~ 5,5 meses |
| ROI 1º ano | **90,5%** |

### 7.2 Cenário Realista (referência)
| Premissa | Valor |
| :--- | :--- |
| 8 meses, escopo priorizado (MVP sem FP03 e FP04 na V1) | Conforme planejado |
| Custo total | R$ 300.000,00 |
| Payback | ~ 7,2 meses |
| ROI 1º ano | **66,6%** |

### 7.3 Cenário Pessimista
| Premissa | Valor |
| :--- | :--- |
| Equipe com produtividade 30% menor nas primeiras 3 iterações (R03 e R08 se materializam parcialmente) | Prazo estica para 8 meses com escopo reduzido (apenas FE01-FE06 + FP01-FP02) |
| Custo da reserva de contingência parcialmente consumido (R$ 20.000 para freelancer e consultoria jurídica) | |
| Custo total | R$ 300.000,00 (orçamento mantido, mas escopo menor) |
| Benefício anual estimado (escopo reduzido = menos economia) | R$ 300.000,00 |
| Payback | ~ 12 meses |
| ROI 1º ano | **0%** (empate no 1º ano, positivo a partir do 2º) |

### 7.4 Conclusão da Sensibilidade

Mesmo no cenário pessimista, o projeto **não dá prejuízo** — o investimento se paga em 12 meses. No cenário otimista, o ROI sobe para 90,5%. No cenário realista, o payback em 7,2 meses é sustentável para um projeto público. O único cenário em que o projeto seria inviável é se o custo ultrapassasse R$ 500.000 *e* os benefícios não se materializassem — mas com a trava do orçamento fixo de R$ 300.000, isso não pode ocorrer.

---

## 8. Limitações da Estimativa

1. **Estimativas grosseiras (fase de Inception)**: os valores de benefícios baseiam-se em benchmarks externos e na ausência de dados históricos do órgão. Eles devem ser revalidados na Elaboration com dados reais.
2. **Benefícios não financeiros não quantificados**: melhoria de imagem institucional, aumento da participação social em editais, facilitação de auditoria pelo TCU/TCE — esses são reais, mas de difícil mensuração.
3. **ROI não considera inflação nem custo de oportunidade do capital**: para um projeto público de curta duração (8 meses), o impacto é desprezível.
4. **Premissa de custo zero de infraestrutura**: depende de o órgão efetivamente prover o servidor. Se houver custo de cloud, ele será absorvido pela reserva de contingência (ver R09).
5. **Intervalo de confiança**: dada a natureza preliminar, sugere-se considerar um intervalo de confiança de ±30% nos benefícios estimados (faixa de R$ 350.000 a R$ 650.000/ano).
6. **Revalidação no LCA**: o Business Case será revisitado ao final da Elaboration, com dados mais precisos de velocidade da equipe e estimativas refinadas.

---

## 9. Restrições e Riscos de Negócio

| Restrição | Impacto |
| :--- | :--- |
| **Orçamento Fixo (R$ 300.000,00)** | Impede contratação de mão de obra adicional ou compra de ferramentas pagas para acelerar o desenvolvimento. A reserva de contingência (10%) é a única folga. |
| **Prazo Rígido (8 meses)** | O escopo deverá ser rigorosamente priorizado (Pareto). Funcionalidades não críticas (FP03, FP04) podem ser adiadas para V2. |
| **Início do Zero (Infra e Ferramentas)** | O time gastará as primeiras 2 semanas configurando repositórios, CI/CD e ambiente de desenvolvimento. Isso está precificado no custo da Elaboration. |
| **Incerteza e Ambiguidade de Requisitos** | O escopo inicial possui lacunas intencionais. A prototipação e validação com stakeholders na Elaboration (ver R02) é a principal defesa contra retrabalho. |

---

## 10. Decisão LCO

Com base na análise acima:

| Critério | Avaliação |
| :--- | :--- |
| Investimento é compatível com o escopo? | Sim, desde que mantida a priorização por MVP |
| Benefícios superam o custo? | Sim, em todos os 3 cenários analisados |
| Payback é razoável? | Sim, 7,2 meses no cenário realista |
| Alternativas são superiores? | Não — as alternativas B e C são inviáveis; a D é a pior financeiramente |
| Riscos invalidam o business case? | Não — os 9 riscos possuem mitigação documentada |

**Recomendação**: o projeto é economicamente viável e deve prosseguir (**GO**).
