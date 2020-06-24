
<h1>Object-Oriented Programming</h1>


<h2>Definition</h2>

In object-oriented programming, concepts are modeled as classes and objects. An idea is defined using a class, and an instance of this class is called an object. Almost everything in Python is an object, including strings, lists, dictionaries, and numbers. When we create a list in Python, we’re creating an object which is an instance of the list class, which represents the concept of a list. Classes also have attributes and methods associated with them. Attributes are the characteristics of the class, while methods are functions that are part of the class.

<h2> Classes and Objects </h2>

We can use the `type()` function to figure out what class a variable or value belongs to. For example, `type(" ")` tells us that this is a `string class`. The only attribute in this case is the string value, but there are a bunch of methods associated with the class. We've seen the `upper()` method, which returns the string in `all uppercase`, as well as `isnumeric()` which returns a `boolean` telling us whether or not the `string is a number`. You can use the `dir()` function to print all the `attributes and methods` of an object. Each string is an instance of the string class, having the same methods of the parent class. Since the content of the string is different, the methods will return different values. You can also use the `help()` function on an object, which will return the documentation for the corresponding class. This will show all the methods for the class, along with parameters the methods receive, types of return values, and a description of the methods.

<h2>Defining Classes</h2>

We can create and define our classes in Python similar to how we define functions. We start with the class keyword, followed by the name of our class and a colon. Python style guidelines recommend class names to start with a capital letter. After the class definition line is the class body, indented to the right. Inside the class body, we can define attributes for the class.

Let's take our Apple class example:

``` python
>>> class Apple:
...     color = ""
...     flavor = ""
... 
```


We can create a new instance of our new class by assigning it to a variable. This is done by calling the class name as if it were a function. We can set the attributes of our class instance by accessing them using dot notation. Dot notation can be used to set or retrieve object attributes, as well as call methods associated with the class.

```python
>>> jonagold = Apple()
>>> jonagold.color = "red"
>>> jonagold.flavor = "sweet"
```

We created an Apple instance called jonagold, and set the color and flavor attributes for this Apple object. We can create another instance of an Apple and set different attributes to differentiate between two different varieties of apples.

```python
>>> golden = Apple()
>>> golden.color = "Yellow"
>>> golden.flavor = "Soft"
```


We now have another Apple object called golden that also has color and flavor attributes. But these attributes have different values.

<h2>What Is a Method?</h2>

Calling methods on objects executes functions that operate on attributes of a specific instance of the class. This means that calling a method on a list, for example, only modifies that instance of a list, and not all lists globally. We can define methods within a class by creating functions inside the class definition. These instance methods can take a parameter called self which represents the instance the method is being executed on. This will allow you to access attributes of the instance using dot notation, like self.name, which will access the name attribute of that specific instance of the class object. When you have variables that contain different values for different instances, these are called instance variables.


<h2>Special Methods</h2>

Instead of creating classes with empty or default values, we can set these values when we create the instance. This ensures that we don't miss an important value and avoids a lot of unnecessary lines of code. To do this, we use a special method called a constructor. Below is an example of an Apple class with a constructor method defined.

```python
>>> class Apple:
...     def __init__(self, color, flavor):
...         self.color = color
...         self.flavor = flavor
```


When you call the name of a class, the constructor of that class is called. This constructor method is always named __init__. You might remember that special methods start and end with two underscore characters. In our example above, the constructor method takes the self variable, which represents the instance, as well as color and flavor parameters. These parameters are then used by the constructor method to set the values for the current instance. So we can now create a new instance of the Apple class and set the color and flavor values all in go:

```python
>>> jonagold = Apple("red", "sweet")
>>> print(jonagold.color)
Red
```

In addition to the __init__ constructor special method, there is also the __str__ special method. This method allows us to define how an instance of an object will be printed when it’s passed to the print() function. If an object doesn’t have this special method defined, it will wind up using the default representation, which will print the position of the object in memory. Not super useful. Here is our Apple class, with the __str__ method added:

```python
>>> class Apple:
...     def __init__(self, color, flavor):
...         self.color = color
...         self.flavor = flavor
...     def __str__(self):
...         return "This apple is {} and its flavor is {}".format(self.color, self.flavor)
...
```


Now, when we pass an Apple object to the print function, we get a nice formatted string:

```python
>>> jonagold = Apple("red", "sweet")
>>> print(jonagold)
This apple is red and its flavor is sweet
```


This apple is red and its flavor is sweet

It's good practice to think about how your class might be used and to define a __str__ method when creating objects that you may want to print later.


