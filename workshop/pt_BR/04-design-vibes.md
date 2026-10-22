<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização orientada por design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Essa abordagem parte do design: comece pela visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> I want to transform this page into a full retro arcade experience. Plan a comprehensive visual overhaul that includes: CRT scanline effects on the background, neon glow on the title that pulses like a neon sign, animated VS badge with gradient color shifts, shine/shimmer overlay on the user result cards, float-in animations for input fields, color-shifting loading text between green and purple, and hover glow effects on contribution squares. Keep the dark background (`#0a0a1a`) with green (`#5fed83`) and purple (`#8a2be2`) accent colors. Use a dark theme with the Press Start 2P retro gaming font from Google Fonts.

O Copilot vai gerar um plano detalhado de implementação com todos os efeitos visuais. **Não aceite de imediato**: revise o plano e faça ajustes:

- Sugira mudanças na duração das animações (por exemplo, *"Make the neon pulse slower, around 3 seconds"*).
- Pergunte sobre efeitos específicos (por exemplo, *"How will the shimmer overlay work on the cards?"*).
- Peça alterações na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implement the retro arcade theme plan we just designed.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições à folha de estilos. Isso pode incluir:

- `@keyframes` para scanlines, pulso neon, shimmer e efeitos de entrada flutuante.
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades personalizadas de CSS para as cores do tema.
- Transições e estados de hover para elementos interativos.

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste os detalhes visuais

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize a página à força (`Ctrl+Shift+R`).

Mantenha a pré-visualização no navegador aberta e itere no design. Experimente prompts como:

> The scanline effect is too strong, reduce opacity to 0.03

> Add a subtle electrical flicker to the title text

> The VS badge should pulse more dramatically

Esse é o desenvolvimento orientado por design: você está iterando no resultado visual em tempo real. Cada prompt refina a experiência até ela ficar do jeito certo. Não se contente com algo apenas "bom o suficiente" — aperfeiçoe o visual até a página parecer saída de um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Add a design guide section to copilot-instructions.md describing our retro arcade theme: colors, fonts, animation style
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Update our repository instructions with a short design guide for the retro arcade theme: colors, fonts, animation style, and the rule that new UI should keep the neon aesthetic.
<!-- track:cli:end -->

Faça commit das instruções atualizadas e das alterações de design quando a página estiver como você quer.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para projetar um **sistema visual antes da implementação**.
- **Iterar no resultado visual** com prompts de acompanhamento para ajustar o design.
- **Atualizar as instruções depois de decisões importantes** para manter uma identidade visual consistente.
