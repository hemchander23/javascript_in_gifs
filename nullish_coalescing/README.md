# Nullish Coalescing
*Scenario 1*:  If the expression at the `left-hand side` of the `??` operator evaluates to `undefined` or `null`, its `right-hand side` is returned.
<img width="900" alt="If the expression at the `left-hand side` of the `??` operator evaluates to `undefined` or `null`, its `right-hand side` is returned." src="https://user-images.githubusercontent.com/19341550/72658476-9217b300-39d7-11ea-95ca-40ffc2bcbdd2.gif">

*Scenario 2*: Behavior of Nullish Coalescing `??` operator with `falsy` Javascript values.
<img width="900" alt="Behavior of Nullish Coalescing `??` operators when `falsy` Javascript values are passed " src="https://user-images.githubusercontent.com/19341550/72626449-bd1aec00-3970-11ea-908a-e23b56f5f33a.gif">

Notice how short-circuiting (denoted by ⚡️) happens when the LHS is `null` or `undefined`. It doesn't matter if the LHS is falsy values (except `null` and `undefined`)

> _Note: Explicit *parentheses groups* are required to mix with `||` and `&&`_

*Scenario 3*: When mixed with other short-circuiting operators `||` and `&&` *without* parentheses
<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *without* parentheses logical or and logical and javascript" src="https://user-images.githubusercontent.com/19341550/72658820-91cde680-39dc-11ea-897d-73be34a174c0.gif">

*Scenario 4*: When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups
<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups" src="https://user-images.githubusercontent.com/19341550/72658821-91cde680-39dc-11ea-80db-5e160724f25c.gif">

<img width="900" alt="When mixed with other short-circuiting operators `||` and `&&` *with* parentheses groups" src="https://user-images.githubusercontent.com/19341550/72658822-91cde680-39dc-11ea-9788-29b89b5f4b96.gif">
