Hello everybody 👋! I created this GIF cheatsheet for my own reference and I hope it will be useful for the community as well ❤️

### Index
 * [How is this organized?](#conventions)
 * [Promise.resolve](#promiseresolve),[Promise.reject](#promisereject)
 * [Promise.all](#promiseall)
 * [Promise.allSettled](#promiseallsettled)
 * [Promise.race](#promiserace)
 * [Promise.any](#promiseany)

# How is this organized? <a name="conventions"></a>

Consider the GIFs like watching a slow-mo video of Promise API methods in action. The scenarios for each Promise API describe how they work with an emphasis on Promise status transition, value/reasons, and the order.

| Color Code  | Promise Status| What it means |
|---|---|---|
|  <img width="45" alt="pending" src="https://user-images.githubusercontent.com/19341550/72203681-cdc0f300-3494-11ea-843e-4b4ce3e7911f.png"> |  `pending` | Represents initial state. The operation represented by the promise is neither fulfilled or rejected. |
|  <img width="45" alt="fulfilled" src="https://user-images.githubusercontent.com/19341550/72203680-cd285c80-3494-11ea-8d6c-b3bb1e52d0fe.png"> | `fulfilled`  | Operation is successful and result _value_ is assigned. Typically, values appear on top of the respective promises upon fulfillment|
| <img width="45" alt="rejected" src="https://user-images.githubusercontent.com/19341550/72203682-cdc0f300-3494-11ea-99eb-40dec7737d60.png">  |  `rejected` | Operation unsuccesful and usually there is a _reason_ for rejection. It appears on top of the rejected promise |

For the sake of simplicity, I have added numbers below each promise representing the order in which they settle. This is handy while understanding the _short-circuiting_ behavior (denoted by ⚡️) of each promise API. 

# `Promise.resolve` <a name="promiseresolve"></a>

*Scenario 1*: If the given value is _not_ a `thenable` but a _valid_ Javascript `value`
<img width="900" alt="If the given value is _not_ a `thenable` but a _valid_ Javascript `value`" src="https://user-images.githubusercontent.com/19341550/72240446-2ebe0780-360a-11ea-8e8c-e6b0c9b9f20a.gif">

*Scenario 2*: If the given value is a `thenable` (i.e., Promise or object with `then()` method
<img width="900" alt="If the given value is a `thenable` (i.e., Promise or object with `then()` method" src="https://user-images.githubusercontent.com/19341550/72240447-2f569e00-360a-11ea-8a63-25a3920da75d.gif">

*Scenario 3*: _Nested_ Promise-like objects
<img width="900" alt="_Nested_ Promise-like objects" src="https://user-images.githubusercontent.com/19341550/72240448-2f569e00-360a-11ea-806c-2b283119374a.gif">


# `Promise.reject` <a name="promisereject"></a>

*Scenario*: Rejection with a `reason`
<img width="900" alt="Rejection with a `reason`" src="https://user-images.githubusercontent.com/19341550/72240449-2f569e00-360a-11ea-82e5-ae18cd4155f0.gif">


# `Promise.all` <a name="promiseall"></a>

*Scenario 1*: All passed-in Promises get fulfilled
<img width="900" alt="Promise.all - All passed-in Promises get fulfilled" src="https://user-images.githubusercontent.com/19341550/72202910-f3e19580-348a-11ea-8a00-49c005f3cdd3.gif">

*Scenario 2*: ⚡️ One or more of the passed-in Promise(s) rejects
<img width="900" alt="⚡️Promise.all - One or more of the passed-in Promise(s) rejects" src="https://user-images.githubusercontent.com/19341550/72202911-f3e19580-348a-11ea-99ff-850ced214ddb.gif">

*Scenario 3*: ⚡️ All passed-in Promises get rejected
<img width="900" alt="⚡️Promise.all - All passed-in Promises get rejected" src="https://user-images.githubusercontent.com/19341550/72202912-f47a2c00-348a-11ea-9ff2-ad6d86514c8c.gif">

*Scenario 4*:  Passing an Empty iterable
<img width="900" alt="Promise.all - Passing an Empty iterable" src="https://user-images.githubusercontent.com/19341550/72202913-f47a2c00-348a-11ea-9642-684ffb5b771e.gif">

# `Promise.allSettled` <a name="promiseallsettled"></a>

*Scenario 1*: All passed-in Promises get fulfilled
<img width="900" alt="Promise.allSettled - All passed-in Promises get fulfilled" src="https://user-images.githubusercontent.com/19341550/72213854-0c4dc080-351c-11ea-9646-c6917ae7df2d.gif">

*Scenario 2*:  One or more of the passed-in Promise(s) rejects
<img width="900" alt="Promise.allSettled - One or more of the passed-in Promise(s) rejects" src="https://user-images.githubusercontent.com/19341550/72213855-0ce65700-351c-11ea-947d-b0be63329f3d.gif">

*Scenario 3*:  All passed-in Promises get rejected
<img width="900" alt="Promise.allSettled - All passed-in Promises get rejected" src="https://user-images.githubusercontent.com/19341550/72213856-0d7eed80-351c-11ea-9961-06d869c9655e.gif">

*Scenario 4*:  Passing an Empty iterable
<img width="900" alt="Promise.allSettled - Passing an Empty iterable" src="https://user-images.githubusercontent.com/19341550/72213857-0d7eed80-351c-11ea-8766-6425dfa4f3e4.gif">

# `Promise.race` <a name="promiserace"></a>

*Scenario 1*: ⚡️ All passed-in Promises get fulfilled
<img width="900" alt="⚡️Promise.race - All passed-in Promises get fulfilled" src="https://user-images.githubusercontent.com/19341550/72214065-79635500-3520-11ea-937e-5d89d2ce1aa5.gif">

*Scenario 2*: ⚡️ One or more of the passed-in Promise(s) rejects
<img width="900" alt="⚡️Promise.race - One or more of the passed-in Promise(s) rejects" src="https://user-images.githubusercontent.com/19341550/72214066-79635500-3520-11ea-9544-949800bb450f.gif">

*Scenario 3*: ⚡️ All passed-in Promises get rejected
<img width="900" alt="⚡️Promise.race - All passed-in Promises get rejected" src="https://user-images.githubusercontent.com/19341550/72214067-79635500-3520-11ea-8737-e6c3198dc2ad.gif">

*Scenario 4*:  Passing an Empty iterable
<img width="900" alt="Promise.race - Passing an Empty iterable" src="https://user-images.githubusercontent.com/19341550/72214068-79635500-3520-11ea-999b-6cbfdc073014.gif">


# `Promise.any` <a name="promiseany"></a>

> `⚠️ Warning` - Promise.any() method is experimental and not fully supported by all browsers. It is currently in the TC39 Candidate stage (Stage 3).

*Scenario 1*: ⚡️ All passed-in Promises get fulfilled
<img width="900" alt="⚡️ Promise.any - All passed-in Promises get fulfilled" src="https://user-images.githubusercontent.com/19341550/72214139-6487c100-3522-11ea-9cc7-137b7f700c0f.gif">

*Scenario 2*: ⚡️ One or more of the passed-in Promise(s) rejects
<img width="900" alt="⚡️ Promise.any - One or more of the passed-in Promise(s) rejects" src="https://user-images.githubusercontent.com/19341550/72214140-6487c100-3522-11ea-9527-609bcc583889.gif">

*Scenario 3*:  All passed-in Promises get rejected
<img width="900" alt=" Promise.any - All passed-in Promises get rejected" src="https://user-images.githubusercontent.com/19341550/72214141-65205780-3522-11ea-96e1-9a8697316fb8.gif">

*Scenario 4*:  Passing an Empty iterable
<img width="900" alt="Promise.any - Passing an Empty iterable" src="https://user-images.githubusercontent.com/19341550/72214142-65205780-3522-11ea-83e7-fbd3bb4e1c18.gif">

Hope this was useful! Please feel free to share your thoughts on the same. Don't forget to share if you found this useful. 

Auf wiedersehen 🙌🏼
