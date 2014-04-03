RubySnippets
============

###Object Oriented
```ruby
  # Output "UPPER"
  puts "upper".upcase
  # Output the absolute value of -5:
  puts -5.abs
  # Output "Ruby Rocks!" 5 times
  5.times do
  puts "Ruby Rocks!"
  end
```

###Classes begin with class and end with end

```ruby
  class Person
  end
```

###Methods begin with class  and end with end
```ruby
  def sayHello
    puts "Hello World"
  end
```

###Blocks
```ruby
  # Print out a list of of people from
  # each person in the Array
  people.each do |person|
    puts "* #{person.name}"
  end
  
  # A block using the bracket syntax
  5.times { puts "Ruby rocks!" }
  
  #yield to the block
  # define the thrice method
  def thrice
    yield
    yield
    yield 
  end
  
  # Output "Blocks are cool!" three times
  thrice { puts "Blocks are cool!" 

```

##Functional Programming
```ruby
  lam = lambda { |x| puts x*2 }
  [1,2,3].each(&lam)
```


##Modules
```ruby
module WarmUp
  def push_ups
    "Phew, I need a break!"
  end
end

class Gym
  include WarmUp
  
  def preacher_curls
    "I'm building my biceps."
  end
end

class Dojo
  include WarmUp
  
  def tai_kyo_kyu
    "Look at my stance!"
  end
end

puts Gym.new.push_ups
puts Dojo.new.push_ups
```

##Dynamic Typing and Introspection
```ruby
  # The Duck class
  class Duck
    def quack
      puts "quack!"
    end
  end
# The Mallard class (without inheritance)
  class Mallard
    def quack
      puts "qwuaacck!! quak!"
    end
  end
  
  def quack_em(ducks)
    ducks.each do |duck|
      if duck.respond_to? :quack
        duck.quack
      end
    end 
  end
  
  birds = [Duck.new, Mallard.new, Object.new]
  quack_em(birds)
```

##Method Missing
```ruby
  class Proxy
    def initialize(object)
      @object = object
    end
    def method_missing(symbol, *args)
      @object.send(symbol, *args)
   end 
  end
  
  object = ["a", "b", "c"]
  proxy = Proxy.new(object)
  puts proxy.first # Outputs: "a"
  
  
  
```



###
