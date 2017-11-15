+++
title = "Virtual DOM"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T12:29:41-05:00
categories = ["Udemy"]
weight = 5001
draft = false
+++

### Objectives {#objectives}

-   Describe the virtual DOM
-   Define a synthetic events
-   Describe changes in React 16


### Definition {#definition}

-   Virtual DOM is a data structure stored by React that tracks changes from one render state to the next.
-   If something has changed from one render to the next, the browser's DOM is updated (Reconciliation)


### Synthetic Events {#synthetic-events}

-   Supports all the native brower events, but provides a consistent API on all browsers


### React 16, What's New? {#react-16-what-s-new}

-   Render can return an array of JSX elements or a string

```js
render(){
    return[
            <div key="a"> First Element</div>,
            <div key="b"> Second Element</div>
    ]
}
```

-   [Fiber](https://www.youtube.com/watch?v=ZCuYPiUIONs) is a reconciliation engine
