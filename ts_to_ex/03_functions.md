%{
    title: "Functions"
}
---
# Public, Private, Anonymous Functions


## Public Functions
### TypeScript

#### Functional Form
```TypeScript
export function addOne(num : number): number {
  return num + 1;
}

// called via
addOne(1)
```

#### Object-Oriented Form
```TypeScript
class numMutator {
  static addOne(num: number) : number {
	  return num + 1;
  }
}

// called via
numMutator.addOne(1);
```
### Elixir

#### Notable Differences
There are a few distinct differences between the TypeScript world and the Elixir world of functions. First and foremost the keyword differences. We use `def` to `define` a public function, and instead of braces we say `do/end` to describe the contents of the body. 

`@spec` is another oddity in elixir; it is our attempt at describing types. rather than cluttering a function declaration with typing, in effect we move it to the line above as a description. a `@spec` is read relatively simply as:
```elixir
@spec $function_name($param1_type, $param2_type, ...) :: $return_type
```

Ergonomically, my biggest hurdle in the elixir world was the lack of `return` as a keyword. I _hated_ it when I started, but have grown to appreciate the way it drives control flow. In elixir we return the final line from a function as its return value. In the following examples, the result of the addition operator is returned implicitly to the caller. This is a pretty big divorce from the C-style `if(err) return;` control flow used to break out of functions early, but I'll touch on that in a future section (TODO - LINK TO CONTROL FLOW SECTION)
#### Standard Form
```Elixir
@spec addOne(integer()) :: integer()
def addOne(num) do
  num + 1
end

# called via
addOne(1)
```

#### One Liner
```elixir
@spec addOne(integer()) :: integer()
def addOne(num), do: num + 1

# called via
addOne(1)
```

## Private Functions

I'll save the word count in this section, as it has very minor differences from the public function section from above.

### TypeScript

#### Functional Form
```TypeScript
function addOne(num : number): number {
  return num + 1;
}

// called via
addOne(1);
```

#### Object-Oriented Form
```TypeScript
class numMutator {
  private addOne(num: number) : number { 
	  return num + 1;
  }
}


```
### Elixir

Want a private in elixir? `defp` instead of `def`. That's all there is to it.
#### Standard Form
```Elixir
@spec addOne(integer()) :: integer()
defp addOne(num) do
  num + 1
end

# called via
addOne(1)
```

#### One Liner
```elixir
@spec addOne(integer()) :: integer()
defp addOne(num), do: num + 1


# Called via
addOne(1)
```

## Anonymous Functions

In TypeScript, there is a embraced love for the idea of functions as a first class citizen. something like `const addOne = (num) => num + 1;` can be seen with fairly liberal use. Elixir has a few variations of the same idea, but they are expressed (usually) at very distinct times - mostly expressed in the various standard library functions as additional logic.

### TypeScript

```TypeScript
const addOne(num) => num + 1;

// which is then called via

addOne(1) // returns 2
```

### Elixir

Elixir has two distinct methods of creating anonymous functions, which have different advantages syntactically but little difference from an implementation perspective. Additionally, calling anonymous functions in elixir has a distinct difference from calling regular functions with the addition of a period between the variable name and the parenthesis surrounding the parameters.

```elixir
addOne = fn num -> num + 1 end

# OR

addOne = &(&1 + 1)


# In either case, we then call them via

addOne.(1) # Notice the `.` !
```



## Closing

Give these a try in your repl and see what you think! In the next section we'll cover control flow TODO - LINK
