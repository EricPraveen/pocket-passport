# Implementation Roadmap

## Stage 0 – Confirm environment
1. Decide Expo or React Native CLI.
2. Check local Node, package manager, Android/iOS tooling.
3. Confirm secure-storage package compatibility with the selected workflow.
4. Initialise TypeScript project.
5. Run the starter app.

## Stage 1 – Foundation
1. Install navigation and Redux dependencies.
2. Create typed store and API base.
3. Create theme tokens and shared state components.
4. Configure lint, typecheck, and Jest.

## Stage 2 – Authentication
1. Build login and registration UI.
2. Add validation.
3. Integrate DummyJSON.
4. Add secure token storage.
5. Implement session restoration and logout.

## Stage 3 – Navigation
1. Add auth flow.
2. Add authenticated bottom tabs.
3. Add Home → Details stack with typed country code param.

## Stage 4 – Countries
1. Verify selected country API version and endpoint docs.
2. Define API response types.
3. Build Home list with summary fields.
4. Add loading/error/retry/empty states.
5. Build Details screen that fetches by code.

## Stage 5 – Smart Search
1. Implement debounce utility/hook.
2. Add search input.
3. Add region filter chips.
4. Combine search + filter.
5. Add empty state.
6. Write tests for debounce and filtering.

## Stage 6 – Favourites
1. Implement favourite state.
2. Add persistence adapter.
3. Add toggle to card/details as appropriate.
4. Build Favourites tab.
5. Test persistence after restart.

## Stage 7 – Quality
1. Add at least three meaningful tests.
2. Run lint/typecheck/tests.
3. Test on device/emulator.
4. Fix edge cases and accessibility/touch targets.

## Stage 8 – Submission
1. Capture required screenshots.
2. Complete README and AI_USAGE.
3. Review feature-based Git history.
4. Record narrated demo under 3 minutes.
5. Check all assignment requirements.
