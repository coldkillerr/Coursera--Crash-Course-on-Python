<h1>Lists Defined</h1>

Lists in Python are defined using square brackets, with the elements stored in the list separated by commas:

`list = ["This", "is", "a", "list"]`. 

You can use the `len()` function to return the number of elements in a list:

`len(list)` would return 4. 

You can also use the `in` keyword to check if a list contains a certain element. If the element is present, it will return a `True` boolean. If the element is not found in the list, it will return `False`. For example, `"This" in list` would return `True` in our example. 

Similar to strings, lists can also use `indexing` to access specific elements in a list based on their position. You can access the first element in a list by doing `list[0]`, which would allow you to access the string "This".


In Python, lists and strings are quite similar. They’re both examples of sequences of data. Sequences have similar properties, like 

1) being able to iterate over them using for loops; 

2) support indexing;

3) using the len function to find the length of the sequence;

4) using the plus operator + in order to concatenate; and

5) using the in keyword to check if the sequence contains a value.


Understanding these concepts allows you to apply them to other sequence types as well.

<h1>Modifying Lists</h1>

While lists and strings are both sequences, a big difference between them is that lists are mutable. This means that the contents of the list can be changed, unlike strings, which are immutable. You can add, remove, or modify elements in a list.

You can add elements to the end of a list using the append method. You call this method on a list using dot notation, and pass in the element to be added as a parameter. For example, `list.append("New data")` would add the string `"New data"` to the end of the list called list.

If you want to add an element to a list in a specific position, you can use the method insert. The method takes two parameters: the first specifies the index in the list, and the second is the element to be added to the list. So `list.insert(0, "New data")` would add the string `"New data"` to the `front of the list`. This wouldn't overwrite the existing element at the start of the list. It would just shift all the other elements by one. If you specify an index that’s larger than the length of the list, the element will simply be added to the end of the list.

You can remove elements from the list using the `remove` method. This method takes an element as a parameter, and removes the first occurrence of the element. If the element isn’t found in the list, you’ll get a `ValueError` error explaining that the element was not found in the list.

You can also remove elements from a list using the pop method. This method differs from the remove method in that it takes an index as a parameter, and returns the element that was removed. This can be useful if you don't know what the value is, but you know where it’s located. This can also be useful when you need to access the data and also want to remove it from the list.

Finally, you can change an element in a list by using indexing to overwrite the value stored at the specified index. For example, you can enter `list[0] = "Old data"` to overwrite the first element in a list with the new string `"Old data"`.

<h1>Iterating Over Lists Using Enumerate</h1>

When we covered for loops, we showed the example of iterating over a list. This lets you iterate over each element in the list, exposing the element to the for loop as a variable. But what if you want to access the elements in a list, along with the index of the element in question? You can do this using the `enumerate()` function. 

<b>The enumerate() function</b> takes a list as a parameter and returns a tuple for each element in the list. The first value of the tuple is the index and the second value is the element itself.

<h1>List Comprehensions</h1>

You can create lists from sequences using a for loop, but there’s a more streamlined way to do this:
list comprehension.

List comprehensions allow you to create a new list from a sequence or a range in a single line.

For example, `[ x*2 for x in range(1,11) ]` is a simple list comprehension. This would iterate over the range 1 to 10, and multiply each element in the range by 2. This would result in a list of the multiples of 2, from 2 to 20.

You can also use conditionals with list comprehensions to build even more complex and powerful statements. You can do this by appending an if statement to the end of the comprehension. For example, `[ x for x in range(1,101) if x % 10 == 0 ]` would generate a list containing all the integers divisible by 10 from 1 to 100. The if statement we added here evaluates each value in the range from 1 to 100 to check if it’s evenly divisible by 10. If it is, it gets added to the list.

List comprehensions can be really powerful, but they can also be super complex, resulting in code that’s hard to read. Be careful when using them, since it might make it more difficult for someone else looking at your code to easily understand what the code is doing.
