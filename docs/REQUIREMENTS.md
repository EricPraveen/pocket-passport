# Requirements Traceability

| ID | Requirement | Source | Planned implementation | Verification |
|---|---|---|---|---|
| R01 | React Native discovery app | Assignment objective | React Native app | App builds and runs |
| R02 | Sign in | Core requirement | DummyJSON login | Successful/failed login tests |
| R03 | Registration with validation | Core requirement | Validated form; simulated DummyJSON registration | Validation tests |
| R04 | Secure auth token storage | Core requirement | Keychain/Keystore | Inspect storage implementation; no token in AsyncStorage/MMKV |
| R05 | Separate auth flow | Navigation | Typed auth navigator | Manual navigation test |
| R06 | Bottom tabs: Home and Favourites | Navigation | Bottom tab navigator | Manual navigation test |
| R07 | Home → Details stack | Navigation | Typed stack | Details receives ID/code only |
| R08 | Country list from public API | Home screen | Country API endpoint | API integration test/manual check |
| R09 | Loading, error/retry, empty states | Home screen | Reusable state components | Test each state |
| R10 | Details fetches its own data by ID | Details screen | Country detail endpoint | Verify route params and request |
| R11 | Favourite toggle in Details | Details screen | Favourite state | Add/remove test |
| R12 | Redux Toolkit async state management | State management | RTK Query preferred | README decision and tests |
| R13 | Favourites persist across restarts | Favourites | AsyncStorage/MMKV | Restart persistence test |
| R14 | Theme tokens and Feather icons | Styling | Theme + Feather | UI review |
| R15 | Responsive and touch targets ≥48 dp | Styling | Responsive layouts | Device review |
| R16 | TypeScript throughout | Code quality | TypeScript | `tsc --noEmit` |
| R17 | Feature-based structure | Code quality | `src/features/*` | Structure review |
| R18 | ESLint no errors | Code quality | ESLint | lint command |
| R19 | At least 3 meaningful tests | Testing | Jest and/or Maestro | Test report |
| R20 | Debounced search | Twist for index 234163 | Debounce utility/hook | Unit test: no early filtering/request |
| R21 | Filter chips | Twist | Region chips | UI/logic test |
| R22 | Empty state when no matches | Twist | Empty-state component | UI test/manual check |
| R23 | README and AI_USAGE | Deliverables | Root Markdown files | Submission review |
| R24 | Demo video ≤3 min | Deliverables | Narrated demo | Duration and content review |

## Assignment mapping
- Index: `234163`
- Last digit `3`: Travel & Countries
- Second-last digit `6`: Smart Search
