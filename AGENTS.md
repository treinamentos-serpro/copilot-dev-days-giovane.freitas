# AGENTS.md

## Mandatory development checklist
Before completing a change, run all three checks from `socops/`:

- [ ] Lint: `./mvnw checkstyle:check`
- [ ] Build: `./mvnw clean package`
- [ ] Test: `./mvnw test`

## Project
Soc Ops is a Java 21 Spring Boot social bingo game. The application lives in `socops/`.

- Overview: [README.md](README.md)
- Workshop: [workshop/GUIDE.md](workshop/GUIDE.md)
- Use the Maven wrapper; prefer the existing Spring Boot structure and small, reviewable changes.
- Keep business logic pure and testable. Controllers stay thin and delegate board behavior to `BoardAssembler`.
- Keep UI and business logic separate. For UI changes, follow the utility CSS conventions in [.github/instructions/css-utilities.instructions.md](.github/instructions/css-utilities.instructions.md) and [socops/src/main/resources/static/css/app.css](socops/src/main/resources/static/css/app.css).

## Design guide
- Keep the application dark and arcade-inspired with deep ink surfaces, subtle grid texture, and restrained neon accents.
- Use CSS variables in [socops/src/main/resources/static/css/app.css](socops/src/main/resources/static/css/app.css) as the source of truth for colors, surfaces, borders, muted text, and accent states.
- Reserve cyan for interaction and system status, lime for selected or actionable states, and amber for bingo or winning states. Maintain readable contrast over effects and glow.
- Keep the interface focused on the game: the lobby should make starting a game obvious, while the active view should prioritize the 5x5 board and prompt readability.
- Keep tile dimensions stable and distinguish open, selected, free, and winning cells. Long prompts must wrap without changing the board layout.
- Prefer existing CSS utility classes and small semantic component classes over new dependencies or inline styling. Keep selectors low-specificity and avoid unrelated visual refactors.
- Give every interactive state visible hover and keyboard focus feedback. Preserve `aria-label`, `aria-pressed`, and disabled behavior when changing tile markup.
- Check the lobby, board, victory modal, and restored snapshot at desktop and narrow mobile widths. Respect `prefers-reduced-motion` for animations.

## Architecture
- Entry point: [socops/src/main/java/com/socops/SocOpsApplication.java](socops/src/main/java/com/socops/SocOpsApplication.java)
- Routes: [socops/src/main/java/com/socops/web/BingoRestController.java](socops/src/main/java/com/socops/web/BingoRestController.java)
- Board and win logic: [socops/src/main/java/com/socops/service/BoardAssembler.java](socops/src/main/java/com/socops/service/BoardAssembler.java)
- Prompts: [socops/src/main/java/com/socops/data/IcebreakerPrompts.java](socops/src/main/java/com/socops/data/IcebreakerPrompts.java)
- Template: [socops/src/main/resources/templates/game.html](socops/src/main/resources/templates/game.html)

## Change guidance
- For game-rule changes, update `BoardAssembler` and its tests under [socops/src/test/java/com/socops/service](socops/src/test/java/com/socops/service).
- Start board work with `BoardAssembler` and its tests; start page work with the template and CSS; start API work with the controller and service boundaries.
- Use existing documentation as the source of truth. Run the app with `cd socops && ./mvnw spring-boot:run`.
