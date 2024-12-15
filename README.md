# React Native FlatList Empty List Bug

This repository demonstrates a common issue in React Native where a FlatList component fails to render data fetched asynchronously using the `useEffect` hook.  The list remains empty even though the data is successfully retrieved.

## Problem

The `DataList` component fetches data from a remote API.  Although the API call is successful and the data array is populated, the FlatList component doesn't re-render to display the data. This issue frequently arises when data is fetched asynchronously and the component state updates don't properly trigger re-rendering of the FlatList. 

## Solution

The solution involves ensuring that the FlatList component is re-rendered after receiving the updated data. We can achieve this with React's state management and the correct use of useEffect's dependency array.