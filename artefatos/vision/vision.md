# Vision Document

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 29/04/2026 | 1.0 | Versão inicial da Inception | Grupo de Processos de Software |

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

#### Situação Atual
O processo de gestão de editais públicos tem a imagem de burocrático e ineficiente. Proponentes relatam dificuldade no acompanhamento do status de suas propostas, e a auditoria do ciclo de vida do edital é comprometida pela fragmentação de ferramentas (planilhas, e-mails, sistemas paralelos). A falta de rastreabilidade digital gera retrabalho e desconfiança.

#### Aspiração
Ser referência em transparência e eficiência na gestão de editais públicos, citado como modelo por outros entes estaduais e federais. A meta é que, em 2 anos após a implantação, 100% dos editais do órgão tramitem exclusivamente pela plataforma, eliminando processos paralelos em papel e planilhas.

#### Como a Plataforma Faz a Ponte
A plataforma sustenta essa transição ao digitalizar e unificar todo o fluxo de editais e projetos, garantindo:
- Rastreabilidade integral: cada ação tem timestamp, autor e IP registrados
- Prazos automáticos: o sistema controla vigência de submissões e notifica vencimentos
- Divulgação digital de resultados: portal público com dados abertos, eliminando a opacidade
- Integração entre fases: do rascunho do edital ao encerramento do projeto, tudo no mesmo sistema

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

- O número de pessoas envolvidas, deve variar mediante ao edital, mas a média provável é de 6 pessoas.
- A duração de um ciclo varia de acordo com o edital, mas em média é de 3 meses.
- O sistema deve ter suporte para uso em plataformas mobile.
- Atualmente, esse processo é realizado de forma fragmentada, com uso de planilhas, e-mails e sistemas desconectados.

### 3.5 Perfis dos Stakeholders

#### 3.5.1 Gestor do Edital

- **Representante**: Servidor público designado pelo órgão financiador
- **Descrição**: Servidor público responsável pela criação e gestão de editais
- **Tipo**: Usuário com conhecimento administrativo, nível técnico básico-intermediário
- **Responsabilidades**: Criar editais, definir critérios de avaliação, publicar resultados, encerrar submissões
- **Critérios de Sucesso**: Processo de edital transparente e eficiente, sem retrabalho
- **Envolvimento**: Requisitos, revisão de artefatos
- **Entregáveis**: Validação de requisitos de gestão de editais
- **Comentários/Problemas**: Resistência a abandonar planilhas. Necessidade de treinamento para uso do novo sistema.

#### 3.5.2 Proponente de Projeto

- **Representante**: Pessoas físicas e jurídicas cadastradas no sistema
- **Descrição**: Pessoa física ou jurídica que submete propostas a editais
- **Tipo**: Usuário externo, nível técnico variável
- **Responsabilidades**: Submeter propostas, acompanhar execução, prestar contas
- **Critérios de Sucesso**: Facilidade de submissão, acompanhamento transparente
- **Envolvimento**: Requisitos, testes de usabilidade
- **Entregáveis**: Feedback sobre usabilidade
- **Comentários/Problemas**: Dificuldade com sistemas digitais se interface for complexa. Precisa de um fluxo guiado e intuitivo.

#### 3.5.3 Avaliador da Proposta

- **Representante**: Especialistas designados pelo órgão financiador por área temática
- **Descrição**: Especialista designado para avaliar propostas submetidas
- **Tipo**: Usuário com conhecimento no tema do edital
- **Responsabilidades**: Avaliar propostas, aplicar critérios, emitir parecer
- **Critérios de Sucesso**: Processo de avaliação claro e rastreável
- **Envolvimento**: Requisitos, validação de critérios
- **Entregáveis**: Validação de fluxo de avaliação
- **Comentários/Problemas**: Pode ter vieses se souber a identidade do proponente. O sigilo do avaliador (quando aplicável) deve ser garantido pelo sistema.

#### 3.5.4 Analista de Prestação de Contas

- **Representante**: Servidores da controladoria ou área financeira do órgão
- **Descrição**: Servidor responsável por analisar a prestação de contas dos projetos
- **Tipo**: Usuário com conhecimento financeiro e administrativo
- **Responsabilidades**: Verificar documentos, analisar conformidade, emitir parecer final
- **Critérios de Sucesso**: Conformidade verificável e auditável
- **Envolvimento**: Requisitos, validação de fluxo de prestação de contas
- **Entregáveis**: Validação de requisitos de prestação de contas
- **Comentários/Problemas**: Volume de prestações de contas pode ser alto em picos. Necessita de ferramentas de filtro, busca e notificações de prazo.

