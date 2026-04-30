# Risk List

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/04/2026 | 1.0 | Versão inicial da Inception | Grupo de Processos de Software |
| 29/04/2026 | 1.1 | Expansão para 9 riscos com matriz e mitigações detalhadas | Grupo de Processos de Software |

---

## 1. Introdução

### 1.1 Propósito

Este documento identifica, prioriza e descreve os principais riscos do projeto da Plataforma de Gestão de Editais Públicos, com estratégias de mitigação detalhadas, responsáveis e prazos. Inclui também uma matriz qualitativa de probabilidade x impacto para fundamentar a priorização.

### 1.2 Escopo

Os riscos listados abrangem riscos técnicos, de negócio, de recursos, de segurança e de adoção, identificados durante a fase de Inception.

### 1.3 Definições, Acrônimos e Abreviações

Ver Glossário no documento de Visão.

### 1.4 Referências

- Vision Document
- Business Case
- Modelo de Domínio

### 1.5 Visão Geral

A seção 2 apresenta os 9 riscos identificados com magnitude, descrição, impactos, indicadores, estratégia de mitigação (com ações, responsável e prazo) e plano de contingência. A seção 3 apresenta a matriz qualitativa de probabilidade x impacto.

---

## 2. Riscos

### 2.1 R01 - Escopo Excessivo para Orçamento e Prazo

#### 2.1.1 Magnitude

**Alta**

#### 2.1.2 Descrição

O escopo do sistema é amplo (gestão completa de editais e projetos), e o orçamento de R$ 300.000,00 com prazo de 8 meses pode ser insuficiente para entregar todas as funcionalidades com qualidade.

#### 2.1.3 Impactos

- Entrega incompleta do sistema
- Redução de qualidade para cumprir prazo
- Estouro de orçamento

#### 2.1.4 Indicadores

- Atraso no cronograma de entregas das iterações
- Número de funcionalidades não implementadas vs. planejadas
- Horas de trabalho da equipe acima do estimado

#### 2.1.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Priorizar funcionalidades por Pareto e definir MVP com funcionalidades essenciais (FE01-FE06, FP01-FP02) | Product Owner / Líder técnico | Final do mês 0.5 (LCO) |
| Estimar esforço de cada funcionalidade do backlog em pessoas-semana | Líder técnico | Início do mês 1 |
| Alocar 20% da capacidade de cada iteração para imprevistos (buffer) | Scrum Master | A partir da iteração 1 |
| Revisar escopo ao final de cada iteração com base na velocidade medida | Product Owner | A cada iteração |

#### 2.1.6 Plano de Contingência

Reduzir escopo para funcionalidades essenciais (criar edital, submeter proposta, avaliar proposta). Adiar funcionalidades de prestação de contas (FP04) e acompanhamento da execução (FP03) para uma segunda versão. Reforçar time com horas extras remuneradas nas últimas 4 semanas (custo estimado: R$ 15.000 da reserva de contingência).

---

### 2.2 R02 - Requisitos Ambíguos ou Incompletos

#### 2.2.1 Magnitude

**Alta**

#### 2.2.2 Descrição

O enunciado é intencionalmente incompleto e ambíguo, o que pode levar a interpretações diferentes e retrabalho se decisões de modelagem não forem bem documentadas e validadas.

#### 2.2.3 Impactos

- Retrabalho por mudança de requisitos
- Funcionalidades que não atendem às necessidades reais
- Conflitos entre membros do time sobre interpretações

#### 2.2.4 Indicadores

- Número de mudanças de requisitos por iteração
- Conflitos de interpretação identificados em revisões
- Feedback negativo de stakeholders em validações

#### 2.2.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Documentar todas as suposições e decisões de modelagem no Modelo de Domínio (seção 7) e no Vision (seção 4.3) | Todo o time | Final da Inception |
| Manter Glossário atualizado com novos termos a cada artefato produzido | Product Owner | Contínuo |
| Realizar workshop de requisitos com stakeholders (gestores e avaliadores do órgão) para validar fluxos críticos | Product Owner + Líder técnico | Semana 2 da Elaboration |
| Prototipar os 3 casos de uso centrais em wireframe navegável para validação antes de implementar | UX/UI Designer | Semanas 3-4 da Elaboration |

#### 2.2.6 Plano de Contingência

Se houver mais de 3 mudanças significativas de requisitos em uma iteração: pausar desenvolvimento, realizar reunião de alinhamento com stakeholders e time, revisar backlog. Se necessário, contratar consultoria de domínio (especialista em editais públicos) por 2 semanas — custo estimado: R$ 10.000 da reserva.

