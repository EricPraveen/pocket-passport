# Pocket Passport

**Your world, in your pocket.**

Pocket Passport is a React Native country-discovery app for IN3210 Mobile Applications Development – Assignment 2. It lets users sign in, explore countries from a public API, inspect country details, and save favourites. The assigned twist is **Smart Search**.

> **Important:** This repository is a project scaffold and planning workspace. It is not a completed assignment. Implement and test each task before marking it complete.

## Assignment identity

- Module: IN3210 – Mobile Applications Development
- Assessment: Assignment 2 – Build Your Own Discovery App
- Index number: `234163`
- Last digit: `3` → **Travel & Countries** domain
- Second-last digit: `6` → **Smart search** twist
- App name: **Pocket Passport**
- Suggested repository: `pocket-passport`
- Deadline stated in the assignment PDF: **13 December 2026, 11:59 PM**

## Required behaviour

1. Register and log in using DummyJSON. Registration may be simulated with `POST /users/add`, followed by login.
2. Validate authentication form inputs.
3. Store the authentication token securely with Keychain/Keystore. **Do not store auth tokens in AsyncStorage or MMKV.**
4. Use React Navigation (or Expo Router) with a separate auth flow, bottom tabs (at least Home and Favourites), and a Home → Details stack. Type route params.
5. Browse country items from a public API.
6. Country Details receives a country ID/code, fetches its own data, and supports a favourite toggle.
7. Use Redux Toolkit with RTK Query, thunks, or Redux-Saga for asynchronous logic. Explain the choice in README.
8. Persist favourites across app restarts using AsyncStorage or MMKV.
9. Implement the assigned Smart Search twist:
   - Debounced search: do not filter/call the API on every keystroke.
   - Filter chips.
   - Clear empty state when there are no matches.
10. Use TypeScript throughout, a feature-based structure, Feather icons, theme tokens, and responsive touch targets (at least 48 dp).
11. ESLint must pass with no errors.
12. Include at least three meaningful Jest unit tests and/or Maestro E2E tests.
13. Include `AI_USAGE.md`, screenshots, architecture overview, setup instructions, Key decisions, and a narrated demo video no longer than three minutes.

## Proposed implementation stack

- React Native + TypeScript
- Expo is permitted by the assignment; React Native CLI is also permitted. Confirm the selected workflow and native-module compatibility before installing packages.
- React Navigation
- Redux Toolkit + RTK Query
- DummyJSON authentication
- REST Countries public API for country data
- `react-native-keychain` (or a compatible Expo-supported secure-storage solution) for secure token storage
- AsyncStorage or MMKV for non-sensitive persisted favourites
- Feather icons
- Jest; optionally Maestro

The assignment permits Expo or React Native CLI. This scaffold does not force either choice. See `docs/DECISIONS.md`.

## Important architecture boundary

**No custom application backend is required for the assignment phase.** The app consumes DummyJSON and the country API directly through a dedicated API/data layer. Local persistence is used for favourites. Do not add a Spring Boot server or PostgreSQL database to the required scope.

A future Spring Boot + PostgreSQL backend may be considered after the assignment is complete for cloud-synchronised trips, reviews, reactions, and multi-device accounts. Those are optional future extensions, not assignment requirements.

## Folder guide

```text
src/
  app/             app providers and root composition
  api/             RTK Query base API and API configuration
  features/
    auth/          login, registration, session handling
    countries/     country list, country details, search and filters
    favourites/    saved country management and persistence
  navigation/      typed navigators and route definitions
  components/      reusable UI components
  hooks/           shared hooks
  store/           Redux store and typed hooks
  services/        secure token and local persistence adapters
  theme/           colours, spacing, typography
  types/           shared domain and API types
  utils/           pure utility functions
```

See `docs/ARCHITECTURE.md` and `docs/FOLDER_STRUCTURE.md`.

## Project status

Track work in `TASKS.md`. Record significant technical decisions in `docs/DECISIONS.md`. Keep `AI_USAGE.md` accurate. Never mark a task complete just because an agent generated code; run the relevant checks and inspect the result.

## Getting started

This scaffold intentionally does not include a generated Expo/React Native native project or installed dependencies. First complete the setup decisions in `docs/ROADMAP.md`, then initialise the chosen React Native workflow and merge its generated files into this structure.

Suggested initial repository setup:

```bash
git init
git add .
git commit -m "chore: add Pocket Passport project plan and scaffold"
```

## API and security notes

- DummyJSON is the assignment-specified authentication service. Treat its sample/demo nature as an assignment constraint, not production identity infrastructure.
- The country API is public and does not require a custom backend for basic country browsing.
- Only request country fields needed by each screen where the chosen API endpoint supports field selection.
- Never place secrets in the repository.
- Do not log passwords, access tokens, or refresh tokens.
- Favourites are non-sensitive app data; auth tokens are sensitive credentials and require secure storage.

## Deliverables checklist

- [ ] Public GitHub repository
- [ ] `README.md` with setup, screenshots, architecture, state-management choice, and at least three Key decisions
- [ ] `AI_USAGE.md`
- [ ] Screenshots: Login, Home, Details, Favourites, Smart Search
- [ ] Demo video (≤ 3 minutes): app flow (~1 minute) and narrated code walkthrough (~2 minutes)
- [ ] Optional release APK

## Source of requirements

The assignment PDF supplied by the user: `IN3210_Assignment_2_React_Native.pdf` (3 pages). The requirements in this README are transcribed and organised from that document. If this README and the assignment PDF ever conflict, follow the assignment PDF and update this document.
