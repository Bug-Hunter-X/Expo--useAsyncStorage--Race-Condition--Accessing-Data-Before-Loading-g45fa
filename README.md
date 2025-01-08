# Expo `useAsyncStorage` Race Condition: Accessing Data Before Loading

This repository demonstrates a common, yet subtle, bug when using Expo's `useAsyncStorage` hook. The issue arises from attempting to access AsyncStorage data before the asynchronous operation of fetching that data completes.  This often results in undefined or null values being displayed or used in calculations, leading to unexpected application behavior.

The `bug.js` file showcases the problematic code. The solution, presented in `bugSolution.js`, addresses this race condition by correctly handling the loading state and providing feedback to the user until data is available.

## How to Reproduce

1. Clone this repository.
2. `npm install`
3. Run the app using Expo Go or a similar Expo client.
4. Observe the initial display and the transition after data is loaded from AsyncStorage.

The provided solution employs the appropriate `useEffect` hook and checks the loading `status` before using the retrieved value.