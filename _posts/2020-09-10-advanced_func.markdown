---
layout: post
title:  "Blog Post #4 - Advanced Functions"
---
![JavaScript Illustration](/assets/advanced-func.png)

## What is recursion?
In simple terms, recursion is a technique in programming where a function calls itself under a condition until it doesn't 
satisfy said condition.
```javascript
function sumTill(n){
    if (n === 1) return n;

    return n + sumTill(n - 1);
}
```

## What are Scopes and Closures in Javascript?
The way I define scope is the region where variables, functions, classes, etc. can be associated to refer to its entity.
Closures have to do with scope where a function has visibility or scope to the variables in the outer function it lies in.
### Why is understanding scopes and closures important?
I think it's important because to fully understand because the computers can't read your mind and just do what you tell it to
do. So, I think understanding scope and closures will help you understand the code you write and save you from bugs and errors
that you will write. Also understanding code will help you know how to keep variables organized in their region of context.

The example below is a usage of a closure inside the function and each for each loop: 
```javascript
function inArr(assertedArr) {
    const numArray = [];
    assertedArr.forEach((el => {
        arr.forEach(subEl => {
            if (el === subEl){
                numArray.push(el);
            }
        });
    }));
    return numArray;
}
```

## What is the Spread Operator?
The ES6 functionality of the spread operator(...) can expand elements without a defined limit. That is why it is useful when
you don't know how many arguments you will need to pass into a function.

The spread operator can be used to make copies of objects, or in the example below merge 2 arrays into 1.
```javascript
function combineArr(arr1, arr2) {
    return [...arr1, ...arr2];
}
```

