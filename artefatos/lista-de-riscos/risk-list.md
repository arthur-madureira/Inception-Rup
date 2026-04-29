# Risk List

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| - | 1.0 | Versão inicial da Inception | - |
| - | 1.1 | Versão inicial da Inception | Caio Trindade |

---

## 1. Introdução

### 1.1 Propósito

Este documento identifica, prioriza e descreve os principais riscos do projeto da Plataforma de Gestão de Editais Públicos, com estratégias iniciais de mitigação.

### 1.2 Escopo

Os riscos listados são aqueles identificados durante a fase de Inception, abrangendo riscos técnicos, de negócio e de recursos.

### 1.3 Definições, Acrônimos e Abreviações

Ver Glossário no documento de Visão.

### 1.4 Referências

- Vision Document
- Business Case

### 1.5 Visão Geral

A seção 2 apresenta os riscos identificados, cada um com magnitude, descrição, impactos, indicadores, estratégia de mitigação e plano de contingência.

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

Priorizar funcionalidades críticas (critério de Pareto). Definir MVP com funcionalidades essenciais para o ciclo de vida do edital. Utilizar desenvolvimento iterativo e incremental para entregar valor desde as primeiras iterações.

#### 2.1.6 Plano de Contingência

Reduzir escopo para funcionalidades essenciais (criar edital, submeter proposta, avaliar proposta). Adiar funcionalidades de prestação de contas e acompanhamento para uma segunda versão.

---

### 2.2 R02 - Requisitos Ambíguos ou Incompletos

#### 2.2.1 Magnitude

**Médoa**

#### 2.2.2 Descrição

O enunciado é intencionalmente incompleto e ambíguo, o que pode levar a interpretações diferentes e retrabalho se decisões de modelagem não forem bem documentadas e validadas.

#### 2.2.3 Impactos

- Retrabalho por mudança de requisitos
- Funcionalidades que não atendem às necessidades reais
- Conflitos entre membros do time sobre interpretações

#### 2.2.4 Indicadores

- Número de mudanças de requisitos por iteração
- Conflitos de interpretação identificados em revisões
- Feedback negativo de stakeholders

#### 2.2.5 Estratégia de Mitigação

Documentar todas as suposições e decisões de modelagem explicitamente. Validar interpretações com stakeholders. Manter o Glossário atualizado para alinhar vocabulário.

#### 2.2.6 Plano de Contingência

Realizar workshops de requisitos com stakeholders para esclarecer ambiguidades, como por exemplo o funcionamento atual da integração entre ferramentas. Prototipar funcionalidades críticas para validar entendimento antes de implementar.

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
- Número de conflitos de integração
- Velocidade da equipe nas primeiras iterações

#### 2.3.5 Estratégia de Mitigação

Definir processos e ferramentas de comunicação no início. Estabelecer convenções de código e fluxo de trabalho. Realizar reuniões de alinhamento frequentes na fase de Elaboration.

#### 2.3.6 Plano de Contingência

Reduzir escopo para compensar menor produtividade. Alocar tempo extra para setup nas primeiras semanas.

---

### 2.4 R04 - Restrições Regulatórias e Legais

#### 2.4.1 Magnitude

**Média**

#### 2.4.2 Descrição

Editais públicos estão sujeitos a legislação específica (Lei de Licitações, LGPD, etc.), e o desconhecimento dessas obrigatoriedades pode levar a não conformidade do sistema.

#### 2.4.3 Impactos

- Sistema não conformidade com legislação
- Necessidade de refatoração para atender requisitos legais
- Risco jurídico para o órgão

#### 2.4.4 Indicadores

- Requisitos legais não mapeados
- Mudanças de requisitos por descoberta de obrigações legais
- Feedback de especialistas legais

#### 2.4.5 Estratégia de Mitigação

Identificar requisitos legais e regulatórios na fase de Inception. Consultar legislação aplicável (Lei 14.133/2021, LGPD). Incluir especialista legal como stakeholder consultivo.

#### 2.4.6 Plano de Contingência

Contratar consultoria jurídica para revisar requisitos. Implementar módulo de compliance separado para facilitar atualizações legais.

---

### 2.5 R05 - Falta de Integração com Sistemas Existentes

#### 2.5.1 Magnitude

**Baixa**

#### 2.6.2 Descrição

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

Mapear sistemas legados existentes na fase de Inception. Projetar a plataforma com arquitetura orientada a APIs desde o início. Priorizar integrações críticas.

#### 2.5.6 Plano de Contingência

Implementar importação/exportação de dados em lote como alternativa à integração em tempo real. Adiar integrações não críticas.

---

## Resumo de Riscos

| ID | Risco | Magnitude | Probabilidade | Impacto | Prioridade |
|----|-------|-----------|--------------|---------|------------|
| R01 | Escopo excessivo para orçamento/prazo | Alta | Alta | Alto | 1 |
| R02 | Requisitos ambíguos ou incompletos | Alta | Alta | Alto | 2 |
| R03 | Equipe sem experiência prévia juntos | Média | Média | Médio | 3 |
| R04 | Restrições regulatórias e legais | Média | Média | Alto | 4 |
| R05 | Falta de integração com sistemas existentes | Baixa | Baixa | Médio | 5 |
