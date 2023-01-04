
# Context API 

# What is global state with React?
  - In React, originally, the state is held and modified within the same React component. In most applications, different components may need to access and update the same state. This is achieved by introducing the global states in your app. The main purpose of the global state is to share a state among multiple components. There are three ways this communication can happen:
    1. With a child component
    2. With a parent component
    3. With a sibling component
    
    
## State traveling down
  - State traveling down through the hierarchy is best managed using the mutable state at the highest level to determine immutable properties that define the lower-level components. Even when these properties are updated, the lower-level component is updated rather than fully recreated.

## State traveling up
  - You need to pass down a callback function for a higher-level component to know the state. In the following version, we add a global state to count the total number of button presses and update this state with a callback function called pushed, which is called whenever a button is pushed.
## State traveling sideways
  - Various sub-components need to communicate updates between them. This can be achieved by passing state, using callback, up to a common parent component, and then passing it back down.

## Context API in React
  - The Context API is a way to share data across a tree of React components without having to pass props down manually at every level. It is particularly useful when you have data that you want to make available to a large part of your component tree, such as a authenticated user or a theme.
  - To use the Context API in a React application, you first need to create a Context object using the createContext function. This function takes an optional default value as an argument, which will be used as the value of the context if a matching provider is not found higher up the tree.
  - Next, you will need to create a provider component that wraps the part of the tree that you want to provide the context value to. The provider component should render a Context.Provider element and pass the value for the context as the value prop.
  - To access the context value from a component, you can use the useContext hook. The useContext hook takes a Context object as an argument and returns the current context value.
  - By using the Context API, you can avoid having to pass props down through multiple levels of the component tree, which can make your code easier to read and maintain


## Comparing Redux & Context API
 ## Context API	
  - Built-in tool that ships with React	
  - Requires minimal Setup	
  - Specifically designed for static data, that is not often refreshed or updated	
  - Adding new contexts requires creation from scratch	
  - Debugging can be hard in highly nested React Component Structure even with Dev Tool	
  - UI logic and State Management Logic are in the same component	

 ## Redux
  - Additional installation Required, driving up the final bundle size
  - Requires extensive setup to integrate it with a React Application
  - Works like a charm with both static and dynamic data
  - Easily extendible due to the ease of adding new data/actions after the initial setup
  - Incredibly powerful Redux Dev Tools to ease debugging
  - Better code organization with separate UI logic and State Management Logic
