# Tutorials and Musings about Developing Software, mostly with Scala 3

## How to be Direct (in Scala)

Good code is clear code.  Unfortunately, many tasks that one needs to solve
are anything but clear intrinsically--the logic can be complex, errors can
intervene at many points, and needed APIs may have intricate constraints and
requirements.

One way to try to tame reality into clarity is by introducing powerful
abstractions that handle common sources of complexity.  Unfortunately, this
often comes with a built in penalty: now your code has to manipulate the
abstraction rather than the thing itself that you care about.

Direct style is an answer to this problem: whenever possible, favor
constructs that let you _just do it_.  Rather than adopting the most
powerful abstraction, you try to find the abstraction with the least
possible cognitive overhead, so you can address your problem as-it-is.

One application of direct style is the idea of [direct style
effects](https://www.inner-product.com/posts/direct-style-effects/), which
is typically conceived of as an effects system similar in power to
explicitly monadic effects.

[Here, I describe a related approach that is inspired more by Rust's `?`
and `Result`]({{site.baseurl}}/direct-style), which emphasizes directness,
and show how it can dramatically simplify code with essentially no loss
of performance in many cases.  You _can_ handle your errors and eat them,
too!