### 3.6 Perfis dos Usuários

Os perfis de usuários são os mesmos dos Stakeholders (Gestor do Edital, Proponente, Avaliador e Analista de Prestação de Contas), já detalhados na seção 3.5.

### 3.7 Necessidades Chave dos Stakeholders e Usuários

| Necessidade | Prioridade | Preocupações | Solução Atual | Solução Proposta |
|-------------|-----------|-------------|---------------|-----------------|
| Gestão integrada de editais | Alta | Fragmentação do processo | Planilhas e e-mails | Plataforma digital unificada |
| Transparência no processo | Alta | Dificuldade de auditoria | Processos manuais | Rastreabilidade e logs |
| Acompanhamento de projetos | Alta | Falta de visibilidade | E-mails e reuniões | Dashboard e notificações |
| Prestação de contas digital | Média | Processo burocrático | Documentos físicos | Upload e análise digital |

### 3.8 Alternativas e Concorrência

Não foram identificados concorrentes diretos no mercado de plataformas de gestão de editais públicos para as áreas esportiva e cultural. As alternativas existentes são:

| Alternativa | Descrição | Limitação |
|------------|-----------|-----------|
| Processo atual (planilhas/e-mails) | Método atualmente em uso pelo órgão | Fragmentado, sem rastreabilidade, difícil auditoria |
| Plataformas genéricas de submissão (Google Forms, JotForm) | Ferramentas de formulário online | Não cobrem o ciclo completo (avaliação, execução, prestação de contas) |
| Sistemas de outros órgãos | Soluções desenvolvidas sob medida para outros entes | Não são reutilizáveis (contextos jurídicos e de processo distintos) |
| Soluções comerciais de grant management (Fluxx, Submittable) | Plataformas SaaS internacionais | Custo em dólar, sem conformidade com legislação brasileira, sem suporte a prestação de contas no modelo nacional |

---

## 4. Visão Geral do Produto

### 4.1 Perspectiva do Produto

O sistema é independente e contido em si próprio, tendo como objetivo centralizar o processo de gestão de editais. No futuro, poderá expor APIs para integração com sistemas de contabilidade e recursos humanos do órgão, mas essas integrações estão fora do escopo da primeira versão e são tratadas como pontos de extensão no Risk R05.

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

| Suposição/Dependência | Descrição | Impacto se não atendida |
|----------------------|-----------|------------------------|
| Infraestrutura de servidor | O sistema requer um servidor para hospedagem | Bloqueante para implantação |
| Acesso à internet | Usuários finais necessitam de conexão para acessar o sistema | Bloqueante para uso |
| Apoio institucional do órgão | O órgão deve designar gestores e analistas para operar o sistema | Sem operadores, o sistema fica ocioso |
| Cadastro de proponentes | Proponentes devem possuir cadastro válido com CPF/CNPJ | Impede submissão de propostas |
| Designação de avaliadores | O órgão deve prover lista de avaliadores qualificados por área temática | Impede fase de avaliação |
| Conformidade legal | O sistema depende do alinhamento com a legislação vigente (LGPD, Lei 14.133/2021) | Risco jurídico para o órgão |
| Ambiente de homologação | Necessário servidor separado para testes antes da publicação de cada release | Risco de regressões em produção |

### 4.4 Custo e Precificação

| Item | Valor |
|------|-------|
| Orçamento máximo total | R$ 300.000,00 |
| Prazo máximo | 8 meses |
| Espaço físico, máquinas, licenças | R$ 0,00 (providos pelo órgão) |

**Distribuição por fase RUP (rateio proporcional):**

| Fase | % do Esforço | Custo Estimado |
|------|:--:|:--:|
| Inception | 6% (0.5 meses) | R$ 16.875,00 |
| Elaboration | 25% (2 meses) | R$ 67.500,00 |
| Construction | 56% (4.5 meses) | R$ 151.875,00 |
| Transition | 13% (1 mês) | R$ 33.750,00 |
| Reserva de Contingência | — | R$ 30.000,00 |

> **Nota**: Os valores são estimativas grosseiras da Inception e devem ser reavaliados no marco LCA da Elaboration.

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

### 6.1 Restrições Técnicas
- O sistema deve ser construído como uma aplicação web, sem dependência de plataformas específicas (Windows/Mac).
- O backend deve usar tecnologias open source (Python, Java ou Node.js) e banco de dados relacional (PostgreSQL).
- O frontend deve ser responsivo, compatível com Chrome, Firefox, Edge e Safari (versões dos últimos 2 anos).
- A comunicação entre frontend e backend deve ser exclusivamente via HTTPS com API REST documentada.
- O deploy deve ser feito em servidor Linux provido pelo órgão, usando Docker.

