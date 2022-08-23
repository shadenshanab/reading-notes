# Class03 read

----

# React Docs - Forms

## 1. What is a ‘Controlled Component’?

### it is an input form element that is controlled by react.  It takes its current value via props and modifies it via callbacks such as onClick, onChange, and so on

## 2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why

### we update the state as soon as the user types anything, to make react state the source of truth and that helps us stay up to dat with every keystroke

## 3. How do we target what the user is entering if we have an event handler on an input field?

### handleChange runs as the person is typing and updates with every keystroke, the input will be passed to other UI elements and resat from other event listeners

# The Conditional (Ternary) Operator Explained

## 1. Why would we use a ternary operator?

### to test a condition, it is like a normal if statement but it has fewer lines of code and is basically simpler

## 2. Rewrite the following statement using a ternary statement

>if(x===y){
> console.log(true);
>} else {
> console.log(false);
>}

### x===y ? true : false

