class 4c reading notes

# https://flaviocopes.com/javascript-callbacks/

Asynchronicity in Programming Languages:

Asynchronous means that things can happen independently of the main program flow.

A callback is a simple function that’s passed as a value to another function, and will only be executed when the event happens. We can do this because JavaScript has first-class functions, which can be assigned to variables and passed around to other functions (called higher-order functions)

Callbacks are great for simple cases!
However every callback adds a level of nesting, and when you have lots of callbacks, the code starts to be complicated very quickly.

Alternatives to callbacks inclue promises and async/await.

## https://flaviocopes.com/javascript-promises/

A promise is commonly defined as a proxy for a value that will eventually become available.

Once a promise has been called, it will start in pending state. This means that the caller function continues the execution, while it waits for the promise to do its own processing, and give the caller function some feedback.

At this point, the caller function waits for it to either return the promise in a resolved state, or in a rejected state, but the function continues its execution while the promise does it work.

initialize a promise with `new Promise ((resolve, reject) => {})

Using resolve and reject we can communicate back a value

A promise can be returned to another promise, creating a chain of promises.

The Fetch API is a promise-based mechanism, and calling fetch() is equivalent to defining our own promise using new Promise().

If you need to synchronize different promises, Promise.all() helps you define a list of promises, and execute something when they are all resolved.

Promise.race() runs as soon as one of the promises you pass to it resolves, and it runs the attached callback just once with the result of the first promise resolved.

If you get the Uncaught TypeError: undefined is not a promise error in the console, make sure you use new Promise() instead of just Promise()

### https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous

