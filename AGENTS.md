# Instructions for AI coding agents

You are working on **Pocket Passport**, an IN3210 Assignment 2 React Native project.

## Authority and scope

1. Read `README.md`, `PROJECT_CONTEXT.md`, `TASKS.md`, and relevant files under `docs/` before making changes.
2. The uploaded assignment specification is the authority. Do not silently add requirements or remove mandatory ones.
3. Index `234163`: last digit `3` means Travel & Countries; second-last digit `6` means Smart Search.
4. The assignment phase has **no custom backend**. Use DummyJSON for auth, a public country API for country data, and local persistence for favourites.
5. Do not add Spring Boot, PostgreSQL, community likes/dislikes, public reviews, or cloud trip sync to the assignment scope unless the user explicitly changes scope.

## Implementation rules

- TypeScript throughout application code.
- Use a feature-based structure.
- Use Redux Toolkit with RTK Query, thunks, or Redux-Saga for asynchronous logic. Prefer RTK Query unless a documented reason favours another option.
- Use React Navigation or Expo Router; keep route parameters typed.
- Keep UI components, API/data access, state, and persistence separate.
- Country Details must receive a country identifier/code, not an entire country object, and load its own data.
- Debounce search so filtering/API work is not triggered on every keystroke. Provide filter chips and a clear empty state.
- Use Feather icons for icons and centralised theme tokens.
- Use touch targets of at least 48 dp.
- Auth tokens must be stored in secure Keychain/Keystore storage. Never store tokens in AsyncStorage or MMKV.
- Favourites may be persisted with AsyncStorage or MMKV.
- Do not invent API response fields. Define and validate types against the selected API response.
- Handle loading, error-with-retry, and empty states.
- Avoid unnecessary dependencies. Check Expo/native compatibility before adding native packages.
- Do not hardcode credentials, tokens, or API secrets.

## Workflow

1. Choose one small task from `TASKS.md`.
2. Inspect the current implementation before editing.
3. Implement only the selected task and related tests.
4. Run formatting/lint/typecheck/tests available in the project.
5. Report files changed, commands run, results, and any remaining limitation.
6. Update `TASKS.md`, `docs/PROGRESS.md`, and `docs/DECISIONS.md` where applicable.
7. Do not claim a check passed unless it was actually run successfully.

## Git

- Use small, feature-focused commits.
- Do not commit generated build artefacts, secrets, or local environment files.
- Do not rewrite history or force-push unless explicitly asked.
