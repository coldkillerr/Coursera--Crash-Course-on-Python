
<h1>Object-Oriented Programming</h1>


<h2>Definition</h2>

In object-oriented programming, concepts are modeled as classes and objects. An idea is defined using a class, and an instance of this class is called an object. Almost everything in Python is an object, including strings, lists, dictionaries, and numbers. When we create a list in Python, we’re creating an object which is an instance of the list class, which represents the concept of a list. Classes also have attributes and methods associated with them. Attributes are the characteristics of the class, while methods are functions that are part of the class.

<h2> Classes and Objects </h2>

We can use the `type()` function to figure out what class a variable or value belongs to. For example, `type(" ")` tells us that this is a `string class`. The only attribute in this case is the string value, but there are a bunch of methods associated with the class. We've seen the `upper()` method, which returns the string in `all uppercase`, as well as `isnumeric()` which returns a `boolean` telling us whether or not the `string is a number`. You can use the `dir()` function to print all the `attributes and methods` of an object. Each string is an instance of the string class, having the same methods of the parent class. Since the content of the string is different, the methods will return different values. You can also use the `help()` function on an object, which will return the documentation for the corresponding class. This will show all the methods for the class, along with parameters the methods receive, types of return values, and a description of the methods.
