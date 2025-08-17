# GitHub Copilot Demo
- Dette er virkelig bra fordi det lar deg legge til helpers i VS Code og slutte å kopiere og lime inn de lagrede prompts dine i GitHub Chat Window.

## Lagrede prompts for gjenbrukshjelpere på tvers av team

| Funksjon            | Forskjeller                                                                                                                | Når bør det brukes                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Custom Chat Modes   | Hvilke verktøy den kan bruke, definert i `.github/chatmodes` og `settings.json`.                  | Lag en front-end developer chat mode, der AI-en kun kan generate og modify code relatert til front-end development. |
| Custom Instructions | Hvordan en oppgave skal utføres, lagret i `.github/instructions`. | Spesifiser kodingspraksis, foretrukne teknologier eller prosjektkrav, slik at generert kode følger dine standarder. |
| Reusable Prompts    | Hva som skal gjøres, lagret i `.github/prompts`, kalt opp via `/prompt-name` i Chat.                 |  Lag gjenbrukbare prompts for vanlige kodeoppgaver, som å sette opp en ny komponent, en API-rute eller generere tester. 
## Saved prompts for reuse helpers across teams

| Feature             | Differences                                                                                                       | Right Time to Use                                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Custom Chat Modes   | Which tools it can use, defined in `.github/chatmodes` and `settings.json`.            | Create a front-end developer chat mode, where the AI can only generate and modify code related to front-end development.  |
| Reusable Prompts    | What should be done, stored in `.github/prompts`, invoked via `/prompt-name` in Chat.            | Create reusable prompts for common coding tasks, such as scaffolding a new component, API route, or generating tests. |
| Custom Instructions | How a task should be done, stored in `.github/instructions`. | Specify coding practices, preferred technologies, or project requirements, so generated code follows your standards.