---
name: setup-landing-stack
description: "Instala o restante do stack de design/animação usado junto com agente-de-paginas e frontend-design: design-taste-frontend (Leonxlnx/taste-skill), as skills de animação do Emil Kowalski, e opcionalmente UI/UX Pro Max e 21st.dev Magic. Rode isso uma vez depois de instalar este pacote."
---

# Setup do stack completo de landing pages

Este pacote já te deu duas skills prontas (`agente-de-paginas` e `frontend-design`). Este passo
final opcional puxa mais três ferramentas de terceiros, direto das fontes originais — nenhuma delas
é distribuída dentro deste repositório, cada uma mantém sua própria licença e autoria.

Ao ser acionado, guie o usuário um passo de cada vez. Se um passo falhar, não pare: avise e dê o
comando manual.

---

### Passo 1 — Critério de design anti-clichê (Leonxlnx/taste-skill)

> 13 skills de design (variância/motion/densidade, brutalista, minimalista, redesign de site
> existente, etc). Repositório: https://github.com/Leonxlnx/taste-skill

Rode:
```bash
npx skills add Leonxlnx/taste-skill
```

---

### Passo 2 — Craft de animação (emilkowalski/skills)

> 6 skills de animação/motion por Emil Kowalski (criador das libs Vaul e Sonner).
> Repositório: https://github.com/emilkowalski/skills

Rode:
```bash
npx skills add emilkowalski/skills
```

---

### Passo 3 (opcional) — UI/UX Pro Max

> Biblioteca de 67+ estilos, paletas e pares tipográficos via CLI própria.

Rode:
```bash
npm install -g uipro-cli
uipro init --ai claude
```

---

### Passo 4 (opcional) — 21st.dev Magic (biblioteca de componentes React)

> Só faz sentido se o projeto for React/Next. Precisa de uma API key **própria** do usuário —
> nunca peça para colar uma chave que não seja dele, e nunca grave uma chave de exemplo neste
> arquivo.

1. Peça para o usuário criar a própria key em https://21st.dev/magic/console (grátis)
2. Quando ele colar a key, adicione ao `mcpServers` do `~/.claude.json` (escopo do projeto atual):
```json
"21st-dev-magic": {
  "command": "npx",
  "args": ["-y", "@21st-dev/magic@latest"],
  "env": { "API_KEY": "<A_KEY_QUE_O_USUARIO_COLOU>" }
}
```
3. Avise que precisa reiniciar o Claude Code para carregar.

---

### Passo 5 — Pronto

> Resumo do que foi instalado e sugestão: "me peça uma landing page e eu já uso o critério de
> design certo automaticamente."
