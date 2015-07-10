---
tags: hashes, iteration
languages: ruby
type: TODO
resources: 1
---

# Key For Min Value

## Objective

Build a method that finds the key in a hash whose value is the lowest.

## Examples

Here are some examples of ideal behavior:

```ruby
ikea = {:chair => 25, :table => 85, :mattress => 450}
key_for_min_value(ikea)
# => :chair

veggies = {"apple" => -45, "banana" => -44.5, "carrot" => -44.9}
key_for_min_value(veggies)
# => "apple"
```

## Instructions

Since some Ruby methods will help you find the solution very easily, the following methods are forbidden:

* `#keys`
* `#values`
* `#min`
* `#sort`
* `#min_by`

We want you to build this out on your own so if a method seems like a shortcut, it probably is. Run your testing suite to get started.
