+++
title = "Events"
date = 2017-11-15T00:00:00-05:00
lastmod = 2017-11-15T08:44:35-05:00
categories = ["Udemy"]
weight = 5002
draft = false
+++

### Objectives {#objectives}

-   Demostrate an onClick event
-   Using bind functions vs inline callbacks


### onClick Event {#onclick-event}

```js
class ClickExample extends Component {
    constructor(props) {
        super(props);
        this.state = {name: "Isaac"};
    }

    render(){
        return(
                <div>
                <p>{this.state.name}</p>
                <button type="button" onClick={() => this.setState({name: "ISAAC"})}> UPPERCASE </button>
                </div>
        );
    }
}
```
{{% panel theme="info" header="Before Click" %}}
<div id="root"><div><p>isaac</p><button type="button">UPPERCASE</button></div></div>
{{% /panel %}}

After clicking the button:

{{% panel theme="success" header="Result" %}}
<div id="root"><div><p>ISAAC</p><button type="button">UPPERCASE</button></div></div>
{{% /panel %}}


### Using predefined function {#using-predefined-function}

```js
class Example extends Component {

    constructor(props){
        super(props);
        this.state = {name: "isaac"};
        this.handleClick = this.handleClick.bind(this);
    }

    handleClick(e){
        this.setState((prevState, props) => ({
            name: prevState.name.toUpperCase()
        }));
    }

    render(){
        return(
                <div>
                <p>{this.state.name}</p>
                <button type="button" onClick={this.handleClick}>UPPERCASE</button>
                </div>
        )
    }

}
```


### Common Mistake {#common-mistake}

Make sure don't invoke the function immediately

```js
<button type="button" onClick={this.handleClick()}>UPPERCASE</button> // Don't invoke the function here
```

In this case, function will be invoked immediately, not on the event


### In line arrow functions vs. Bind {#in-line-arrow-functions-vs-dot-bind}

There's no noticable performance benefits of using bind in the constructor.

