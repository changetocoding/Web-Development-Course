# What is a promise

Promises are a way of handling asynchronous code, specifically for what happens after an asynchronous task is completed.

Promises can only be resolved once if there is more than one resolve in a promise only the first action in the promise will be resolved, the second resolve will do nothing.

 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});

We should use Promises when working with ajax requests or any async task that requires an action after it has been complete.

# What is async?

Asynchronous task is a task that can be executed on a seperate thread while another process is running. (So you don't have to wait for something else to finish before executing the task),
Think of making washing the dishes or grabbing a cup while boiling a hot water in a kettle.

# Promise constructor

Two ways of creating a promise, 

1. We can store a promise as a variable 

 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});

2.

# .Then

# Promise states

Fulfilled / Resolved - The action related to promise succeeded

Rejected - Promise action failed

Pending - The promise action hasn't yet been fulfilled or rejected

Settled - Either the promise action has been fulfilled or rejected


