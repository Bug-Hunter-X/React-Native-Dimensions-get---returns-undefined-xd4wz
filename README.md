# React Native Dimensions.get() returns undefined

This repository demonstrates a common error in React Native where `Dimensions.get('window')` or `Dimensions.get('screen')` unexpectedly returns `undefined`, causing runtime crashes.  The solution uses the `useEffect` hook and `Dimensions.addEventListener` to ensure dimensions are available before accessing them.

## Bug
The main bug is a direct use of `Dimensions.get()` without handling the case of it returning `undefined`. This is unreliable, especially during the application's initial rendering phase.

## Solution
The solution utilizes `useEffect` and `Dimensions.addEventListener` for more reliable dimension retrieval.  This ensures that the dimensions are available before being used within the component. 