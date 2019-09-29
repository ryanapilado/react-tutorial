# Tutorial Notes

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


    

