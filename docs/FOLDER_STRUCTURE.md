# Folder Structure

Proposed application structure after initialising Expo or React Native CLI:

```text
pocket-passport/
├── assets/
│   ├── fonts/
│   ├── images/
│   └── screenshots/
├── docs/
├── src/
│   ├── app/
│   │   ├── AppProviders.tsx
│   │   └── RootNavigator.tsx
│   ├── api/
│   │   ├── baseApi.ts
│   │   └── apiTags.ts
│   ├── components/
│   │   ├── CountryCard/
│   │   ├── EmptyState/
│   │   ├── ErrorState/
│   │   ├── LoadingState/
│   │   └── SearchBar/
│   ├── features/
│   │   ├── auth/
│   │   │   ├── api/
│   │   │   ├── components/
│   │   │   ├── hooks/
│   │   │   ├── screens/
│   │   │   ├── types/
│   │   │   └── validation/
│   │   ├── countries/
│   │   │   ├── api/
│   │   │   ├── components/
│   │   │   ├── hooks/
│   │   │   ├── screens/
│   │   │   ├── types/
│   │   │   └── utils/
│   │   └── favourites/
│   │       ├── components/
│   │       ├── screens/
│   │       ├── state/
│   │       └── storage/
│   ├── navigation/
│   │   ├── types.ts
│   │   ├── AuthNavigator.tsx
│   │   ├── MainTabNavigator.tsx
│   │   └── CountriesNavigator.tsx
│   ├── services/
│   │   ├── secureTokenStorage.ts
│   │   └── favouritesStorage.ts
│   ├── store/
│   │   ├── index.ts
│   │   └── hooks.ts
│   ├── theme/
│   │   ├── colors.ts
│   │   ├── spacing.ts
│   │   ├── typography.ts
│   │   └── index.ts
│   ├── types/
│   └── utils/
├── __tests__/
├── .env.example
├── .gitignore
├── AGENTS.md
├── AI_USAGE.md
├── README.md
├── PROJECT_CONTEXT.md
└── TASKS.md
```

This is a target structure, not a claim that these files have already been implemented. Adapt file names to the selected Expo/React Native setup while preserving feature boundaries.
