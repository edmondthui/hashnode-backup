## A beginner's guide to functional programming

**Functional programming is a way of programming that creates clean and maintainable code.** It was something that I wanted to get into and have started to learn in these last few months. The company I am working at now uses functional programming heavily. You can read about [how I got my first developer job here](https://www.blog.edmondhui.com/first-developer-job).

In this article, I will try to teach you everything I know about functional programming. **It is a powerful tool to have in your belt that is used in many different languages. **

**One of my favorite things about functional programming is its ability to prevent side effects.** Side effects happen when there is a modification of some kind of state. 

Often in object-oriented programming objects have a state which is mutated causing side effects. The reason we don't want side effects is they can cause unpredictable results depending on the state when a function is run. We want to limit side effects and only use them when necessary. 

## Pure functions

This is where pure functions come in with functional programming.** These are functions that only rely on the input to the function to generate a predictable output. **This means that if you pass in the same input one hundred times you will get the same result every time. 

![Majin_Buu_turns_guy_into_milk.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1662951083131/xD9EXmYms.webp align="center")

Pure functions are the basic building blocks of functional programming because of their simplicity. 

They are easier to debug than object-oriented programming because you do not have to use methods that interact with states which can change. 

Here is the simplest example of a pure function:

```
const double = (a) => a * 2
```
 
Now that you have a pure function which is a basic building block you can use them with other functions. This is because they have an input that will always return the same output. 

## Higher order functions

**These are functions that can accept another function as an argument. **You can use these functions to operate with other functions. 

![d41586-020-00060-1_17560840.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662950923529/IEH8Tbg6R.gif align="center")

Common examples of these kinds of functions in javascript are array methods like `map` or `filter`. This is where functional programming is the most useful. When working with data which is a collection of objects in an array you can use pure functions to easily manipulate the results with fewer bugs because there are no side effects.

A simple example of a higher order function using the pure function `double` we created above would look like this:
```
const numbers = [1,2,3,4,5];

const doubledNumbers = numbers.map(double);

console.log(doubledNumbers); // [2,4,6,8,10]
```

## First class functions

The next concept I want to go over is the first class function which will be used in the next section of this article.

![6t2ark.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1662951212072/P8sk03Fiw.jpg align="center")

**First class functions are important since functions are treated like variables in functional programming.** In functional programming, functions are often passed around and not always invoked. 

They are called first class functions since they are treated as "first class" elements and act the same way as any other normal elements.
- Functions can be assigned to variables
- Functions can be passed to other functions
- Functions can be returned from functions
- Functions can be included in data structures e.g. array

The example above treats the double function as first class because it is being passed into the map function.

## Currying 

Last we have currying which is a way of **creating functions that will return functions** until it has all the parameters before doing something.

![200w.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662950865991/CigoHlQIg.gif align="center")

It will be easier to understand with an example.

We can use our `double` function from earlier and change it into a curried function.

The easiest way of doing this would be changing it from `double` to `multiply` and taking in two parameters:
```
const multiply = (a) => (b) => a*b

const multiplied = multiply(1)(2) // 2
```
However, now that we have this multiply curried function we can now easily recreate our double function by calling it with a two:
```
const double = multiply(2) // double = (b) => 2 * (b)
```

I hope this demonstrates the power that currying will have on your code. With currying you can:
- Clean up functions
- Have less repetitive code
- Have more reusable code

## Conclusion

I hope this intro article to functional programming opens your eyes to the possibilities of using a new coding paradigm and inspires you to learn functional programming. 

In future articles, I hope to expand on functional programming and write about an open-source library called CooperTS which was developed by the talented programmers at my current job. 

If you didn't know I am a [real estate broker turned software engineer](https://www.blog.edmondhui.com/software-engineer-in-3-months) and I hope to teach you everything I know about programming. Please follow me if you found this helpful to get more content like this. 

![Copy of Beginner Developer Tutorials (1).gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1662952012374/15fLJumPZ.gif align="center")
