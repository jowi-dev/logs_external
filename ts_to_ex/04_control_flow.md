

As mentioned in the previous post on [functions](link), control flow is where we first start to really feel the difference of thinking elixir vs a C-Style language. Elixir's control flow can be broken into 5 concepts: `if`, `with`, `case`,  `cond`, and as a more general concept, pattern matching.

## If/else/unless

If statements are pretty much as you'd expect, with a few notable differences

```typescript
let num = 2;
if (num === 2){
  console.log("2");
} else {
  console.log("Not 2");
}
```


```elixir
num = 2
if num == 2 do
  IO.puts"2"
else
  IO.puts"Not 2"
end
```

If/do  and else/end replace brackets for wrapping control.

### Bonus: Ternary

One thing I (ab)used in TypeScript was the use of the ternary operator. Elixir has its own form.

```TypeScript
let sheWalkedAwayFromMe = true;
let age = sheWalkedAwayFromMe ? 23 : 21;
```

```elixir
she_walked_away_from_me = true
age = if she_walked_away_from_me, do: 23, else: 21
```


If statements, as well as all control flow statements can be used in assignments. For example, we could write the ternary from above in expanded form

```elixir
she_walked_away_from_me = true
age = 
  if she_walked_away_from_me do 
    23
  else
    21
  end
```

and `age` would be 23. It was hard to wrap my head around that at first, but you'll find it very useful in some situations.

## with

With statements... what the hell are they even for really? 

## Pattern Matching

## case

## cond
