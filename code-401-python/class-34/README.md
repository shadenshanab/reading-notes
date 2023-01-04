# class 34

## Context API

--------------

## Global State


### Role of the global state

In React, originally, the state is held and modified within the same React component. In most applications, different components may need to access and update the same state. This is achieved by introducing the global states in your app. The main purpose of the global state is to share a state among multiple components.

There are three ways this communication can happen:

1. With a child component
2. With a parent component
3. With a sibling component

### State traveling down

State traveling down through the hierarchy is best managed using the mutable state at the highest level to determine immutable properties that define the lower-level components. Even when these properties are updated, the lower-level component is updated rather than fully recreated.

As a result, the state tracked by the lower-level component will persist unless the component disappears (as could happen with conditional rendering). The following is how the change in a higher-level component is reflected in the lower-level components.

### State traveling up

You need to pass down a callback function for a higher-level component to know the state. In the following version, we add a global state to count the total number of button presses and update this state with a callback function called pushed, which is called whenever a button is pushed.

Notice that the pushed App method is passed as a property (prop) to the Clock component, accessed as this.prop.callback. A new final line, number 18, in alterOffset calls it with this.props.callback().

### State traveling sideways

Various sub-components need to communicate updates between them. This can be achieved by passing state, using callback, up to a common parent component, and then passing it back down.

--------------

## context API

Context is a way to pass data through the component tree without having to pass props down manually at every level. It is designed to share data that is considered "global" for a tree of React components, such as the currently authenticated user, the theme, or the preferred language.

Here are some tips on when to use context:

- You should use context when you have data that is deeply nested in your component tree and you want to avoid the overhead of prop drilling. Prop drilling can get cumbersome when you have a deeply nested component structure and you need to pass props down through multiple levels just to reach a leaf component that needs the data.
- You should use context when you have data that needs to be accessed by multiple components at different nesting levels, and you don't want to lift the state up to the common ancestor of those components.
- You should use context when you have a small amount of data that changes frequently, and you want to avoid re-rendering all the components that depend on that data.

Before you use context, you should consider whether it is the best solution for your use case. Here are some things to consider:

- Context can make your code more difficult to understand because it introduces a layer of indirection. It can be hard to tell where the data comes from and how it is being used.
- Context can make your code more fragile because it relies on the component tree structure to pass data. If you change the component tree structure, it can break the data flow and cause bugs.
- Context can cause performance issues if you use it to pass a large amount of data or if you use it to pass data that changes frequently. This is because it will trigger a re-render of all the components that depend on the context data, even if the data has not actually changed.

Now let's look at the API for context in React.

The `React.createContext` function is used to create a context object. It takes an optional default value as an argument, which will be used if a component does not have a matching `Provider` above it in the tree.

```

const MyContext = React.createContext('default value');

```


The `Context.Provider` component is used to provide a value for the context. It takes a `value` prop, which can be any type of data. The `Provider` should be placed higher up in the component tree, above the components that need access to the context data.

```
<MyContext.Provider value={'some value'}>
    <MyComponent />
</MyContext.Provider>

```

To consume the context data, you can use the `useContext` hook in a functional component, or you can use the `static contextType` property in a class component.

```
function MyComponent() {
  const value = useContext(MyContext);
  return <p>{value}</p>;
}

class MyClassComponent extends React.Component {
  static contextType = MyContext;
  render() {
    return <p>{this.context}</p>;
  }
}
```

Context can be a useful tool in React, but it should be used with caution because it can make your code harder to understand and maintain. It is best suited for sharing small amounts of frequently changing data that needs to be accessed by multiple components at different nesting levels.

