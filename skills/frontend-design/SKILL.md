---
name: frontend-design
description: Cria interfaces visuais e código (HTML + CSS) com identidade distinta, intencional e ancorada no universo do cliente. É a camada de execução visual que complementa a skill 'landing-alta-conversao' (estratégia). Use quando o pedido envolver criar uma página, montar interface, gerar código front-end de qualidade, ou criar um design system do zero. Acionada automaticamente pela skill 'landing-alta-conversao' na Etapa 4, ou diretamente quando o usuário pedir '/frontend-design'.
---

# Skill: Frontend Design

## Princípio central

Você é o **design lead de um estúdio pequeno conhecido por entregar a cada cliente uma identidade visual que não pode ser confundida com a de mais ninguém**. Este cliente já rejeitou propostas que pareciam template — está pagando por um ponto de vista **opinativo e deliberado**. Faça escolhas conscientes de paleta, tipografia, layout, e arrisque **uma estética real que você consiga justificar**.

**Estética adaptativa ao contexto**, mas com disciplina: nada de cair em default só porque é cômodo.

## Filosofia: ancorar no sujeito, não no estilo

Antes de desenhar, **fixe o sujeito**. Se o brief não define produto, público e objetivo, defina você mesmo e declare. O universo do próprio cliente — seus materiais, instrumentos, artefatos, linguagem — é onde nascem as escolhas distintas. Construa com o conteúdo real do brief, não com placeholders genéricos.

## 3 looks defaults de IA que você DEVE evitar

Hoje, design gerado por IA se concentra em três looks óbvios. **Evite cair neles sem motivo real**:

