<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización orientada al diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Este enfoque empieza por el diseño: parte de una visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo de planificación.
<!-- track:cli:end -->

Escribe este prompt:

> I want to transform this page into a full retro arcade experience. Plan a comprehensive visual overhaul that includes: CRT scanline effects on the background, neon glow on the title that pulses like a neon sign, animated VS badge with gradient color shifts, shine/shimmer overlay on the user result cards, float-in animations for input fields, color-shifting loading text between green and purple, and hover glow effects on contribution squares. Keep the dark background (`#0a0a1a`) with green (`#5fed83`) and purple (`#8a2be2`) accent colors. Use a dark theme with the Press Start 2P retro gaming font from Google Fonts.

Copilot generará un plan de implementación detallado con todos los efectos visuales. **No lo aceptes de inmediato**: revísalo e itera:

- Propón ajustes en la duración de las animaciones (por ejemplo, *"Make the neon pulse slower, around 3 seconds"*).
- Pregunta por efectos concretos (por ejemplo, *"How will the shimmer overlay work on the cards?"*).
- Solicita cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés conforme con el plan, pide a Copilot que lo implemente.

> Implement the retro arcade theme plan we just designed.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a la hoja de estilos. Puede incluir:

- `@keyframes` para los efectos de scanlines, pulso neón, shimmer y aparición flotante.
- Pseudoelementos (`::before`, `::after`) para efectos de superposición.
- Propiedades personalizadas de CSS para los colores del tema.
- Transiciones y estados hover para los elementos interactivos.

<!-- track:cli:start -->
Cuando los cambios estén listos, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta los detalles visuales

> **⚠️ ¿No ves los cambios?** Si no aparecen el tema nuevo o las animaciones, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y fuerza la actualización del navegador (`Ctrl+Shift+R`).

Mantén abierta la vista previa en el navegador e itera sobre el diseño. Prueba prompts como:

> The scanline effect is too strong, reduce opacity to 0.03

> Add a subtle electrical flicker to the title text

> The VS badge should pulse more dramatically

Este es el desarrollo orientado al diseño: iteras sobre el resultado visual en tiempo real. Cada prompt refina la experiencia hasta que tenga el aspecto adecuado. No te conformes con algo «suficientemente bueno»: perfecciona el diseño hasta que la página parezca sacada de una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deberían reflejar las decisiones de diseño importantes para mantener la coherencia de los prompts posteriores.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Add a design guide section to copilot-instructions.md describing our retro arcade theme: colors, fonts, animation style
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Update our repository instructions with a short design guide for the retro arcade theme: colors, fonts, animation style, and the rule that new UI should keep the neon aesthetic.
<!-- track:cli:end -->

Haz commit de las instrucciones actualizadas y los cambios de diseño cuando la página tenga el aspecto adecuado.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para diseñar un **sistema visual antes de implementarlo**.
- **Iterar sobre el resultado visual** con prompts de seguimiento para ajustar el diseño.
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener una identidad visual coherente.