---

### 2.3 R03 - Equipe Sem Experiência Prévia Juntos

#### 2.3.1 Magnitude

**Média**

#### 2.3.2 Descrição

O time e toda a infraestrutura técnica começam do zero, sem histórico de trabalho conjunto, o que pode gerar dificuldades de comunicação e coordenação.

#### 2.3.3 Impactos

- Curva de aprendizado com ferramentas e processos
- Conflitos de comunicação
- Produtividade reduzida nas primeiras iterações

#### 2.3.4 Indicadores

- Tempo gasto em setup de infraestrutura
- Número de conflitos de integração (merge conflicts)
- Velocidade da equipe (story points por iteração)

#### 2.3.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Definir ferramentas, convenções de código, branching strategy e code owners no GitHub | Líder técnico | Semana 1 da Elaboration |
| Configurar CI/CD com linter, testes automatizados e code review obrigatório | Líder técnico + DevOps | Semanas 1-2 da Elaboration |
| Realizar daily de 15 min e retrospectiva ao final de cada iteração | Scrum Master | Contínuo |
| Fazer pair programming nas primeiras 2 semanas para nivelar conhecimento da stack | Líder técnico | Semanas 1-2 da Elaboration |

#### 2.3.6 Plano de Contingência

Se a velocidade nas primeiras 2 iterações for menor que 60% da estimada: reduzir escopo do MVP e realocar membros com mais afinidade para tarefas críticas. Estender prazo de Elaboration em até 2 semanas (consumindo buffer).

---

### 2.4 R04 - Restrições Regulatórias e Legais

#### 2.4.1 Magnitude

**Média**

#### 2.4.2 Descrição

Editais públicos estão sujeitos a legislação específica (Lei de Licitações, LGPD, Lei de Acesso à Informação), e o desconhecimento dessas obrigatoriedades pode levar a não conformidade do sistema.

#### 2.4.3 Impactos

- Sistema não conforme com legislação
- Necessidade de refatoração para atender requisitos legais
- Risco jurídico para o órgão

#### 2.4.4 Indicadores

- Requisitos legais não mapeados
- Mudanças de requisitos por descoberta de obrigações legais
- Feedback de especialistas legais

#### 2.4.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Mapear requisitos da LGPD, Lei 14.133/2021 e LAI aplicáveis ao sistema (ver Vision 9.1) | Product Owner | Final da Inception |
| Incluir assessoria jurídica do órgão como stakeholder consultivo para validação de requisitos legais | Product Owner | Semana 3 da Elaboration |
| Implementar módulo de auditoria (logs imutáveis) e anonimização de avaliadores desde a arquitetura inicial | Líder técnico | Elaboration |
| Revisar conformidade legal antes do IOC (marco da Construction) | Assessoria jurídica | Mês 6 |

#### 2.4.6 Plano de Contingência

Contratar consultoria jurídica especializada em licitações e LGPD para revisão de 40h — custo estimado: R$ 12.000 da reserva. Implementar módulo de compliance separado para isolar regras legais e facilitar atualizações futuras.

---

### 2.5 R05 - Falta de Integração com Sistemas Existentes

#### 2.5.1 Magnitude

**Baixa**

#### 2.5.2 Descrição

O órgão pode possuir sistemas legados (financeiro, contábil, RH) com os quais a plataforma precisará se integrar, e a falta de APIs ou documentação pode dificultar essa integração.

#### 2.5.3 Impactos

- Dados duplicados entre sistemas
- Processos manuais de consolidação
- Inconsistência de dados

#### 2.5.4 Indicadores

- Número de sistemas legados identificados
- Disponibilidade de APIs ou interfaces de integração
- Tempo gasto em atividades manuais de consolidação

#### 2.5.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Mapear sistemas legados existentes e sua documentação de API | Product Owner + Líder técnico | Semana 2 da Elaboration |
| Projetar arquitetura com camada de integração (API Gateway) desde o início | Líder técnico | Elaboration |
| Priorizar integrações: apenas exportação de dados contábeis (CSV) na V1 | Product Owner | Final da Elaboration |

#### 2.5.6 Plano de Contingência

Implementar exportação/importação de dados em lote (CSV) como alternativa à integração em tempo real. Adiar todas as integrações para V2, exceto a exportação contábil obrigatória por lei.

---

### 2.6 R06 - Resistência à Adoção pelos Usuários

#### 2.6.1 Magnitude