1. **Cream + serif + terracota** — fundo creme (~#F4F1EA), display serif de alto contraste, acento terracota. Bonito, mas virou "default do AI".
2. **Preto + verde-ácido/vermelho** — fundo quase preto com um único acento brilhante. Estilo "tech bro".
3. **Broadsheet** — layout de jornal, hairline rules, border-radius zero, colunas densas. Estilo "editorial genérico".

**Onde o brief pinar uma direção, siga exatamente.** Onde deixar um eixo livre, **não gaste essa liberdade num desses defaults**. A pergunta certa: "se eu recebesse um brief parecido, chegaria no mesmo lugar?" Se sim, revise.

## Princípios de design

### O hero é uma tese
Abra com a coisa **mais característica do universo do sujeito**, na forma que fizer sentido: headline, imagem, animação, demo ao vivo, momento interativo. **Evite o template**: "número grande com label pequeno + stats de apoio + gradiente de acento" só se for genuinamente a melhor opção.

### Tipografia carrega a personalidade
Emparelhe **deliberadamente** display + body, não as mesmas famílias que você alcançaria em qualquer projeto. Defina uma escala clara com pesos, larguras e espaçamentos intencionais. **O tratamento tipográfico em si** deve ser memorável, não apenas um veículo neutro para o conteúdo.

### Estrutura é informação
Numerações, eyebrows, divisores, labels devem **codificar algo verdadeiro sobre o conteúdo**, não decorar. Marcadores numerados (01/02/03) só fazem sentido se o conteúdo for realmente uma sequência. Questione cada escolha estrutural antes de incorporar.

### Movimento com propósito
Pense **onde** a animação serve ao sujeito: sequência de page-load, reveal no scroll, microinterações de hover, atmosfera ambiente. Um momento orquestrado costuma bater mais forte que efeitos espalhados. **Às vezes, menos é mais** — animação extra contribui para a sensação de "design gerado por IA".

### Complexidade casada com a visão
Direção maximalista precisa de execução elaborada. Minimalista precisa de precisão em espaçamento, tipo e detalhe. **Elegância é executar bem a visão escolhida.**

### Copy é material de design
Palavras aparecem no design por um motivo: **facilitar compreensão, portanto uso**. Traga a mesma intencionalidade ao copy que traz a espaçamento e cor. **Não separe copy de UI** — ambos são design.

## Processo: brainstorm → crítica → código

### Passada 1 — Brainstorm
Crie um **plano de design compacto** com:
- **Paleta**: 4–6 valores hex nomeados (não 50 tons, não "primary/secondary" genérico)
- **Tipo**: 2+ papéis — display com personalidade usado com parcimônia, body complementar, utility para legendas/dados se necessário
- **Layout**: conceito em prosa de uma frase + wireframe ASCII para idear e comparar
- **Signature**: o **único elemento memorável** pelo qual esta página será lembrada, que personifica o brief

### Passada 2 — Crítica
Revise o plano contra o brief:
- Alguma parte parece o default genérico que você produziria para qualquer página parecida? → **revise**
- Você consegue dizer **o que mudou e por quê**?

Só depois dessa crítica, comece a escrever o código. **Derive toda decisão de cor e tipo do plano aprovado**, não do instinto.

## Princípio da contenção

**Gaste sua ousadia em UM lugar só.** Deixe o signature element ser a coisa memorável; mantenha todo o resto quieto e disciplinado. Corte qualquer decoração que não sirva ao brief. **Construa até um piso de qualidade sem anunciar**: responsivo até mobile, foco de teclado visível, `prefers-reduced-motion` respeitado.

**Critique seu próprio trabalho enquanto constrói.** Tire screenshots se o ambiente permitir. Considere o conselho da Chanel: antes de sair, olhe no espelho e tire um acessório. Se você tem um espaço para anotar rapidamente o que tentou, isso ajuda em passadas futuras.

## Copy como decisão de design

**Voz ativa por padrão.** Um controle deve dizer exatamente o que acontece: "Salvar alterações", não "Enviar". A ação mantém o mesmo nome por todo o fluxo — botão "Publicar" gera toast "Publicado". **Coesão e consistência** são como as pessoas aprendem a se virar.

**Trate falha e vazio como momentos de direção, não de humor.** Explique o que deu errado e como corrigir, na voz da interface, não na de uma pessoa. Erros não se desculpam, e nunca são vagos. Tela vazia é **convite para agir**, não estado triste.

**Registro conversacional e afinado**: verbos simples, sentence case, sem preenchimento, tom casado com marca e audiência. **Cada elemento faz exatamente um trabalho.** Um label rotula, um exemplo demonstra, nada faz dupla função silenciosamente.

## Quando esta skill é acionada

1. **Pela skill `landing-alta-conversao`**: ao final da Etapa 3 (arquitetura aprovada), com todo o contexto estratégico passado como input.
2. **Diretamente pelo usuário**: via `/frontend-design` ou quando o pedido for claramente sobre UI/código front-end.

### Entrada esperada (contexto)
- [ ] Objetivo da página
- [ ] Nicho e público
- [ ] Identidade da marca (cores, tipografia, tom, referências visuais)
- [ ] Mapa de seções aprovado
- [ ] Copy final (ou aprovação para criar)
- [ ] Restrições técnicas

Se algo faltar, **perguntar antes de codar** — especialmente referências visuais e cores.

---

# EXECUÇÃO TÉCNICA

## Etapa T1 — Design System (tokens)

Sempre criar os **tokens** via CSS variables no `:root` **antes** de qualquer componente.

### Tokens obrigatórios:

```css
:root {
  /* === Paleta: 4-6 valores hex NOMEADOS, não escalas genéricas === */
  --ink: #0a0a0a;          /* principal: texto, marca forte */
  --paper: #fafaf7;         /* fundo principal */
  --rust: #b8451f;          /* acento (apenas 1, com parcimônia) */
  --mist: #e8e6df;          /* superfície sutil, divisores */
  --slate: #4a4a48;         /* texto secundário */
  --highlight: #f5d547;     /* destaque raro */
  
  /* === Tipografia: 2+ papéis === */
  --font-display: 'Fraunces', Georgia, serif;   /* personalidade, com parcimônia */
  --font-body: 'Inter', system-ui, sans-serif;  /* leitura confortável */
  --font-mono: 'JetBrains Mono', monospace;     /* dados/códigos/legendas */
  
  /* Escala (1.250 — terceira maior) */
  --text-xs: 0.75rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-lg: 1.125rem;
  --text-xl: 1.25rem;
  --text-2xl: 1.5rem;
  --text-3xl: 1.875rem;
  --text-4xl: 2.25rem;
  --text-5xl: 3rem;
  --text-6xl: 3.75rem;
  --text-7xl: 4.5rem;
  
  /* Pesos */
  --font-normal: 400;
  --font-medium: 500;
  --font-semibold: 600;
  --font-bold: 700;
  
  /* Line height */
  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --leading-normal: 1.5;
  --leading-relaxed: 1.65;
  
  /* Tracking */
  --tracking-tight: -0.02em;
  --tracking-normal: 0;
  --tracking-wide: 0.05em;
  
  /* === Espaçamento (escala 4px) === */
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-5: 1.25rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-10: 2.5rem;
  --space-12: 3rem;
  --space-16: 4rem;
  --space-20: 5rem;
  --space-24: 6rem;
  --space-32: 8rem;
  
  /* === Bordas === */
  --radius-sm: 0.25rem;
  --radius-md: 0.5rem;
  --radius-lg: 0.75rem;
  --radius-xl: 1rem;
  --radius-2xl: 1.5rem;
  --radius-full: 9999px;
  
  /* === Sombras === */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
  
  /* === Transições === */
  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 400ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
  
  /* === Layout === */
  --container-sm: 640px;
  --container-md: 768px;
  --container-lg: 1024px;
  --container-xl: 1280px;
  --container-2xl: 1440px;
  
  /* === Z-index === */
  --z-base: 0;
  --z-dropdown: 100;
  --z-sticky: 200;
  --z-overlay: 300;
  --z-modal: 400;
  --z-toast: 500;
}
```

### Regra de ouro
- **NUNCA** usar cor hex, px solto, ou font-family direto no código dos componentes.
- **SEMPRE** referenciar os tokens via `var(--...)`.

## Etapa T2 — Componentes base

Criar antes da página final. Cada componente deve ser **reutilizável, responsivo, acessível**.

### Componentes essenciais:

1. **Botões** — `sm/md/lg/xl` × `primary/secondary/ghost/destructive`. Estados: default, hover, focus, active, disabled, loading. Slot para ícone.
2. **Cards** — variantes `elevated`, `bordered`, `filled`, `horizontal`.
3. **Formulários** — input, textarea, select, checkbox, radio. Sempre com label associado, hint, mensagem de erro.
4. **Badges/Tags** — para status, categorias, "novo", "limitado".
5. **Avatares** — para depoimentos, equipe. `sm/md/lg`.
6. **Navbar** — sticky, responsivo (hambúrguer no mobile), com CTA principal.
7. **Footer** — links em colunas, copyright, redes sociais, legal.
8. **Modal/Dialog** — para exit intent, confirmações, vídeos.
9. **Toast** — feedback de ações.
10. **Accordion (FAQ)** — expansível, com animação suave.

## Etapa T3 — Animações e microinterações

**Sutis, funcionais, respeitando `prefers-reduced-motion`.**

### Princípios:
- Animar **transform** e **opacity** (evitar `width`, `height`, `top`, `left` — causam reflow)
- Duração curta (150–400ms) exceto decorativos
- Easing consistente: `cubic-bezier(0.4, 0, 0.2, 1)` como padrão
- **Nunca** sem propósito — corte o que não serve

### Animações essenciais:

```css
/* Hover em botões/cards */
.btn {
  transition: transform var(--transition-fast), 
              background-color var(--transition-base),
              box-shadow var(--transition-base);
}
.btn:hover {
  transform: translateY(-1px);
  box-shadow: var(--shadow-md);
}

/* Reveal no scroll */
.reveal {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity var(--transition-slow), 
              transform var(--transition-slow);
}
.reveal.is-visible {
  opacity: 1;
  transform: translateY(0);
}

/* Respeitar preferência do usuário */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

## Etapa T4 — Acessibilidade (WCAG 2.1 AA)

- [ ] Contraste: texto normal ≥ 4.5:1, grande ≥ 3:1, UI ≥ 3:1
- [ ] Foco visível em todos os elementos focáveis
- [ ] HTML semântico: `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`
- [ ] Labels associados a inputs (ou `aria-label`)
- [ ] Alt text descritivo (ou `alt=""` se decorativa)
- [ ] ARIA apenas quando necessário
- [ ] Navegação por teclado (Tab order lógico, Esc fecha modais)
- [ ] `<html lang="pt-BR">`
- [ ] Mensagens de erro claras, associadas via `aria-describedby`

## Etapa T5 — SEO on-page

- [ ] `<title>` único, ≤ 60 caracteres
- [ ] `<meta name="description">` único, ≤ 160 caracteres
- [ ] Open Graph: `og:title`, `og:description`, `og:image` (1200x630), `og:type`, `og:url`
- [ ] Twitter Card: `twitter:card`, `twitter:title`, `twitter:description`, `twitter:image`
- [ ] Canonical URL
- [ ] Headings hierárquicos (um único `<h1>`)
- [ ] Imagens com `alt` descritivo
- [ ] JSON-LD quando aplicável: Organization, Product, FAQ, Article

## Etapa T6 — Performance

- [ ] CSS em arquivo único; mínimo de JS
- [ ] Imagens WebP/AVIF, `srcset` + `sizes`, `loading="lazy"` abaixo da dobra
- [ ] `preload` de fontes críticas; `font-display: swap`
- [ ] Sem dependências externas desnecessárias
- [ ] `meta viewport` correto
- [ ] LCP < 2.5s, CLS < 0.1 (objetivo)

## Etapa T7 — Cuidado com especificidade CSS

**Atenção:** seletores por classe (`.section`) e por elemento (`.cta`) podem se cancelar. É fácil gerar CSS em que `.section { padding: 4rem }` é sobrescrito por `.cta { padding: 0 }` ou vice-versa. Estruture com cuidado: use modificadores explícitos (`.section--hero`, `.section--tight`) e mantenha o fluxo de cascata previsível.

## Etapa T8 — Entrega do código

### Estrutura:
```
projeto/
├── index.html
├── styles.css
└── assets/
    ├── images/
    ├── icons/
    └── fonts/ (se auto-hospedadas)
```

### No `index.html`:
- `<!DOCTYPE html>`, `<html lang="pt-BR">`
- Meta tags completas (charset, viewport, description, og, twitter)
- `<title>` otimizado
- Preconnect/preload de fontes
- Link para `styles.css`
- Estrutura semântica completa
- JSON-LD se aplicável

### No `styles.css`:
- `:root` com todos os tokens
- Reset minimalista
- Estilos base (tipografia, links)
- Componentes (na ordem em que aparecem)
- Utilities (`.container`, `.visually-hidden`)
- Media queries agrupadas por componente

## Etapa T9 — Saída final

Entregar:
1. **Resumo do plano de design** — paleta, tipo, layout, signature element, com justificativa
2. **Mapa de componentes** criados e onde são usados
3. **Código completo** (`index.html` + `styles.css`)
4. **Notas de implementação** — onde trocar placeholders, integrações pendentes
5. **Sugestões de evolução** — A/B tests, próximos passos

## Princípios inegociáveis

- **Mobile-first** — começa pelo design para telas pequenas
- **Tokens antes de componentes** — design system pronto antes de qualquer CSS solto
- **Semântica antes de estilo** — HTML correto primeiro, depois embelezar
- **Performance é UX** — imagem de 5MB destrói mais conversão que qualquer copy
- **Acessibilidade é pré-requisito, não polimento**
- **Menos é mais** — se um elemento não tem propósito, remova
- **Consistência > criatividade** — use os tokens
- **Ousadia em um lugar só** — signature element carrega a personalidade, o resto é disciplina

## O que NUNCA fazer

- ❌ Cair nos 3 looks defaults de IA sem motivo
- ❌ Usar valores hardcoded (px, hex, font-family) fora dos tokens
- ❌ Animar `width`, `height`, `top`, `left` (usar `transform`/`opacity`)
- ❌ Esquecer `alt` em imagens
- ❌ Botão sem estado de foco visível
- ❌ Contraste insuficiente
- ❌ Texto sobre imagem sem overlay/tratamento de legibilidade
- ❌ Mais de uma fonte sem propósito
- ❌ Animação que bloqueia o usuário
- ❌ Misturar unidades (`rem` e `px` no mesmo contexto)
- ❌ Esquecer `<meta name="viewport">`
- ❌ Decorações que não servem ao brief
- ❌ Gerar código sem ter passado pela crítica do plano
