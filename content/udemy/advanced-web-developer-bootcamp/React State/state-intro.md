+++
title = "Intro to State"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T09:17:12-05:00
categories = ["Udemy"]
weight = 5001
draft = false
+++

### Objectives {#objectives}

-   Define State in React
-   Create a component with a constructor and state
-   Describe what happens when setState is called


### State Definition {#state-definition}

-   Stateful Data: Data in our applications that can be changed
-   Unlike `props` that cannot be changed


### State Example {#state-example}

An example:

```js
class App extends Component {
    constructor(props) {
        super(props);
        this.state = {favColor: "red"};
    }

    render() {
        return (

            <div>
                My favorite color: {this.state.favColor}
            </div>
        )
    }
}
```


### setState {#setstate}

-   How to change the state here? The correct way to change state in the app is using setState
-   setState accepts an object with new properties and values for this.state
-   Create a new object and change the state for newly created object
-   Should never never modify state directly in the original object

```js
this.setState({});
```

Example of changing state

```js
class App extends Component {
    constructor(props) {
        super(props);
        this.state = {favColor: "red"};
        setTimeout(() => {
            this.setState({favColor: "blue"})
        }, 3000);
    }

    render(){
        return(
          <div>
            The current Color is:
            {this.state.favColor}
          </div>
        );
    }
}
```
