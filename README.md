# Ruby Variables, Types, and Methods

## SWBATS (Students Will Be Able To)
- Assign names to values with variables
- Create numbers
- Use basic number operators - `+`, `-`, `*`, `/`
- Distinguish strings from code
- Use basic string methods, `+`, `.length`, `.downcase`, `.upcase`
- Create arrays, add elements, and access them
- Recognize `nil` values
- Define methods with `def`

![](https://media.giphy.com/media/CjmvTCZf2U3p09Cn0h/giphy-downsized.gif)

## Outline

```text
 5m Introduce variables and types
 5m Demonstrate number methods
 5m Strings and string methods
 5m Arrays and array access
 5m Booleans and Nil
10m Methods
--
35m Total
```

## Variables

- When we use `""` to create a string, or mention a number like `5`, we are using it _literally_
- We don't always know what the value is going to be when we are writing the program - we need a way to refer to data without using the literal value
- We can use _variables_!
- You've seen this before in math class!
- In ruby, we can assign a name to a value like `name="Dana"` or `number=3`
- Then, when we mention `name` or `number` later, we get the value out!
- Demonstrate in REPL
- Demonstrate in ruby files

```ruby
> name = "Dana"
=> "Dana"
> name
=> "Dana"
> number = 3
=> 3
> number
3
```


## Types: Strings, Numbers, Arrays

- When we are programming, our values have different _types_
- We want to perform different operations depending on what kind of data something is
- If it's a number, we want to do "mathy" things with it
- If it's text, we want to do "texty" things with it
- We're going to focus on Numbers, Strings, and Arrays

### Numbers

- We can create a number in ruby by typing the number - `5` or `-100` or `61342`
- Ruby also knows how to do math
- We can use operations like `+` and `*` and `-` and `/`

```ruby
> 5 + 5
=> 10
> 3 * 4
=> 12
> 9 - 8
=> 1
> 100 / 10
> 10
```

- Ruby also knows some more fancy operators!

- `**` for exponents:

```ruby
> 6 ** 2
=> 36
> 8 ** 2
=> 64
> 3 ** 3
=> 27
```

What other operators can you find? Try looking up more ruby number operators with Google and the Ruby docs!

### Strings
- In order to distinguish the _text we want to print_ from the _code that we want to execute_, we wrap our words in `"quote marks"`.
- In ruby, these _things in quotes_ are called **Strings**
- What kinds of operations can we do on Strings?

`+` adds strings together:

```ruby
> "cat" + "dog"
=> "catdog"
> "I'm going to the" + " store " + " to buy " + " some groceries " + "."
```

`.length` reports on the string's length:

```ruby
> "abracadabra".length
=> 11
> "Zap".length
=> 3
> "Zap!".length
=> 4
```

`.upcase` creates an UPPERCASE version of the string
```ruby
> "shouting".upcase
=> "SHOUTING"
```

Similarly, `.downcase` returns a lowercase version

```ruby
> "ALAKAZAM!".downcase
=> "alakazam!"
```

There are lots of other string methods! Browse the ruby docs to see more.

### Arrays

- Arrays are lists of values
- We use `[]` to create arrays


```ruby
> array = [1,2,3]
=> [1,2,3]
```

- We can add new values to the array with the `<<` "shovel" method

```ruby
> array << 4
=> [1,2,3,4]
```

- We can get an item out of the array ('access' it) with `[]`

```ruby
> array[0]
=> 1
> array[1]
=> 2
```

- Notice that array indices start at `0` - the first element is the 0th element, the second element has index `1`, etc.



### Nil
- Sometimes we want to represent that 'nothing is there'
- We use a special value `nil` to mean 'nothing'

```ruby
> nil
=> nil
```

It'll pop up, so that's what it means when you see it.

## Methods

- Typing everything that happens every time is annoying
- DRY - don't repeat yourself!
- Instead of copying and pasting, lets write a method!
- A _method_ in ruby is a set of instructions that we can run later (the word _function_ is used interchangeably)
- we create a method with

```ruby
def greet
  # body of method
  puts "Hello, world!"
end
```

- We run the method ("call" or "invoke" the method) by calling its name

```ruby
greet
```

## Arguments

- We want to be able to customize our methods
- Methods can take input
- We declare what _arguments_ a method takes when we define the method
- We can refer to those arguments in the body of the method, and customize what the method does

```ruby
def greet_person(name)
  puts "Hello, " + name
end
```

- Then we "pass in" values when we call the method

```ruby
greet_person("Rob")
```

If we want methods to accept more than one argument, we mention multiple arguments when we define the method
```ruby
def print_product(first, second)
  puts first * second
end

print_product(6, 7)
```

The order of the values that we pass in is important! Each argument will get 'matched up' with the argument in that position in the method's definition.

```ruby
def print_in_order(name_one, name_two, name_three, name_four)
  puts "Hello " + name_one
  puts "Welcome " + name_two
  puts "Hi " + name_three
  puts "Greetings, " + name_four
end

print_in_order("Hillary", "Jake", "Ann", "Rob")
```

If we pass in the values in a different order, the values will be assigned to different names in the body of the method

```ruby
print_in_order("Rob", "Hillary", "Jake", "Ann")
print_in_order("Ann", "Rob", "Hillary", "Jake")
```

### Labs
- [Variable Assignment Lab](https://learn.co/tracks/full-stack-web-development-v6/intro-to-ruby-development/variables/variable-assignment-lab)
- [Tic Tac Toe Board](https://learn.co/tracks/full-stack-web-development-v6/intro-to-ruby-development/variables/tic-tac-toe-board)
- [Say Hello](https://learn.co/tracks/full-stack-web-development-v6/intro-to-ruby-development/methods/say-hello)
- [Display Tic Tac Toe Board](https://learn.co/tracks/full-stack-web-development-v6/intro-to-ruby-development/methods/display-tic-tac-toe-board)
