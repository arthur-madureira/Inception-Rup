# Modelo de Domínio (Inicial)

## Plataforma de Gestão de Editais Públicos

| Campo | Valor |
|-------|-------|
| **Projeto** | Plataforma de Gestão de Editais Públicos |
| **Versão** | 1.0 - Inception |

---

## 1. Introdução

Este documento apresenta o modelo conceitual inicial do domínio da Plataforma de Gestão de Editais Públicos, identificando os principais conceitos, seus atributos e relacionamentos. O modelo está em nível de Inception e será refinado nas fases subsequentes.

---

## 2. Principais Conceitos

### 2.1 Edital

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| titulo | String | Título do edital |
| descricao | String | Descrição detalhada |
| areaTematica | String | Área temática (esportivo, cultural, etc.) |
| valorTotal | Decimal | Valor total de financiamento |
| valorMaximoProjeto | Decimal | Valor máximo por projeto |
| dataPublicacao | Date | Data de publicação |
| inicioSubmissao | Date | Início do período de submissão |
| fimSubmissao | Date | Fim do período de submissão |
| status | Enum | Estado do ciclo de vida |

**Ciclo de Vida do Edital**:

```
Rascunho → Publicado → Em submissão → Em avaliação → Finalizado
```

### 2.2 Proposta / Projeto

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| titulo | String | Título do projeto |
| descricao | String | Descrição do projeto |
| objetivos | Text | Objetivos gerais e específicos do projeto |
| justificativa | Text | Justificativa da relevância do projeto |
| publicoAlvo | String | Público beneficiado pelo projeto |
| valorSolicitado | Decimal | Valor solicitado ao edital |
| cronograma | Text | Cronograma de execução com etapas e marcos |
| dataInicioPrevista | Date | Data prevista para início da execução |
| dataFimPrevista | Date | Data prevista para término da execução |
| dataSubmissao | Date | Data de submissão da proposta |
| status | Enum | Estado do ciclo de vida |

**Ciclo de Vida do Projeto**:

```
Submetido → Em triagem → Em avaliação → Aprovado/Reprovado → Em execução → Prestação de contas → Encerrado
```

### 2.3 Critério de Avaliação

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| nome | String | Nome do critério |
| descricao | String | Descrição do critério |
| peso | Decimal | Peso do critério na avaliação |
| pontuacaoMinima | Decimal | Pontuação mínima |
| pontuacaoMaxima | Decimal | Pontuação máxima |
| obrigatorio | Boolean | Se é critério eliminatório |

### 2.4 Avaliação

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| pontuacao | Decimal | Pontuação atribuída |
| parecer | Text | Parecer do avaliador |
| tipoParecer | Enum | Favorável / Favorável com ressalvas / Desfavorável |
| dataAvaliacao | Date | Data da avaliação |

### 2.5 Prestação de Contas

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| periodo | String | Período de referência |
| relatorioExecucao | Text | Relatório de execução |
| relatorioFinanceiro | Text | Relatório financeiro |
| dataSubmissao | Date | Data de submissão |
| status | Enum | Pendente / Em análise / Aprovada / Reprovada |

### 2.6 Documento

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| nome | String | Nome do documento |
| tipo | Enum | Tipo (regulamento, proposta, comprovante, etc.) |
| formato | String | Formato do arquivo |
| tamanho | Integer | Tamanho em bytes |
| dataUpload | Date | Data de upload |

### 2.7 Recurso

| Atributo | Tipo | Descrição |
|----------|------|-----------|
| id | Integer | Identificador único |
| tipo | Enum | Tipo de recurso (contra resultado, contra inabilitação, etc.) |
| justificativa | Text | Justificativa do recurso |
| dataInterposicao | Date | Data de interposição |
| status | Enum | Pendente / Deferido / Indeferido |

---

## 3. Atores

| Ator | Descrição |
|------|-----------|
| Gestor do Edital | Cria, configura e gerencia editais |
| Proponente | Submete propostas e presta contas |
| Avaliador | Avalia propostas submetidas |
| Analista de Prestação de Contas | Analisa prestação de contas dos projetos |

---

## 4. Relacionamentos

