<h1>String Indexing and Slicing</h1>

String indexing allows you to access individual characters in a string. 
You can do this by using square brackets and the location, or index, of the character you want to access.
It's important to remember that Python starts indexes at 0. So to access the first character in a string, you would use the `index [0]`. If you try to access an index that’s larger than the length of your string, you’ll get an `IndexError`.
This is because you’re trying to access something that doesn't exist! You can also access indexes from the end of the string going towards the start of the string by using negative values. 
The `index [-1]` would access the last character of the string, and the `index [-2]` would access the second-to-last character.
You can also access a portion of a string, called a slice or a substring.
This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like `[2:5]`. This range is similar to the `range()` function we saw previously. It includes the first number, but goes to one less than the last number. You can also easily reference the start or end of the string by leaving one value blank. For example `[:5]` would give us all characters from the `start to the fourth character` in the string. We can also use `[5:]` to get the characters from the `fourth character to the end` of the string.

<h1>Basic String Methods</h1>

In Python, strings are immutable. This means that they can't be modified. So if we wanted to fix a typo in a string, we can't simply modify the wrong character. We would have to create a new string with the typo corrected. We can also assign a new value to the variable holding our string.

If we aren't sure what the index of our typo is, we can use the string method index to locate it and return the index. Let's imagine we have the string `"lions tigers and bears"` in the variable animals. We can locate the index that contains the `letter g` using `animals.index("g")`, which will return the index; in this case `8`. We can also use substrings to locate the index where the substring begins. `animals.index("bears")` would return `17`, since that’s the start of the substring. If there’s more than one match for a substring, the index method will return the first match. If we try to locate a substring that doesn't exist in the string, we’ll receive a `ValueError` explaining that the substring was not found.

We can avoid a `ValueError` by first checking if the substring exists in the string. This can be done using the in keyword. We saw this keyword earlier when we covered for loops. In this case, it's a conditional that will be either True or False. If the substring is found in the string, it will be `True`. If the substring is not found in the string, it will be `False`.

Using our previous variable animals, we can do `"horses" in animals` to check if the substring "horses" is found in our variable. In this case, it would evaluate to False, since horses aren’t included in our example string. If we did `"tigers" in animals`, we'd get `True`, since this substring is contained in our string.

<h1>Advanced String Methods</h1>

We've covered a bunch of String class methods already, so let's keep building on those and run down some more advanced methods.

The string method `lower` will return the string with all characters changed to lowercase. The inverse of this is the `upper` method, which will return the string all in uppercase. Just like with previous methods, we call these on a string using dot notation, like `"this is a string".upper()`. This would return the string `"THIS IS A STRING"`. This can be super handy when checking user input, since someone might type in all lowercase, all uppercase, or even a mixture of cases.

You can use the `strip` method to `remove surrounding whitespace from a string`. Whitespace includes spaces, tabs, and newline characters. You can also use the methods  `lstrip` and `rstrip` to remove whitespace only from the left or the right side of the string, respectively.

The method `count` can be used to return the number of times a substring appears in a string. This can be handy for finding out how many characters appear in a string, or counting the number of times a certain word appears in a sentence or paragraph.

If you wanted to check if a string ends with a given substring, you can use the method `endswith`. This will return `True if the substring is found at the end of the string`, and False if not.

The `isnumeric` method can check if a string is `composed of only numbers`. If the string contains only numbers, this method will return True. We can use this to check if a string contains numbers before passing the string to the int() function to convert it to an integer, avoiding an error. Useful!

We took a look at string concatenation using the plus sign, earlier. We can also use the `join` method to `concatenate strings`. This method is called on a string that will be used to join a list of strings. The method takes a list of strings to be joined as a parameter, and returns a new string composed of each of the strings from our list joined using the initial string. For example, `" ".join(["This","is","a","sentence"])` would return the string `"This is a sentence"`.

The inverse of the join method is the `split` method. This allows us to `split a string into a list of strings`. By default, it splits by any whitespace characters. You can also split by any other characters by passing a parameter.

<h1>String Formatting</h1>

You can use the format method on strings to concatenate and format strings in all kinds of powerful ways. To do this, create a string containing curly brackets, `{}`, as a placeholder, to be replaced. Then call the format method on the string using `.format()` and pass variables as parameters. The variables passed to the method will then be used to replace the curly bracket placeholders. This method automatically handles any conversion between data types for us. 

If the curly brackets are empty, they’ll be populated with the variables passed in the order in which they're passed. However, you can put certain expressions inside the curly brackets to do even more powerful string formatting operations. You can put the name of a variable into the curly brackets, then use the names in the parameters. This allows for more easily readable code, and for more flexibility with the order of variables.

You can also put a formatting expression inside the curly brackets, which lets you alter the way the string is formatted. For example, the formatting expression `{:.2f}` means that you’d format this as a `float number, with two digits after the decimal dot`. The colon acts as a separator from the field name, if you had specified one. You can also specify text alignment using the greater than operator: `>`. For example, the expression `{:>3.2f}` would align the text `three spaces to the right`, as well as specify a `float number with two decimal places`. String formatting can be very handy for outputting easy-to-read textual output.


