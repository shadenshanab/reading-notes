# class 33

## Next- Forms and Conditional Rendering 

--------------

## Custom Hooks

In React, a "hook" is a function that adds additional functionality to a functional component. Custom hooks are just like the built-in hooks in React, such as `useState` and `useEffect`, but they are user-defined functions that can abstract stateful logic and reuse it across multiple components.

Custom hooks allow you to extract component logic into reusable functions. This can make your code easier to understand, test, and maintain.

Here's an example of a custom hook that tracks the mouse position on the page:

```
import { useState, useEffect } from 'react';

function useMousePosition() {
  const [position, setPosition] = useState({ x: 0, y: 0 });

  useEffect(() => {
    const handleMouseMove = (event) => {
      setPosition({
        x: event.clientX,
        y: event.clientY
      });
    };

    document.addEventListener('mousemove', handleMouseMove);

    return () => {
      document.removeEventListener('mousemove', handleMouseMove);
    };
  }, []);

  return position;
}

export default useMousePosition;

}
```


To use this custom hook in a component, you can simply import it and call it like a regular function:

```

import useMousePosition from './useMousePosition';

function MyComponent() {
  const position = useMousePosition();

  return (
    <p>Mouse position: {position.x}, {position.y}</p>
  );
}
```

---------------------

## Lifting State Up

Lifting state up means moving the shared state from a child component to a parent component, so that the parent component can pass the state down to the child components that need it as props. This is a common pattern in React because it allows you to share state between components that are not directly related.

For example, suppose you have two components that need to reflect the same changing data:

```
function ChildA(props) {
  return <p>Data: {props.data}</p>;
}

function ChildB(props) {
  return <p>Data: {props.data}</p>;
}
```

Instead of storing the data state in both ChildA and ChildB, you can lift the state up to their closest common ancestor, which could be a parent component:

```
function Parent(props) {
  const [data, setData] = useState('initial data');

  return (
    <div>
      <ChildA data={data} />
      <ChildB data={data} />
    </div>
  );
}
```

Now, the Parent component is responsible for managing the data state, and it can pass the data down to the ChildA and ChildB components as props. This allows both child components to reflect the same changing data.

Lifting state up can make your code easier to understand and maintain because it allows you to centralize the management of shared state in a single place, rather than scattered throughout multiple components. It can also make your code more efficient because it avoids unnecessary prop drilling, where a prop is passed down through multiple levels of components just to reach a child component that needs it.

---------------------

## Memorization

### WHAT IS MEMOIZATION?

There are some times when re-rendering of the component results in performance issues. To overcome this, React provides us with a performance feature known as memoization.

Memoization is an optimization technique that allows an increase in the performance of a program by storing the results of some expensive function so that we don’t need to call that function when the same inputs are given.

### HOW TO IMPLEMENT MEMOIZATION IN REACT

React has the features PureComponent and memo hook which allow us to implement memoization in React.
PureComponent allows us to perform optimization. It depends on the shouldComponentUpdate() lifecycle method but it can only be used with the class component.
React also gives us a memo() hook to apply memoization for functional components.
If we need a function component that gives the same result for the same props and we don’t want to re-render it, we can use memoization to skip the re-render of the component by storing and reusing the last rendered result.

### MEMOIZATION USING PURECOMPONENT

PureComponent is similar to Components in React except that PureComponent implements shouldComponentUpdate() with shallow prop and state comparison and Components does not.
In some cases, if our component re-renders the same result with the same given props and state which results in performance issues, then we can use PureComponent to increase performance. PureComponent’s shouldComponentUpdate() only shallowly compares the object.
But we should make sure that props and state are simple. If they contain any complex data structures then PureComponent may produce wrong results. Also, we should make sure that all the children components of PureComponent are also PureComponent since PureComponent’s shouldComponentUpdate() skips prop updates for the full component subtree.
