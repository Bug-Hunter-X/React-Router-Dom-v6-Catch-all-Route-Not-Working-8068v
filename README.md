# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router Dom v6.  The catch-all route is intended to handle any invalid routes and display a 404 page. However, in this example, the catch-all route is not working correctly, even when navigating to an invalid URL. 

## Problem:

The `NotFound` component is not rendering when a non-existent route is accessed.  This is due to how React Router handles route matching, particularly with the order of routes and the catch-all route's placement.

## Solution:

The solution involves ensuring the catch-all route (`/*`) is placed as the *last* route within the `Routes` component. By placing it last, React Router will only reach this route after it has checked all other, more specific routes. 