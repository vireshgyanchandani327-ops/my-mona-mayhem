<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construye el juego con flujos de trabajo basados en agentes

---

En esta parte, Copilot pasa de planificar a implementar. En lugar de escribir código línea por línea, describes lo que necesitas y dejas que Copilot realice el trabajo en los archivos necesarios.

## Tarea 1: Conecta la batalla

<!-- track:vscode:start -->
1. Cambia al modo **Agent** en Copilot Chat.
2. Escribe este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Devuelve Copilot CLI a su flujo de programación habitual (o mantén el modo autopilot si quieres que siga trabajando hasta que lo detengas).
2. Si te resulta útil, menciona el archivo de la página para dar más contexto: `@src/pages/index.astro`.
3. Escribe este prompt:
<!-- track:cli:end -->

   > Add client-side JavaScript to the battle page that:
   > 1. When the Battle button is clicked, gets both usernames from the inputs
   > 2. Validates both are filled (show error if not)
   > 3. Fetches both users' contribution data in parallel from our API
   > 4. Renders contribution graphs as colored grids — each day is a colored square using GitHub's color palette
   > 5. Shows a VS badge between the two users
   > 6. Displays username, total contributions, and date range for each user
   > 7. Handles loading states and errors
   > 8. Also triggers on Enter key in input fields.
   > 9. Simple UI for now that is already scaffolded.
   >
   > Use TypeScript interfaces for the contribution data structure.

<!-- track:vscode:start -->
3. Deja que Agent Mode implemente los cambios en varios archivos a través de `index.astro`.
4. Revisa los cambios propuestos en la vista de diferencias antes de aceptarlos.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deja que Copilot CLI realice los cambios en `src/pages/index.astro`.
5. Usa `/diff` para revisar los cambios generados y, después, apruébalos.
<!-- track:cli:end -->

## Tarea 2: Prueba la batalla

> **⚠️ ¿No ves los cambios?** Si la página de batalla no se ha actualizado, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y actualiza el navegador.

1. Escribe `octocat` y `torvalds` como nombres de usuario y haz clic en **Battle**.
2. Deberían aparecer los dos gráficos de contribuciones, uno junto al otro, con cuadrículas de colores.
3. Comprueba los casos de error:
   - Deja vacío uno o ambos campos y haz clic en Battle: debería aparecer un error de validación.
   - Escribe un nombre de usuario no válido: la aplicación debería mostrar un error de la API.
4. Pulsa **Enter** en cualquiera de los campos: debería iniciar la batalla igual que al hacer clic en el botón.

## Tarea 3: Itera con Copilot

Si algo no está del todo bien, da directamente a Copilot comentarios para que lo ajuste. Por ejemplo:

- *"The contribution squares are too large, make them 12x12px"*
- *"Add a hover tooltip showing the date and contribution count"*
- *"The loading state needs a pulse animation"*

<!-- track:vscode:start -->
Agent Mode gestiona de forma natural los cambios en varios archivos y las iteraciones. Cada prompt de seguimiento aprovecha la conversación anterior, así que puedes perfeccionar la implementación poco a poco sin empezar de cero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Las sesiones de Copilot CLI conservan el historial, por lo que cada prompt de seguimiento se basa en el anterior. Usa `/session` o `/context` para revisar lo que Copilot mantiene como contexto, y `/review` después de una iteración grande para buscar errores o posibles mejoras.
<!-- track:cli:end -->

## Consejos para esta parte

- **Especifica lo que necesitas**: los requisitos claros suelen dar mejores resultados.
- **Divide las tareas grandes en prompts más pequeños** si Copilot se desvía.
- **Revisa los cambios antes de aceptarlos**: es más rápido inspeccionar el código generado que tener que reescribirlo después.
- **Prueba la aplicación después de cada implementación** para detectar pronto los problemas.

## ✅ Parte 3 completada

Has aprendido a:

- Usar Copilot para **implementar cambios en varios archivos**.
- **Iterar sobre los resultados** con comentarios concretos.
- Gestionar el **ciclo completo de una funcionalidad**: implementación, revisión, pruebas y ajustes.
