# escalaIA — CLAUDE.md

## Visao Geral
Projeto em fase inicial. Atualizar esta secao com proposito e stack ao comecar.

Stack: [A DEFINIR]
Submodulo: .agnostic-core/  (instalar via: git submodule add https://github.com/paulinett1508-dev/agnostic-core .agnostic-core)

---

## Antes de implementar

Consulte a skill do dominio relevante:

  Planejamento:        .agnostic-core/skills/workflow/goal-backward-planning.md
  Workflow 6 fases:    .agnostic-core/skills/workflow/project-workflow.md
  Commits:             .agnostic-core/skills/git/commit-conventions.md
  Branching:           .agnostic-core/skills/git/branching-strategy.md
  Debugging:           .agnostic-core/skills/audit/systematic-debugging.md
  Fact checking:       .agnostic-core/skills/ai/fact-checker.md

---

## Agents disponiveis (apos instalar agnostic-core)

  Project Planner:     .agnostic-core/agents/generators/project-planner.md
  Codebase Mapper:     .agnostic-core/agents/reviewers/codebase-mapper.md
  Code Inspector:      .agnostic-core/agents/reviewers/code-inspector.md

---

## Uso de Subagents

- Use subagents para pesquisa de arquitetura, comparacao de stacks e levantamento de requisitos em paralelo
- Offload investigacao de codebase e analise de dependencias para subagents dedicados
- Para decisoes de stack: subagent de pesquisa antes de comecar a implementar

## Verificacao antes de Concluir

- Nunca marque tarefa como concluida sem provar que funciona (build, teste, screenshot)
- Pergunta padrao: *"Um senior engineer aprovaria esse diff?"*
- Verificar que o projeto roda do zero em uma maquina limpa

## Elegancia (features nao-triviais)

- Para mudancas que tocam 3+ arquivos: pause e avalie se ha solucao mais simples
- Se a solucao parece hack: "sabendo tudo o que sei agora, qual e a implementacao elegante?"
- **Excecao:** fixes simples e obvios — nao over-engenheirar