```
Edital 1 ────── N Proposta
Edital 1 ────── N Critério de Avaliação
Edital 1 ────── N Documento
Proposta 1 ──── N Avaliação
Proposta * ──── 1 Proponente
Proposta 1 ──── N Documento
Proposta 1 ──── 1 Prestação de Contas (quando aprovada)
Prestação de Contas 1 ──── N Documento
Avaliação 1 ──── 1 Avaliador
Proposta 1 ──── N Recurso
```

---

## 5. Diagrama de Classes UML

```mermaid
classDiagram
    class Edital {
        +id: int
        +titulo: string
        +descricao: string
        +areaTematica: string
        +valorTotal: decimal
        +valorMaximoProjeto: decimal
        +dataPublicacao: date
        +inicioSubmissao: date
        +fimSubmissao: date
        +status: EditalStatus
    }

    class Proposta {
        +id: int
        +titulo: string
        +descricao: string
        +valorSolicitado: decimal
        +cronograma: text
        +dataSubmissao: date
        +status: PropostaStatus
    }

    class CriterioAvaliacao {
        +id: int
        +nome: string
        +descricao: string
        +peso: decimal
        +pontuacaoMinima: decimal
        +pontuacaoMaxima: decimal
        +obrigatorio: boolean
    }

    class Avaliacao {
        +id: int
        +pontuacao: decimal
        +parecer: text
        +tipoParecer: TipoParecer
        +dataAvaliacao: date
    }

    class PrestacaoContas {
        +id: int
        +periodo: string
        +relatorioExecucao: text
        +relatorioFinanceiro: text
        +dataSubmissao: date
        +status: PrestacaoStatus
    }

    class Documento {
        +id: int
        +nome: string
        +tipo: TipoDocumento
        +formato: string
        +tamanho: int
        +dataUpload: date
    }

    class Recurso {
        +id: int
        +tipo: TipoRecurso
        +justificativa: text
        +dataInterposicao: date
        +status: RecursoStatus
    }

    class GestorEdital {
        +nome: string
        +email: string
    }

    class Proponente {
        +nome: string
        +email: string
        +cpfCnpj: string
    }

    class Avaliador {
        +nome: string
        +email: string
        +especialidade: string
    }

    class AnalistaPrestacaoContas {
        +nome: string
        +email: string
    }

    Edital "1" --> "*" Proposta : possui
    Edital "1" --> "*" CriterioAvaliacao : define
    Edital "1" --> "*" Documento : inclui
    Proposta "1" --> "*" Avaliacao : recebe
    Proposta "*" --> "1" Proponente : submetida por
    Proposta "1" --> "*" Documento : contém
    Proposta "1" --> "1" PrestacaoContas : gera
    Proposta "1" --> "*" Recurso : pode ter
    PrestacaoContas "1" --> "*" Documento : inclui
    Avaliacao "1" --> "1" Avaliador : feita por
    PrestacaoContas "1" --> "1" AnalistaPrestacaoContas : analisada por
    Edital "1" --> "1" GestorEdital : criado por
```

---

## 6. Enumerações

### EditalStatus
- Rascunho
- Publicado
- Em submissão
- Em avaliação
- Finalizado

### PropostaStatus
- Rascunho
- Submetido
- Em triagem
- Em avaliação
- Aprovado
- Reprovado
- Em execução
- Prestação de contas
- Encerrado

### TipoParecer
- Favorável
- Favorável com ressalvas
- Desfavorável

### PrestacaoStatus
- Pendente
- Em análise
- Aprovada
- Reprovada

### TipoDocumento
- Regulamento
- Proposta
- Comprovante
- Relatório
- Outro

### TipoRecurso
- Contra resultado
- Contra inabilitação
- Contra enquadramento
- Outro

### RecursoStatus
- Pendente
- Deferido
- Indeferido

---

## 7. Notas e Suposições

### 7.1 Decisões de Modelagem

