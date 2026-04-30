# Parecer Final

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

---

## Decisão

**GO**

---

## Justificativa

### Com base no Business Case

A justificativa econômica sustenta a continuidade do projeto. O orçamento de R$ 300.000,00 está integralmente alocado para manutenção do time de 7 integrantes ao longo de 8 meses (custo médio de R$ 4.821,42 por integrante/mês), sem custos adicionais com infraestrutura, licenças ou espaço físico. Os benefícios anuais estimados em R$ 500.000,00 — provenientes da economia de horas-trabalho de servidores (R$ 180.000,00), redução de multas e falhas de prestação de contas (R$ 250.000,00) e maior agilidade no repasse de recursos (R$ 70.000,00) — superam o investimento total. O ROI projetado para o primeiro ano é de 66,6%, com payback estimado em aproximadamente 7,2 meses após a implantação. O cronograma distribui adequadamente as fases do RUP (Inception 0,5 mês, Elaboration 2 meses, Construction 4,5 meses, Transition 1 mês), respeitando o prazo máximo de 8 meses.

### Com base nos Riscos Identificados

Foram identificados 5 riscos principais, todos com estratégias de mitigação e planos de contingência definidos:

- **R01 (Escopo excessivo para orçamento/prazo)** — Magnitude Alta, Prioridade 1. A estratégia de priorização por Pareto e definição de MVP com funcionalidades essenciais (criar edital, submeter proposta, avaliar proposta) é adequada. O plano de contingência de adiar prestação de contas e acompanhamento para uma segunda versão é viável.
- **R02 (Requisitos ambíguos ou incompletos)** — Magnitude Alta, Prioridade 2. A documentação explícita de suposições e decisões de modelagem, combinada com validação junto a stakeholders, reduz significativamente a probabilidade de retrabalho.
- **R03 (Equipe sem experiência prévia juntos)** — Magnitude Média, Prioridade 3. Mitigável com definição antecipada de processos, convenções e reuniões de alinhamento na Elaboration.
- **R04 (Restrições regulatórias e legais)** — Magnitude Média, Prioridade 4. A consulta à legislação aplicável (Lei 14.133/2021, LGPD) e a inclusão de especialista legal como stakeholder consultivo são medidas proporcionais ao risco.
- **R05 (Falta de integração com sistemas existentes)** — Magnitude Baixa, Prioridade 5. A arquitetura orientada a APIs desde o início mitiga esse risco de forma preventiva.

Nenhum risco identificado é bloqueante. Todos possuem estratégias de mitigação proporcionais e planos de contingência realistas.

### Com base na Clareza dos Requisitos

Os requisitos, embora intencionalmente ambíguos no enunciado, foram suficientemente esclarecidos para prosseguir. As lacunas foram identificadas e abordadas por meio de decisões de modelagem documentadas nos artefatos. O Glossário com 15 termos estabelece um vocabulário comum entre todos os envolvidos. Os 3 casos de uso centrais (Criar e Configurar Edital, Submeter Proposta, Avaliar Proposta) cobrem os fluxos arquiteturalmente mais significativos e representam aproximadamente 20% do total esperado, conforme preconizado para a fase de Inception. Os ciclos de vida do Edital e do Projeto foram modelados com estados bem definidos. As suposições e decisões de modelagem estão explicitadas no Modelo de Domínio.

### Com base na Viabilidade Técnica e Organizacional

O projeto é tecnicamente viável. Trata-se de uma plataforma web com complexidade moderada, sem requisitos de infraestrutura especializada. O time de 7 integrantes é adequado para o escopo proposto. A inexistência de custos com espaço físico, máquinas e licenças elimina riscos orçamentários de infraestrutura. A arquitetura orientada a APIs, definida como premissa no Modelo de Domínio, garante extensibilidade e facilita integrações futuras. O uso de tecnologias web padrão e padrões abertos assegura que não há dependência de fornecedores ou licenças proprietárias. O cronograma de 8 meses é compatível com o escopo priorizado, desde que mantida a disciplina de MVP definida na mitigação do R01.

