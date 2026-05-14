# Limrun Detox Expo Sample

This is a small Expo Go app built for the Limrun Detox example. It exposes stable
React Native `testID`s so Detox can drive a visible end-to-end flow on a Limrun
remote iOS simulator.

## Run With Expo Go

```bash
npm install
npm run tunnel
```

Copy the `exp://` tunnel URL from Expo CLI and use it as `EXPO_URL` in
`typescript-sdk/examples/detox-ios`.

Tunnel support is included through the local `@expo/ngrok` dev dependency.

## Detox Test Contract

The Limrun example expects these stable selectors:

- `demo-home-screen`
- `demo-home-title`
- `demo-counter-value`
- `demo-increment-button`
- `demo-decrement-button`
- `demo-name-input`
- `demo-submit-name-button`
- `demo-greeting-message`
- `demo-open-detail-button`
- `demo-detail-screen`
- `demo-automation-switch`
- `demo-complete-task-button`
- `demo-success-message`
- `demo-reset-button`

It also asserts the visible text `Limrun Detox Demo` and `Hello, Limrun!`.

The app intentionally avoids custom native modules so it can run inside Expo Go.
