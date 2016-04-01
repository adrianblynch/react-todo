# React Todo

After going through Dan Abramov's [https://egghead.io/series/getting-started-with-redux](Getting Started with Redux) on [https://egghead.io/](egghead.io), this is my attempt at a Todo application.

## Notes

I have skipped all the building steps, no npm, no webpack, just React, ReactDOM, Redux and Babel in the browser.

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
