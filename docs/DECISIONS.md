# Architecture Decision Log

Record date, context, decision, alternatives, and consequences for each meaningful decision.

## D-001 – No custom backend in assignment MVP
- Status: Accepted
- Context: Assignment specifies DummyJSON for authentication and a public API for discovery. It does not require a custom backend.
- Decision: Consume external APIs directly from the mobile app through a dedicated API layer. Persist favourites locally.
- Consequence: Less infrastructure and time spent; no cross-device sync or shared community data.
- Future: A separate backend may be added after assignment delivery.

## D-002 – Redux Toolkit for state management
- Status: Proposed
- Context: Redux Toolkit with RTK Query, thunks, or Redux-Saga is explicitly required.
- Decision: Prefer RTK Query for remote API data and caching; use a small slice for client-owned favourites/session UI state where appropriate.
- Consequence: Centralised request lifecycle and cache; explain final implementation in README.

## D-003 – Secure token storage
- Status: Required
- Context: Assignment forbids AsyncStorage/MMKV for auth tokens.
- Decision: Use Keychain/Keystore-backed secure storage compatible with chosen workflow.
- Consequence: Verify native-module compatibility and test session clearing.

## D-004 – Local favourites persistence
- Status: Proposed
- Context: Favourites must persist across restarts.
- Decision: Use AsyncStorage or MMKV for favourite country identifiers, not auth credentials.
- Consequence: Favourites are device-local in the assignment version.

## D-005 – Country API version and fields
- Status: Pending verification
- Context: Assignment names REST Countries but does not prescribe a specific version or field list.
- Decision: Verify official docs at implementation time; request list summary fields separately from detail fields where supported.
- Consequence: Avoid overfetching while ensuring Details has all required information.

## D-006 – Expo vs React Native CLI
- Status: Pending
- Context: Assignment recommends React Native CLI but explicitly permits Expo.
- Decision: Select after checking developer environment and secure-storage/native dependency compatibility.
- Consequence: Record final choice and rationale here.
