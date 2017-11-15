+++
title = "Forms"
date = 2017-11-15T00:00:00-05:00
lastmod = 2017-11-15T17:34:49-05:00
categories = ["Udemy"]
weight = 5003
draft = false
+++

### Objectives {#objectives}

-   Describe a controlled component vs. uncontrolled
-   Handle submit onSubmit


### Uncontrolled Component {#uncontrolled-component}

The component that react doesn't have control over

```js
<input type="text" />
```

React is not aware of what the user is typing, the browser is in charge of the state


### Controlled Component without Update {#controlled-component-without-update}

```js
<input type="text" value={this.state.inputText}/>
```

React is now in control of the state via this.state.inputText, but the input can't be updated


### Controlled Component with Update {#controlled-component-with-update}

```js
<input
  type="text"
  name="inputText"
  value = {this.state.inputText}
  onChange{
      (e) => {
          this.setState({inputText: e.target.value})
      }
  }
/>
```

React is not in control of the state via this.state.inputText and the state can change via onChange


### onSubmit {#onsubmit}

Lastly, let's discuss how to submit a form

```js
<form onSubmit={(e) => {
  e.preventDefault();
  const data = [...this.state.data, this.state.inputText];
  this.setState({data, inputText: ''});
}}>
<input
  type="text"
  name="inputText"
  value={this.state.inputText}
  onChange={(e) => {
      this.setState({[e.target.name]: e.target.value})
  }}
>
</form>
```

A button's click is not the same as a submit, use onSubmit
