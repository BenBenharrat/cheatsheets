# How does javascript work under the hood 

## The Call stack 

The Call stack is the place whre javascript keep in track of where it is in relation to the functions it goes into. In other words, with the call stack javascript knows exactly from where
it started to enter a function and where it actually obtains a return. 

## The web apis 

Javascript being a single threaded language (meaining it can only do one thing at a time), it uses web apis included in most browsers to allow it to do multiple asynchronous actions 
For instance the `setTimeOut(3000)` function will be executed not in the call stack, that is a part of Javascript runtime, but in the web api that will complete the timer in 3 seconds.

## The callback queue

Once the web api actions has been fufilled, the action is send to the callback queue. The callback queue job is simple: once the call stack of Javascript is empty, it will send the action
the instant it's cleared. That's the reason for instance that a `setTimeOut(0)` is still not instant because it will be processed first by the web apis and it will need for the stack to 
be empty to actually fulfill it's action.