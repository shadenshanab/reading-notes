# Class05 read

-----

# Thinking in React

## 1. What is the single responsibility principle and how does it apply to components?

### When a component should ideally only do one thing. If it grows, it should be broken down into smaller subcomponents

## 2. What does it mean to build a ‘static’ version of your application?

### it's when you create components that reuse other components and use props to pass data. it is a data that doesn't change with interactivity

## 3. Once you have a static application, what do you need to add?

### UI

## 4. What are the three questions you can ask to determine if something is state?

### 1. Is it passed in from a parent via props? If so, it probably isn’t state

### 2. Does it remain unchanged over time? If so, it probably isn’t state

### 3. Can you compute it based on any other state or props in your component? If so, it isn’t state

## 5. How can you identify where state needs to live?

### 1. Identify every component that renders something based on that state

### 2. Find a common owner component (a single component above all the components that need the state in the hierarchy)

### 3. Either the common owner or another component higher up in the hierarchy should own the state

### 4. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component

# Higher-order functions

## 1. What is a “higher-order function”?

### Functions that perform operations on other functions, either as arguments or by returning them

## 2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

### compares m and n and returns true if m was greater than n

## 3. Explain how either map or reduce operates, with regards to higher-order functions

### a map method applies a function to all the elements and builds a new array with the same length as the original one with the elements mapped to a new form by the function