**Média**

#### 2.6.2 Descrição

Usuários acostumados com planilhas e e-mails podem resistir à migração para a plataforma digital, especialmente servidores com baixa afinidade tecnológica e proponentes de regiões com conectividade limitada.

#### 2.6.3 Impactos

- Sistema implantado mas subutilizado
- Persistência de processos paralelos em planilhas (shadow IT)
- Baixo retorno sobre investimento

#### 2.6.4 Indicadores

- Taxa de adoção por perfil de usuário (ex: % de editais criados no sistema vs. fora dele)
- Número de chamados de suporte por dificuldade de uso
- Feedback qualitativo em entrevistas com usuários

#### 2.6.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Realizar teste de usabilidade com 5 usuários representativos (1 gestor, 2 proponentes, 1 avaliador, 1 analista) | UX Designer | Semana 4 da Elaboration |
| Oferecer treinamento presencial para gestores e analistas (servidores internos) | Product Owner | Mês 7 (Transition) |
| Criar vídeos tutoriais de 3 min para cada fluxo principal (submeter proposta, avaliar, prestar contas) | UX Designer | Mês 7 (Transition) |
| Suporte prioritário por chat e telefone nas primeiras 4 semanas pós-implantação | Equipe de sustentação | Mês 8 |

#### 2.6.6 Plano de Contingência

Se adoção for inferior a 50% após 2 meses: realizar entrevistas com usuários para identificar barreiras. Se necessário, implementar modo simplificado (wizard) para submissão de propostas. Reforçar comunicação institucional via ofício circular do órgão determinando uso obrigatório.

---

### 2.7 R07 - Segurança da Informação e Vazamento de Dados

#### 2.7.1 Magnitude

**Alta**

#### 2.7.2 Descrição

A plataforma armazenará dados sensíveis de proponentes (CPF/CNPJ, dados bancários), documentos de avaliação sigilosos e pareceres técnicos. Um vazamento ou ataque bem-sucedido pode expor esses dados e gerar danos reputacionais e legais.

#### 2.7.3 Impactos

- Vazamento de dados pessoais (LGPD: multa de até 2% do faturamento)
- Acesso indevido a avaliações sigilosas antes da divulgação
- Perda de credibilidade do órgão

#### 2.7.4 Indicadores

- Vulnerabilidades encontradas em pen test
- Tentativas de acesso não autorizado (logs)
- Incidentes de segurança reportados

#### 2.7.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Adotar HTTPS com TLS 1.3, bcrypt para senhas, JWT com expiração curta (15 min + refresh token) | Líder técnico | Desde o dia 1 |
| Proteção contra OWASP Top 10: XSS (CSP header), CSRF (token), SQL Injection (ORM com prepared statements) | Desenvolvedores | Em toda implementação |
| Restringir acesso a dados de avaliação: avaliador só vê suas próprias avaliações até a divulgação final | Desenvolvedores | Construction |
| Realizar pen test externo antes da Transition | Consultoria externa | Mês 7 |
| Configurar backup diário criptografado do banco de dados | DevOps | Mês 1 |

#### 2.7.6 Plano de Contingência

Em caso de incidente: acionar time de resposta (líder técnico + assessoria jurídica), notificar ANPD em até 72h (LGPD), isolar sistema afetado, restaurar backup. Reserva para consultoria de resposta a incidentes: R$ 8.000.

---

### 2.8 R08 - Rotatividade da Equipe

#### 2.8.1 Magnitude

**Média**

#### 2.8.2 Descrição

Com 7 integrantes ao longo de 8 meses, a saída de um membro (especialmente líder técnico ou desenvolvedor sênior) pode impactar o cronograma. O custo médio de R$ 4.821,42 por integrante pode ser pouco competitivo, aumentando o risco de saída voluntária.

#### 2.8.3 Impactos

- Perda de conhecimento do domínio e do código
- Atraso nas entregas da iteração afetada
- Sobrecarga nos membros remanescentes

#### 2.8.4 Indicadores

- Saída de membros da equipe
- Satisfação da equipe (avaliada em retrospectivas)
- Concentração de conhecimento crítico em uma única pessoa (bus factor)

#### 2.8.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Documentar decisões de arquitetura (ADR), código (javadoc/docstring) e processos (wiki do repo) | Todo o time | Contínuo |
| Praticar code review obrigatório para todo pull request (mínimo 2 aprovadores) | Líder técnico | A partir da semana 1 |
| Rotacionar tarefas críticas entre membros (não deixar uma pessoa dona de um módulo inteiro) | Scrum Master | A cada iteração |
| Realizar 1:1 quinzenal para identificar insatisfações e agir preventivamente | Scrum Master | Quinzenal |

