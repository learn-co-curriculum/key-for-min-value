# Key For Minimum Value

## Objectives

1. Build a method that accepts an argument of a hash and iterates over it.

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
We want you to build this on your own. Some of the following methods are helpful but ***off limits*** for this exercise. (We'll cover a few below in more depth in subsequent lessons). 

* `#keys`
* `#values`
* `#min`
* `#sort`
* `#min_by`

**A Helpful Hint:** 

* Think about how to determine which value is the lowest. Do you need to compare each value to something as you iterate? 
* Think about how to collect or store the correct key. Remember that you need your method to return *just this key*. 

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/key-for-min-value' title='Key For Minimum Value'>Key For Minimum Value</a> on Learn.co and start learning to code for free.</p>
