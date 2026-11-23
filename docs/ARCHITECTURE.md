# Architecture

## High-level design

```text
React Native UI
  ├── Authentication screens
  ├── Home / Country list
  ├── Country Details
  └── Favourites
        |
        v
Navigation (typed routes)
        |
        v
Feature hooks / RTK Query hooks
        |
        v
Redux Toolkit store
  ├── RTK Query API cache
  └── Client feature state
        |
        +--------------------+
        |                    |
        v                    v
DummyJSON API          Country public API
(auth only)            (country information)

Local persistence adapters
  ├── Secure token storage: Keychain/Keystore
  └── Favourites: AsyncStorage or MMKV
```

## Architectural rules

- Screens render state and compose components; they should not contain raw fetch logic.
- API definitions live in the API/data layer.
- RTK Query owns server response caching and request lifecycle.
- Redux slices are for client-owned state not better represented by RTK Query.
- Secure token storage is separate from favourites persistence.
- Country Details receives a stable identifier (prefer a country code) and fetches its own details.
- Search and filter logic should be isolated and testable.
- Avoid duplicating the same country dataset in multiple stores.

## Suggested state ownership

| State | Owner |
|---|---|
| Country API results/cache | RTK Query |
| Auth request lifecycle | RTK Query or auth thunk |
| Auth token | Secure storage + minimal session state |
| Favourite country codes | Redux slice + persistence adapter |
| Search text | Local screen state |
| Debounced search term | Hook/local derived state |
| Selected region chip | Local screen state |

## Future backend boundary

A later backend can replace local travel data persistence or add social features. Keep repository interfaces/adapters separate so UI components do not depend directly on storage implementation. This is a future extension only; no custom backend is needed for the assignment.
