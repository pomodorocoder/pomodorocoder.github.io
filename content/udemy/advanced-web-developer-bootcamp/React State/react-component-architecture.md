+++
title = "React Component Architecture"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T11:43:52-05:00
categories = ["Udemy"]
weight = 5003
draft = false
+++

Where to put state and how props and state interact with each other.


### Objectives {#objectives}

-   Pass State to Child Components as props
-   Define which components own state
-   Use stateless functional components


### How is State Shared? {#how-is-state-shared}

-   State is always passed from a parent down to a child component **as a prop**
-   State should not be passed to a sibling or a parent


### Key Takeaway {#key-takeaway}

-   State should be owned by 1 component


### Bad Practice {#bad-practice}

Never assign a prop to a state

```js
class InstructorItem extends Component {
    constructor(props) {
        super(props);
        this.state = {
            name: this.props.name, // Should never assign props to the state here
            hobbies: this.props.hobbies // this could be a duplicate, bad practice
        };
    }

    render() {
        return (
                <div>
                <h3>{this.state.name}</h3>
                <h4>Hobbies: {this.state.hobbies.join(", ")}</h4>
                </div>
        )
    }
}
```


### Stateless Functional Components {#stateless-functional-components}

-   Components implemented using a function not a class
-   The function implements the render method only: no constructor, no state

Here's a stateless functional component example:

```js
import React from 'react';

const Greeting = props => (
        <h1> Hello, {props.name} </h1>
);

export default Greeting;
```


### Thinking in React {#thinking-in-react}

Thinkning in React is not that intuitive at the beginning. This [post](https://reactjs.org/docs/thinking-in-react.html) provides some instructions about how to think about solving problems in React.
