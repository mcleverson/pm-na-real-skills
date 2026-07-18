---
name: product-decision-brief
description: Criar, revisar, atualizar ou avaliar Product Decision Briefs, PDBs, em modo enxuto ou completo. Usar quando o usuário pedir para estruturar uma decisão de produto, conectar problema e objetivo à execução, documentar alternativas e trade-offs, preparar uma iniciativa para engenharia ou execução, reduzir um PDB às seções obrigatórias, expandir um PDB enxuto ou revisar a prontidão de um PDB existente. Preservar as perguntas e informações fornecidas sem inventar estratégia, evidências, experiência, decisão ou métricas.
---

# Product Decision Brief

Aplicar o Método PM na Real para transformar um problema ou decisão de produto em um documento curto, justificável e utilizável na execução. Evitar burocracia, contexto inflado e preenchimento artificial de lacunas.

## Princípios

- Conectar problema, objetivo e execução.
- Tratar clareza como prioridade, sem confundi-la com completude artificial.
- Diferenciar fato, hipótese, recomendação e decisão.
- Não inventar evidência, estratégia, persona, prioridade, experiência, decisão, meta ou restrição.
- Preservar perguntas, dados e formulações relevantes fornecidos pelo usuário. Não alterar seu significado.
- Declarar lacunas em vez de preenchê-las silenciosamente.
- Usar somente as seções determinadas pelo modo escolhido.
- Ser direto, técnico quando necessário e proporcional à decisão.

## Escolher o modo

Oferecer dois modos:

### PDB enxuto

Usar exatamente as quatro seções obrigatórias:

1. Problema
2. Objetivo
3. Experiência
4. Métrica de sucesso

Não acrescentar Exploração, Comparação, Decisão, Fora de escopo, riscos, prontidão ou qualquer outra seção ao documento enxuto.

### PDB completo

Usar as seções obrigatórias e incluir as opcionais aplicáveis:

1. Problema
2. Objetivo
3. Exploração, opcional e recomendada quando houver alternativas
4. Comparação, opcional e recomendada quando houver alternativas
5. Decisão, opcional, mas esperada quando o PDB estiver pronto para execução
6. Experiência
7. Métrica de sucesso
8. Fora de escopo, opcional

Não preencher uma seção opcional apenas para completar o template.

### Regra de seleção

- Usar o modo enxuto quando o usuário disser “enxuto”, “resumido”, “direto”, “somente seções obrigatórias” ou equivalente.
- Usar o modo completo quando o usuário disser “completo”, “detalhado”, “para decisão”, “para execução” ou equivalente.
- Perguntar qual modo o usuário deseja quando ele não indicar e a escolha não estiver clara.
- Recomendar o modo completo para decisões com múltiplas alternativas, riscos relevantes ou necessidade de justificativa, sem substituir a escolha do usuário.
- Informar brevemente o modo escolhido antes do documento quando ele tiver sido inferido.

## Entradas

Aceitar como entrada mínima um problema, uma iniciativa ou uma decisão em discussão.

Usar, quando fornecidos:

- estratégia ou North Star;
- prioridades de decisão;
- personas ou operações afetadas;
- evidências e dados;
- restrições;
- alternativas consideradas;
- decisão tomada;
- experiência ou comportamento esperado;
- métricas e metas.

Não presumir alinhamento estratégico quando o contexto do produto não tiver sido fornecido. Perguntar apenas por informações realmente bloqueantes; caso contrário, produzir o documento com lacunas explícitas.

## Construir as seções

### Problema

Incluir obrigatoriamente.

Descrever de forma específica:

- situação observada;
- usuário, cliente, negócio, sistema ou operação afetada, quando informado;
- impacto;
- evidências disponíveis;
- consequência de não agir, quando conhecida.

Não exigir que todo problema seja técnico. Não inserir solução na definição do problema. Quando não houver evidência, registrar essa ausência sem criar dados.

### Objetivo

Incluir obrigatoriamente.

Definir o estado desejado diretamente relacionado ao problema. Focar no resultado, sem antecipar solução ou entrega. Alinhar à estratégia somente quando ela tiver sido fornecida.

### Exploração

Incluir somente no modo completo e quando houver alternativas reais ou uma decisão ainda em aberto.

Apresentar abordagens possíveis de forma concisa. Não inventar alternativas artificiais. Não transformar Exploração em lista extensa de funcionalidades.

### Comparação

Incluir somente no modo completo e quando duas ou mais alternativas precisarem ser comparadas.

Selecionar critérios relevantes, como:

