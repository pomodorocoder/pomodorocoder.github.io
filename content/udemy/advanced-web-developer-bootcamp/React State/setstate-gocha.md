+++
title = "setState Gotcha!"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T12:00:28-05:00
categories = ["Udemy"]
weight = 5004
draft = false
+++

### Objectives {#objectives}

-   Use a function as the first parameter to setState
-   Add a callback to setState to determine when the state is up to date


### setState that depends on previous state {#setstate-that-depends-on-previous-state}

```js
this.state = {counter: 1};

// New value of the counter depends on the old value
this.setState({
    counter: this.state.counter + 1
})

// If we do this again and for multiple times
this.setState({
    counter: this.state.counter + 1
})
```

We expect the result to be 3, however it's actually 2. The reason is setState is Asychronous. It's eventually doing this:

```js
this.setState({
    counter: this.state.counter + 1
});

Object.assign(
    {},
    {counter: this.state.counter + 1}, // this.state.counter will always be 1
    {counter: this.state.counter + 1},
    {counter: this.state.counter + 1}
);
```

The solution is to update function

```js
this.setState((prevState, props) => {
    return {
        counter: prevState.counter + 1
    };
});
```

The rule is whenever a setState depends on previous state, use a function parameter.


### setState is Asynchronous {#setstate-is-asynchronous}

Sometimes, I use console.log for debugging, however the method below won't work because setState is asynchronous

```js
this.setState({name: "Tim"});
console.log(this.state.name); // Won't be updated yet
```

The correct way should use a callback function

```js
this.setState({name: "Tim"}, () => {
    console.log(
        "Now state is up to date",
        this.state.name
    );
});
```
