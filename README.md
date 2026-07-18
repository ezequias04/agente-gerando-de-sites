# Agente Gerando de Sites

Skills para Claude Code (e outros agentes compatíveis com o [skills.sh](https://skills.sh)) para
criar landing pages de alta conversão com identidade visual própria — sem "cara de IA" genérica.

## O que tem aqui

| Skill | O que faz |
|---|---|
| [`agente-de-paginas`](skills/agente-de-paginas) | Fluxo completo: descoberta do negócio → token system de design → arquitetura de seções → implementação → autocrítica → entrega |
| [`frontend-design`](skills/frontend-design) | Camada de execução visual — design system em tokens CSS, componentes, responsividade |
| [`setup-landing-stack`](skills/setup-landing-stack) | Instalador opcional que puxa mais 3 ferramentas de terceiros (ver abaixo) |

As duas primeiras são autorais. `setup-landing-stack` não redistribui código de ninguém — ele só
roda os comandos oficiais de instalação de cada projeto de terceiro, direto da fonte.

## Instalação

Requer [Node.js](https://nodejs.org) e o [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
(ou outro agente suportado pelo `skills` CLI).

```bash
npx skills add ezequias04/agente-gerando-de-sites
```

Isso instala as 3 skills acima no seu projeto atual. Depois, opcionalmente, peça para o agente
rodar a skill `setup-landing-stack` (ou digite `/setup-landing-stack`) para puxar o resto do stack
de design/animação.

## Como usar

Não precisa chamar nada manualmente depois de instalado. Descreva o que você quer construir
("crie uma landing page para [negócio], focada em [objetivo]") e o agente identifica sozinho
quando usar `agente-de-paginas` e `frontend-design`, na ordem certa.

Se quiser o fluxo completo guiado (identidade visual, estratégia, design, interatividade,
auditoria), use o template em [`prompts/prompt-mestre-landing-page.md`](prompts/prompt-mestre-landing-page.md)
como primeira mensagem de uma conversa nova.

## Stack opcional de terceiros (via `setup-landing-stack`)

Nenhum destes é distribuído neste repositório — a skill `setup-landing-stack` só orquestra a
instalação oficial de cada um, com crédito:

- [**design-taste-frontend**](https://github.com/Leonxlnx/taste-skill) — critério de design
  anti-clichê, por [@Leonxlnx](https://github.com/Leonxlnx)
- [**skills de animação**](https://github.com/emilkowalski/skills) — craft de motion/interação,
  por [Emil Kowalski](https://github.com/emilkowalski) (criador do Vaul e Sonner)
- **UI/UX Pro Max** (`uipro-cli` no npm) — biblioteca de estilos/paletas/tipografia
- **21st.dev Magic** (opcional, só para projetos React) — requer API key própria do usuário,
  nunca incluída aqui

## Licença

MIT — veja [LICENSE](LICENSE). As skills de terceiros mencionadas acima mantêm suas próprias
licenças; instale-as diretamente das fontes originais.
