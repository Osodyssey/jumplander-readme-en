
# JumpLander — Hero coder (Interactive User Panel Guide)

This guide is a practical, step-by-step user manual for the **JumpLander** AI coding panel. It assumes you are already logged in and have access to the editor, AI chat, and Agents. The goal: help you work efficiently and safely with the platform to generate, refactor, secure, and ship code using AI assistants.

---

## Quick Start — First Steps After Login

1. **Check the Dashboard**  
   After login, glance at your dashboard: active plan, remaining credits, and recent notifications. If credits are low, use the “Top up / Subscription” button.

2. **Open or Upload a Project**  
   Click “Upload Project” or “New Project”. Pick a workspace folder to enable editor features and tools.

3. **Choose a Model & Mode**  
   At the top of the panel choose a model and one of the modes: `Standard`, `Debug`, `Security`, `Agent`. Suggested choices:
   - Quick code generation: `Fast` model
   - Precise refactor: `High-Quality` model
   - Security checks: `Security` mode

---

## The Workspace — Four Key Areas

- **File Explorer (left)** — browse project files and open them in the editor.  
- **Editor (center)** — code editing with inline suggestions and patch application.  
- **AI Chat (right)** — send prompts, receive answers, and run tools.  
- **Terminal / Runner (bottom)** — run tests, commands, or view CI results.

Tip: AI responses appear in the chat panel. Use `Preview` to inspect patches and `Apply` to insert changes into the editor.

---

## Practical Workflows (Examples)

### 1) Generate a New Function or Module
1. Open the AI chat and type your request, e.g.:  
   `Generate: Create a Python function "fast_prime" that checks primality up to 10^9 efficiently, include docstring and unit tests.`  
2. Review the result in chat.  
3. Click `Preview` then `Apply` to insert the code into the editor, or `Copy` for manual use.

If you want explanations in Persian, add: `Explain in Persian`.

---

### 2) Refactor Selected Code
1. Select the code in the editor.  
2. In the chat: `Refactor selected code: convert to async, add type hints, improve performance.`  
3. The platform returns a unified diff/patch.  
4. Preview the patch and `Accept` or `Reject`. After `Apply`, run tests to validate.

---

### 3) Security Scan and Auto-Fix
1. Choose a file or the whole project, then click `Security Scan`.  
2. The system lists vulnerabilities ranked by severity.  
3. Click `Auto-Fix` on a finding to let an Agent propose a patch.  
4. Review the patch, run tests in the sandbox, then apply.

---

### 4) Run an Agent (Multi-step Pipeline)
Agents perform complex pipelines like `analyze → propose_fix → test → report`.  
Example: `Test-Generator Agent`:
- Scans code for untested functions  
- Generates unit tests  
- Runs tests in an isolated environment  
- Creates a PR or applies changes directly (based on settings)

Jobs are tracked with Job IDs in the `Jobs` list (logs and step-by-step traces available).

---

## Controls & Shortcuts (Hotkeys)

- `Ctrl + Enter` — send prompt to chat  
- `Ctrl + Space` — accept inline suggestion / trigger completions  
- `Ctrl + .` — open quick fix actions for the current line  
- `Ctrl + S` — save file  
- `Alt + Enter` — run action on selection (e.g., Refactor, Explain)

---

## Prompting Tips (How to get the best results)

- Be **specific**: `Refactor selected code to reduce memory use` beats `Make it better`.  
- Provide **examples** or desired style if you want a particular format.  
- Set constraints: `max 60 lines`, `no new dependencies`.  
- Ask for an explanation: `Explain the change in 2 sentences`.

---

## Cost & Credit Management

- Each AI action consumes credits. The panel shows the **estimated cost** before execution. Typical examples:
  - `Generate` = small cost
  - `Refactor` = medium cost
  - `Agent runs` = larger cost

Always confirm the cost before running heavy operations like full-project scans or long-running Agents.

---

## Best Practices

- Always `Preview` patches before applying.  
- Make a commit (or snapshot) before large changes so you can rollback easily.  
- Run generated code in a sandbox before merging to main.  
- Use language-specific prompts when you want idiomatic code.

---

## Troubleshooting

- **No response from the model**: Check model selection and that credits are available.  
- **Patch won’t apply**: Line endings or merge conflicts might be the cause — check file versions.  
- **Runtime errors after applying changes**: Inspect sandbox logs and re-run tests.

---

## Ready Prompts (Copy & Use)

- **Generate**: `Generate a REST API endpoint in Node.js (Express) for user login with JWT auth and input validation.`  
- **Refactor**: `Refactor selected code to use dependency injection and improve testability.`  
- **Security**: `Scan this file for SQL injection vulnerabilities and suggest fixes.`  
- **Explain**: `Explain this function in plain Persian in 3 bullet points.`

---

## Security & Privacy Notes

- Never paste API keys or secrets into chat.  
- Execute untrusted code only in sandboxed environments with resource limits.  
- Mask or remove sensitive user data before sending code to an external model.

