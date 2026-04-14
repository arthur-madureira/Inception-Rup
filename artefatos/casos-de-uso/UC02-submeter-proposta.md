# UC02 - Submeter Proposta de Projeto

## Use-Case Specification

| Campo | Valor |
|-------|-------|
| **Caso de Uso** | UC02 - Submeter Proposta de Projeto |
| **Ator Primário** | Proponente de Projeto |
| **Stakeholders e Interesses** | Proponente (quer submissão fácil), Gestor do Edital (quer propostas completas), Avaliadores (querem propostas padronizadas) |
| **Versão** | 1.0 - Inception |

---

## 1. Descrição Breve

O Proponente submete uma proposta de projeto a um edital aberto para submissões, preenchendo os dados do projeto e anexando os documentos necessários.

---

## 2. Fluxo Básico de Eventos

1. O Proponente acessa a lista de editais com submissões abertas.
2. O Proponente seleciona o edital desejado.
3. O sistema exibe os detalhes do edital (critérios, prazos, valores).
4. O Proponente inicia a submissão de proposta.
5. O sistema apresenta o formulário de proposta com os campos definidos pelo edital.
6. O Proponente preenche os dados do projeto (título, descrição, objetivos, justificativa, cronograma, orçamento).
7. O Proponente anexa os documentos exigidos pelo edital.
8. O Proponente revisa os dados e documentos antes da submissão.
9. O sistema valida a conformidade da proposta com os requisitos do edital.
10. O Proponente confirma a submissão.
11. O sistema registra a proposta em estado **Submetido**.
12. O sistema envia confirmação de recebimento ao Proponente.

---

## 3. Fluxos Alternativos

### 3.1 Documentos Pendentes

- **3.1.1 Documento Obrigatório Não Anexado**
  - No passo 9, se algum documento obrigatório não foi anexado, o sistema exibe alerta indicando os documentos pendentes.
  - O Proponente anexa os documentos faltantes e retoma o fluxo no passo 8.

### 3.2 Prazo Expirado

- **3.2.1 Submissão Após Prazo**
  - No passo 4, se o prazo de submissão já expirou, o sistema informa que o edital não aceita mais submissões.
  - O caso de uso é encerrado.

### 3.3 Salvar Rascunho da Proposta

- **3.3.1 Salvar Proposta Incompleta**
  - Em qualquer passo entre 6 e 8, o Proponente pode salvar a proposta como rascunho.
  - O sistema salva a proposta em estado de Rascunho.
  - O Proponente pode retomar a edição posteriormente.

### 3.4 Edital com Requisitos Específicos

- **3.4.1 Proposta Não Atende Requisitos Mínimos**
  - No passo 9, se a proposta não atende algum requisito mínimo do edital (ex: valor acima do máximo, área temática divergente), o sistema exibe alerta.
  - O Proponente ajusta a proposta ou cancela a submissão.

### 3.5 Proposta Duplicada

- **3.5.1 Proponente Já Possui Proposta no Mesmo Edital**
  - No passo 4, se o Proponente já submeteu uma proposta para o mesmo edital, o sistema informa e pergunta se deseja editar a proposta existente.
  - Se sim, o sistema carrega a proposta existente para edição.

---

## 4. Subfluxos

### 4.1 Preenchimento de Orçamento

O Proponente detalha o orçamento do projeto, incluindo itens, quantidades, valores unitários e totais, e memória de cálculo.

### 4.2 Preenchimento de Cronograma

O Proponente define as etapas do projeto com prazos e marcos de entrega.

---

## 5. Cenários Chave

| Cenário | Descrição |
|---------|-----------|
| Submissão completa | Proponente preenche todos os dados e documentos e submite com sucesso |
| Submissão com rascunho | Proponente salva rascunho e finaliza depois |
| Proposta não conforme | Proponente tenta submeter proposta que não atende requisitos do edital |
| Prazo expirado | Proponente tenta submeter após o prazo de submissão |

---

## 6. Pré-condições

### 6.1 O Proponente deve estar autenticado no sistema.

### 6.2 O edital deve estar em estado "Em submissão".

### 6.3 O Proponente deve ter cadastro válido no sistema.

---

## 7. Pós-condições

### 7.1 A proposta é registrada no sistema em estado "Submetido".

### 7.2 A proposta fica disponível para triagem e avaliação.

### 7.3 O Proponente recebe confirmação de recebimento.

### 7.4 O histórico de submissão é registrado para auditoria.

---

## 8. Pontos de Extensão

### 8.1 Análise de Conformidade Automática

- Localização: Após o passo 9.
- O sistema pode realizar uma verificação automática de conformidade documental.

### 8.2 Notificação ao Gestor

- Localização: Após o passo 11.
- O sistema pode notificar o Gestor do Edital sobre novas submissões.

---

## 9. Requisitos Especiais

### 9.1 O sistema deve garantir que submissões após o prazo sejam automaticamente rejeitadas.

### 9.2 Documentos anexados devem ser validados quanto ao formato e tamanho máximo.

### 9.3 O sistema deve permitir o upload de múltiplos documentos simultaneamente.

### 9.4 A confirmação de recebimento deve incluir número de protocolo e data/hora.

---

## 10. Informações Adicionais

<!-- Incluir diagramas ou exemplos, se necessário -->