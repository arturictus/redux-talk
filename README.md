# redux-talk

## What's redux
- Pattern
- Functional
- library?

## What is not
- framework
- library?

## OOP/ Functional

- OOP:
  * Split responsabilities by state
  * has behaviour, can transform it self
  * when responsability is to transform Split by dependencies (bigger state)
  * unit =~ Class

```ruby
'String'.downcase
'String'.size
```

- functional:
  * Immutable
  * Split by process/ transformation/ operation

```elixir
Enum.map([1, 2, 3], fn(x) -> x * 2 end)
```
  * state is independent of processes or behaviour
  * unit =~ function (group in modules)

```elixir
String.downcase("String")
String.length("String")
```

## MVC?

- Reducer =~ controller
- Action (creators) =~ Controller actions
- Store =~ Model
- React Component =~ view

## Redux Responsabilities
 - https://github.com/reactjs/redux/tree/master/examples/todos/src

### Components (Views)
  - https://github.com/reactjs/redux/blob/master/examples/todos/src/components/Link.js
  - View "no" logic
  - Does not know anything about store, props pass the data

### Actions (Events)
  - https://github.com/reactjs/redux/blob/master/examples/todos/src/actions/index.js

### Reducers (Return updated store)
  - https://github.com/reactjs/redux/blob/master/examples/todos/src/reducers/visibilityFilter.js

### Containers (Get from Store what you need)

  - https://github.com/reactjs/redux/blob/master/examples/todos/src/containers/VisibleTodoList.js

  - dependency injection (inject actions)
  - data to props

## Store (Save it all)
  - getState | subscribe | dispatch

### Useful

  - [Redux Thunk](https://github.com/gaearon/redux-thunk)
  - [Immutable](https://facebook.github.io/immutable-js/)

### Code Walkthrough

### Tricks

- reusable components
  inline styles VS css style (webpack)
  - https://github.com/3mundi/path/tree/develop/client/app/components

- possible structure for complex app
  - forms Store
    - flight form Store
    - hotel form Store
    - etc
  - http://redux.js.org/docs/api/combineReducers.html
- complex actions: (thunk)
  actions triggering actions
  - https://github.com/3mundi/path/blob/develop/client/app/bundles/FlightForm/actions/apiActions.jsx

- Immutable js to ensure components are only view
