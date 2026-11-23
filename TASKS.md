# Task Tracker

Update this file as work progresses. A task is complete only after implementation and verification.

Status key: `[ ]` not started · `[-]` in progress · `[x]` implemented and verified · `[!]` blocked

## 0. Project setup
- [ ] Decide Expo vs React Native CLI and record why
- [ ] Initialise React Native + TypeScript project
- [ ] Add lint, formatting, and TypeScript configuration
- [ ] Add navigation dependencies compatible with chosen workflow
- [ ] Add Redux Toolkit and RTK Query
- [ ] Add Feather icon package compatible with chosen workflow
- [ ] Create feature-based source folders
- [ ] Verify clean initial app build/run

## 1. App foundation
- [ ] Create app theme tokens (colours, spacing, typography)
- [ ] Create reusable loading, error, empty-state components
- [ ] Configure Redux store and typed hooks
- [ ] Configure RTK Query base API
- [ ] Add app providers and root entry point
- [ ] Add ESLint scripts and verify no errors

## 2. Authentication
- [ ] Build Login screen
- [ ] Build Register screen
- [ ] Add form validation and clear field-level errors
- [ ] Integrate DummyJSON login endpoint
- [ ] Implement simulated registration via DummyJSON users/add
- [ ] Add secure token storage (Keychain/Keystore)
- [ ] Restore session securely on app launch
- [ ] Implement logout and clear secure session
- [ ] Show authenticated user's name in header/profile
- [ ] Test invalid credentials and validation cases

## 3. Navigation
- [ ] Create typed root navigation params
- [ ] Create separate unauthenticated/authenticated flows
- [ ] Create Home → Details stack
- [ ] Create bottom tabs with Home and Favourites at minimum
- [ ] Verify Details route passes country ID/code only

## 4. Country API
- [ ] Verify current official REST Countries API documentation and endpoint/version
- [ ] Define CountrySummary and CountryDetails TypeScript types from actual response
- [ ] Create country API endpoints
- [ ] Fetch only required summary fields for Home where supported
- [ ] Fetch country details by identifier/code on Details screen
- [ ] Add loading, error + retry, and empty states
- [ ] Handle missing optional fields safely
- [ ] Add API response mapping/normalisation if needed

## 5. Home and Details UI
- [ ] Build country card component
- [ ] Build Home country list
- [ ] Show flag, name, capital/region or other selected summary fields
- [ ] Build Country Details screen
- [ ] Display available details without assuming every country has every field
- [ ] Add favourite toggle on Details screen
- [ ] Check responsive layout and 48 dp touch targets

## 6. Smart Search – assigned twist
- [ ] Implement debounced search input
- [ ] Ensure filter/API work is not triggered on every keystroke
- [ ] Add region filter chips
- [ ] Combine text search and selected region correctly
- [ ] Add clear empty state for no matches
- [ ] Add clear/reset search and filter behaviour
- [ ] Test debounce and filter logic

## 7. Favourites and persistence
- [ ] Choose AsyncStorage or MMKV for non-sensitive favourites
- [ ] Implement favourites storage adapter
- [ ] Add/remove favourites from list and Details
- [ ] Build Favourites tab
- [ ] Restore favourites after app restart
- [ ] Handle duplicate entries and storage errors

## 8. Testing and quality
- [ ] Add test for form validation
- [ ] Add test for Smart Search debounce/filter utility
- [ ] Add test for favourites reducer/storage logic
- [ ] Add additional meaningful tests as appropriate
- [ ] Run Jest suite
- [ ] Run ESLint with no errors
- [ ] Run TypeScript check
- [ ] Verify app on at least one emulator/device
- [ ] Check loading, error, retry, empty, and persistence flows

## 9. Documentation and submission
- [ ] Complete README setup instructions
- [ ] Add architecture overview
- [ ] Add at least three Key decisions in README
- [ ] Add screenshots: Login, Home, Details, Favourites, Smart Search
- [ ] Complete AI_USAGE.md honestly
- [ ] Review Git history for feature-based commits
- [ ] Record demo script and technical walkthrough
- [ ] Record demo video (maximum 3 minutes)
- [ ] Verify public GitHub repository
- [ ] Final check against assignment PDF
- [ ] Submit before 13 December 2026, 11:59 PM

## Optional future extensions – not assignment requirements
- [ ] Travel wishlist / planned / in-progress / visited status
- [ ] Personal travel journal and photos
- [ ] Trip planner
- [ ] Travel budget tracker
- [ ] World travel map
- [ ] Community likes/dislikes/reviews with a real backend
- [ ] Spring Boot + PostgreSQL backend and account-based cloud sync