---

## Detalhamento da Decisão

### Análise de Trade-off: GO vs PIVOT

A decisão PIVOT foi considerada e descartada pelos seguintes motivos:

| Fator | GO | PIVOT | Avaliação |
|-------|-----|-------|-----------|
| **Escopo** | Reduzir se necessário (R01 já prevê plano de contingência) | Reduzir escopo como premissa inicial | Pivotar o escopo agora seria prematuro — o R01 já define MVP e contingência. A redução só deve ocorrer se a velocidade da equipe for insuficiente. |
| **Riscos** | Todos os 9 riscos têm mitigação documentada | Revisão de escopo por risco (mais conservador) | Os riscos são gerenciáveis. Pivotar por precaução eliminaria funcionalidades (FP03, FP04) que podem ser entregues se o cenário otimista se confirmar. |
| **Business Case** | ROI 66,6%, payback 7,2 meses no cenário realista | Mesmo no PIVOT (escopo menor), o ROI cai mas não fica negativo | Pivotar reduz os benefícios anuais de R$ 500.000 para ~R$ 300.000, piorando o payback para 12 meses. O GO maximiza o valor entregue. |
| **Requisitos** | Ambiguações foram suficientemente esclarecidas para prosseguir | Esperar mais clareza dos stakeholders | O workshop com stakeholders está planejado para a semana 2 da Elaboration. Prosseguir permite validar com dados reais em vez de postergar. |
| **Custo de adiar** | Iniciar a Elaboration imediatamente | Perder 1-2 meses refinando requisitos | O prazo é rígido (8 meses) e o time começa do zero. Cada semana de delay consome 2,2% do cronograma total. |

**Conclusão**: O GO é suportado pelos artefatos. O principal risco (R01) é contornável com redução de escopo SE e QUANDO necessário, não como premissa. A decisão de pivotar permanece como opção tática ao final de cada iteração, se os indicadores mostrarem desvio.

### Stack Tecnológica Sugerida e Justificativa

| Camada | Tecnologia Sugerida | Justificativa |
|--------|---------------------|---------------|
| **Backend** | Python 3.13 + FastAPI | Curva de aprendizado baixa, ecossistema rico (SQLAlchemy, Alembic), async nativo para picos de submissão, boa relação produtividade/desempenho |
| **Frontend** | React 19 + Tailwind CSS | Responsivo por padrão (WCAG), componentização reaproveitável entre fluxos de gestor e proponente |
| **Banco de Dados** | PostgreSQL 16 | Relacional maduro, gratuito, JSONB para campos flexíveis de critérios de avaliação, full-text search para buscas em editais |
| **Cache / Filas** | Redis | Gerenciamento de prazos automáticos e notificações em background (Celery com Redis broker) |
| **Infraestrutura** | Docker Compose (dev) / Docker Swarm ou Podman (prod) | Sem custo de licença, rebuild simples em novo servidor (ver R09), padronizado entre dev e prod |
| **CI/CD** | GitHub Actions | Gratuito para repositórios públicos, integração nativa com GitHub |

> **Alternativas rejeitadas**:
> - **Java/Spring Boot**: curva mais íngreme para time novo (R03), mais verboso, consome mais horas de desenvolvimento.
> - **MongoDB**: schema-less atraente para critérios flexíveis, mas prestação de contas e auditoria exigem integridade relacional (transações ACID).
> - **GraphQL**: complexidade desnecessária para a V1. REST simples com OpenAPI documentada resolve todos os casos de uso atuais.

### Pontos de atenção para a Elaboration

