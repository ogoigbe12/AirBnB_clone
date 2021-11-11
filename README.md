## AirBnB clone - The console
### Learning Objectives

General

    How to create a Python package
    How to create a command interpreter in Python using the cmd module
    What is Unit testing and how to implement it in a large project
    How to serialize and deserialize a Class
    How to write and read a JSON file
    How to manage datetime
    What is an UUID
    What is *args and how to use it
    What is **kwargs and how to use it
    How to handle named arguments in a function

First step: Write a command interpreter to manage your AirBnB objects

This is the first step towards building your first full web application: the AirBnB clone. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration.

Each task is linked and will help you to:

    put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
    create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
    create all classes used for AirBnB (User, State, City, Place) that inherit from BaseModel
    create the first abstracted storage engine of the project: File storage.
    create all unittests to validate all our classes and storage engine

Whats a command interpreter?

Do you remember the Shell? Its exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

    Create a new object (ex: a new User or a new Place)
    Retrieve an object from a file, a database etc
    Do operations on objects (count, compute stats, etc)
    Update attributes of an object
    Destroy an object

### Execution

Your shell should work like this in interactive mode:

$ ./console.py

(hbnb) help

Documented commands (type help ):

========================================

EOF help quit

(hbnb)

(hbnb)

(hbnb) quit

$

But also in non-interactive mode: (like the Shell project in C)

$ echo "help" | ./console.py

(hbnb)

Documented commands (type help ):

========================================

EOF help quit

(hbnb)

$

$ cat test_help

help

$

$ cat test_help | ./console.py

(hbnb)

Documented commands (type help ):

========================================

EOF help quit

(hbnb)

$
### Examples

    (hbnb)create BaseModel
    49faff9a-6318-451f-87b6-910505c55907
    (hbnb)show BaseModel 49faff9a-6318-451f-87b6-910505c55907
    [BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'updated_at': datetime.datetime(2021, 2, 18, 18, 4, 12, 756946), 'created_at': datetime.datetime(2021, 2, 18, 18, 4, 12, 75683\
    6), 'id': '49faff9a-6318-451f-87b6-910505c55907'}
    (hbnb)update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"
    (hbnb)show BaseModel 49faff9a-6318-451f-87b6-910505c55907
    [BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}
    (hbnb)destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907
    (hbnb)show BaseModel 49faff9a-6318-451f-87b6-910505c55907
    ** no instance found **
    (hbnb) quit

### Authors

Samuel Ogoigbe

Mark Tanui
