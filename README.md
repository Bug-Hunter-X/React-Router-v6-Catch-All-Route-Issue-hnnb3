# React Router v6 Catch-All Route Unexpected Behavior

This repository demonstrates an issue with the catch-all route (`/*`) in React Router v6.  The catch-all route is unexpectedly triggered even when other routes match, leading to incorrect rendering.

## Problem

The provided code shows a simple React Router setup. Despite having specific routes defined (`/` and `/about`), the catch-all route (`/*`) is always activated. This means the 404 page renders instead of the Home or About component.  This contradicts the expected behavior where the catch-all should only be used if no other route matches.

## Solution

The issue stems from the order of routes.  Catch-all routes (`/*`) should always be placed last in the `Routes` component.  By reordering the routes, the specific routes are correctly matched before the catch-all is considered. 

## Setup

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
