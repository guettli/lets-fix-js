# Let's fix JS

JavaScript and JSON are everywhere. JavaScript got better during the last years, but some things are still  inconvenient.

## Long term goal: fix the flaws.

Goal: fix the flaws by influencing future specification.

Before fixing the flaws consensus is needed.

## How to make the transition?

The transition to the cleaned up version could be done to improve the [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

## Current step: Write down the flaws

Before consensus can be reached, the flaws need to be written down.

## Later

[Contributing to ECMAScript](https://github.com/tc39/ecma262/blob/master/CONTRIBUTING.md)

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

### JavaScript Equality
"Equality is one of the most initially confusing aspects of JavaScript." Source: http://adripofjavascript.com/blog/drips/object-equality-in-javascript.html

If it is confusing, then it is not obvious. This is a flaw.


### JavaScript: Support for BigInts

https://stackoverflow.com/questions/48802728/how-to-marshal-json-with-bigints

Works in Python
```python
import json
>>> json.dumps(json.loads('{"NETWORK_ID": 6000370005980500000071}'))
'{"NETWORK_ID": 6000370005980500000071}'
```

### JSON: binary data type

There thousand ways to work around it. Very common is base64 encoding. But that's a useless work-around.

In Python you can create binary data with the "b" prefix. Example:

```
binary_data = b'\x00\xff....'
```

### JSON: No Datetime data type

It would be nice to support it.

Other tools which support this:

* [PostgreSQL Date/Time](https://www.postgresql.org/docs/12/datatype-datetime.html#DATATYPE-DATETIME-INPUT)
* [Protobuf Timestamp](https://developers.google.com/protocol-buffers/docs/reference/google.protobuf#google.protobuf.Timestamp)
* [Python datetime](https://docs.python.org/3/library/datetime.html#datetime-objects)


### JSON: Timedelta

A timedelta datatype would be very nice.

Other tools which support this: 

* [PostgreSQL Interval](https://www.postgresql.org/docs/12/datatype-datetime.html#DATATYPE-INTERVAL-INPUT)
* [Protobuf Duration](https://developers.google.com/protocol-buffers/docs/reference/google.protobuf#duration)
* [Python timedelta](https://docs.python.org/3/library/datetime.html#timedelta-objects)

### JSON: Comments

Quoting @asb:

> Leave comments is essential for human beings understand what is going up.
> Is the best practice in any programming language.
> Is kind and nice for all who will study what is done.
> Every one knows that JSON was, -was- a encapsuled internal way to exchange data in javascript
> but now JSON is used do describe the data for all world.
> So, please make // into comments for JSON, let the spice flow.

## New Features

Here some new features for JS and JSON

### Bidirectional replication

If would be very handy if bidirectional replication would be made available in JavaScript.

PouchDB already implements such a feature. See: https://pouchdb.com/guides/replication.html#couchdb-sync

This would make it much easier to write "offline first" applications.

I how no clue how to implement this, but I would love to use it, if it was available.

## Thanks

- @orta at https://gitter.im/Microsoft/TypeScript
- @MicahZoltu at https://gitter.im/Microsoft/TypeScript
- @agsb issue #1
