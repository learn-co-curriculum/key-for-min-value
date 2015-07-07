# Manipulating Hashes: Iteration

## Objectives

1. Understand how to iterate over hashes
2. Practice iterating over hashes

In this lesson, we'll be learning how to use lower level iterators like `.each` on a hash. Then, you'll complete the lab challenge. In the next lesson, we'll be introduced to some higher level hash methods. 

## Iterating Over Hashes

Previously, we've compared hashes to dictionaries or storage containers. Just like with these storage methods in real life, we'll find we need not only to access our stored information but to operate on it, change it, collect it etc. 

The `.each` and `.collect` iterators that we encountered in previous units are also used to iterate over hashes. However, when we iterate over arrays, we iterate over one element at a time: each index in an array contains just one object. In a hash, data is stored in key/value pairs, so we will be iterating over *pairs*. Let's take a look: 

```ruby
hash = {key1: "value1", key2: "value2"}

hash.each do |key, value|
	puts "#{key}, #{value}"
end
```

When we iterate over a hash, the `.each` method yields the key/value pair *together* to the block. Inside that block, you have access to the key and the value and can manipulate them. 

Drop into IRB and copy and paste the above code. You should see this output: 

```ruby
key1, value1
key2, value2
 => {:key1=>"value1", :key2=>"value2"} 
```

Inside the iteration, we have access to and can puts out the key and value of a single pair. Then, the return value is the original hash. **Remember that `.each` returns the original collection on which you are calling the method.**

Let's take a look at one more example of iteration and manipulation before you try it on your own:

## Example: Cruise Ship	

The good news is you're on a cruise ship! The bad news is that you're not on vacation. You are a cruise ship director and you're selecting the day's lucky winner of free tickets to the 8:00 magic show in the super swanky Blue Room. The criteria for picking the winner is that this person must be staying in Suite A and their name must start with "A". We have a hash of passengers that looks like this: 

```ruby
passengers = {
suite_a: "Amanda Presley", 
suite_b: "Seymour Hoffman", 
suite_c: "Alfred Tennyson", 
suite_d: "Charlie Chaplin", 
suite_e: "Crumpet the Elf"
}
```

We need to iterate over that hash and collect the name of the passenger who is staying in Suite A *and* whose name begins with "A". Let's give it a shot: 

```ruby
winner = ""
passengers.each do |suite, name|
	if suite == :suite_a && name.start_with?("A")
		winner = name
	end
end

winner	
```
Let's break this down: 

* We iterate through the hash using `.each`. We chose `.each` instead of collect because we don't want to collect the key/value pair that contains the winner, just the *name* of the winner. With `.each`, we have the control we need to simple grab the winner's name and set it equal to a variable that we can return later on. 
* Inside our iteration, we use an `if` statement combined with the `&&` boolean operator to check if we have the right suite and if the person in that suite has a name that begins with "A". 
* If that condition returns true, we've found our winner! We set their name equal to the `winner` variable and end our iteration. 
* Then, we call on our `winner` variable to return the name of the lucky winner. 

This is just one example of how iterating over hashes allows us to access and manipulate the values that they contain. Now, try it out by following the instructions for completing this lab below. 


## Instructions 

1. Fork and clone this lab
2. Build a method `key_for_min_value` that accepts an argument of a hash. This method should iterate over the hash and return the *key* (not the value!) that points to the smallest value of the set. If the method is called and passed an argument of an empty hash, it should return `nil`. 

Here are some examples: 

```ruby
ikea = {:chair => 25, :table => 85, :mattress => 450}
key_for_min_value(ikea)
# => :chair

veggies = {"apple" => -45, "banana" => -44.5, "carrot" => -44.9}
key_for_min_value(veggies)
# => "apple"
```

**A Few Restrictions:**
We want you to build this on your own. Some of the following methods are helpful but off limits for this exercise. We're going to learn more about them in the next lesson: 
since some Ruby methods will help you find the solution very easily, the following methods are forbidden:

* `#keys`
* `#values`
* `#min`
* `#sort`
* `#min_by`

**A Helpful Hint:** 

* Think about how to determine which value is the lowest. Do you need to compare each value to something as you iterate? 
* Think about how to collect/store the correct key. Remember that you need your method to return *just this key*. 
