# Business Case

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
| :--- | :--- |
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

### Histórico de Revisões

| Data | Versão | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| [Data Atual] | 1.0 | Versão inicial da Inception estruturada a partir do escopo do projeto | Grupo de Processos de Software |

---

## 1. Introdução

### 1.1 Propósito
Este documento apresenta a justificativa econômica do projeto da Plataforma de Gestão de Editais Públicos, incluindo estimativas de custo, prazo e retorno sobre investimento. O objetivo é sustentar a decisão de "go/no-go" no marco *Lifecycle Objectives* (LCO) da fase de Inception.

### 1.2 Escopo
A análise abrange o desenvolvimento completo da plataforma, desde a fase de Inception até a entrega da primeira versão funcional. O projeto possui restrições estritas, incluindo um orçamento máximo de R$ 300.000,00 e um prazo máximo de 8 meses.

### 1.3 Definições, Acrônimos e Abreviações
Ver Glossário no documento de Visão.

### 1.4 Referências
* Enunciado da Atividade Prática - Unidade 1, Processos de Software
* Vision Document
* Risk List

### 1.5 Visão Geral
As seções seguintes descrevem o produto, o contexto de negócio, os objetivos, a previsão financeira e as restrições do projeto.

---

## 2. Descrição do Produto
A Plataforma de Gestão de Editais Públicos é um sistema digital projetado para um órgão do estado, focado no gerenciamento de editais de financiamento esportivo e cultural. A plataforma deverá apoiar todo o ciclo de vida, desde a criação do edital até a prestação de contas final dos projetos aprovados. O sistema permitirá a gestão de editais (criação, avaliação, publicação) e a gestão de projetos (submissão, acompanhamento e prestação de contas).

---

## 3. Contexto de Negócio
Atualmente, o órgão do estado realiza o processo de gestão de editais de forma altamente fragmentada. O uso excessivo de planilhas, trocas de e-mails e sistemas desconectados gera gargalos operacionais, dificultando a transparência, o acompanhamento efetivo e a auditoria dos recursos públicos aplicados. O desenvolvimento desta plataforma própria (construída do zero) visa unificar esses fluxos, garantindo maior controle governamental e facilitando a interação com proponentes e avaliadores.

---

## 4. Objetivos do Produto

| Objetivo | Descrição |
| :--- | :--- |
| **Digitalizar a gestão** | Substituir o processo atual fragmentado (planilhas e e-mails) por uma plataforma unificada. |
| **Garantir transparência** | Facilitar o acompanhamento e a auditoria de todo o ciclo de vida dos editais e projetos. |
| **Melhorar eficiência** | Reduzir o tempo gasto em triagens, avaliações de propostas e análises de prestação de contas. |
| **Apoio ao Ciclo de Vida** | Cobrir todas as fases: Rascunho do edital até Encerramento e prestação de contas do projeto. |

### Cronograma Provisório (Baseado no prazo de 8 meses)

| Fase RUP | Duração Estimada | Marco |
| :--- | :--- | :--- |
| **Inception** | 0.5 meses | LCO (*Lifecycle Objectives*) - Concordância sobre escopo e viabilidade. |
| **Elaboration** | 2 meses | LCA (*Lifecycle Architecture*) - Arquitetura base e mitigação de riscos críticos. |
| **Construction** | 4.5 meses | IOC (*Initial Operational Capability*) - Sistema construído e pronto para testes beta. |
| **Transition** | 1 mês | PR (*Product Release*) - Implantação e entrega final. |

> **Nota**: O prazo máximo total não ultrapassará 8 meses.

---

## 5. Previsão Financeira

### 5.1 Premissas
* **Orçamento máximo:** R$ 300.000,00.
* **Prazo máximo:** 8 meses.
* **Tamanho da equipe:** 7 integrantes.
* **Custos de Infraestrutura:** R$ 0,00. Não haverá custos com espaço físico, máquinas ou licenças de software.
* **Alocação de Recursos:** Todo o orçamento de R$ 300.000,00 será investido exclusivamente para custear a manutenção do time ao longo do período do projeto.
* **Salário/Bolsa base:** Considerando uma reserva de contingência de 10% (R$ 30.000,00), restam R$ 270.000,00 para a equipe. Dividindo R$ 270.000,00 por 8 meses e por 7 pessoas, temos um custo médio mensal aproximado de **R$ 4.821,42** por integrante.

### 5.2 Estimativa de Custos

| Item de Custo | Estimativa |
| :--- | :--- |
| Manutenção do time (7 pessoas x 8 meses) | R$ 270.000,00 |
| Infraestrutura técnica (código, ferramentas) | R$ 0,00 (começará do zero, sem custos) |
| Licenças e Espaço Físico | R$ 0,00 |
| Reserva de Contingência (10%) | R$ 30.000,00 |
| **Custo Total Estimado** | **R$ 300.000,00** |

> **Base da estimativa**: O cálculo considerou o teto orçamentário fornecido no escopo, dedicando o valor inteiramente ao capital humano conforme exigido pelo contexto.

### 5.3 Estimativa de Retorno / Benefícios
Como se trata de um órgão público, o ROI não é medido em lucro direto, mas em **economia gerada** e **redução de perdas financeiras** por má gestão ou falta de auditoria.

| Benefício | Estimativa Anual |
| :--- | :--- |
| Economia de horas-trabalho de servidores (fim de retrabalho com planilhas desconectadas) | R$ 180.000,00 |
| Redução de multas, processos e falhas de prestação de contas | R$ 250.000,00 |
| Maior agilidade no repasse de recursos (eficiência operacional) | R$ 70.000,00 |
| **Total de Benefícios Estimados** | **R$ 500.000,00** |

### 5.4 ROI Preliminar

| Indicador | Valor |
| :--- | :--- |
| Investimento total | R$ 300.000,00 |
| Benefício anual estimado | R$ 500.000,00 |
| Payback period (Retorno do investimento) | ~ 7,2 meses após a implantação |
| ROI (1º ano) | **66,6%** |

> **Cálculo do ROI**: ((500.000 - 300.000) / 300.000) * 100.
> **Nota**: As estimativas de custo e retorno são grosseiras na fase de Inception e deverão ser revalidadas no marco LCA da fase de Elaboração.

---

## 6. Restrições e Riscos de Negócio

| Restrição | Impacto |
| :--- | :--- |
| **Orçamento Fixo (R$ 300.000,00)** | Impede a contratação de mão de obra adicional ou compra de ferramentas pagas para acelerar o desenvolvimento. |
| **Prazo Rígido (8 meses)** | O escopo deverá ser rigorosamente priorizado para garantir que os ciclos de vida de editais e projetos sejam entregues a tempo. |
| **Início do Zero (Infra e Ferramentas)** | O time gastará tempo inicial nas primeiras iterações configurando repositórios e processos de CI/CD, o que impacta a velocidade inicial. |
| **Incerteza e Ambiguidade de Requisitos** | O escopo inicial possui lacunas intencionais. Decisões de modelagem erradas no início podem gerar retrabalho. |
