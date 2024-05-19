
# Preface TODO - LINKS

This series is both my introductory exploration into writing (bare with me), and an effort to help curious JavaScript(JS) or TypeScript(TS) developers bridge the gap to other syntactic families. Although the examples will be mostly in JS/TS, I hope this can provide reference to any engineer who has worked in a C-style language (JS/TS/C/C++/Java/C#), but wants to explore other horizons. 

I'd also like to call out, in varying degrees of necessity, that I won't be bashing C-style languages in any capacity; I LOVE JS, I think Bun will make it the defacto single threaded language soon enough, and I frequently reach for it over any scripting language for its ease of use, intuitiveness, and versatility. 

# Why Elixir? - TODO - LINKS

I learned about elixir fairly early into my career, while working as a JavaScript/C# developer doing full-stack development. What drew me to elixir originally was how different it was, and how performant it seemed to be in a multi-threaded context. At that point in my career I was searching for "one language to rule them all", or more simply put a language that I could use for everything. To me, everything meant:
- A language I could use server-side, preferably with an ORM comparable to entity framework, with the ability to spawn multiple threads
- A language I could use client side without having a user experience banished to the early days of the internet. 

.NET/MVC at that point had, and maybe still has, an ORM that was so flexible I really never felt it necessary to reach for raw sql. What it lacked was a better templating system. LiveView was that better templating system, offering reactivity and interaction akin to React, Vue, or Angular, without the productivity hit of switching back and forth between apps. 

Finally, elixir just seemed fun. I try to balance all of my tech decisions between `What is actually a good engineering decision` vs `what am I going to enjoy working on?` This admittedly is less than total idealism from an engineering perspective, but if we're going to spend this many hours hacking, building, debugging, its important to at least _somewhat_ enjoy it. 

There's a boatload of other languages out there, I encourage you to try as many different ideas as possible, as it will give you new perspectives and ideas that you can bring along with you forever. The Ralph Waldo Emerson quote frequently rings in my head:

"The mind, once stretched by a new idea, never returns to its original dimensions." 

# Structure of this series

Elixir is not only different from JavaScript in syntax but also in approach; my aim is to show you both syntactic equivalents, but also idiomatic equivalents. Ideas like anonymous functions exist in elixir, but are not used as liberally as they are in elixir. I will do my best to show equivalents, and explain WHY it is that way, so you can be equipped to reference syntax and ideas when working in an elixir code base.

I'll also aim to keep articles on the shorter side so they can be easily referenced. If these notes are open on a second screen while writing code, I've done my job.


# Setup - TODO - LINKS

I'm going to point you to ASDF, the elixir language website, or anything that is not me for setup; setup instructions inevitably go out of sync with reality, and I don't want to create a maintenance nightmare in the form of a markdown document.


# Running the Examples

To run these examples yourself - I would recommend installing `bun` (TODO LINK) for the typescript examples, and `elixir` for the elixir ones. Once they are installed, you should be able to experiment with them by using either:

### TypeScript
```bash
bun repl
```

### Elixir
```bash
iex
```

Recommending Bun for the TypeScript side of things because (AFAIK) the node repl is JavaScript only without a transpiler, while the `bun repl` command will run TypeScript natively.

# Conclusion

I'm bad at goodbyes, so how about we get started?


[Assignments](01_assignment_statements)