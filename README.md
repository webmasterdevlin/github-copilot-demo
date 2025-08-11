# GitHub Copilot Demo

## Tilpass AI-responsene og hjelpere i VS Code

| Funksjon            | Forskjeller                                                                                                                | Når bør det brukes                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Custom Instructions | Hvordan en oppgave skal utføres, lagret i `.github/instructions`. | Spesifiser kodingspraksis, foretrukne teknologier eller prosjektkrav, slik at generert kode følger dine standarder. |
| Reusable Prompts    | Hva som skal gjøres, lagret i `.github/prompts`, kalt opp via `/prompt-name` i Chat.                 |  Lag gjenbrukbare prompts for vanlige kodeoppgaver, som å sette opp en ny komponent, en API-rute eller generere tester. |
| Custom Chat Modes   | Hvilke verktøy den kan bruke, definert i `.github/chatmodes` og `settings.json`.                  | Lag en front-end developer chat mode, der AI-en kun kan generate og modify code relatert til front-end development. |
| MCP Servers         | Automatisk aktiveres som en del av svaret på en brukerforespørsel, konfigurert i VS Code for Agent/Chat modes.        | Aktiver database scaffolding og querying for dynamisk å gi LLM-en relevant kontekst. |

## Customize AI responses and helpers in VS Code

| Feature             | Differences                                                                                                       | Right Time to Use                                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Custom Instructions | How a task should be done, stored in `.github/instructions`. | Specify coding practices, preferred technologies, or project requirements, so generated code follows your standards. |
| Reusable Prompts    | What should be done, stored in `.github/prompts`, invoked via `/prompt-name` in Chat.            | Create reusable prompts for common coding tasks, such as scaffolding a new component, API route, or generating tests. |
| Custom Chat Modes   | Which tools it can use, defined in `.github/chatmodes` and `settings.json`.            | Create a front-end developer chat mode, where the AI can only generate and modify code related to front-end development. |
| MCP Servers         | Automatically invoked as part of responding to a user prompt, configured in VS Code for Agent/Chat modes.  | Enable database scaffolding and querying to dynamically provide the LLM with relevant context. |
