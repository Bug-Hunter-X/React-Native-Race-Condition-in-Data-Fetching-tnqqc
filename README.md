# React Native Race Condition in Data Fetching

This repository demonstrates a common race condition in React Native applications involving asynchronous data fetching. The issue arises when a component unmounts before an asynchronous operation (in this case, a `fetch` call) completes. This results in the application trying to update the state of an already unmounted component, leading to errors and warnings.

The example shows an attempt to mitigate the problem using the deprecated `isMounted` method, which is unreliable.  The solution illustrates a more robust approach using a cleanup function and the `useEffect` hook.