# Project Context – Pocket Passport

## One-sentence description

Pocket Passport is a React Native mobile discovery app where users authenticate, browse countries, view country details, save favourites, and use a debounced Smart Search with region filter chips.

## User's assignment mapping

Index number: **234163**

| Index digit | Value | Assignment mapping |
|---|---:|---|
| Last digit | 3 | Travel & Countries domain |
| Second-last digit | 6 | Smart Search twist |

The domain and twist are selected independently using the last and second-last digits respectively.

## Product goals

- Make country discovery easy and visually clear.
- Show a useful lightweight country summary in the Home list.
- Load detailed country information on the Details screen.
- Let users save and revisit favourite countries.
- Make country discovery efficient through debounced search and region filters.
- Demonstrate sound mobile engineering: navigation, state management, API integration, persistence, validation, testing, and maintainable structure.

## Core user journeys

### Authentication
1. User opens app.
2. User chooses Login or Register.
3. Inputs are validated.
4. Login calls DummyJSON.
5. Successful session token is stored securely.
6. User enters the authenticated app.
7. User can log out; secure session is cleared.

Registration is allowed to be simulated using DummyJSON `POST /users/add`, then redirecting the user to Login, as described by the assignment.

### Country discovery
1. Home loads countries from the selected public country API.
2. Cards show a small set of fields (for example flag, common name, capital, region).
3. Loading, error/retry, and empty states are visible.
4. User taps a card.
5. Details screen receives only the country identifier/code and fetches its own country data.

### Smart Search
1. User types a country name.
2. Search waits for a debounce interval before filtering or requesting.
3. User can select a region filter chip.
4. Search and region filter work together.
5. If there are no matches, a clear empty state is displayed.

### Favourites
1. User toggles a favourite from a country card or details screen.
2. The Favourites tab shows saved countries.
3. Favourite state persists after app restart.

## Data ownership

| Data | Source / persistence |
|---|---|
| Country names, flags, capitals, population, region, etc. | Public country API |
| Login response and demo auth token | DummyJSON |
| Auth token | Secure Keychain/Keystore storage |
| Favourites | Local AsyncStorage or MMKV |
| Search text and selected region | UI/client state |
| Optional travel journal/trip ideas | Not in mandatory assignment scope |

## Explicitly out of scope for assignment phase

- Custom backend server
- PostgreSQL database
- Cloud synchronisation
- Community likes/dislikes
- Public user reviews and ratings
- Social feed
- Real booking/payment functionality

These can be considered after assignment delivery as a separate product extension. Do not implement them ahead of mandatory marks.

## Quality principles

- Prefer simple, testable functions.
- Keep network calls out of screen components.
- Keep API response types explicit.
- Keep secure credentials separate from ordinary app data.
- Provide accessible touch targets and readable states.
- Document any deviation from the assignment.
