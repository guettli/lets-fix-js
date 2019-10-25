# Let's fix JS

JavaScript is everywhere. It got better during the last years, but some things are still  inconvenient.

## Long term goal: fix the flaws.

Goal: fix the flaws by influencing future specification.

Before fixing the flaws consensus is needed.

## How to make the transition?

The transition to the cleaned up version could be done to improve the [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

## Current step: Write down the flaws

Before consensus can be reached, the flaws need to be written down.

## What is a flaw?

Everything which can be done simpler or more obivious is a flaw. 

If unsure, the [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python) is a good general guideline.

Of course there is no single truth. Agreement need to be found by discussing and maybe voting.

Just for fun I keep a list of synomys for "flaw" which I saw while discussing how to fix JS:

- JS baggage ("if you want to see what a version of TypeScript without JS baggage looks like, check out static TypeScript")
- horribleness ("I suspect someone out there has documented all of JavaScript's horribleness.")
- terribleness ("For example, JS equality terribleness will never be fixed by TS, and there is a laundry list of things like that which will never be fixed.")

But let's focus on the way we want it to be.

## Feedback needed

Please tell me what you think:

- Which flaws does JS have?
- Why do you prefer a different language? What could be added to JS to make it more attractive?
- Why did you avoid JS in the past? Please provide feedback!


Let's influence the future **together** :-)

Don't wait for others or projects like TypeScript to fix this. There are fundamental issues, which can't be solved in [TypeScript](https://en.wikipedia.org/wiki/TypeScript), [Polyfill](https://en.wikipedia.org/wiki/Polyfill_%28programming%29), [Shim](https://en.wikipedia.org/wiki/Shim_(computing)), [WebAssembly](https://en.wikipedia.org/wiki/WebAssembly), ...

Please create a new issue and tell us how you would like JS to look like in the future: https://github.com/guettli/lets-fix-js/issues/new

## Flaws

### Equality
"Equality is one of the most initially confusing aspects of JavaScript." Source: http://adripofjavascript.com/blog/drips/object-equality-in-javascript.html

If it is confusing, then it is not obvious. This is a flaw.

## Thanks

- @orta at https://gitter.im/Microsoft/TypeScript
- @MicahZoltu at https://gitter.im/Microsoft/TypeScript