#### 2.8.6 Plano de Contingência

Se houver saída de membro: redistribuir tarefas, renegociar escopo da iteração corrente. Usar reserva de contingência para contratação emergencial de freelancer por até 2 meses (R$ 10.000). Se saída for do líder técnico: promover desenvolvedor mais sênior e contratar consultoria arquitetural pontual.

---

### 2.9 R09 - Indisponibilidade da Infraestrutura

#### 2.9.1 Magnitude

**Baixa**

#### 2.9.2 Descrição

O sistema depende de um servidor para hospedagem. Se o órgão prover esse servidor, há risco de indisponibilidade por manutenção não programada, falha de hardware ou conectividade. Se usar nuvem pública, há risco de custos inesperados ou vendor lock-in.

#### 2.9.3 Impactos

- Indisponibilidade do sistema durante picos de acesso (encerramento de submissões)
- Perda de dados não salvos
- Custos adicionais não previstos

#### 2.9.4 Indicadores

- Uptime do servidor
- Tempo de recuperação após falha
- Alertas de capacidade (CPU, disco, memória)

#### 2.9.5 Estratégia de Mitigação

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Especificar requisitos de infraestrutura (CPU, RAM, disco) e SLA esperado (99.5%) para o órgão | Líder técnico | Final da Elaboration |
| Containerizar aplicação (Docker) para facilitar migração entre servidores se necessário | DevOps | Elaboration |
| Configurar monitoring com alertas (Prometheus + Grafana ou CloudWatch) | DevOps | Mês 3 |
| Manter documentação de deploy atualizada para rebuild rápido em caso de falha catastrófica | DevOps | Contínuo |

#### 2.9.6 Plano de Contingência

Manter imagem Docker atualizada em registry externo (Docker Hub ou ECR). Documentar procedimento de rebuild completo em novo servidor (target: 4h). Se infraestrutura do órgão for instável: migrar para nuvem pública (AWS/GCP) usando reserva de contingência (custo estimado: R$ 1.500/mês).

---

## 3. Matriz Qualitativa de Probabilidade x Impacto

|  | Baixo Impacto | Médio Impacto | Alto Impacto |
|--|:--:|:--:|:--:|
| **Alta Probabilidade** | — | — | **R01** (Escopo) **R02** (Requisitos) |
| **Média Probabilidade** | — | **R03** (Equipe) **R06** (Adoção) **R08** (Rotatividade) | **R04** (Legal) **R07** (Segurança) |
| **Baixa Probabilidade** | — | **R05** (Integração) **R09** (Infra) | — |

### Legenda

| Quadrante | Ação |
|-----------|------|
| Alta Probabilidade + Alto Impacto | **Prioridade máxima** — mitigar ativamente, revisar em toda iteração |
| Alta Probabilidade + Médio Impacto / Média Probabilidade + Alto Impacto | **Atenção** — executar mitigações, monitorar indicadores |
| Média Probabilidade + Médio Impacto | **Monitorar** — executar mitigações leves, reavaliar no LCA |
| Baixa Probabilidade + Baixo/Médio Impacto | **Observar** — manter plano de contingência documentado |

---

## 4. Resumo Consolidado

| ID | Risco | Magnitude | Probabilidade | Impacto | Prioridade | Quadrante na Matriz |
|----|-------|-----------|--------------|---------|------------|---------------------|
| R01 | Escopo excessivo para orçamento/prazo | Alta | Alta | Alto | 1 | Vermelho |
| R02 | Requisitos ambíguos ou incompletos | Alta | Alta | Alto | 2 | Vermelho |
| R07 | Segurança da informação e vazamento de dados | Alta | Média | Alto | 3 | Amarelo |
| R04 | Restrições regulatórias e legais | Média | Média | Alto | 4 | Amarelo |
| R03 | Equipe sem experiência prévia juntos | Média | Média | Médio | 5 | Azul |
| R06 | Resistência à adoção pelos usuários | Média | Média | Médio | 6 | Azul |
| R08 | Rotatividade da equipe | Média | Média | Médio | 7 | Azul |
| R05 | Falta de integração com sistemas existentes | Baixa | Baixa | Médio | 8 | Verde |
| R09 | Indisponibilidade da infraestrutura | Baixa | Baixa | Médio | 9 | Verde |