- impacto;
- esforço;
- risco;
- experiência;
- confiabilidade;
- reversibilidade;
- alinhamento estratégico.

Não usar critérios sem relação com o contexto. Explicitar incertezas e ausência de dados.

### Decisão

Incluir somente no modo completo e quando existir uma decisão ou quando o usuário pedir uma recomendação.

Registrar uma única abordagem escolhida, sua justificativa e os principais trade-offs. Quando a decisão ainda não tiver sido tomada, não inventar uma. Diferenciar explicitamente uma recomendação do modelo de uma decisão do time.

### Experiência

Incluir obrigatoriamente nos dois modos.

Definir, com base nos insumos disponíveis:

- fluxo ou comportamento esperado;
- comportamento em erro, quando aplicável;
- critérios de avanço, recuperação ou rollback, quando aplicáveis;
- mock, fluxo, diagrama, Figma ou contrato técnico fornecido ou solicitado.

Não inventar mock, fluxo ou experiência. Quando a iniciativa não alterar diretamente a experiência do usuário nem o fluxo operacional, manter a seção e registrar de forma concisa:

```text
Não se aplica a esta iniciativa, pois não existe alteração direta na experiência do usuário ou no fluxo operacional.
```

Adaptar a justificativa ao contexto real, sem repetir automaticamente o texto do exemplo.

### Métrica de sucesso

Incluir obrigatoriamente.

Definir medida de resultado, não apenas entrega. Usar métricas fornecidas ou deriváveis diretamente do objetivo. Não inventar metas numéricas. Quando a métrica ainda não estiver definida, registrar a lacuna e indicar o que precisa ser estabelecido.

### Fora de escopo

Incluir somente no modo completo e quando ajudar a limitar a decisão ou impedir expansão indevida.

Não criar exclusões arbitrárias.

## Formatos

### Saída enxuta

Usar exatamente:

```markdown
# Product Decision Brief

## Problema

## Objetivo

## Experiência

## Métrica de sucesso
```

### Saída completa

Usar as seções aplicáveis, respeitando esta ordem:

```markdown
# Product Decision Brief

## Problema

## Objetivo

## Exploração
[Quando aplicável]

## Comparação
[Quando aplicável]

## Decisão
[Quando aplicável]

## Experiência

## Métrica de sucesso

## Fora de escopo
[Quando aplicável]
```

Não escrever marcadores como “[Quando aplicável]” no documento final.

## Revisar um PDB

Respeitar o modo solicitado. Não reescrever o documento inteiro quando uma correção localizada for suficiente.

Avaliar:

- clareza e evidência do problema;
- relação entre objetivo e problema;
- antecipação indevida de solução;
- qualidade das alternativas e comparação, quando existentes;
- justificativa e trade-offs da decisão, quando existente;
- definição da experiência ou justificativa de não aplicação;
- relação entre métrica e resultado;
- limites do escopo, quando existentes;
- lacunas que impedem decisão ou execução.

Ao revisar, apresentar a avaliação fora do corpo do PDB. Não adicionar essas seções ao PDB enxuto.

Classificar a prontidão como:

| Estado | Critério |
|---|---|
| Rascunho | Faltam informações obrigatórias ou existem lacunas relevantes |
| Pronto para decisão | Problema, objetivo, evidências e alternativas permitem uma decisão responsável |
| Pronto para execução | Existe decisão, experiência definida ou justificada e métrica suficiente para avançar |
| Bloqueado | Uma ausência específica impede avanço responsável |

Um documento bem escrito não está automaticamente pronto para execução.

## Transformar entre modos

- Ao reduzir um PDB completo para enxuto, preservar apenas Problema, Objetivo, Experiência e Métrica de sucesso.
- Ao expandir um PDB enxuto para completo, usar somente informações fornecidas e solicitar ou marcar os dados ausentes das seções opcionais relevantes.
- Não perder fatos, evidências ou decisões importantes durante a transformação. Incorporar informações relevantes dentro das quatro seções obrigatórias quando necessário, sem criar novas seções no modo enxuto.

## Restrições absolutas

- Nunca alterar perguntas ou dados fornecidos pelo usuário.
- Nunca inventar evidência, meta, decisão, experiência, estratégia, persona ou prioridade.
- Nunca confundir recomendação do modelo com decisão do time.
- Nunca preencher seção opcional apenas para completar um template.
- Nunca adicionar seções extras ao PDB enxuto.
- Nunca transformar o PDB em um PRD longo.
- Nunca declarar prontidão quando houver bloqueios materiais.

