# Nullish Coalescing
Good day folks! 👋 Today, we are going to cover something small, yet, an important feature in Javascript. In this post, we will see how `Nullish Coalescing` or Nullish Koala-sing 🐨🎤 (whichever sounds good 😅) works using GIFs.

_Note: Short-circuiting is denoted by ⚡️_


*Scenario 1 (Base case)*:  If the expression at the `left-hand side` of the `??` operator evaluates to `undefined` or `null`, its `right-hand side` is returned.
<img width="900" alt="If the expression at the `left-hand side` of the `??` operator evaluates to `undefined` or `null`, its `right-hand side` is returned." src="https://user-images.githubusercontent.com/19341550/72685059-487cb480-3b0c-11ea-9948-463070e500dd.gif">

*Scenario 2*: Behavior of Nullish Coalescing `??` operator with `falsy` Javascript values.
<img width="900" alt="Behavior of Nullish Coalescing `??` operators when `falsy` Javascript values are passed " src="https://user-images.githubusercontent.com/19341550/72626449-bd1aec00-3970-11ea-908a-e23b56f5f33a.gif">

Notice how short-circuiting (denoted by ⚡️) happens when the LHS is `null` or `undefined`. It doesn't matter if the LHS is falsy values _except_ for `null` and `undefined`

> _Note: Explicit *parentheses groups* are required to mix with `||` and `&&`_

*Scenario 3*: When mixed with other short-circuiting operators `||` and `&&` *without* parentheses
<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *without* parentheses logical or and logical and javascript" src="https://user-images.githubusercontent.com/19341550/72658820-91cde680-39dc-11ea-897d-73be34a174c0.gif">

*Scenario 4*: When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups
<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups" src="https://user-images.githubusercontent.com/19341550/72658821-91cde680-39dc-11ea-80db-5e160724f25c.gif">

<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups" src="https://user-images.githubusercontent.com/19341550/72658822-91cde680-39dc-11ea-9788-29b89b5f4b96.gif">

That's it for today and I hope you found it useful!

And hey, I ❤️ learning from and staying in touch with the curious folks out there (I'm looking at you. Yeah, YOU!). So, please feel free to reach out if you have any questions or suggestions 🙋‍♀️🙋‍♂️ I'm all ears 🤩

| [🐥Twitter](https://twitter.com/HemSays) | [💼LinkedIn](https://www.linkedin.com/in/hems23/) |
|---|---|

Auf wiedersehen 🙌🏼

