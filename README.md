# PM na Real Skills

Skills abertas para transformar problemas, evidências e decisões de produto em análises claras e utilizáveis.

Esta coleção aplica princípios do [PM na Real](https://pmnareal.com.br) em fluxos reutilizáveis por agentes de IA compatíveis com o padrão aberto Agent Skills.

## Skills disponíveis

| Skill | O que faz | Status |
|---|---|---|
| [Challenge Product Problem](skills/challenge-product-problem/SKILL.md) | Desafia uma definição de problema antes que o time avance para solução, priorização ou investimento | Disponível |
| [Identify Underserved Needs](skills/identify-underserved-needs/SKILL.md) | Identifica e avalia necessidades potencialmente mal atendidas | Disponível |
| [Product Decision Brief](skills/product-decision-brief/SKILL.md) | Cria e revisa PDBs enxutos ou completos | Disponível |

## Challenge Product Problem

A primeira skill da coleção ajuda a:

- diferenciar problema, sintoma, causa presumida, oportunidade e solução disfarçada;
- separar evidências, hipóteses e lacunas;
- avaliar a qualidade da definição sem inventar notas ou dados;
- formular perguntas críticas de discovery;
- melhorar o enunciado sem antecipar uma solução;
- indicar se o problema ainda está mal definido ou pronto para priorização.

## Instalação

Copie a pasta da skill desejada para o diretório de skills do agente utilizado.

| Agente | Diretório no projeto |
|---|---|
| Codex | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Gemini CLI | `.gemini/skills/` |

Exemplo para Codex:

```bash
mkdir -p .agents/skills
cp -R skills/challenge-product-problem .agents/skills/
```

Depois, solicite explicitamente o uso da skill ou apresente uma definição de problema que corresponda à sua descrição.

Exemplo:

```text
Use a skill challenge-product-problem para analisar esta definição:
"Os clientes precisam de um aplicativo para acompanhar melhor seus pedidos."
```

## Princípios da coleção

- Não inventar evidências ou contexto.
- Diferenciar fatos, hipóteses e decisões.
- Não esconder incertezas com documentos bem escritos.
- Permanecer no problema antes de antecipar a solução.
- Priorizar clareza e aplicabilidade.

## Compatibilidade

As skills seguem o formato `SKILL.md` do padrão aberto Agent Skills. Cada skill é autocontida e pode ser instalada separadamente.

## Licença

Distribuído sob a licença MIT. Consulte [LICENSE](LICENSE).

## Autor

Criado por Cleverson Gallego como parte do Método PM na Real.
