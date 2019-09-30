# Tutorial Notes

### Overview

* Components in React have a render() method which returns JSX
* JSX can refer to previously defined components and evaluate expressions inside curly braces
* A component can pass properties to children as attributes, in the child it is accessible in `this.props`
* In a constructor, always call `super(props)` at the top

### Lifting State Up

* It's usually better to store state in a parent component, and then pass that state down to children as properties
* Controlled components are components whose parents have full control over them (they don't have state of their own)

### Why Immutability Is Important

* Two approaches to changing data:
    * Mutate (directly change its values)
    * Replace (reassign variable to a new copy with desired changes)
* Can perform replacement using `Object.assign({}, object, {property: new_value})`
    * `{}` is source object, object and `{property: new_value}` are target objects
    * Copies the values of all enumerable own properties from one or more source objects to the target object
* Benefits of immutability
    1. Complex features become simple
    2. Easier to detect changes because the entire object has to change; it's difficult to detect changes to mutable objects since they are modified directly.
    3. Lets you build 'pure components' in React

### Function Components

* Function components are a simpler way to write components which only contain a `render` method and don't maintain their own state
* Written as a function which takes `props` as input (rather than defining a new class which extends React.Component)
* When should I use one or the other then?
* I didn't even have to change any of the code inside board - JSX treats the classes and functions identically. Square inside the jsx calls either Square the function or Square the class.

### Picking a Key

* Each child in an array or iterator should have a unique "key" prop
* They key can be anything as long as it's unique within the sibling components (doesn't need to be globally unique)
* This allows React to keep track of which item is which between re-renders
    * If current list has item with new key, React creates a component
    * If current list is missing a key, React destroys that component
    * If two keys match, React moves the component
* `key` is a reserved property, but it's not stored in `props`
* After element creation, React stores the `key` directly on the returned element
* If not key specified, React will use the array indice by default, but this is problematic when re-ordering items the list or inserting/removing etc.


    

