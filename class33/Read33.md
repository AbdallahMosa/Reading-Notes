# Next- Forms and Conditional Rendering 

## Custom Hooks :
  - custom hook is a JavaScript function that starts with the word "use" and that may call other hooks. Custom hooks allow you to extract component logic into reusable functions. They can make your code more organized and easier to understand. You can use custom hooks to share logic between multiple components or to abstract complex logic into a single function. To create a custom hook, you can use the useState, useEffect, and other built-in hooks in a function. You can then call this function from any functional component in your application.


## Lifting State Up :
  - lifting state up refers to the process of moving shared state from a child component to a parent component. This is often necessary when you have two or more components that need to access the same state data, but the state is owned by only one of the components.
  - To lift state up in Next.js, you can follow these steps:
    - Identify the state that you want to lift up. This state should be owned by a child component that needs to share it with other components.
    - Create a new state variable in the parent component. This will be the shared state that the child components will access.
    - Pass the state variable and a setter function for it as props to the child components that need to access the state
    - In the child components, use the state and setter function from the props instead of the local state.

  - By lifting state up to the parent component, you can ensure that all components that need to access the shared state are always in sync and that the state is managed in a single, centralized location. This can make your code easier to understand and debug.

## Memoization in React
  - Memoization is a technique for optimizing the performance of a function by storing the results of its previous invocations and returning the cached result when the same input is provided again. This can be particularly useful in React when you have a component that is expensive to render, such as a component that generates a complex UI or performs a lot of calculations.
  - To use memoization in a React component, you can use the useMemo hook. The useMemo hook takes a function and an array of dependencies as arguments, and it will only recompute the memoized value when one of the dependencies changes.

  
  
      ``` 
      import { useMemo } from 'react';

      function MyComponent(props) {
        const expensiveValue = useMemo(() => {
          // This function will only be called if one of the dependencies has changed.
          return computeExpensiveValue(props.a, props.b);
        }, [props.a, props.b]);

        return <div>{expensiveValue}</div>;
      }

     
      ```
 - By using the useMemo hook, you can ensure that the computeExpensiveValue function is only called when one of its dependencies changes, which can improve the performance of your component.
