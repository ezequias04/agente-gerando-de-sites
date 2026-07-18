# Prompt-mestre — Fluxo completo de Landing Page (criação e remodelação)

> Use este prompt como ponto de partida em uma nova conversa. Preencha os colchetes com as informações do projeto e apague o que não se aplicar.

---

## 1. Tipo de projeto

- [ ] **Landing page nova** — vou te passar o máximo de informação possível (links, logos, fotos, vídeos, referências).
- [ ] **Remodelação de página existente** — vou te passar o link/código atual + o que quero mudar.

## 2. Informações da marca/empresa

- **Nome da marca/empresa:** [nome]
- **Nicho/segmento:** [ex: perfumaria de luxo, SaaS B2B, infoproduto, e-commerce...]
- **Público-alvo:** [quem é, o que busca]
- **Tom de voz desejado:** [ex: luxo minimalista, técnico/confiável, jovem/despojado, divertido]
- **Ação principal que o visitante deve tomar (CTA):** [comprar, agendar, cadastrar, falar no WhatsApp...]
- **Materiais que vou enviar:** [logo, fotos de produto, vídeos, prints da concorrência, paleta de cor já existente, etc.]

## 3. Referências de design (opcional)

- [ ] Tenho um arquivo do **Figma** de referência aberto no app desktop (ou vou colar o link com `node-id`) para extrair paleta/tipografia/componentes como ponto de partida.
- [ ] Não tenho Figma — usar só a curadoria de estilo premium (`lp-design-library`) como base.
- [ ] Já tenho identidade visual definida (cores/tipografia) — não precisa recombinar, só aplicar.

## 4. Nível de interatividade desejado

- [ ] Interatividade cinematográfica completa (hero 3D, scroll storytelling, cursor customizado, partículas, etc. — nível Apple/Stripe/Linear/Awwwards)
- [ ] Interatividade moderada (reveal on scroll, hover nos cards, transições suaves)
- [ ] Só a estrutura/copy por enquanto, interatividade depois

## 5. Onde o resultado vai rodar

- [ ] Só quero ver/testar no chat (artifact)
- [ ] É para um projeto real (deploy, repositório, Claude Code, Lovable) com a stack completa disponível

---

## Instrução para o Claude — como conduzir o fluxo

Com base no que eu marcar acima, siga este pipeline, usando as skills correspondentes em cada etapa:

**Etapa 1 — Identidade visual (`identidade-visual-marca`)**
Se eu tiver Figma de referência, extraia os tokens (cores, tipografia, espaçamento) do arquivo/nó aberto ou do link que eu passar. Sempre cruze isso com a curadoria da `lp-design-library` e com as informações da marca da seção 2 acima. **Nunca copie a referência 1:1** — recombine em uma identidade própria, documentada como um mini design system (paleta, tipografia, princípios de textura, 1-2 frases de "caráter" da marca). Me mostre esse resumo antes de seguir.

**Etapa 2 — Estratégia comercial (`landing-alta-conversao`)**
Se for página nova: use o nicho, público e CTA da seção 2 para definir a arquitetura de seções (Hero, prova social, features, depoimentos, preços, FAQ, CTA final — o que fizer sentido para o meu caso) e a copy.
Se for remodelação: **antes** desta etapa, rode `landing-page-auditoria` na página atual para diagnosticar o que preservar e o que travar conversão, e use esse diagnóstico como ponto de partida em vez de recomeçar do zero.

**Etapa 3 — Design system aplicado (`frontend-design`)**
Aplique a identidade da Etapa 1 na estrutura da Etapa 2 — layout, componentes, responsividade.

**Etapa 4 — Interatividade (`landing-page-interativa`)**
Conforme o nível marcado na seção 4, monte o plano de efeitos seção por seção (consultando o catálogo completo de 20 categorias) e implemente, respeitando a stack do ambiente de destino (seção 5) e os guardrails de performance/acessibilidade/mobile. Se a Etapa 1 gerou conceitos de imagem de fundo, use os prompts gerados lá (ou as imagens que eu enviar depois de gerá-las) nos efeitos de Hero/Fundo.

**Etapa 5 — Auditoria final (`landing-page-auditoria`)**
Antes de eu levar o projeto ao cliente, rode a auditoria completa: conformidade com o planejado, estratégia de conversão, interatividade/performance, consistência técnica, e se todo material que eu enviei foi de fato incorporado.

**Loop de feedback do cliente**
Depois que eu levar o projeto e trouxer retorno do cliente (aprovação, pedido de mudança, ou material novo — fotos/vídeos/logo/texto), volte às etapas pertinentes (não precisa refazer tudo) e rode a `landing-page-auditoria` de novo no final, com atenção especial a confirmar que o material novo entrou na página.

---

*Preenchi as seções 1-5 acima com as informações do meu projeto — pode seguir o pipeline.*