### 6.2 Restrições Regulatórias
- Conformidade com a LGPD (Lei 13.709/2018): consentimento para coleta de dados pessoais, anonimização de avaliadores, direito de exclusão.
- Conformidade com a Lei 14.133/2021 (Licitações): transparência, publicação de resultados, fase recursal.
- Conformidade com a Lei de Acesso à Informação (12.527/2011): portal de dados abertos com editais e projetos.

### 6.3 Restrições Operacionais
- Escopo limitado a editais das áreas esportiva e cultural do órgão estadual.
- Orçamento máximo de R$ 300.000,00, prazo máximo de 8 meses.
- Time fixo de 7 integrantes, sem possibilidade de contratação adicional.
- Infraestrutura técnica começa do zero (repositórios, CI/CD, ambientes).

---

## 7. Faixas de Qualidade

| Atributo | Faixa | Medição |
|---------|-------|---------|
| **Desempenho** | Tempo de resposta de até 3 segundos para operações CRUD; até 10 segundos para submissão com upload de múltiplos documentos | Medido via APM no servidor |
| **Disponibilidade** | 99,5% em horário comercial (8h-18h em dias úteis); 97% fora desse horário | Uptime monitorado |
| **Usabilidade** | Proponentes (público externo, nível técnico variável) devem conseguir submeter uma proposta sem necessidade de treinamento ou manual | Teste de usabilidade com 5 usuários representativos |
| **Segurança** | Dados trafegados exclusivamente via HTTPS; autenticação com senha e MFA para usuários internos; proteção contra OWASP Top 10 (XSS, CSRF, SQL Injection) | Pen test antes da Transition |
| **Escalabilidade** | Suporte a múltiplos editais simultâneos e milhares de editais no banco de dados; picos de acesso em datas de encerramento de submissão | Teste de carga simulando 500 usuários simultâneos |
| **Auditabilidade** | Toda ação de criação, edição, exclusão, avaliação e aprovação deve gerar log imutável com timestamp, usuário e IP | Verificação por amostragem de logs |
| **Acessibilidade** | Atender critérios WCAG 2.1 Nível AA, garantindo uso por pessoas com deficiência visual e motora | Auditoria com leitor de tela e navegação por teclado |

---

## 8. Precedência e Prioridade

1. Criação e configuração de editais
2. Definição de critérios de avaliação
3. Submissão e análise de recursos
4. Submissão de propostas
5. Avaliação e seleção
6. Publicação de editais
7. Encerramento de submissões
8. Divulgação de resultados
9. Acompanhamento da execução
10. Prestação de contas
11. Emissão de parecer final

---

## 9. Outros Requisitos do Produto

### 9.1 Normas Aplicáveis

| Norma | Descrição | Impacto no sistema |
|-------|-----------|-------------------|
| **LGPD (Lei 13.709/2018)** | Proteção de dados pessoais de proponentes e avaliadores | Consentimento, anonimização de avaliações, direito à exclusão de dados |
| **Lei 14.133/2021** | Nova Lei de Licitações e Contratos Administrativos | Transparência na divulgação, prazos regimentais, fase recursal |
| **Lei de Acesso à Informação (Lei 12.527/2011)** | Transparência ativa de dados públicos | Portal de transparência com dados abertos de editais e projetos financiados |
| **WCAG 2.1 (Nível AA)** | Acessibilidade em sistemas web governamentais | Contraste, navegação por teclado, leitores de tela, texto alternativo |
| **Resoluções estaduais específicas** | Normas do órgão financiador para cada área temática | Campos customizáveis por tipo de edital |

### 9.2 Requisitos de Sistema

| Requisito | Especificação |
|----------|---------------|
| **Sistema operacional do servidor** | Linux (Ubuntu Server 22.04 LTS ou superior) |
| **Navegadores suportados** | Chrome 90+, Firefox 90+, Edge 90+, Safari 15+ |
| **Dispositivos** | Desktop (primário), Tablet e Mobile (responsivo) |
| **Resolução mínima** | 360px de largura (mobile); 1280px (desktop recomendado) |
| **Stack sugerida** | Backend: Python (FastAPI/Django) ou Java (Spring Boot). Frontend: React ou Vue.js. Banco: PostgreSQL |
| **Infraestrutura** | Servidor único (início). Possibilidade de escalar para balanceamento de carga se os picos de acesso exigirem |