1. **Refinar o escopo do MVP** — Formalizar quais funcionalidades compõem a primeira versão, com base na matriz de prioridades do Vision (itens 1 a 8 como essenciais; 9 a 11 como secundários).
2. **Validar requisitos com stakeholders** — Realizar workshops para esclarecer ambiguidades remanescentes, especialmente quanto às regras de avaliação, critérios de desempate e fluxo de recursos.
3. **Definir a arquitetura de referência** — Selecionar stack tecnológica, modelar a arquitetura em camadas e produzir um protótipo arquitetural para validar os casos de uso críticos.
4. **Mitigar o R01 ativamente** — Iniciar a Elaboration com a definição clara do backlog priorizado, aplicando estritamente o critério de Pareto (20% das funcionalidades que entregam 80% do valor).
5. **Estabelecer processo de desenvolvimento** — Definir cerimônias, ferramentas, convenções de código e pipeline de CI/CD nas primeiras semanas.
6. **Revisar requisitos legais** — Consultar a Lei 14.133/2021 e a LGPD para garantir conformidade desde a arquitetura.
7. **Preparar protótipo de interface** — Produzir wireframes ou protótipos navegáveis para validação de usabilidade com os perfis de usuário identificados.

**Prioridades para a próxima fase:**

| Prioridade | Atividade | Artefato RUP esperado |
|-----------|-----------|----------------------|
| 1 | Definição da arquitetura | Software Architecture Document |
| 2 | Protótipo arquitetural | Architectural Proof-of-Concept |
| 3 | Refinamento dos casos de uso | Use-Case Specification (revisados) |
| 4 | Plano de iterações | Software Development Plan |
| 5 | Refinamento do modelo de domínio | Design Model (inicial) |

### Checklist do Marco LCO (Lifecycle Objectives)

| Pergunta-chave do LCO | Resposta | Evidência |
|-----------------------|----------|-----------|
| Escopo documentado e acordado? | **Sim** | Vision (seções 2, 4, 5, Glossário) |
| Stakeholders identificados? | **Sim** | Vision (seção 3.2-3.5) — 5 stakeholders com perfis detalhados |
| Casos de uso arquiteturalmente significativos especificados? | **Sim** | UC01, UC02, UC03 — 3 casos de uso centrais (~20% do total), com fluxos e diagramas de atividade |
| Riscos mapeados e com mitigação? | **Sim** | Risk List — 9 riscos com ações, responsáveis, prazos e planos de contingência |
| Business Case positivo? | **Sim** | ROI 66,6% (cenário realista), payback 7,2 meses, análise de 3 cenários com sensibilidade |
| Modelo de domínio inicial definido? | **Sim** | Modelo de Domínio — 7 entidades com atributos, UML, relacionamentos e restrições OCL |
| Suposições e decisões de modelagem explicitadas? | **Sim** | Vision (4.3), Modelo de Domínio (seção 7) |
| Viabilidade técnica confirmada? | **Sim** | Stack definida e justificada; time de 7 pessoas compatível com escopo priorizado |
| Alternativas avaliadas? | **Sim** | Business Case (seção 6): 4 alternativas analisadas (construir, SaaS, adaptar, do nothing) |
| Decisão de continuidade fundamentada? | **Sim** | Este parecer: GO com justificativas baseadas nos 4 critérios e análise de trade-off |

**Resultado do LCO**: todas as 10 perguntas-chave do marco Lifecycle Objectives têm resposta positiva e evidenciada. O projeto atinge o marco LCO e está apto a prosseguir para a Elaboration.

---

## Resumo dos Artefatos Produzidos

| Artefato | Localização | Status |
|----------|-------------|--------|
| Vision | `artefatos/vision/vision.md` | Completo |
| Use-Case Specification (UC01) | `artefatos/casos-de-uso/UC01-criar-editais.md` | Completo |
| Use-Case Specification (UC02) | `artefatos/casos-de-uso/UC02-submeter-proposta.md` | Completo |
| Use-Case Specification (UC03) | `artefatos/casos-de-uso/UC03-avaliar-proposta.md` | Completo |
| Risk List | `artefatos/lista-de-riscos/risk-list.md` | Completo |
| Business Case | `artefatos/business-case/business-case.md` | Completo |
| Modelo de Domínio | `artefatos/modelo-de-dominio/modelo-dominio.md` | Completo |
