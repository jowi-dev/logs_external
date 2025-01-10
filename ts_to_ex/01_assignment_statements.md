%{
    title: "Assignments"
}
---

# Assignments

## JavaScript `let` assignment

Starting out with the basics, lets take a look at assigning values to variables. In JavaScript that's going to look like:

```typescript
let val : number = 5;
```

Elixir has a slightly more direct version:

```elixir
val = 5
```

few notes
- no keyword for variable declarations in elixir - in this case `let`
- no type options for declaring variables - it is ALWAYS(mostly) an implicit declaration
- no semi-colons
## JavaScript `const` assignment

In JavaScript, if you want a variable to stay the same value, slap a `const` keyword on it:

```typescript
const val : number = 5;
```

Elixir:

```elixir
val = 5
```

### Wait, What?

Yep. You're reading that correctly - elixir has the same declaration no matter what. The reasoning for this is _all_ variables in elixir are immutable i.e. they can't be changed, or this is what is advertised. Ergonomically variables in elixir will function similar to how `let` works in JavaScript, but behind the scenes elixir makes a copy of a variable, discards the old value, and assigns the new one. This alleviates mutability concerns, but won't give you the familiar interpreter errors you're using to seeing with `const`. Let me see if I can hack together an example:

```elixir
val = 5

val = val + 1 #discards the old version of `val`, and creates a new variable named `val` with a value of 6
```

I've seen this described as `labeling` by some internet strangers, i.e. the label `val` represents the number `5`, then the label `val` represents the number `6` after the second assignment. YMMV, my recommendation is to keep it simple and think about it however fits.


# Conclusion

Not much to see here. Lets move into each language's type system to get an idea of what all can be assigned to a variable.

[Basic Types](02_basic_types)
