# Stale Location Data in React Router v6

This repository demonstrates a common issue encountered when using React Router v6: accessing the `location` object outside of the route's children.  The example shows how directly accessing `location` results in stale data and how using the `useLocation` hook within the route's children provides the correct behavior.  The solution focuses on proper utilization of the `useLocation` hook within the correct routing context to access the current location state consistently.

## Problem

When the location object is accessed outside of the `children` in a route, it doesn't always reflect the current URL.  This leads to unexpected rendering or data fetching based on an outdated location state.

## Solution

The solution involves restructuring the component to correctly utilize the `useLocation` hook within the route's children or leveraging the `useParams` and `useSearchParams` hook to obtain the required data directly.