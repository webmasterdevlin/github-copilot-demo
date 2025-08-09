# GitHub Copilot Demo

## Norsk

| Funksjon            | Forskjeller                                                                                                                | Når bør det brukes                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Custom Instructions | Brukes automatisk på forhåndsdefinerte kodestandarder for alle Copilot Chat-forespørsler, lagret i `.github/instructions`. | Bruk for konsistente .NET/React SPA-standarder i et repo, som å håndheve TypeScript eller sikre API-praksiser.              |
| Reusable Prompts    | Templated prompts for spesifikke oppgaver, lagret i `.github/prompts`, kalt opp via `/prompt-name` i Chat.                 | Bruk for gjentakende oppgaver som å generere .NET-endepunkter eller React-komponenter i ditt SPA-prosjekt.                  |
| Custom Chat Modes   | Konfigurerer oppgavespesifikk Chat-atferd med verktøy, definert i `.github/chatmodes` og `settings.json`.                  | Bruk for fokuserte økter som debugging av SQL i .NET eller refaktorering av React UI, ikke dekket av standardmoduser.       |
| MCP Servers         | Utvider Copilot med eksterne verktøy/API-er via Model Context Protocol, konfigurert i VS Code for Agent/Chat modes.        | Bruk for å integrere eksterne tjenester (f.eks. tilpassede API-er) i Agent mode for avansert .NET/React SPA-automatisering. |

## English

| Feature             | Differences                                                                                                       | Right Time to Use                                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Custom Instructions | Automatically applies predefined coding standards to all Copilot Chat requests, stored in `.github/instructions`. | Use for consistent .NET/React SPA standards across a repo, like enforcing TypeScript or secure API practices.   |
| Reusable Prompts    | Templated prompts for specific tasks, stored in `.github/prompts`, invoked via `/prompt-name` in Chat.            | Use for repeatable tasks like generating .NET endpoints or React components in your SPA project.                |
| Custom Chat Modes   | Configures task-specific Chat behavior with tools, defined in `.github/chatmodes` and `settings.json`.            | Use for focused sessions like debugging SQL in .NET or refactoring React UI, not covered by default modes.      |
| MCP Servers         | Extends Copilot with external tools/APIs via Model Context Protocol, configured in VS Code for Agent/Chat modes.  | Use for integrating external services (e.g., custom APIs) in Agent mode for advanced .NET/React SPA automation. |
