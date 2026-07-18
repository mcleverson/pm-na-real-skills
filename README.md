# PM na Real Skills

Skills abertas para transformar problemas, necessidades e decisões de produto em análises claras, críticas e utilizáveis.

Esta coleção aplica princípios do [PM na Real](https://pmnareal.com.br) em fluxos reutilizáveis por agentes de IA. Cada skill é independente, não contém uma estratégia de produto específica e pode ser adaptada ao contexto fornecido pelo usuário.

## Da descoberta à decisão

As três skills podem ser usadas separadamente ou como uma sequência:

1. **Challenge Product Problem** questiona a qualidade do problema.
2. **Identify Underserved Needs** identifica necessidades relevantes e potencialmente mal atendidas.
3. **Product Decision Brief** transforma os insumos validados em uma decisão pronta para execução.

## Skills disponíveis

| Skill | Quando usar | Resultado principal |
|---|---|---|
| [Challenge Product Problem](skills/challenge-product-problem/SKILL.md) | Antes de avançar para solução, priorização ou investimento | Diagnóstico crítico do problema, lacunas e perguntas de discovery |
| [Identify Underserved Needs](skills/identify-underserved-needs/SKILL.md) | Ao analisar dores, reclamações, comportamentos, entrevistas ou hipóteses | Necessidades independentes de solução, evidências e avaliação de atendimento atual |
| [Product Decision Brief](skills/product-decision-brief/SKILL.md) | Ao estruturar ou revisar uma decisão de produto para execução | PDB enxuto ou completo, com riscos, trade-offs e prontidão explícita |

## Challenge Product Problem

Ajuda a:

- diferenciar problema, sintoma, causa presumida, oportunidade e solução disfarçada;
- separar evidências, hipóteses e lacunas;
- formular perguntas críticas de discovery;
- melhorar o enunciado sem antecipar uma solução;
- indicar se o problema está pronto para priorização.

Exemplo:

```text
Use a skill challenge-product-problem para analisar esta definição:
"Os clientes precisam de um aplicativo para acompanhar melhor seus pedidos."
```

## Identify Underserved Needs

Ajuda a:

- transformar dores e observações em necessidades independentes de solução;
- identificar a persona e o contexto da necessidade;
- distinguir evidência, hipótese e lacuna;
- avaliar importância e satisfação atual sem inventar dados;
- destacar necessidades potencialmente mal atendidas.

Exemplo:

```text
Use a skill identify-underserved-needs para analisar estas entrevistas e identificar
necessidades potencialmente mal atendidas. Não proponha funcionalidades.
```

## Product Decision Brief

Cria ou revisa um Product Decision Brief em dois modos:

- **Enxuto:** contém somente as seções obrigatórias: Problema, Objetivo, Experiência e Métrica de sucesso.
- **Completo:** também inclui Exploração, Comparação, Decisão e Fora de escopo quando houver insumos ou premissas suficientes.

A skill não inventa estratégia, evidências, experiência, decisão ou métricas. Quando faltar informação essencial, explicita a lacuna ou solicita dados adicionais.

Exemplos:

```text
Use a skill product-decision-brief para criar um PDB enxuto com base nestes insumos.
```

```text
Use a skill product-decision-brief para criar um PDB completo. Compare as alternativas,
explicite os trade-offs e não invente informações ausentes.
```

## Instalação e uso

> A compatibilidade depende da aplicação que executa o modelo. ChatGPT, Codex, Gemini CLI, Claude Code e claude.ai possuem formas diferentes de instalar skills.

### ChatGPT

O ChatGPT não usa uma pasta local de skills. A instalação é feita pela interface:

1. Baixe este repositório ou somente a pasta da skill desejada.
2. Compacte a pasta da skill em um arquivo ZIP, mantendo o `SKILL.md` dentro dela.
3. No ChatGPT, abra **Plugins > Skills > Create > Upload from computer**.
4. Envie o ZIP e conclua a instalação após a verificação.
5. Peça o uso da skill pelo nome ou faça uma solicitação compatível com sua descrição.

Consulte a [documentação oficial de Skills no ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt).

### Codex CLI e IDE

O Codex reconhece skills nestes diretórios:

- usuário: `~/.agents/skills/`
- projeto: `.agents/skills/`

Exemplo de instalação para o usuário:

```bash
git clone https://github.com/mcleverson/pm-na-real-skills.git
mkdir -p ~/.agents/skills
cp -R pm-na-real-skills/skills/challenge-product-problem ~/.agents/skills/
```

Para instalar outra skill, substitua `challenge-product-problem` pelo nome da pasta desejada. Depois, reinicie o Codex se a skill não aparecer imediatamente. Ela pode ser selecionada pela lista de skills ou acionada por uma solicitação compatível.

Consulte a [documentação oficial de Skills no Codex](https://developers.openai.com/codex/build-skills).

### Gemini CLI

O Gemini CLI reconhece skills nestes diretórios:

- usuário: `~/.gemini/skills/` ou `~/.agents/skills/`
- projeto: `.gemini/skills/` ou `.agents/skills/`

Também é possível instalar diretamente deste repositório:

```bash
gemini skills install https://github.com/mcleverson/pm-na-real-skills.git \
  --path skills/challenge-product-problem \
  --scope user
```

Substitua o caminho pela skill desejada. Use `--scope workspace` para instalar apenas no projeto atual.

Estas instruções se referem ao Gemini CLI. Elas não significam que toda interface baseada nos modelos Gemini aceite pastas locais de skills.

Consulte a [documentação oficial de Agent Skills no Gemini CLI](https://geminicli.com/docs/cli/skills/).

### Claude Code

O Claude Code reconhece skills nestes diretórios:

- usuário: `~/.claude/skills/`
- projeto: `.claude/skills/`

Exemplo de instalação para o usuário, após clonar este repositório:

```bash
mkdir -p ~/.claude/skills
cp -R pm-na-real-skills/skills/challenge-product-problem ~/.claude/skills/
```

### claude.ai

No claude.ai, a instalação é feita por upload:

1. Compacte a pasta da skill desejada em ZIP.
2. Abra **Settings > Features**.
3. Envie a skill personalizada.
4. Ative a skill antes de iniciar o uso.

A disponibilidade pode depender do plano e da execução de código habilitada. Consulte a [documentação oficial de Agent Skills da Anthropic](https://platform.claude.com/docs/pt-BR/agents-and-tools/agent-skills/overview).

## Nomes das pastas

Use um destes nomes nos comandos de instalação:

```text
challenge-product-problem
identify-underserved-needs
product-decision-brief
```

## Como usar as skills em conjunto

Exemplo de fluxo:

```text
1. Analise esta definição com challenge-product-problem.
2. Com base apenas nas evidências fornecidas, use identify-underserved-needs.
3. Depois da minha validação, gere um product-decision-brief no modo completo.
```

Não é obrigatório seguir essa ordem. Cada skill funciona de maneira independente.

## Princípios da coleção

- Não inventar evidências, métricas ou contexto.
- Diferenciar fatos, hipóteses, lacunas e decisões.
- Não esconder incertezas com documentos bem escritos.
- Permanecer no problema antes de antecipar a solução.
- Preservar estratégia e restrições fornecidas pelo usuário.
- Priorizar clareza, pensamento crítico e aplicabilidade.

## Estrutura do repositório

```text
skills/
├── challenge-product-problem/
│   ├── SKILL.md
│   └── agents/openai.yaml
├── identify-underserved-needs/
│   ├── SKILL.md
│   └── agents/openai.yaml
└── product-decision-brief/
    ├── SKILL.md
    └── agents/openai.yaml
```

O arquivo `SKILL.md` contém as instruções portáveis da skill. O arquivo `agents/openai.yaml` contém metadados adicionais usados por aplicações OpenAI compatíveis.

## Compatibilidade

As skills seguem o formato baseado em `SKILL.md` adotado por ferramentas compatíveis com Agent Skills. Cada aplicação pode interpretar recursos e metadados de forma diferente, portanto a portabilidade deve ser validada no ambiente em que a skill será usada.

## Licença

Distribuído sob a licença MIT. Consulte [LICENSE](LICENSE).

## Autor

Criado por Cleverson Gallego como parte do Método PM na Real.
