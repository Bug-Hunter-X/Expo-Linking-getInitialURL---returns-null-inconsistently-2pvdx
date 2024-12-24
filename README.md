# Expo Linking.getInitialURL() Inconsistency Bug

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where the method inconsistently returns `null`, even when a deep link successfully launched the app. This makes it difficult to reliably handle deep links.

## Bug Description
The `Linking.getInitialURL()` method is used to retrieve the initial URL that launched the application. However, in certain scenarios, even with a valid deep link, it returns `null`, causing unexpected application behavior. The inconsistency makes it challenging to build reliable deep link handling logic.

## Reproduction Steps
1. Clone this repository.
2. Run the app using `expo start`.
3. Open a deep link to launch the application (the specific deep link may need to be adapted based on your configuration).
4. Observe the console output - `Linking.getInitialURL()` might return `null` inconsistently.

## Solution
The provided solution implements a workaround to mitigate the issue by adding a delay and multiple attempts to retrieve the URL. This doesn't resolve the underlying issue within the Expo Linking API, but it provides a more robust solution for handling deep links in practice.