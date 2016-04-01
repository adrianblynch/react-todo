# React Todo

After going through Dan Abramov's [Getting Started with Redux](https://egghead.io/series/getting-started-with-redux) on [egghead.io](https://egghead.io/), this is my attempt at a Todo application.

[Available here](http://adrianblynch.github.io/react-todo/)

## Notes

I have skipped all the building steps, no npm, no webpack, just React, ReactDOM, Redux and Babel in the browser. All loaded via [cdnjs.com](https://cdnjs.com/). All are the latest versions except for babel-core which remains at 5 due to the packaging needed from 6 onwards.

Components are simple objects:

```
const Component = ({
	property
}) => (
	<button>{property}</button>
)
```

Rather than:

```
const Component = React.createClass({
	render() {
		...
	}
})
```

Or:

```
class Component extends React.Component {
	render() {
		...
	}
}
```
Application state is stored and managed with Redux.

However, I don't pass behaviour through parent components to child components, instead I let the child components dispatch actions directly.

Why? To simplify parent usage and so as not to introduce container components.

One reducer is used, again to simplify things for now. Although you could argument the bigger reducer is less simple than separate ones.

I've tried to remember to use ES2015 JS where possible. Spreading over arrays and objects, lambda functions, default arguments and shorthand object properties.
