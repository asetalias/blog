+++
title = 'The Future is Rust(y)?'
slug = 'future-with-rust'
image = 'https://cdn.dribbble.com/users/241205/screenshots/4977779/drib_00_webasm_tank.png'
date = "2019-06-01T00:00:00"
author = 'Swarnim Arun'
tags=['rust','programming']
categories =['code-philosophy']
description = 'My quick take on how I see Rust as the new leader of this ever changing programming world'
+++

**Rust is the system programming language for the future.** Quite a presumptuous statement, said my confreres. I would be inclined to agree with them but for the experience of the agony of using C.

![](https://doc.rust-lang.org/nomicon/img/safeandunsafe.svg)

> “Having been tortured by C during my years of wiring security-critical software, I don’t think I exaggerate when I compare programming in it with walking through a minefield.”
by Ivan Ristic, Founder of SSL Labs

I will not add more comments to the above statement as I believe it to be the most accurate description of C language by far. I won't proclaim myself as a C language expert nevertheless I assume all the 'C citizens' here would agree with it.


### But sire isn't C++ the next step? Why Rust if we have C++?
C++, as described by Linus Torvalds, it's a not-so-good programming language(actually he called it horrible and crappy). Or as stated by Donald Knuth, "C++ has a lot of good features, but it has a lot of dirty corners".

Now with the perspective of such awesome people out of the way let me explain why C++ sucks from my view (again I am not an expert).
1- It feels like an abstract collage of a slew of languages like ALGOL, Ada, Simula, CLU and C (of course). 
2- It forces OOP ideologies on the programmer in a very ambiguous manner.
3- It overly complicated for little gain in ease of use. And the so-called efficient abstractions make it hard to change code down the line.

[Read here for Linus Torvalds Comments](http://harmful.cat-v.org/software/c++/linus)
[And, here for why C++ sucks](https://news.ycombinator.com/item?id=11147031)


### So what makes Rust any better?
- Rust is a very different language from C++ and probably what can be called the modern man's C.
- Rust is a language that guarantees to deny memory leaks and data races by compile-time checks without a Garbage Collector, using the concept of Ownership & Borrowing.
- Rust also has zero-cost abstraction which allows for almost C-like performance.

Call me a fanboy of Rust but here are some stats for the analytical minds to gnaw at, 
[StackOverFlow Survey for Most Loved Language:](https://insights.stackoverflow.com/survey/2018#most-loved-dreaded-and-wanted) And... the victor is, you guessed it, Rust.
While C and C++ score really high on the list of most dreaded languages.
Also if you check you will find that the stats are quite the same for the few years since Rust 1.0 came out and Rust became a stable language.

#### But I heard Go is backed by Google. And it can also give C-like performance. So how come you aren't selling Go?
Because Rust has the backing of Mozilla group (the people behind Firefox). And Go is extremely opinionated for it to be viable for System Level Programming (in my view). This means that Go is better used for higher level tasks. Also considering it has a garbage collector attached to its hip.

![put-your-trust-in-rust](https://blog.mozilla.org/firefox/files/2017/03/Put-Your-Trust-in-Rust.png)

### So how does Rust provide memory safety?
> It's elementary my dear Watson.
Rust has compile-time reference counting and "Ownership and Borrowing". Which allows it to check the code for possible mistakes, and clear up memory without the need for clunky garbage collectors.
And yes, it's quite similar to what you refer to as unique_pointer in C++. But the difference lies in the fact that in Rust it's a compile-time check whereas in C++ it's performed at runtime.

This comes from the observation that memory becomes `unsafe` when we have aliasing(pointer/reference) of data which is then mutated and then very likely leaves us behind with dangling hope... *cough* I mean pointer.
![guaranteeing-memory-safety-in-rust](https://image.slidesharecdn.com/rustoverview-140913055618-phpapp02/95/guaranteeing-memory-safety-in-rust-13-638.jpg?cb=1410587857)

So now we have some idea how taking away shared mutability and using the Ownership and Borrowing model helps us with memory safety in Rust.


### But I like my language. Why should I switch to Rust?
So at this point, I am sure you think that Rust is just the same old candy in a new wrapper. But that's pretty ill-advised, Rust has a bunch of amazing features that make it worth the switch.
One such thing is the lovely Web Assembly. Which has become the way to go for the performance intensive frontend web tasks. And Rust has the best integration possible with the format which makes it the clear choice for the performance hungry web developers.


So is that all? Not at all, Rust is a rather fascinating language, and I will surely be covering it in much greater detail in the coming months. Ciao!

#### Find me at @swarnimarun on [Twitter](https://twitter.com/swarnimarun) or [Github](https://github.com/swarnimarun). Or my blog at [swarnimarun.github.io](https://swarnimarun.github.io)

PS: Hopefully the blog will be a little more lively when you all read it. Also have a rough log of my GSoC experience as a first year :P