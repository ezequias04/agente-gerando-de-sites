---
name: agente-de-paginas
version: 1.0.0
type: agent
commands:
  - /criar-pagina
  - /revisar-pagina
  - /rebrand-pagina
entry: SKILL.md
description: Agente autônomo que constrói landing pages de alta conversão para clientes pagantes, com identidade visual exclusiva por marca e um elemento interativo obrigatório.
---

# Agente de Páginas

Este agente transforma o pedido do usuário em uma landing page pronta para entrega comercial, sempre preservando a disciplina de squad de dois papéis (estratégia → implementação) e o checklist anti-clichê.

## Quando me invocar

- Usuário pede página de captura, landing page, página de vendas, squeeze page, VSL page, página institucional, site one-page, página de lançamento, waitlist.
- Usuário pede revisão ou upgrade de página existente.
- Usuário pede rebrand (mesma estrutura, nova cara) para teste A/B ou para outro cliente do mesmo segmento.

## Como o sistema me aciona

1. Detecta a intenção (palavras-chave + contexto).
2. Direciona para o comando certo:
   - `/criar-pagina` → fluxo completo Etapas 1–8 do `SKILL.md`.
   - `/revisar-pagina` → auditoria de página existente, devolve diagnóstico + plano.
   - `/rebrand-pagina` → troca identidade visual mantendo arquitetura.
3. Carrega `agents/landing-builder.md` para o perfil técnico de capabilities.
4. Carrega `SKILL.md` para o fluxo editorial e processo de qualidade.

## Arquivos

- `SKILL.md` — fluxo principal (descoberta → token system → arquitetura → implementação → autocrítica → entrega).
- `agents/landing-builder.md` — perfil técnico: o que o agente sabe/não sabe fazer, integrações suportadas, padrões de código.
- `references/anti-cliche-palette.md` — referência rápida dos três clichês a evitar e como substituí-los.
