# Python and Object Oriented Programming

Through our research and collaboration with our industry partners, Make School has decided to focus on four core languages.

* **Python** - For computer science, data science, and whiteboard coding.
* **JavaScript** - For backend and front end web development
* **Swift** - For mobile iOS development
* **Ruby** - For backend API and web development

We use Python for our computer science courses because of its beautiful and elegant syntax, its wide-spread use across finance, data science, and web development, and because of its classical, object-oriented structure.

# Try Python

Complete [Try Python](https://www.codeschool.com/courses/try-python) (2 hours), a gentle introductory tutorial to the language with fun videos.

# HackerRank Python Challenges

Hacker Rank is a fantastic tool to drill coding and algorithmic problem solving. HackerRank will automatically test all your code submissions for correctness.

Create an account and complete all the challenge sets:

1. [Introductory Challenges](https://www.hackerrank.com/domains/python/py-introduction) (1 hour)
1. [Basic Data Types](https://www.hackerrank.com/domains/python/py-basic-data-types) (1 hour)
1. [Strings](https://www.hackerrank.com/domains/python/py-strings)

# Intro to OOP - 6 Videos

Settle in and get ready for some more videos :D - Watch these 6 videos for [Python OOP Tutorials](https://www.youtube.com/watch?v=ZDa-Z5JzLYM&list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc) by Corey Schafer.

Pay attention to the following words and how they are used:

* Class
* Instance
* Assignment
* Method
* Class Variables
* Static Method
* Class Methods
* Instance method
* Inheritance
* `self`
* `print()`

# Intro to OOP - Hands On

Object-Oriented Programming is a common and useful **coding paradigm**, one way to organize code and code's functionality. Object-Oriented programming is best understood through examples of classes. (This example is taken from [An Introduction to Classes and Inheritance](http://www.jesshamrick.com/2011/05/18/an-introduction-to-classes-and-inheritance-in-python/) by Jess Hamrick)

Let's look at a Pet class written in python. Open your terminal and create a file called `pets.py` and then open it in atom.

```bash
$ touch pets.py
$ atom pets.py
```

Now copy and paste the following code the file called `pets.py` and save it with the keyboards shortcut Command+S.

```py
class Pet(object):

    def __init__(self, name, species):
        self.name = name
        self.species = species

    def getName(self):
        return self.name

    def getSpecies(self):
        return self.species

    def __str__(self):
        return "%s is a %s" % (self.name, self.species)
```

Now let's look at how this code will work if we want to create some instances of the Pet class in the command line. Open your terminal in the directory where `pets.py` lives and type `python` to begin a python REPL. Now try the following code in the python REPL.

```py
# Polly the Parrot
>>> from pets import Pet
>>> polly = Pet("Polly", "Parrot")
>>> polly.getName()
>>> polly.getSpecies()
>>> print polly

# Ginger the Cat
>>> ginger = Pet("Ginger", "Cat")
>>> ginger.getName()
>>> ginger.getSpecies()
>>> print ginger

# Clifford the Dog
>>> clifford = Pet("Clifford", "Dog")
>>> clifford.getName()
>>> clifford.getSpecies()
>>> print clifford
```

Now let's add two **Subclasses** to Pet called Dog and Cat. These subclasses **Inherit** from their **Superclass** Pet. Add the following two subclasses to the `pets.py` file

```py
...

class Dog(Pet):

    def __init__(self, name, chases_cats):
        Pet.__init__(self, name, "Dog")
        self.chases_cats = chases_cats

    def chasesCats(self):
        return self.chases_cats

class Cat(Pet):

    def __init__(self, name, hates_dogs):
        Pet.__init__(self, name, "Cat")
        self.hates_dogs = hates_dogs

    def hatesDogs(self):
        return self.hates_dogs
```

Let's see how these work now

```python
>>> from pets import Pet, Dog
>>> mister_pet = Pet("Mister", "Dog")
>>> mister_dog = Dog("Mister", True)
>>> isinstance(mister_pet, Pet)
>>> isinstance(mister_pet, Dog)
>>> isinstance(mister_dog, Pet)
>>> isinstance(mister_dog, Dog)
>>> mister_pet.chasesCats()
>>> mister_dog.chasesCats()
>>> mister_pet.getName()
>>> mister_dog.getName()
```

Now create a bunch of cats and dogs.

```python
>>> from pets import Cat, Dog
>>> fido = Dog("Fido", True)
>>> rover = Dog("Rover", False)
>>> mittens = Cat("Mittens", True)
>>> fluffy = Cat("Fluffy", False)
>>> print fido
>>> print rover
>>> print mittens
>>> print fluffy
>>> print "%s chases cats: %s" % (fido.getName(), fido.chasesCats())
>>> print "%s chases cats: %s" % (rover.getName(), rover.chasesCats())
>>> print "%s hates dogs: %s" % (mittens.getName(), mittens.hatesDogs())
>>> print "%s hates dogs: %s" % (fluffy.getName(), fluffy.hatesDogs())
```

Can you answer the following questions:

* What is a 'class'? What is an example of a class besides pets and dogs and cats?
* How are classes used in OOP?
* What is 'inheritance'? What is an example of inheritance?

# Make School's OOP Challenge

This is a fun story-driven tutorial that teaches the major concepts of OOP (classes, objects, instance methods, inheritance, polymorphism, and composition). Please complete in Python. You can also complete it in Swift, Python, JavaScript, Java, or C++;

Complete Make School's [OOP Coding Challenge](http://hr.gs/ooptest) (1-2 hours)
