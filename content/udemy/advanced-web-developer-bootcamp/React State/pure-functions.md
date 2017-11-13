+++
title = "Pure Functions"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T09:17:21-05:00
categories = ["Udemy"]
weight = 5002
draft = false
+++

### Objectives {#objectives}

-   Define Pure Functions


### Pure Function Definition {#pure-function-definition}

-   A function with no side effects
-   It does not modify its inputs
-   It's repeatable
-   To generate the outputs, we don't need to change the inputs


### Example A.1: Not a Pure Function {#example-a-dot-1-not-a-pure-function}

-   The code below is not a pure function as it changes the values in the input array
-   It is not repeatable: if we run the function multiple times it won't generate the same results

```js
function doubleVals(arr) {
    for(var i = 0; i < arr.length; i++) {
        arr[i] = arr[i] * 2;    // Note here, the value of input array is changed
    }
    return arr;
}
```


### Example A.2: A Pure Function {#example-a-dot-2-a-pure-function}

-   Can use the `map` method which returns an array
-   The input value is not changed
-   The process is repeatable: with same input array, will always generate the same output array

```js
function doubleVals(arr){
    return arr.map(d => d * 2);
}
```


### Example B.1: Not a Pure Function {#example-b-dot-1-not-a-pure-function}

-   In the case below, we are modifying global state
-   Will add a property called job to the person object

```js
var person = {id: 53, name: "Iza"};

function addJob(job){
    person.job = job;
}
addJob("Data Scientist");
```


### Example B.2: Pure Function {#example-b-dot-2-pure-function}

```js
var person = {id: 88, name: "Iza"};

function addJob(personObj, job){
    return Object.assign(
        {}, personObj, {job}
    );
}
addJob(person, "Data Scientist");
```


### Example B.3: Use Object Spread operator for the Pure Function {#example-b-dot-3-use-object-spread-operator-for-the-pure-function}

```js
var person = {id: 88, name: "Iza"}

function addJob(personObj, job){
    return(...personObj, job); //Spread operator puts all the keys and values from personObj and put them into the new object we are creating
}
addJob(person, "Data Scientist")
```


### Pure function with React {#pure-function-with-react}

-   All changes to this.state should be pure
