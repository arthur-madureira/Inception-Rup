# Vision Document

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| - | 1.0 | Versão inicial da Inception | - |

---

## 1. Introdução

Este documento de Visão define o problema, os stakeholders, as necessidades de alto nível e as características principais da Plataforma de Gestão de Editais Públicos. Ele estabelece o "porquê" do projeto e serve como artefato central da fase de Inception do RUP.

### 1.1 Propósito

Definir a visão de alto nível do sistema, seus stakeholders, necessidades e funcionalidades principais, servindo como base para a decisão de continuidade (go/no-go) no marco Lifecycle Objectives (LCO).

### 1.2 Escopo

Este documento abrange a definição de escopo da Plataforma de Gestão de Editais Públicos para financiamento de projetos esportivos e culturais, cobrindo a gestão do ciclo de vida completo de editais e projetos financiados.

### 1.3 Definições, Acrônimos e Abreviações

Ver seção **Glossário** ao final deste documento.

### 1.4 Referências

- Enunciado da Atividade Prática - Unidade 1 (Processos de Software)
- [Templates Oficiais do RUP](https://files.defcon.no/RUP/process/templates.htm)

### 1.5 Visão Geral

As seções seguintes apresentam o posicionamento do produto, os stakeholders e usuários, as funcionalidades do sistema, restrições e requisitos de qualidade.

---

## 2. Posicionamento

### 2.1 Oportunidade de Negócio

Atualmente, o processo de gerenciar editais públicos de financiamento de projetos esportivos e culturais é realizado de forma fragmentada, com uso de planilhas, e-mails e sistemas desconectados, dificultando a transparência, o acompanhamento e a auditoria. O projeto atual se propõe a desenvolver uma plataforma digital para gerenciar esses editais.

### 2.2 Declaração do Problema

| Campo | Descrição |
|-------|-----------|
| **O problema** | A gestão de editais públicos é realizada de forma fragmentada, com planilhas, e-mails e sistemas desconectados |
| **Afeta** | Gestores de editais, proponentes de projetos, avaliadores e analistas de prestação de contas |
| **Impacto** | Dificuldade de transparência, acompanhamento e auditoria dos editais e projetos financiados |
| **Uma solução bem-sucedida** | Uma plataforma digital integrada que apoie todo o ciclo de vida dos editais e projetos financiados |

### 2.3 Declaração de Posição do Produto

| Campo | Descrição |
|-------|-----------|
| **Para (For)** | Órgãos públicos que gerenciam editais de financiamento |
| **Que (Who)** | Necessitam de transparência e eficiência na gestão de editais |
| **O (The)** | Plataforma de Gestão de Editais Públicos |
| **Que (That)** | Apoia todo o ciclo de vida dos editais e projetos financiados |
| **Ao contrário de (Unlike)** | Processos manuais fragmentados (planilhas, e-mails, sistemas desconectados) |
| **Nosso produto (Our)** | Unifica e digitaliza todo o processo, garantindo transparência, rastreabilidade e auditoria |

---

## 3. Descrição dos Stakeholders e Usuários

### 3.1 Demográficos do Mercado

O processo que envolve a gestão dos editais tem a imagem de burocrático e proponentes relatam dificuldade no acompanhamento e a auditoria no ciclo de vida do edital. A aspiração é ser referência em transparência e eficiência na gestão de editais, citado como modelo por outros entes. A plataforma sustenta essa transição ao digitalizar e unificar todo o fluxo, garantindo rastreabilidade, prazos automáticos e divulgação digital de resultados — eliminando a fragmentação que alimenta a imagem atual e viabilizando a reputação desejada.

### 3.2 Resumo dos Stakeholders

| Nome | Descrição | Responsabilidades |
|------|-----------|-------------------|
| Órgão financiador | Entidade governamental que publica editais | Definir políticas, alocar orçamento |
| Gestor do edital | Servidor público responsável pelo edital | Criar, configurar e gerenciar editais | 
| Proponente de projeto | Pessoa/entidade que submete propostas | Submeter propostas, prestar contas |
| Avaliador da proposta | Especialista que avalia propostas | Avaliar, classificar propostas e aprovar editais |
| Analista de prestação de contas | Servidor que analisa a prestação de contas | Verificar conformidade, emitir parecer |

### 3.3 Resumo dos Usuários

| Nome | Descrição | Responsabilidades | Stakeholder representante |
|------|-----------|-------------------|--------------------------|
| Gestor do edital | Cria e configura editais no sistema | Criar editais, definir critérios, publicar resultados | Órgão financiador |
| Proponente | Submete propostas e presta contas | Submeter propostas, enviar relatórios, prestar contas | Proponente de projeto |
| Avaliador | Avalia propostas submetidas | Aplicar critérios, emitir parecer de avaliação | Órgão financiador |
| Analista de prestação de contas | Analisa relatórios financeiros e de execução | Verificar documentos, emitir parecer final | Órgão financiador |

### 3.4 Ambiente do Usuário

<!-- Descrever o ambiente de trabalho dos usuários: número de pessoas, ciclo de tarefas, plataformas, etc. -->

### 3.5 Perfis dos Stakeholders

#### 3.5.1 Gestor do Edital

- **Representante**: [a definir]
- **Descrição**: Servidor público responsável pela criação e gestão de editais
- **Tipo**: Usuário com conhecimento administrativo, nível técnico básico-intermediário
- **Responsabilidades**: Criar editais, definir critérios de avaliação, publicar resultados, encerrar submissões
- **Critérios de Sucesso**: Processo de edital transparente e eficiente, sem retrabalho
- **Envolvimento**: Requisitos, revisão de artefatos
- **Entregáveis**: Validação de requisitos de gestão de editais
- **Comentários/Problemas**: [a definir]

#### 3.5.2 Proponente de Projeto

- **Representante**: [a definir]
- **Descrição**: Pessoa física ou jurídica que submete propostas a editais
- **Tipo**: Usuário externo, nível técnico variável
- **Responsabilidades**: Submeter propostas, acompanhar execução, prestar contas
- **Critérios de Sucesso**: Facilidade de submissão, acompanhamento transparente
- **Envolvimento**: Requisitos, testes de usabilidade
- **Entregáveis**: Feedback sobre usabilidade
- **Comentários/Problemas**: [a definir]

#### 3.5.3 Avaliador da Proposta

- **Representante**: [a definir]
- **Descrição**: Especialista designado para avaliar propostas submetidas
- **Tipo**: Usuário com conhecimento no tema do edital
- **Responsabilidades**: Avaliar propostas, aplicar critérios, emitir parecer
- **Critérios de Sucesso**: Processo de avaliação claro e rastreável
- **Envolvimento**: Requisitos, validação de critérios
- **Entregáveis**: Validação de fluxo de avaliação
- **Comentários/Problemas**: [a definir]

#### 3.5.4 Analista de Prestação de Contas

- **Representante**: [a definir]
- **Descrição**: Servidor responsável por analisar a prestação de contas dos projetos
- **Tipo**: Usuário com conhecimento financeiro e administrativo
- **Responsabilidades**: Verificar documentos, analisar conformidade, emitir parecer final
- **Critérios de Sucesso**: Conformidade verificável e auditável
- **Envolvimento**: Requisitos, validação de fluxo de prestação de contas
- **Entregáveis**: Validação de requisitos de prestação de contas
- **Comentários/Problemas**: [a definir]

### 3.6 Perfis dos Usuários

<!-- Expandir perfis detalhados de cada tipo de usuário, seguindo a mesma estrutura dos stakeholders -->

### 3.7 Necessidades Chave dos Stakeholders e Usuários

| Necessidade | Prioridade | Preocupações | Solução Atual | Solução Proposta |
|-------------|-----------|-------------|---------------|-----------------|
| Gestão integrada de editais | Alta | Fragmentação do processo | Planilhas e e-mails | Plataforma digital unificada |
| Transparência no processo | Alta | Dificuldade de auditoria | Processos manuais | Rastreabilidade e logs |
| Acompanhamento de projetos | Alta | Falta de visibilidade | E-mails e reuniões | Dashboard e notificações |
| Prestação de contas digital | Média | Processo burocrático | Documentos físicos | Upload e análise digital |

### 3.8 Alternativas e Concorrência

<!-- Descrever alternativas existentes e concorrentes, se houver -->

---

## 4. Visão Geral do Produto

### 4.1 Perspectiva do Produto

<!-- Descrever como o produto se relaciona com outros sistemas. Incluir diagrama de blocos se possível. -->

A plataforma é um sistema autônomo que centraliza a gestão de editais públicos, substituindo processos fragmentados.

### 4.2 Resumo das Capacidades

| Benefício do Cliente | Funcionalidades de Suporte |
|---------------------|---------------------------|
| Gestão completa do ciclo de vida dos editais | Criação, configuração, publicação e encerramento de editais |
| Submissão digital de propostas | Portal de submissão com upload de documentos |
| Avaliação estruturada de propostas | Sistema de avaliação por critérios definidos |
| Acompanhamento de projetos financiados | Dashboard com status e relatórios |
| Prestação de contas digital | Upload de comprovantes e análise de conformidade |
| Transparência e rastreabilidade | Logs, histórico e auditoria |

### 4.3 Suposições e Dependências

<!-- Listar fatores que podem afetar as funcionalidades -->

### 4.4 Custo e Precificação

- Orçamento máximo: R$ 300.000,00
- Prazo máximo: 8 meses
- Sem custos com espaço físico, máquinas ou licenças

### 4.5 Licenciamento e Instalação

<!-- Endereçar questões de licenciamento e instalação -->

---

## 5. Funcionalidades do Produto

### 5.1 Gestão de Editais

- **FE01**: Criação e configuração de editais
- **FE02**: Definição de critérios de avaliação
- **FE03**: Submissão e análise de recursos
- **FE04**: Publicação de editais
- **FE05**: Encerramento de submissões
- **FE06**: Divulgação de resultados

### 5.2 Gestão de Projetos

- **FP01**: Submissão de propostas
- **FP02**: Avaliação e seleção
- **FP03**: Acompanhamento da execução
- **FP04**: Prestação de contas
- **FP05**: Emissão de parecer final

---

## 6. Restrições

<!-- Listar restrições de design, externas ou outras dependências -->

- Orçamento de no máximo R$ 300.000,00
- Prazo de no máximo 8 meses
- Time e infraestrutura começam do zero

---

## 7. Faixas de Qualidade

<!-- Definir faixas de qualidade para desempenho, robustez, usabilidade, etc. -->

---

## 8. Precedência e Prioridade

<!-- Definir prioridades das funcionalidades -->

---

## 9. Outros Requisitos do Produto

### 9.1 Normas Aplicáveis

<!-- Listar normas legais, regulatórias, de comunicação, etc. -->

### 9.2 Requisitos de Sistema

<!-- Definir sistemas operacionais, plataformas, configurações suportadas -->

### 9.3 Requisitos de Desempenho

<!-- Detalhar questões de desempenho -->

### 9.4 Requisitos Ambientais

<!-- Condições de uso, recursos disponíveis, manutenção -->

---

## 10. Requisitos de Documentação

### 10.1 Manual do Usuário

<!-- Descrever propósito e conteúdo do manual -->

### 10.2 Ajuda Online

<!-- Endereçar sistema de ajuda online -->

### 10.3 Guias de Instalação e Configuração

<!-- Instruções de instalação e configuração -->

### 10.4 Rotulagem e Empacotamento

<!-- Definir necessidades de rotulagem -->

---

## Glossário

| Termo | Definição |
|-------|-----------|
| **Edital** | Documento oficial que divulga regras e critérios para financiamento de projetos |
| **Proponente** | Pessoa física ou jurídica que submete uma proposta a um edital |
| **Proposta** | Projeto submetido a um edital de financiamento, seguindo os critérios definidos |
| **Avaliador** | Especialista designado para analisar e classificar propostas submetidas |
| **Prestação de Contas** | Conjunto de documentos e relatórios que comprovam a aplicação dos recursos recebidos |
| **Parecer** | Opinião técnica ou administrativa emitida sobre uma proposta ou prestação de contas |
| **Triagem** | Verificação inicial de conformidade de uma proposta antes da avaliação detalhada |
| **Recurso** | Pedido de revisão de uma decisão relacionada a um edital ou proposta |
| **Ciclo de Vida do Edital** | Conjunto de estados pelos quais um edital passa (Rascunho → Publicado → Em submissão → Em avaliação → Finalizado) |
| **Ciclo de Vida do Projeto** | Conjunto de estados pelos quais um projeto financiado passa (Submetido → Em triagem → Em avaliação → Aprovado/Reprovado → Em execução → Prestação de contas → Encerrado) |
| **Gestor do Edital** | Servidor público responsável pela criação e gestão de editais |
| **Analista de Prestação de Contas** | Servidor responsável por verificar a conformidade da prestação de contas dos projetos |
| **RUP** | Rational Unified Process - processo de desenvolvimento de software iterativo e incremental |
| **Inception** | Primeira fase do RUP, focada em entender o escopo e viabilidade do projeto |
| **LCO** | Lifecycle Objectives - marco da fase de Inception que avalia a viabilidade do projeto |

---

## Apêndice A. Atributos de Funcionalidades

| Atributo | Descrição |
|----------|-----------|
| **Status** | Proposed / Approved / Incorporated |
| **Benefit** | Critical / Important / Useful |
| **Effort** | Estimativa de esforço (pessoas-semana) |
| **Risk** | High / Medium / Low |
| **Stability** | Probabilidade de mudança |
| **Target Release** | Versão pretendida para a funcionalidade |
| **Assigned To** | Equipe responsável |
| **Reason** | Origem da solicitação |
