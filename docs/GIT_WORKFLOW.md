# Git Workflow

Use small, feature-focused commits rather than one final bulk commit.

Suggested branch names:
- `chore/project-setup`
- `feat/auth-screens`
- `feat/dummyjson-auth`
- `feat/secure-session`
- `feat/navigation`
- `feat/countries-api`
- `feat/country-home`
- `feat/country-details`
- `feat/smart-search`
- `feat/favourites`
- `test/core-flows`
- `docs/submission`

Suggested commit messages:
- `chore: initialise React Native TypeScript app`
- `feat: add typed authentication navigation`
- `feat: integrate DummyJSON login`
- `feat: persist favourites locally`
- `feat: add debounced country search`
- `test: cover search and favourites logic`
- `docs: add setup and architecture guide`

Before each commit:
1. Review `git diff`.
2. Run relevant tests and lint.
3. Ensure no secrets or local environment files are staged.
4. Update task/progress documentation.
