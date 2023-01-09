# Data Fetching
## What is SWR?
  - SWR stands for stale-while-revalidate, a HTTP cache invalidation strategy popularized by HTTP RFC 5861. It basically means that it performs data fetching in 3 steps:
    1. Returns cached data first (stale)
    2. Sends the fetch request (revalidate)
    3. Returns the up-to-date data


## Why use SWR?
  - 1. Built-in Cache + Real-Time Experience
    - When we use Fetch or Axios for data fetching in React, we usually need to show the user some loading message or spinner while data is being fetched. Using SWR’s strategy, the user sees the cached (stale) data first and requests are automatically being cached. Components will always be constantly updated with the most recent data, ensuring UI will always be fast and reactive.
  - 2. Auto Revalidation
    - SWR ensures that the user sees the most up-to-date data. So even with multiple tabs or windows, the data is always fresh and in sync when the window/tab is refocused.
    - Instead of just revalidating data on focus, SWR can also revalidate data on interval, to make sure multiple sessions will render the same components based on the data.Finally, there’s revalidation on reconnect. In the event the user disconnects from the internet, SWR will automatically revalidates data once the user is online again.

  - 3. Pagination 
    - One of the most useful features of SWR is that it supports pagination and infinite loading of data.
    - Instead of having to write your own logic with Fetch or Axios to paginate data or create an infinite loading UI for your app, SWR provides a simple Hook called useSWRInfinite to handle this for you.

  - 4. More Features + Benefits of SWR
    - There are many more reasons why you should use SWR in your React apps. Some of them are:
    1. Local mutation
    2. Dependent fetching
    3. Smart error retry
    4. Supports fetching from both REST and GraphQL APIs
    5. Typescript and React Native ready


