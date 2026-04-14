# UC03 - Avaliar Proposta de Projeto

## Use-Case Specification

| Campo | Valor |
|-------|-------|
| **Caso de Uso** | UC03 - Avaliar Proposta de Projeto |
| **Ator Primário** | Avaliador da Proposta |
| **Stakeholders e Interesses** | Avaliador (quer processo eficiente), Proponente (quer avaliação justa), Gestor do Edital (quer resultado transparente) |
| **Versão** | 1.0 - Inception |

---

## 1. Descrição Breve

O Avaliador analisa uma proposta de projeto submetida a um edital, aplicando os critérios de avaliação definidos, emitindo parecer e atribuindo pontuação para fundamentar a decisão de aprovação ou reprovação.

---

## 2. Fluxo Básico de Eventos

1. O Avaliador acessa a lista de propostas atribuídas para avaliação.
2. O sistema exibe as propostas pendentes de avaliação com seus dados resumidos.
3. O Avaliador seleciona uma proposta para avaliar.
4. O sistema exibe os dados completos da proposta e os critérios de avaliação do edital.
5. O Avaliador analisa a proposta, verificando documentos, cronograma e orçamento.
6. O Avaliador preenche a ficha de avaliação, pontuando cada critério e registrando observações.
7. O Avaliador emite seu parecer (favorável, favorável com ressalvas, ou desfavorável).
8. O sistema valida se todos os critérios foram pontuados.
9. O sistema registra a avaliação.
10. O sistema atualiza o status da proposta e notifica o Gestor do Edital.

---

## 3. Fluxos Alternativos

### 3.1 Avaliação Parcial

- **3.1.1 Salvar Avaliação Incompleta**
  - No passo 6, o Avaliador pode salvar a avaliação parcialmente preenchida.
  - O sistema salva o progresso e permite que o Avaliador retome depois.

### 3.2 Proposta Em Triagem

- **3.2.1 Proposta Não Passou na Triagem**
  - No passo 3, se a proposta ainda está em triagem, o sistema informa que a proposta não está disponível para avaliação.
  - O Avaliador retorna à lista de propostas.

### 3.3 Conflito de Interesses

- **3.3.1 Avaliador Com Conflito de Interesses**
  - No passo 3, o Avaliador pode declarar conflito de interesses com a proposta.
  - O sistema registra o conflito e remove a proposta da lista do avaliador.
  - O sistema reatribui a proposta a outro avaliador.

### 3.4 Solicitação de Esclarecimento

- **3.4.1 Avaliador Precisa de Mais Informações**
  - No passo 5, o Avaliador pode solicitar esclarecimentos ao Proponente.
  - O sistema envia solicitação ao Proponente.
  - O caso de uso é suspenso até o Proponente responder.
  - Após resposta, o Avaliador retoma o fluxo no passo 5.

### 3.5 Parecer Divergente

- **3.5.1 Avaliadores Com Pareceres Divergentes**
  - Após o passo 9, se houver divergência significativa entre avaliadores, o sistema sinaliza ao Gestor.
  - O Gestor pode solicitar uma terceira avaliação ou mesa de debate.

---

## 4. Subfluxos

### 4.1 Pontuação por Critério

Para cada critério de avaliação, o Avaliador:
1. Verifica se a proposta atende ao critério.
2. Atribui uma pontuação dentro da faixa definida.
3. Registra justificativa para a pontuação.

### 4.2 Consolidação de Avaliações

Após todas as avaliações individuais, o sistema consolida as pontuações e gera o ranking de propostas.

---

## 5. Cenários Chave

| Cenário | Descrição |
|---------|-----------|
| Avaliação completa | Avaliador pontua todos os critérios e emite parecer |
| Conflito de interesses | Avaliador declara conflito e proposta é reatribuída |
| Solicitação de esclarecimento | Avaliador pede mais informações ao Proponente |
| Avaliação parcial salva | Avaliador salva progresso para continuar depois |

---

## 6. Pré-condições

### 6.1 O Avaliador deve estar autenticado no sistema.

### 6.2 A proposta deve ter passado pela triagem (estado "Em avaliação").

### 6.3 O Avaliador deve estar designado para avaliar a proposta.

### 6.4 Os critérios de avaliação devem estar definidos no edital.

---

## 7. Pós-condições

### 7.1 A avaliação é registrada e associada à proposta.

### 7.2 O parecer do avaliador fica disponível para o Gestor do Edital.

### 7.3 A pontuação é considerada no ranking de propostas.

### 7.4 O histórico de avaliação é registrado para auditoria.

---

## 8. Pontos de Extensão

### 8.1 Notificação ao Proponente

- Localização: Após o passo 10.
- O sistema pode notificar o Proponente sobre o resultado da avaliação (depende da política do edital).

### 8.2 Recurso da Avaliação

- Localização: Após o passo 10.
- O Proponente pode interpor recurso contra o resultado da avaliação.

---

## 9. Requisitos Especiais

### 9.1 O sistema deve garantir que avaliadores não tenham acesso a avaliações de outros avaliadores antes de finalizar a sua.

### 9.2 O sistema deve registrar data/hora de início e fim de cada avaliação.

### 9.3 O sistema deve garantir a rastreabilidade de todas as ações de avaliação.

### 9.4 A identidade dos avaliadores deve ser mantida sigilosa até a divulgação dos resultados (quando aplicável).

---

## 10. Informações Adicionais

<!-- Incluir diagramas ou exemplos, se necessário -->