### 9.3 Requisitos de Desempenho

| Requisito | Alvo | Condição |
|----------|------|----------|
| Tempo de carregamento de página | Até 2 segundos | Conexão banda larga (10 Mbps) |
| Tempo de upload de documentos | Até 30 segundos para arquivo de 10 MB | Conexão banda larga |
| Processamento de ranking | Até 15 segundos para consolidação de 500 propostas com 3 avaliadores cada | Operação em lote, fora do horário de pico |
| Geração de relatório de auditoria | Até 10 segundos | Relatório completo de um edital |
| Concorrência | Suporte a 200 usuários simultâneos sem degradação acima de 20% no tempo de resposta | Pico de encerramento de submissões |

### 9.4 Requisitos Ambientais

| Requisito | Descrição |
|----------|-----------|
| **Ambiente de desenvolvimento** | Máquinas locais dos desenvolvedores, com Docker para uniformização |
| **Ambiente de homologação** | Servidor separado, réplica reduzida de produção, para validação pré-release |
| **Ambiente de produção** | Servidor único gerenciado pelo órgão, com acesso restrito via SSH |
| **Backup** | Backup diário do banco de dados, retenção de 30 dias |
| **Manutenção** | Janela de manutenção programada: domingos 0h-6h, com aviso prévio de 48h aos usuários |
| **Monitoramento** | Logs centralizados, alertas de erro 5xx e downtime via e-mail para o time de sustentação |

---

## 10. Requisitos de Documentação

### 10.1 Manual do Usuário

O sistema deve oferecer um manual do usuário em PDF, separado por perfil (Gestor, Proponente, Avaliador e Analista). O manual deve conter capturas de tela e descrever o passo a passo para cada fluxo principal. Deve ser entregue junto com a versão final, na fase de Transition.

### 10.2 Ajuda Online

Tooltips contextuais em campos de formulário (ex: "Descreva o objetivo geral do projeto em até 500 caracteres"). Link "Central de Ajuda" no rodapé com FAQ pesquisável, cobrindo dúvidas frequentes de proponentes (como anexar documentos, prazos, requisitos de formatação).

### 10.3 Guias de Instalação e Configuração

Readme no repositório com instruções para setup do ambiente de desenvolvimento (Docker Compose). Guia de deploy em produção com checklist de pré-requisitos (servidor Linux, PostgreSQL instalado, certificado SSL ativo, variáveis de ambiente configuradas).

### 10.4 Rotulagem e Empacotamento

O sistema será distribuído como imagem Docker (backend) e bundle estático (frontend), versionados semânticamente (MAJOR.MINOR.PATCH). A página de login deve exibir o nome do sistema ("Plataforma de Gestão de Editais Públicos"), o brasão do órgão e a versão corrente no rodapé.

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

| Funcionalidade | Status | Benefit | Effort (pessoas-semana) | Risk | Stability | Target Release | Assigned To | Reason |
|---------------|--------|---------|------------------------|------|-----------|---------------|-------------|--------|
| FE01 - Criação e configuração de editais | Proposed | Critical | 4 | Medium | Stable | V1.0 | Equipe | Enunciado |
| FE02 - Definição de critérios de avaliação | Proposed | Critical | 3 | Low | Stable | V1.0 | Equipe | Enunciado |
| FE03 - Submissão e análise de recursos | Proposed | Important | 4 | Medium | Medium | V1.0 | Equipe | Enunciado |
| FE04 - Publicação de editais | Proposed | Critical | 1 | Low | Stable | V1.0 | Equipe | Enunciado |
| FE05 - Encerramento de submissões | Proposed | Important | 1 | Low | Stable | V1.0 | Equipe | Enunciado |
| FE06 - Divulgação de resultados | Proposed | Critical | 2 | Low | Stable | V1.0 | Equipe | Enunciado |
| FP01 - Submissão de propostas | Proposed | Critical | 6 | Medium | Medium | V1.0 | Equipe | Enunciado |
| FP02 - Avaliação e seleção | Proposed | Critical | 5 | Medium | Medium | V1.0 | Equipe | Enunciado |
| FP03 - Acompanhamento da execução | Proposed | Important | 4 | Medium | High | V1.0 | Equipe | Enunciado |
| FP04 - Prestação de contas | Proposed | Important | 5 | High | High | V1.0 | Equipe | Enunciado |
| FP05 - Emissão de parecer final | Proposed | Important | 2 | Low | Medium | V1.0 | Equipe | Enunciado |
