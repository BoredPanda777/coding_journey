# Python Notes

## Basics

* Python is case sensitive.
* To print a message: `print("Hello, World")`
* To run a script, `type python filenamehere.py`
* To start the REPL, simply type *python* into the terminal.
* To see how does a function work, type `help(print)`.
* To clear the console, use the `clear` command.
* To set a variable, `name_of_variable = "What we are referring to"`
* To use the user's input as a variable, `first_name = input"What is your name?`.
  

## Math Operations

* `1 + 2`
* `2 - 1`
* `3 * 7`
* `10 / 2` *= 5.0*
* `10 // 2` *= 5*
* `7 % 3` *= 1* (The remainder)
* `6 % 2` = 0 (The remainder)
* `4 ** 2` = 16 (X to the power of Y)
* `5 > 3`
* `5 >= 4`
* `6 <= 7`
* `3 < 6`
* `round(4.3)` *= 4*
* `round(4.9)` *= 5*
* `int(11.23)` *= 11*
* `float(12)` *= 12.0*
* integer + integer = integer
* float + float = float
* integer + float  = float
* integer + integer + float= float



## Strings

* `'This is a string'`
* `"This is also a string"`
* `"""They said, "Yes! This is a string"."""`
* `\n` to skip one line in strings.
* `"chocolate" + " and marshmallows"` = *"chocolate and marshmallows"*
* `dessert = "chocolate" + "and marshmallows"` *= chocolate and marshmallows*
* `dessert += ", yum"` *= chocolate and marshmallows, yum*
* `len("USA")` *= 3*
* `"hi".upper()` *= HI*
* `"HI".lower()` *= hi*
* `"Hi, how are you?".title()` *=Hi, How Are You?*
* `quote.count(string)` Counts the number of time a string was mentioned in a quote. Note it is case sensitive and only returns the first time the string has appeared.
* `str(42)` Converts it to a string.
* `quote.rstrip()`
* `quote.lstrip()`
* `quote.strip()`



## Templates

* `print("Bye {}!".format("Nihad"))` *=Bye Nihad!*
* `example = "Hi {}!"`
  `example.format("Nihad")` *= Hi Nihad!*



## Booleans

* `bool(0)` *= False*
* `bool(42)` *= True*
* The result of `bool(a and b)` is **true** if **both** are true. Otherwise, it would be false.
* The result of `bool(a or b)` is **true** if **at least one** of a is true or b is true. Otherwise, it is false.
* It is also possible to use **not false** and **not true**.



## Conditions and loops

* `"Test" == "Test"` *= True*

* `"Yay" != "Nay"` *= True*

* ```python
  river = "mississippi"
  
  for letter in river:
      print("* " + letter.upper())
  ```

* ```python
  name = input("What is your name?")
  
  if name == "Justin":
      print(name, "is learning Python")
  elif name == "Max":
      print("I miss you", name)
  else:
      print("You are not learning anything!")
  ```

* ```python
  import sys
  
  username = "max123"
  prompt = input("Please enter your username...")
  
  attempt = 1
  while prompt != username:
      if attempt > 3:
          sys.exit("Too many invalid tries")
      prompt = input("You entered an invalid username. Please try again...")
      attempt += 1
      
  print("Weclome!")
  ```

  

## Functions

* ```python
  def rect_surafce(a, b):
      result = a * b
      print(result)
  
  side_a = int(input("What is the lenght of side A?"))
  side_b = int(input("What is the lenght of sibe B?"))
  
  rect_surafce(side_a, side_b)
  ```




## Error Handling

* ```python
  def rect_surafce(a, b):
      result = a * b
      print(result)
      
  try:
  	side_a = int(input("What is the lenght of side A?"))
  	side_b = int(input("What is the lenght of sibe B?"))
  except ValueError:
      print("Please enter a valid number...")
  else:
      rect_surafce(side_a, side_b)
  ```

  

## Lists

* `listname = ["item1", "item2", "item3", "item4"]`
  `listname [0]` *= item1*
  `listname [1]` *=item2*
  `listname [-1]` *= item4*
* `listname [2] = ("new item")`
* `listname [3] += ("addition")`
* `list = [1, 2, 3]`
  `list.extend([4, 5, 6])` *list = [1, 2, 3, **4, 5, 6**]*
* `list = [1, 2, 3]`
  `list.append([4, 5, 6])` *list = [1, 2, 3, **[4, 5, 6]**]*
* `list.insert(0, "item1")`
* `names = ["Jack, "Max", "Tom"]`
  `del names [0]` *names = ["Max", "Tom"]*
  `names.remove("Max")` *names = ["Jack", "Tom"]*
  `names.pop(0)` *names = ["Max", "Tom"]* **+** *Python returns the value*
* `grades = [5.3, 4.7, 3.8]`
  `gradesbackup = grades.copy()`
* `quote = "To be or"`
  `words = quote.split(" ")` *words = ["To", "be", "or"]
* `students = ["Lucy", "Anna", "Katy"]`
  `names = ", ".join(students)` *= 'Lucy, Anna, Katy'*
* `prices = [5.7, 8.9, 7.4]`
  `sum(prices)` *= 22.0*
  `min(prices)` *= 5.7*
  `max(prices)` *= 8.9*



## Tupils

* `example = ("age", "location", "occupation")`

* `example = "age", "location", "occupation"`

* `example [0]` *= "age"*

* ```python
  def total(*args):
      total=sum(args)
      print(total)
      
  total(25, 100, 250, 300, 75)
  ```

* ```python
  def unpacker():
      return(1, 2, 3)
  
  var1, var2, var3 = unpacker()
  ```

* `first, last = input("Enter your full name:").split(" ")`



## Sequences

* `alphabet = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']`
  `alpahbet[0]` *= "A"*
  `alpahbet[1:4]` *= ['B', 'C', 'D']*
  `alphabet[3:]` *= ['D', 'E', 'F', 'G', 'H']*
  `alphabet[::2]` *= ['A', 'C', 'E', 'G']*
  `alphabet[::-1]` *= ['H', 'G', 'F', 'E', 'D', 'C', 'B', 'A']*

* ```python
  x = range(3, 20, 2)
  for number in x:
    print(number)
  ```

* ```python
  letters = ["a", "b", "c", "d", "e"]
  
  for index, item in enumerate(letters, 1):
  	print("{}. {}".format(index, item))
  ```

  

## Dictionaries

* `user = {"name":"Paula", "city":"Berlin", "age":24}`

* `user["name"] = "Ben"`

* `user["name"]` *= "Paula"

* `user.keys()` *= ["name", "city", "age"]*

* `user.values()` *= ["Paula", "Berlin", 24]

* `del(user["age"])`

* ```python
  for key, value in user.items():
  	print(key)
  	print(value)
  ```

* ```python
  def announce(**kwargs):
  	for key, value in kwargs.items():
  		print('{}: {}'.format(key, value))
  		
  announce(name='Dora', job='Manager', country='USA')
  ```



## Dunder Main

* `__name__ == '__main__'`

* ```python
  if __name__ == '__main__':
      print("This is the main file.")
  ```

  