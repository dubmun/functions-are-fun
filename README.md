# functions-are-fun
I stand by the statement.

> This is an exercise in functional programming using ```javascript```, but by all means, use any programing language that supports the concept of passing and returning functions from other functions!

## Introduction
You may use the included file or generate something more robust. You can open it in the VSCode preview window and it should update answers in real time, but beware crashing your editor with memory leaks and infinite loops. 

These instructions are kept simple to focus on the coding solutions, but if you'd like to perform the exercises with a test watcher, that would be another way to get quick feedback. 

The important thing is working through the exercises in a way that challenges you and helps you learn.

### Rule
> If you have a question, you must ask it.

### Definitions
> Function types based on the number of arguments they accept:
> 
> ```function oneArg(x) //unary```
>
> ```function twoArgs(x,y) //binary```
>
> ```function threeArgs(x,y,z) //trinary```
> 
> ```//etc...```



## Exercises
### 0. (already complete)
Write an ```identity``` function that takes an argument and returns that argument. 

```identity(3)    // 3```

### 1.
Write three binary functions, ```add``` , ```sub```, and ```mul```, that take two numbers and return their sum, difference, and product.

```add(3, 4)    //  7```

```sub(3, 4)    // -1```

```mul(3, 4)    // 12```

### 2.
Write a function ```identityf``` that takes an argument and returns a function that returns that argument.

```var three = identityf(3)```

```three()    // 3```

### 3.
Write a function ```addf``` that adds from two invocations.

```addf(3)(4)    // 7```

### 4.
Write a function ```liftf``` that takes a binary function, and makes it callable with two invocations.

```var addf = liftf(add)```

```addf(3)(4)           // 7```

```liftf(mul)(5)(6)     // 30```

### 5.
Write a function ```curry``` that takes a binary function and an argument, and returns a function that can take a second argument. It's possible to write this function by reusing a previous exercise's function ;)

```var add3 = curry(add, 3)```

```add3(4)              // 7```

```curry(mul, 5)(6)     // 30```

### 6.
Without writing any new functions, show three ways to create the ```inc``` function.

```inc(5)              // 6```

```inc(inc(5))         // 7```


### 7.
Write a function ```twice``` that takes a binary function and returns a unary function that passes its single argument to the binary function twice.

```add(11, 11)   // 22```

```var double = twice(add);```

```double(11)     // 22```

```var square = twice(mul);```

```square(11)    // 121```


### 8.
Write ```reverse```, a function that reverses the arguments of a binary function.

```var bus = reverse(sub);```

```bus(3, 2)    // -1```


### 9.
Write a function ```composeu``` that takes two unary functions and returns a unary function that calls them both.

```composeu(double, square)(5)    // 100```

### 10.
Write a function ```composeb``` that takes two binary functions and returns a function that calls them both.

```composeb(add, mul)(2, 3, 7)    // 35```

### 11.
Write a ```once``` function that allows a binary function to be called only once.

```var add_once = once(add);```

```add_once(3, 4)    // 7```

```add_once(3, 5)    // undefined```


### 12.
Write a ```fromTo``` function that produces a generator that will produce values in a range.

```var index = fromTo(0, 3);```

```index()    // 0 ```

```index()    // 1```

```index()    // 2```

```index()    // undefined```


### 13.
Write an ```element``` function that takes an array and an optional generator (like the result of fromTo) and produces a generator that will produce the elements of the array.

```var ele = element(['a', 'b', 'c', 'd'], fromTo(1, 3))``` 

```ele()    // 'b'```

```ele()    // 'c'```

```ele()    // undefined```


### 14.
EXERCISE

```example```

## Hello
If you made it this far in the exercises, and would like to do more, lmk.