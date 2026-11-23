# API Notes

## 1. Authentication – DummyJSON

The assignment specifies DummyJSON for authentication. Registration can be simulated with `POST /users/add`, then the user is redirected to Login.

Before implementation:
- Check the current DummyJSON auth documentation and endpoint paths.
- Confirm request/response fields against the live docs.
- Do not assume simulated registration creates a real account that can authenticate unless the API documentation confirms it.
- Keep demo credentials out of source control.
- Store returned auth token securely (Keychain/Keystore).
- Never persist auth tokens in AsyncStorage or MMKV.

## 2. Country data – REST Countries

Use a public REST Countries API for country data. Verify the current official API documentation and chosen API version before coding; do not blindly rely on old endpoint examples.

Likely app data needs:

### Home summary
- Country common name
- Flag image / emoji
- Capital (may be absent)
- Region
- Population
- Stable country code for navigation and favourites

### Details
- Common and official names
- Flag and coat of arms if available
- Capital and capital coordinates if available
- Region and subregion
- Population
- Area
- Currencies
- Languages
- Time zones
- Borders
- Maps link if provided

Not all countries necessarily have every field. Model optional fields accurately and render graceful fallbacks.

## 3. Avoid overfetching

- Request only fields required for the country list when the chosen endpoint supports field selection.
- Fetch detail data by country identifier/code when the Details screen opens.
- Use RTK Query caching to avoid unnecessary repeated requests.
- Do not make one request per card if one list endpoint can supply the summary fields.

## 4. Avoid underfetching

- List all data required by each screen before defining endpoint field selections.
- Verify Details screen fields against actual API responses.
- If a field is absent for a country, handle it as unavailable rather than assuming the API is broken.

## 5. Smart Search

The assignment twist requires debounced search plus filter chips and an empty state. Decide whether search operates on the already-loaded country list or uses a country API search endpoint. Either way, ensure work is not triggered on every keystroke. Region filtering can usually be applied to loaded data if the full country list is already cached.

## 6. API error handling

Handle:
- Network unavailable
- Non-success HTTP response
- Invalid/unexpected response shape
- Missing optional country fields
- Empty result
- Retry action

## Reference links

- DummyJSON: https://dummyjson.com/docs/auth
- REST Countries: https://restcountries.com/