| Decisão | Justificativa |
|---------|---------------|
| Proposta e Projeto são a mesma entidade | O enunciado usa os termos de forma intercambiável. Na fase de submissão, é uma "proposta"; após aprovação, torna-se um "projeto". Modelamos como uma única entidade (`Proposta`) cujo status evolui no ciclo de vida, evitando duplicação de estrutura. |
| Edital tem Critérios de Avaliação como entidade separada | Cada edital pode definir seus próprios critérios, com pesos e pontuações distintas. Separar `CriterioAvaliacao` de `Edital` permite reutilização e flexibilidade na configuração. |
| Prestação de Contas é 1:1 com Proposta aprovada | Cada projeto aprovado gera exatamente um processo de prestação de contas. Não modelamos prestações parciais nesta fase — se necessário, será refinado na Elaboration. |
| Documento é entidade polimórfica | Um mesmo conceito de "documento" serve para anexos de editais (regulamentos), propostas (formulários) e prestações de contas (comprovantes), diferenciados pelo enum `TipoDocumento`. |
| Recurso vinculado à Proposta, não ao Edital | Recursos são interpostos contra decisões específicas (resultado de avaliação, inabilitação), portanto pertencem ao escopo da proposta. |
| Atores modelados como classes separadas | Mesmo que não persistidos diretamente no modelo de classes de domínio, representar atores como classes facilita a visualização de suas associações com entidades do sistema. |

### 7.2 Suposições

| Suposição | Fundamentação |
|-----------|---------------|
| O sistema não requer integração com sistemas externos na primeira versão | O enunciado menciona sistemas desconectados como problema, mas a plataforma é o movimento de unificação. Integrações são tratadas como risco (R05) e postergadas. |
| Um Proponente pode ter apenas uma proposta ativa por edital | Simplificação para a Inception, suportada pelo UC02 (fluxo alternativo 3.5.1). Pode ser revista na Elaboration se o órgão permitir múltiplas submissões. |
| A triagem é uma etapa automatizada de verificação documental | O UC03 pressupõe que a proposta chega ao Avaliador já triada. Assumimos que a triagem consiste em validação automática de campos obrigatórios e documentos anexados. |
| Os ciclos de vida seguem os exemplos do enunciado | Adotamos os ciclos de vida sugeridos (Rascunho → Publicado → Em submissão → Em avaliação → Finalizado para editais; Submetido → Em triagem → Em avaliação → Aprovado/Reprovado → Em execução → Prestação de contas → Encerrado para projetos) como base. Os grupos podem estender esses estados. |
| Autenticação e autorização são resolvidas por framework | Não modelamos o sistema de login/permissões no domínio. Assumimos que um mecanismo padrão (OAuth2, JWT) será adotado na Elaboration. |

### 7.3 Pontos em Aberto para a Elaboration

- Refinar o modelo de `Recurso`: o fluxo de análise de recursos (quem analisa, prazos, efeito suspensivo) precisa ser detalhado.
- Modelar notificações como eventos do domínio (ex: `SubmissaoRealizada`, `AvaliacaoConcluida`).
- Avaliar se `Proponente` deve ser uma classe de domínio ou se basta como ator externo.
- Definir o modelo de endereçamento/perfis de usuário (papéis RBAC: Admin, Gestor, Avaliador, Proponente, Analista).

---

### 7.4 Restrições de Integridade (OCL)

| Restrição | Expressão OCL | Descrição |
|-----------|--------------|-----------|
| Prazo de submissão coerente | `context Edital inv: fimSubmissao > inicioSubmissao` | A data de fim da submissão deve ser posterior à de início |
| Data de publicação coerente | `context Edital inv: dataPublicacao >= inicioSubmissao` | A publicação não pode ser posterior ao início das submissões |
| Valor solicitado dentro do limite | `context Proposta inv: valorSolicitado <= edital.valorMaximoProjeto` | Uma proposta não pode solicitar mais do que o valor máximo permitido pelo edital |
| Pesos dos critérios totalizando 100 | `context Edital inv: criteriosAvaliacao->collect(peso)->sum() = 100` | A soma dos pesos de todos os critérios do edital deve ser 100 |
| Pontuação dentro da faixa | `context Avaliacao inv: pontuacao >= criterio.pontuacaoMinima and pontuacao <= criterio.pontuacaoMaxima` | A nota atribuída deve estar dentro da faixa definida pelo critério |
| Avaliador único por avaliação (sigilo) | `context Proposta inv: avaliacoes->forAll(a1, a2 | a1 <> a2 implies a1.avaliador <> a2.avaliador)` | Uma proposta não pode ser avaliada mais de uma vez pelo mesmo avaliador |
| Edital publicado não volta a rascunho | `context Edital inv: status = EditalStatus::Rascunho implies dataPublicacao = null` | Um edital em rascunho não pode ter data de publicação preenchida |
| Proposta só existe com edital aberto | `context Proposta inv: edital.status = EditalStatus::Em_submissao` | Só é possível submeter proposta quando o edital está em período de submissão |