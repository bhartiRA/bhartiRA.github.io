---
layout: post
title:  "Object orientation"
date:   2016-12-02 21:14:49 +0000
---


Object Oriented Programming, often referred to as OOP, is a programming paradigm that was created to deal with the growing complexity of large software systems. Programmers found out very early on that as applications grew in complexity and size, they became very difficult to maintain. One small change at any point in the program would trigger a ripple effect of errors due to dependencies throughout the entire program.

Programmers needed a way to create containers for data that could be changed and manipulated without affecting the entire program. They needed a way to section off areas of code that performed certain procedures so that their programs could become the interaction of many small parts, as opposed to one massive blob of dependency.

Enter OOP. 

**Encapsulation** is hiding pieces of functionality and making it unavailable to the rest of the code base. It is a form of data protection, so that data cannot be manipulated or changed without obvious intention. It is what defines the boundaries in the application and allows the code to achieve new levels of complexity. Ruby, like many other OO languages, accomplishes this task by creating objects, and exposing interfaces (i.e., methods) to interact with those objects.

**Inheritance** : The concept of inheritance is used in Ruby where a class inherits the behaviors of another class, referred to as the superclass. This gives Ruby programmers the power to define basic classes with large reusability and smaller subclasses for more fine-grained, detailed behaviors. It allows us to define a class in terms of another class, which makes it easier to create and maintain an application.

Inheritance also provides an opportunity to reuse the code functionality and fast implementation time but unfortunately **Ruby does not support multiple levels of inheritances** but Ruby supports mixins. A mixin is like a specialized implementation of multiple inheritance in which only the interface portion is inherited.

When creating a class, instead of writing completely new data members and member functions, the programmer can designate that the new class should inherit the members of an existing class. This existing class is called the base class or superclass, and the new class is referred to as the derived class or sub-class.  The syntax for extending a class is simple. Just add a < character and the name of the superclass to your class statement


**Polymorphism** is the ability for data to be represented as many different types. "Poly" stands for "many" and "morph" stands for "forms". OOP gives us flexibility in using pre-written code for new purposes.

**A way to apply polymorphic structure to Ruby programs is to use a Module**. Modules are similar to classes in that they contain shared behavior. However, you cannot create an object with a module. A module must be mixed in with a class using the reserved word include. This is called a mixin. After mixing in a module, the behaviors declared in that module are available to the class and its objects.

Here's how we'd do it.

**# good_dog.rb**

module Speak
  def speak(sound)
    puts "#{sound}"
  end
end

class GoodDog
  include Speak
end

class HumanBeing
  include Speak
end

sparky = GoodDog.new
sparky.speak("Arf!")        # => Arf!
bob = HumanBeing.new
bob.speak("Hello!")         # => Hello!

Note that in the above example, both the GoodDog object, which we're calling sparky, as well as the HumanBeing object, which we're calling bob, have access to the speak instance method. This is possible through "mixing in" the module Speak. It's as if we copy-pasted the speak method into the GoodDog and HumanBeing classes.



