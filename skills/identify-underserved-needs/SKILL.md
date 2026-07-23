---
name: identify-underserved-needs
description: Transformar dores, reclamações, comportamentos, observações, entrevistas e hipóteses em necessidades independentes de solução e avaliar quais podem estar mal atendidas. Usar quando o usuário pedir para identificar underserved needs, desired outcomes ou necessidades de uma persona, revisar necessidades existentes, separar dores de soluções, ou priorizar necessidades com base em importância, satisfação atual e evidências. Não usar para propor funcionalidades, produtos, MVPs ou tecnologias.
---

# Identify Underserved Needs

Identificar necessidades candidatas e avaliar seu nível de atendimento sem transformar suposições em conclusões. Diferenciar uma necessidade plausível de uma necessidade comprovadamente mal atendida.

## Princípios

- Permanecer no espaço da necessidade e não antecipar soluções.
- Manter cada necessidade ligada a uma entrada fornecida.
- Separar observação, interpretação e conclusão.
- Não confundir dor com necessidade, nem solução sugerida com resultado desejado.
- Não chamar uma necessidade de mal atendida apenas porque ela parece relevante.
- Não inventar persona, contexto, importância, satisfação, frequência ou evidência.
- Preservar o significado das informações fornecidas pelo usuário.
- Ser direto, específico e proporcional à qualidade das entradas.

## Modos

Executar um ou mais modos conforme o pedido:

1. Gerar necessidades candidatas a partir de dores, observações ou entrevistas.
2. Avaliar se necessidades existentes estão mal atendidas.
3. Revisar e melhorar a formulação de necessidades.

Quando o modo não estiver explícito, inferir pelo material recebido e informar brevemente o que será feito.

## Entradas

Aceitar como entrada mínima pelo menos uma dor, reclamação, comportamento, dificuldade, hipótese de necessidade ou trecho de entrevista.

Usar, quando fornecidos:

- persona ou segmento;
- contexto em que a situação ocorre;
- evidências e respectivas fontes;
- frequência;
- importância para o usuário;
- alternativas utilizadas atualmente;
- satisfação com as alternativas;
- consequência de a necessidade não ser atendida.

Não bloquear a geração de necessidades candidatas pela ausência de dados adicionais. Impedir apenas conclusões que dependam de dados ausentes.

## Fluxo

### 1. Interpretar as entradas

Classificar cada informação relevante como:

| Tipo | Regra |
|---|---|
| Observação | Comportamento, fala, evento ou dado apresentado |
| Dor | Dificuldade, perda, frustração ou consequência percebida |
| Sintoma | Manifestação que pode ter causas diferentes |
| Causa presumida | Explicação ainda não sustentada pelas entradas |
| Necessidade | Resultado desejado ou atrito a reduzir |
| Solução sugerida | Produto, funcionalidade, canal, tecnologia ou implementação antecipada |
| Lacuna | Informação necessária que não foi apresentada |

Não tratar interpretação como observação.

### 2. Gerar necessidades candidatas

Formular cada necessidade como resultado desejado ou atrito a reduzir. Preferir a estrutura:

```text
[Verbo de direção] + [resultado ou atrito] + [contexto, quando conhecido]
```

Usar verbos como reduzir, aumentar, minimizar, maximizar, evitar ou melhorar quando ajudarem a expressar direção.

Garantir que cada necessidade:

- seja independente de solução;
- possa ser atendida de diferentes maneiras;
- represente um único resultado principal;
- esteja ligada a uma entrada fornecida;
- seja específica sem inventar contexto;
- não contenha produto, funcionalidade, canal ou tecnologia.

Não forçar um número fixo de necessidades. Gerar apenas as que puderem ser justificadas pelas entradas.

### 3. Revisar a qualidade

Para cada necessidade, verificar:

- independência de solução;
- clareza do resultado desejado;
- especificidade;
- vínculo com a evidência ou hipótese de origem;
- ausência de necessidades duplicadas;
- ausência de múltiplos resultados na mesma frase.

Reescrever formulações fracas sem alterar seu significado. Marcar como hipótese quando a origem não constituir evidência.

### 4. Avaliar o nível de atendimento

Avaliar cada necessidade somente com as informações disponíveis:

| Dimensão | Valores permitidos |
|---|---|
| Importância | Alta, média, baixa ou não avaliada |
| Satisfação atual | Alta, média, baixa ou não avaliada |
| Evidência | Forte, parcial, fraca ou inexistente |
| Confiança | Alta, média ou baixa |

Justificar cada avaliação. Não inferir baixa satisfação apenas porque existe uma dor. Não inferir alta importância apenas porque o usuário mencionou a necessidade.

### 5. Classificar a necessidade

Aplicar um único estado:

| Estado | Critério |
|---|---|
| Necessidade candidata | Formulação plausível, mas sem evidência suficiente |
| Potencialmente mal atendida | Existem sinais de importância ou de baixa satisfação, ainda incompletos |
| Necessidade mal atendida | Importância e baixa satisfação estão sustentadas por evidências |
| Não sustentada | As informações disponíveis não apoiam a necessidade formulada |

Não usar “necessidade mal atendida” quando importância ou satisfação não tiverem sido avaliadas com evidências.

### 6. Priorizar quando houver base

Destacar as necessidades mais promissoras somente quando existirem informações comparáveis de importância, satisfação e evidência.

Quando não houver base suficiente, usar o título “Candidatas prioritárias para validação” e explicar por que merecem investigação. Não apresentar essa seleção como priorização conclusiva.

### 7. Indicar lacunas e validação

Listar as informações necessárias para confirmar ou rejeitar as principais necessidades. Formular perguntas sobre comportamento, contexto, importância, alternativas atuais, satisfação, frequência e consequências.

Não propor testes de solução, protótipos ou funcionalidades.

## Formato de resposta

Usar a estrutura abaixo. Adaptar as linhas das tabelas ao material recebido, sem omitir as seções.

```markdown
# Análise de necessidades

## 1. Entendimento das entradas
[Resumo e ambiguidades]

## 2. Diagnóstico
| Entrada | Tipo | Observação |
|---|---|---|

## 3. Necessidades candidatas
| Necessidade | Origem | Evidência | Confiança |
|---|---|---|---|

## 4. Avaliação de atendimento
| Necessidade | Importância | Satisfação atual | Estado | Justificativa |
|---|---|---|---|---|

## 5. Prioridade
[Necessidades mais promissoras ou candidatas prioritárias para validação]

## 6. Lacunas e perguntas de validação
[Lacunas e perguntas priorizadas]
```

## Restrições absolutas

- Nunca propor solução, funcionalidade, produto, aplicativo, plataforma, canal, automação ou tecnologia.
- Nunca propor MVP, arquitetura ou roadmap.
- Nunca inventar importância, satisfação, evidência ou frequência.
- Nunca classificar uma necessidade como mal atendida sem evidência de importância e baixa satisfação.
- Nunca criar ranking conclusivo sem informações comparáveis.
- Nunca apresentar uma hipótese gerada pelo modelo como fala ou comportamento observado.
- Se o usuário pedir soluções, explicar brevemente que esta etapa avalia necessidades e oferecer concluir primeiro a análise.

