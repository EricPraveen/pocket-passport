# Test Plan

Minimum assignment target: at least three meaningful tests using Jest and/or Maestro.

## Suggested unit tests

1. **Authentication validation**
   - Empty username/password rejected.
   - Invalid input produces useful validation errors.
   - Valid input passes.

2. **Smart Search**
   - Search is case-insensitive.
   - Search matches expected country names.
   - Region chip filters the list.
   - Search and region filters combine correctly.
   - Empty result is represented correctly.
   - Debounce does not invoke work before the configured delay.

3. **Favourites**
   - Add a country once.
   - Adding the same country twice does not create duplicates.
   - Remove a favourite.
   - Persisted country codes restore correctly.

## Suggested integration / E2E checks

- Login success and failure.
- Auth flow redirects to Home after success.
- Home loads countries and handles retry.
- Details fetches using country code route param.
- Favourite survives app restart.
- Logout clears secure token.
- Smart Search filter chips and empty state work on device.

## Test evidence

Record command, environment, date, and pass/fail result in `docs/PROGRESS.md`.
