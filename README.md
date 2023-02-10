0x00. AirBnB clone - The console
Group project
Python
OOP
 By: Guillaume
 Weight: 5
 Project to be done in teams of 2 people (your team: Yisihake Kassa, Ephrem Fereja)
 Project will start Feb 6, 2023 6:00 AM, must end by Feb 13, 2023 6:00 AM
 Checker will be released at Feb 11, 2023 12:00 PM
 Manual QA review must be done (request it when you are done with the project)
 An auto review will be launched at the deadline
Concepts
For this project, we expect you to look at these concepts:

Python packages
AirBnB clone


Background Context
Welcome to the AirBnB clone project!
Before starting, please read the AirBnB concept page.






First step: Write a command interpreter to manage your AirBnB objects.
This is the first step towards building your first full web application: the AirBnB clone. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel
create the first abstracted storage engine of the project: File storage.
create all unittests to validate all our classes and storage engine
What’s a command interpreter?
Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

Create a new object (ex: a new User or a new Place)
Retrieve an object from a file, a database etc…
Do operations on objects (count, compute stats, etc…)
Update attributes of an object
Destroy an object
Resources
Read or watch:

cmd module
cmd module in depth
packages concept page
uuid module
datetime
unittest module
args/kwargs
Python test cheatsheet
cmd module wiki page
python unittest
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

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
Copyright - Plagiarism
You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
You are not allowed to publish any content of this project.
Any form of plagiarism is strictly forbidden and will result in removal from the program.
Requirements
Python Scripts
Allowed editors: vi, vim, emacs
All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
All your files should end with a new line
The first line of all your files should be exactly #!/usr/bin/python3
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the pycodestyle (version 2.8.*)
All your files must be executable
The length of your files will be tested using wc
All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
Python Unit Tests
Allowed editors: vi, vim, emacs
All your files should end with a new line
All your test files should be inside a folder tests
You have to use the unittest module
All your test files should be python files (extension: .py)
All your test files and folders should start by test_
Your file organization in the tests folder should be the same as your project
e.g., For models/base_model.py, unit tests must be in: tests/test_models/test_base_model.py
e.g., For models/user.py, unit tests must be in: tests/test_models/test_user.py
All your tests should be executed by using this command: python3 -m unittest discover tests
You can also test file by file by using this command: python3 -m unittest tests/test_models/test_base_model.py
All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
We strongly encourage you to work together on test cases, so that you don’t miss any edge case
GitHub
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

More Info
Execution
Your shell should work like this in interactive mode:

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
But also in non-interactive mode: (like the Shell project in C)

$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
All tests should also pass in non-interactive mode: $ echo "python3 -m unittest discover tests" | bash






Tasks
0. README, AUTHORS
mandatory
Write a README.md:
description of the project
description of the command interpreter:
how to start it
how to use it
examples
You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository. For format, reference Docker’s AUTHORS page
You should use branches and pull requests on GitHub - it will help you as team to organize your work
Repo:

GitHub repository: AirBnB_clone
File: README.md, AUTHORS
 
1. Be pycodestyle compliant!
mandatory
Write beautiful code that passes the pycodestyle checks.

Repo:

GitHub repository: AirBnB_clone
  
2. Unittests
mandatory
All your files, classes, functions must be tested with unit tests

guillaume@ubuntu:~/AirBnB$ python3 -m unittest discover tests
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK
guillaume@ubuntu:~/AirBnB$
Note that this is just an example, the number of tests you create can be different from the above example.

Warning:

Unit tests must also pass in non-interactive mode:

guillaume@ubuntu:~/AirBnB$ echo "python3 -m unittest discover tests" | bash
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK
guillaume@ubuntu:~/AirBnB$
Repo:

GitHub repository: AirBnB_clone
File: tests/
  
3. BaseModel
mandatory
Write a class BaseModel that defines all common attributes/methods for other classes:

models/base_model.py
Public instance attributes:
id: string - assign with an uuid when an instance is created:
you can use uuid.uuid4() to generate unique id but don’t forget to convert to a string
the goal is to have unique id for each BaseModel
created_at: datetime - assign with the current datetime when an instance is created
updated_at: datetime - assign with the current datetime when an instance is created and it will be updated every time you change your object
__str__: should print: [<class name>] (<self.id>) <self.__dict__>
Public instance methods:
save(self): updates the public instance attribute updated_at with the current datetime
to_dict(self): returns a dictionary containing all keys/values of __dict__ of the instance:
by using self.__dict__, only instance attributes set will be returned
a key __class__ must be added to this dictionary with the class name of the object
created_at and updated_at must be converted to string object in ISO format:
format: %Y-%m-%dT%H:%M:%S.%f (ex: 2017-06-14T22:31:03.285259)
you can use isoformat() of datetime object
This method will be the first piece of the serialization/deserialization process: create a dictionary representation with “simple object type” of our BaseModel
guillaume@ubuntu:~/AirBnB$ cat test_base_model.py
#!/usr/bin/python3
from models.base_model import BaseModel

my_model = BaseModel()
my_model.name = "My First Model"
my_model.my_number = 89
print(my_model)
my_model.save()
print(my_model)
my_model_json = my_model.to_dict()
print(my_model_json)
print("JSON of my_model:")
for key in my_model_json.keys():
    print("\t{}: ({}) - {}".format(key, type(my_model_json[key]), my_model_json[key]))

guillaume@ubuntu:~/AirBnB$ ./test_base_model.py
[BaseModel] (b6a6e15c-c67d-4312-9a75-9d084935e579) {'my_number': 89, 'name': 'My First Model', 'updated_at': datetime.datetime(2017, 9, 28, 21, 5, 54, 119434), 'id': 'b6a6e15c-c67d-4312-9a75-9d084935e579', 'created_at': datetime.datetime(2017, 9, 28, 21, 5, 54, 119427)}
[BaseModel] (b6a6e15c-c67d-4312-9a75-9d084935e579) {'my_number': 89, 'name': 'My First Model', 'updated_at': datetime.datetime(2017, 9, 28, 21, 5, 54, 119572), 'id': 'b6a6e15c-c67d-4312-9a75-9d084935e579', 'created_at': datetime.datetime(2017, 9, 28, 21, 5, 54, 119427)}
{'my_number': 89, 'name': 'My First Model', '__class__': 'BaseModel', 'updated_at': '2017-09-28T21:05:54.119572', 'id': 'b6a6e15c-c67d-4312-9a75-9d084935e579', 'created_at': '2017-09-28T21:05:54.119427'}
JSON of my_model:
    my_number: (<class 'int'>) - 89
    name: (<class 'str'>) - My First Model
    __class__: (<class 'str'>) - BaseModel
    updated_at: (<class 'str'>) - 2017-09-28T21:05:54.119572
    id: (<class 'str'>) - b6a6e15c-c67d-4312-9a75-9d084935e579
    created_at: (<class 'str'>) - 2017-09-28T21:05:54.119427

guillaume@ubuntu:~/AirBnB$ 
Repo:

GitHub repository: AirBnB_clone
File: models/base_model.py, models/__init__.py, tests/
  
4. Create BaseModel from dictionary
mandatory
Previously we created a method to generate a dictionary representation of an instance (method to_dict()).

Now it’s time to re-create an instance with this dictionary representation.

<class 'BaseModel'> -> to_dict() -> <class 'dict'> -> <class 'BaseModel'>
Update models/base_model.py:

__init__(self, *args, **kwargs):
you will use *args, **kwargs arguments for the constructor of a BaseModel. (more information inside the AirBnB clone concept page)
*args won’t be used
if kwargs is not empty:
each key of this dictionary is an attribute name (Note __class__ from kwargs is the only one that should not be added as an attribute. See the example output, below)
each value of this dictionary is the value of this attribute name
Warning: created_at and updated_at are strings in this dictionary, but inside your BaseModel instance is working with datetime object. You have to convert these strings into datetime object. Tip: you know the string format of these datetime
otherwise:
create id and created_at as you did previously (new instance)
guillaume@ubuntu:~/AirBnB$ cat test_base_model_dict.py
#!/usr/bin/python3
from models.base_model import BaseModel

my_model = BaseModel()
my_model.name = "My_First_Model"
my_model.my_number = 89
print(my_model.id)
print(my_model)
print(type(my_model.created_at))
print("--")
my_model_json = my_model.to_dict()
print(my_model_json)
print("JSON of my_model:")
for key in my_model_json.keys():
    print("\t{}: ({}) - {}".format(key, type(my_model_json[key]), my_model_json[key]))

print("--")
my_new_model = BaseModel(**my_model_json)
print(my_new_model.id)
print(my_new_model)
print(type(my_new_model.created_at))

print("--")
print(my_model is my_new_model)

guillaume@ubuntu:~/AirBnB$ ./test_base_model_dict.py
56d43177-cc5f-4d6c-a0c1-e167f8c27337
[BaseModel] (56d43177-cc5f-4d6c-a0c1-e167f8c27337) {'id': '56d43177-cc5f-4d6c-a0c1-e167f8c27337', 'created_at': datetime.datetime(2017, 9, 28, 21, 3, 54, 52298), 'my_number': 89, 'updated_at': datetime.datetime(2017, 9, 28, 21, 3, 54, 52302), 'name': 'My_First_Model'}
<class 'datetime.datetime'>
--
{'id': '56d43177-cc5f-4d6c-a0c1-e167f8c27337', 'created_at': '2017-09-28T21:03:54.052298', '__class__': 'BaseModel', 'my_number': 89, 'updated_at': '2017-09-28T21:03:54.052302', 'name': 'My_First_Model'}
JSON of my_model:
    id: (<class 'str'>) - 56d43177-cc5f-4d6c-a0c1-e167f8c27337
    created_at: (<class 'str'>) - 2017-09-28T21:03:54.052298
    __class__: (<class 'str'>) - BaseModel
    my_number: (<class 'int'>) - 89
    updated_at: (<class 'str'>) - 2017-09-28T21:03:54.052302
    name: (<class 'str'>) - My_First_Model
--
56d43177-cc5f-4d6c-a0c1-e167f8c27337
[BaseModel] (56d43177-cc5f-4d6c-a0c1-e167f8c27337) {'id': '56d43177-cc5f-4d6c-a0c1-e167f8c27337', 'created_at': datetime.datetime(2017, 9, 28, 21, 3, 54, 52298), 'my_number': 89, 'updated_at': datetime.datetime(2017, 9, 28, 21, 3, 54, 52302), 'name': 'My_First_Model'}
<class 'datetime.datetime'>
--
False
guillaume@ubuntu:~/AirBnB$ 
Repo:

GitHub repository: AirBnB_clone
File: models/base_model.py, tests/
  
5. Store first object
mandatory
Now we can recreate a BaseModel from another one by using a dictionary representation:

<class 'BaseModel'> -> to_dict() -> <class 'dict'> -> <class 'BaseModel'>
It’s great but it’s still not persistent: every time you launch the program, you don’t restore all objects created before… The first way you will see here is to save these objects to a file.

Writing the dictionary representation to a file won’t be relevant:

Python doesn’t know how to convert a string to a dictionary (easily)
It’s not human readable
Using this file with another program in Python or other language will be hard.
So, you will convert the dictionary representation to a JSON string. JSON is a standard representation of a data structure. With this format, humans can read and all programming languages have a JSON reader and writer.

Now the flow of serialization-deserialization will be:

<class 'BaseModel'> -> to_dict() -> <class 'dict'> -> JSON dump -> <class 'str'> -> FILE -> <class 'str'> -> JSON load -> <class 'dict'> -> <class 'BaseModel'>
Magic right?

Terms:

simple Python data structure: Dictionaries, arrays, number and string. ex: { '12': { 'numbers': [1, 2, 3], 'name': "John" } }
JSON string representation: String representing a simple data structure in JSON format. ex: '{ "12": { "numbers": [1, 2, 3], "name": "John" } }'
Write a class FileStorage that serializes instances to a JSON file and deserializes JSON file to instances:

models/engine/file_storage.py
Private class attributes:
__file_path: string - path to the JSON file (ex: file.json)
__objects: dictionary - empty but will store all objects by <class name>.id (ex: to store a BaseModel object with id=12121212, the key will be BaseModel.12121212)
Public instance methods:
all(self): returns the dictionary __objects
new(self, obj): sets in __objects the obj with key <obj class name>.id
save(self): serializes __objects to the JSON file (path: __file_path)
reload(self): deserializes the JSON file to __objects (only if the JSON file (__file_path) exists ; otherwise, do nothing. If the file doesn’t exist, no exception should be raised)
Update models/__init__.py: to create a unique FileStorage instance for your application

import file_storage.py
create the variable storage, an instance of FileStorage
call reload() method on this variable
Update models/base_model.py: to link your BaseModel to FileStorage by using the variable storage

import the variable storage
in the method save(self):
call save(self) method of storage
__init__(self, *args, **kwargs):
if it’s a new instance (not from a dictionary representation), add a call to the method new(self) on storage
guillaume@ubuntu:~/AirBnB$ cat test_save_reload_base_model.py
#!/usr/bin/python3
from models import storage
from models.base_model import BaseModel

all_objs = storage.all()
print("-- Reloaded objects --")
for obj_id in all_objs.keys():
    obj = all_objs[obj_id]
    print(obj)

print("-- Create a new object --")
my_model = BaseModel()
my_model.name = "My_First_Model"
my_model.my_number = 89
my_model.save()
print(my_model)

guillaume@ubuntu:~/AirBnB$ cat file.json
cat: file.json: No such file or directory
guillaume@ubuntu:~/AirBnB$ 
guillaume@ubuntu:~/AirBnB$ ./test_save_reload_base_model.py
-- Reloaded objects --
-- Create a new object --
[BaseModel] (ee49c413-023a-4b49-bd28-f2936c95460d) {'my_number': 89, 'updated_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47381), 'created_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47372), 'name': 'My_First_Model', 'id': 'ee49c413-023a-4b49-bd28-f2936c95460d'}
guillaume@ubuntu:~/AirBnB$ 
guillaume@ubuntu:~/AirBnB$ cat file.json ; echo ""
{"BaseModel.ee49c413-023a-4b49-bd28-f2936c95460d": {"my_number": 89, "__class__": "BaseModel", "updated_at": "2017-09-28T21:07:25.047381", "created_at": "2017-09-28T21:07:25.047372", "name": "My_First_Model", "id": "ee49c413-023a-4b49-bd28-f2936c95460d"}}
guillaume@ubuntu:~/AirBnB$
guillaume@ubuntu:~/AirBnB$ ./test_save_reload_base_model.py
-- Reloaded objects --
[BaseModel] (ee49c413-023a-4b49-bd28-f2936c95460d) {'name': 'My_First_Model', 'id': 'ee49c413-023a-4b49-bd28-f2936c95460d', 'updated_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47381), 'my_number': 89, 'created_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47372)}
-- Create a new object --
[BaseModel] (080cce84-c574-4230-b82a-9acb74ad5e8c) {'name': 'My_First_Model', 'id': '080cce84-c574-4230-b82a-9acb74ad5e8c', 'updated_at': datetime.datetime(2017, 9, 28, 21, 7, 51, 973308), 'my_number': 89, 'created_at': datetime.datetime(2017, 9, 28, 21, 7, 51, 973301)}
guillaume@ubuntu:~/AirBnB$ 
guillaume@ubuntu:~/AirBnB$ ./test_save_reload_base_model.py
-- Reloaded objects --
[BaseModel] (080cce84-c574-4230-b82a-9acb74ad5e8c) {'id': '080cce84-c574-4230-b82a-9acb74ad5e8c', 'updated_at': datetime.datetime(2017, 9, 28, 21, 7, 51, 973308), 'created_at': datetime.datetime(2017, 9, 28, 21, 7, 51, 973301), 'name': 'My_First_Model', 'my_number': 89}
[BaseModel] (ee49c413-023a-4b49-bd28-f2936c95460d) {'id': 'ee49c413-023a-4b49-bd28-f2936c95460d', 'updated_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47381), 'created_at': datetime.datetime(2017, 9, 28, 21, 7, 25, 47372), 'name': 'My_First_Model', 'my_number': 89}
-- Create a new object --
[BaseModel] (e79e744a-55d4-45a3-b74a-ca5fae74e0e2) {'id': 'e79e744a-55d4-45a3-b74a-ca5fae74e0e2', 'updated_at': datetime.datetime(2017, 9, 28, 21, 8, 6, 151750), 'created_at': datetime.datetime(2017, 9, 28, 21, 8, 6, 151711), 'name': 'My_First_Model', 'my_number': 89}
guillaume@ubuntu:~/AirBnB$ 
guillaume@ubuntu:~/AirBnB$ cat file.json ; echo ""
{"BaseModel.e79e744a-55d4-45a3-b74a-ca5fae74e0e2": {"__class__": "BaseModel", "id": "e79e744a-55d4-45a3-b74a-ca5fae74e0e2", "updated_at": "2017-09-28T21:08:06.151750", "created_at": "2017-09-28T21:08:06.151711", "name": "My_First_Model", "my_number": 89}, "BaseModel.080cce84-c574-4230-b82a-9acb74ad5e8c": {"__class__": "BaseModel", "id": "080cce84-c574-4230-b82a-9acb74ad5e8c", "updated_at": "2017-09-28T21:07:51.973308", "created_at": "2017-09-28T21:07:51.973301", "name": "My_First_Model", "my_number": 89}, "BaseModel.ee49c413-023a-4b49-bd28-f2936c95460d": {"__class__": "BaseModel", "id": "ee49c413-023a-4b49-bd28-f2936c95460d", "updated_at": "2017-09-28T21:07:25.047381", "created_at": "2017-09-28T21:07:25.047372", "name": "My_First_Model", "my_number": 89}}
guillaume@ubuntu:~/AirBnB$ 
Repo:

GitHub repository: AirBnB_clone
File: models/engine/file_storage.py, models/engine/__init__.py, models/__init__.py, models/base_model.py, tests/
  
6. Console 0.0.1
mandatory
Write a program called console.py that contains the entry point of the command interpreter:

You must use the module cmd
Your class definition must be: class HBNBCommand(cmd.Cmd):
Your command interpreter should implement:
quit and EOF to exit the program
help (this action is provided by default by cmd but you should keep it updated and documented as you work through tasks)
a custom prompt: (hbnb)
an empty line + ENTER shouldn’t execute anything
Your code should not be executed when imported
Warning:

You should end your file with:

if __name__ == '__main__':
    HBNBCommand().cmdloop()
to make your program executable except when imported. Please don’t add anything around - the Checker won’t like it otherwise

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) help quit
Quit command to exit the program

(hbnb) 
(hbnb) 
(hbnb) quit 
guillaume@ubuntu:~/AirBnB$ 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
7. Console 0.1
mandatory
Update your command interpreter (console.py) to have these commands:

create: Creates a new instance of BaseModel, saves it (to the JSON file) and prints the id. Ex: $ create BaseModel
If the class name is missing, print ** class name missing ** (ex: $ create)
If the class name doesn’t exist, print ** class doesn't exist ** (ex: $ create MyModel)
show: Prints the string representation of an instance based on the class name and id. Ex: $ show BaseModel 1234-1234-1234.
If the class name is missing, print ** class name missing ** (ex: $ show)
If the class name doesn’t exist, print ** class doesn't exist ** (ex: $ show MyModel)
If the id is missing, print ** instance id missing ** (ex: $ show BaseModel)
If the instance of the class name doesn’t exist for the id, print ** no instance found ** (ex: $ show BaseModel 121212)
destroy: Deletes an instance based on the class name and id (save the change into the JSON file). Ex: $ destroy BaseModel 1234-1234-1234.
If the class name is missing, print ** class name missing ** (ex: $ destroy)
If the class name doesn’t exist, print ** class doesn't exist ** (ex:$ destroy MyModel)
If the id is missing, print ** instance id missing ** (ex: $ destroy BaseModel)
If the instance of the class name doesn’t exist for the id, print ** no instance found ** (ex: $ destroy BaseModel 121212)
all: Prints all string representation of all instances based or not on the class name. Ex: $ all BaseModel or $ all.
The printed result must be a list of strings (like the example below)
If the class name doesn’t exist, print ** class doesn't exist ** (ex: $ all MyModel)
update: Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). Ex: $ update BaseModel 1234-1234-1234 email "aibnb@mail.com".
Usage: update <class name> <id> <attribute name> "<attribute value>"
Only one attribute can be updated at the time
You can assume the attribute name is valid (exists for this model)
The attribute value must be casted to the attribute type
If the class name is missing, print ** class name missing ** (ex: $ update)
If the class name doesn’t exist, print ** class doesn't exist ** (ex: $ update MyModel)
If the id is missing, print ** instance id missing ** (ex: $ update BaseModel)
If the instance of the class name doesn’t exist for the id, print ** no instance found ** (ex: $ update BaseModel 121212)
If the attribute name is missing, print ** attribute name missing ** (ex: $ update BaseModel existing-id)
If the value for the attribute name doesn’t exist, print ** value missing ** (ex: $ update BaseModel existing-id first_name)
All other arguments should not be used (Ex: $ update BaseModel 1234-1234-1234 email "aibnb@mail.com" first_name "Betty" = $ update BaseModel 1234-1234-1234 email "aibnb@mail.com")
id, created_at and updated_at cant’ be updated. You can assume they won’t be passed in the update command
Only “simple” arguments can be updated: string, integer and float. You can assume nobody will try to update list of ids or datetime
Let’s add some rules:

You can assume arguments are always in the right order
Each arguments are separated by a space
A string argument with a space must be between double quote
The error management starts from the first argument to the last one
guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) all MyModel
** class doesn't exist **
(hbnb) show BaseModel
** instance id missing **
(hbnb) show BaseModel My_First_Model
** no instance found **
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
(hbnb) all BaseModel
["[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}"]
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}
(hbnb) destroy
** class name missing **
(hbnb) update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}
(hbnb) create BaseModel
2dd6ef5c-467c-4f82-9521-a772ea7d84e9
(hbnb) all BaseModel
["[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}", "[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}"]
(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
** no instance found **
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
8. First User
mandatory
Write a class User that inherits from BaseModel:

models/user.py
Public class attributes:
email: string - empty string
password: string - empty string
first_name: string - empty string
last_name: string - empty string
Update FileStorage to manage correctly serialization and deserialization of User.

Update your command interpreter (console.py) to allow show, create, destroy, update and all used with User.

guillaume@ubuntu:~/AirBnB$ cat test_save_reload_user.py
#!/usr/bin/python3
from models import storage
from models.base_model import BaseModel
from models.user import User

all_objs = storage.all()
print("-- Reloaded objects --")
for obj_id in all_objs.keys():
    obj = all_objs[obj_id]
    print(obj)

print("-- Create a new User --")
my_user = User()
my_user.first_name = "Betty"
my_user.last_name = "Bar"
my_user.email = "airbnb@mail.com"
my_user.password = "root"
my_user.save()
print(my_user)

print("-- Create a new User 2 --")
my_user2 = User()
my_user2.first_name = "John"
my_user2.email = "airbnb2@mail.com"
my_user2.password = "root"
my_user2.save()
print(my_user2)

guillaume@ubuntu:~/AirBnB$ cat file.json ; echo ""
{"BaseModel.2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4": {"__class__": "BaseModel", "id": "2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4", "updated_at": "2017-09-28T21:11:14.333862", "created_at": "2017-09-28T21:11:14.333852"}, "BaseModel.a42ee380-c959-450e-ad29-c840a898cfce": {"__class__": "BaseModel", "id": "a42ee380-c959-450e-ad29-c840a898cfce", "updated_at": "2017-09-28T21:11:15.504296", "created_at": "2017-09-28T21:11:15.504287"}, "BaseModel.af9b4cbd-2ce1-4e6e-8259-f578097dd15f": {"__class__": "BaseModel", "id": "af9b4cbd-2ce1-4e6e-8259-f578097dd15f", "updated_at": "2017-09-28T21:11:12.971544", "created_at": "2017-09-28T21:11:12.971521"}, "BaseModel.38a22b25-ae9c-4fa9-9f94-59b3eb51bfba": {"__class__": "BaseModel", "id": "38a22b25-ae9c-4fa9-9f94-59b3eb51bfba", "updated_at": "2017-09-28T21:11:13.753347", "created_at": "2017-09-28T21:11:13.753337"}, "BaseModel.9bf17966-b092-4996-bd33-26a5353cccb4": {"__class__": "BaseModel", "id": "9bf17966-b092-4996-bd33-26a5353cccb4", "updated_at": "2017-09-28T21:11:14.963058", "created_at": "2017-09-28T21:11:14.963049"}}
guillaume@ubuntu:~/AirBnB$
guillaume@ubuntu:~/AirBnB$ ./test_save_reload_user.py
-- Reloaded objects --
[BaseModel] (38a22b25-ae9c-4fa9-9f94-59b3eb51bfba) {'id': '38a22b25-ae9c-4fa9-9f94-59b3eb51bfba', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 13, 753337), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 13, 753347)}
[BaseModel] (9bf17966-b092-4996-bd33-26a5353cccb4) {'id': '9bf17966-b092-4996-bd33-26a5353cccb4', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 963049), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 963058)}
[BaseModel] (2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4) {'id': '2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 333852), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 333862)}
[BaseModel] (a42ee380-c959-450e-ad29-c840a898cfce) {'id': 'a42ee380-c959-450e-ad29-c840a898cfce', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 15, 504287), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 15, 504296)}
[BaseModel] (af9b4cbd-2ce1-4e6e-8259-f578097dd15f) {'id': 'af9b4cbd-2ce1-4e6e-8259-f578097dd15f', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 12, 971521), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 12, 971544)}
-- Create a new User --
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'id': '38f22813-2753-4d42-b37c-57a17f1e4f88', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848291), 'email': 'airbnb@mail.com', 'first_name': 'Betty', 'last_name': 'Bar', 'password': 'root'}
-- Create a new User 2 --
[User] (d0ef8146-4664-4de5-8e89-096d667b728e) {'id': 'd0ef8146-4664-4de5-8e89-096d667b728e', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848280), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848294), 'email': 'airbnb2@mail.com', 'first_name': 'John', 'password': 'root'}
guillaume@ubuntu:~/AirBnB$
guillaume@ubuntu:~/AirBnB$ cat file.json ; echo ""
{"BaseModel.af9b4cbd-2ce1-4e6e-8259-f578097dd15f": {"id": "af9b4cbd-2ce1-4e6e-8259-f578097dd15f", "updated_at": "2017-09-28T21:11:12.971544", "created_at": "2017-09-28T21:11:12.971521", "__class__": "BaseModel"}, "BaseModel.38a22b25-ae9c-4fa9-9f94-59b3eb51bfba": {"id": "38a22b25-ae9c-4fa9-9f94-59b3eb51bfba", "updated_at": "2017-09-28T21:11:13.753347", "created_at": "2017-09-28T21:11:13.753337", "__class__": "BaseModel"}, "BaseModel.9bf17966-b092-4996-bd33-26a5353cccb4": {"id": "9bf17966-b092-4996-bd33-26a5353cccb4", "updated_at": "2017-09-28T21:11:14.963058", "created_at": "2017-09-28T21:11:14.963049", "__class__": "BaseModel"}, "BaseModel.2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4": {"id": "2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4", "updated_at": "2017-09-28T21:11:14.333862", "created_at": "2017-09-28T21:11:14.333852", "__class__": "BaseModel"}, "BaseModel.a42ee380-c959-450e-ad29-c840a898cfce": {"id": "a42ee380-c959-450e-ad29-c840a898cfce", "updated_at": "2017-09-28T21:11:15.504296", "created_at": "2017-09-28T21:11:15.504287", "__class__": "BaseModel"}, "User.38f22813-2753-4d42-b37c-57a17f1e4f88": {"id": "38f22813-2753-4d42-b37c-57a17f1e4f88", "created_at": "2017-09-28T21:11:42.848279", "updated_at": "2017-09-28T21:11:42.848291", "email": "airbnb@mail.com", "first_name": "Betty", "__class__": "User", "last_name": "Bar", "password": "root"}, "User.d0ef8146-4664-4de5-8e89-096d667b728e": {"id": "d0ef8146-4664-4de5-8e89-096d667b728e", "created_at": "2017-09-28T21:11:42.848280", "updated_at": "2017-09-28T21:11:42.848294", "email": "airbnb_2@mail.com", "first_name": "John", "__class__": "User", "password": "root"}}
guillaume@ubuntu:~/AirBnB$ 
guillaume@ubuntu:~/AirBnB$ ./test_save_reload_user.py
-- Reloaded objects --
[BaseModel] (af9b4cbd-2ce1-4e6e-8259-f578097dd15f) {'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 12, 971544), 'id': 'af9b4cbd-2ce1-4e6e-8259-f578097dd15f', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 12, 971521)}
[BaseModel] (2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4) {'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 333862), 'id': '2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 333852)}
[BaseModel] (9bf17966-b092-4996-bd33-26a5353cccb4) {'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 963058), 'id': '9bf17966-b092-4996-bd33-26a5353cccb4', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 14, 963049)}
[BaseModel] (a42ee380-c959-450e-ad29-c840a898cfce) {'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 15, 504296), 'id': 'a42ee380-c959-450e-ad29-c840a898cfce', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 15, 504287)}
[BaseModel] (38a22b25-ae9c-4fa9-9f94-59b3eb51bfba) {'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 13, 753347), 'id': '38a22b25-ae9c-4fa9-9f94-59b3eb51bfba', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 13, 753337)}
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'password': '63a9f0ea7bb98050796b649e85481845', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'email': 'airbnb@mail.com', 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848291), 'last_name': 'Bar', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88', 'first_name': 'Betty'}
[User] (d0ef8146-4664-4de5-8e89-096d667b728e) {'password': '63a9f0ea7bb98050796b649e85481845', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848280), 'email': 'airbnb_2@mail.com', 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848294), 'id': 'd0ef8146-4664-4de5-8e89-096d667b728e', 'first_name': 'John'}
-- Create a new User --
[User] (246c227a-d5c1-403d-9bc7-6a47bb9f0f68) {'password': 'root', 'created_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611352), 'email': 'airbnb@mail.com', 'updated_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611363), 'last_name': 'Bar', 'id': '246c227a-d5c1-403d-9bc7-6a47bb9f0f68', 'first_name': 'Betty'}
-- Create a new User 2 --
[User] (fce12f8a-fdb6-439a-afe8-2881754de71c) {'password': 'root', 'created_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611354), 'email': 'airbnb_2@mail.com', 'updated_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611368), 'id': 'fce12f8a-fdb6-439a-afe8-2881754de71c', 'first_name': 'John'}
guillaume@ubuntu:~/AirBnB$
guillaume@ubuntu:~/AirBnB$ cat file.json ; echo ""
{"BaseModel.af9b4cbd-2ce1-4e6e-8259-f578097dd15f": {"updated_at": "2017-09-28T21:11:12.971544", "__class__": "BaseModel", "id": "af9b4cbd-2ce1-4e6e-8259-f578097dd15f", "created_at": "2017-09-28T21:11:12.971521"}, "User.38f22813-2753-4d42-b37c-57a17f1e4f88": {"password": "63a9f0ea7bb98050796b649e85481845", "created_at": "2017-09-28T21:11:42.848279", "email": "airbnb@mail.com", "id": "38f22813-2753-4d42-b37c-57a17f1e4f88", "last_name": "Bar", "updated_at": "2017-09-28T21:11:42.848291", "first_name": "Betty", "__class__": "User"}, "User.d0ef8146-4664-4de5-8e89-096d667b728e": {"password": "63a9f0ea7bb98050796b649e85481845", "created_at": "2017-09-28T21:11:42.848280", "email": "airbnb_2@mail.com", "id": "d0ef8146-4664-4de5-8e89-096d667b728e", "updated_at": "2017-09-28T21:11:42.848294", "first_name": "John", "__class__": "User"}, "BaseModel.9bf17966-b092-4996-bd33-26a5353cccb4": {"updated_at": "2017-09-28T21:11:14.963058", "__class__": "BaseModel", "id": "9bf17966-b092-4996-bd33-26a5353cccb4", "created_at": "2017-09-28T21:11:14.963049"}, "BaseModel.a42ee380-c959-450e-ad29-c840a898cfce": {"updated_at": "2017-09-28T21:11:15.504296", "__class__": "BaseModel", "id": "a42ee380-c959-450e-ad29-c840a898cfce", "created_at": "2017-09-28T21:11:15.504287"}, "BaseModel.38a22b25-ae9c-4fa9-9f94-59b3eb51bfba": {"updated_at": "2017-09-28T21:11:13.753347", "__class__": "BaseModel", "id": "38a22b25-ae9c-4fa9-9f94-59b3eb51bfba", "created_at": "2017-09-28T21:11:13.753337"}, "BaseModel.2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4": {"updated_at": "2017-09-28T21:11:14.333862", "__class__": "BaseModel", "id": "2bf3ebfd-a220-49ee-9ae6-b01c75f6f6a4", "created_at": "2017-09-28T21:11:14.333852"}, "User.246c227a-d5c1-403d-9bc7-6a47bb9f0f68": {"password": "root", "created_at": "2017-09-28T21:12:19.611352", "email": "airbnb@mail.com", "id": "246c227a-d5c1-403d-9bc7-6a47bb9f0f68", "last_name": "Bar", "updated_at": "2017-09-28T21:12:19.611363", "first_name": "Betty", "__class__": "User"}, "User.fce12f8a-fdb6-439a-afe8-2881754de71c": {"password": "root", "created_at": "2017-09-28T21:12:19.611354", "email": "airbnb_2@mail.com", "id": "fce12f8a-fdb6-439a-afe8-2881754de71c", "updated_at": "2017-09-28T21:12:19.611368", "first_name": "John", "__class__": "User"}}
guillaume@ubuntu:~/AirBnB$ 
No unittests needed for the console

Repo:

GitHub repository: AirBnB_clone
File: models/user.py, models/engine/file_storage.py, console.py, tests/
  
9. More classes!
mandatory
Write all those classes that inherit from BaseModel:

State (models/state.py):
Public class attributes:
name: string - empty string
City (models/city.py):
Public class attributes:
state_id: string - empty string: it will be the State.id
name: string - empty string
Amenity (models/amenity.py):
Public class attributes:
name: string - empty string
Place (models/place.py):
Public class attributes:
city_id: string - empty string: it will be the City.id
user_id: string - empty string: it will be the User.id
name: string - empty string
description: string - empty string
number_rooms: integer - 0
number_bathrooms: integer - 0
max_guest: integer - 0
price_by_night: integer - 0
latitude: float - 0.0
longitude: float - 0.0
amenity_ids: list of string - empty list: it will be the list of Amenity.id later
Review (models/review.py):
Public class attributes:
place_id: string - empty string: it will be the Place.id
user_id: string - empty string: it will be the User.id
text: string - empty string
Repo:

GitHub repository: AirBnB_clone
File: models/state.py, models/city.py, models/amenity.py, models/place.py, models/review.py, tests/
  
10. Console 1.0
mandatory
Update FileStorage to manage correctly serialization and deserialization of all our new classes: Place, State, City, Amenity and Review

Update your command interpreter (console.py) to allow those actions: show, create, destroy, update and all with all classes created previously.

Enjoy your first console!

No unittests needed for the console

Repo:

GitHub repository: AirBnB_clone
File: console.py, models/engine/file_storage.py, tests/
  
11. All instances by class name
#advanced
Update your command interpreter (console.py) to retrieve all instances of a class by using: <class name>.all().

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.all()
[[User] (246c227a-d5c1-403d-9bc7-6a47bb9f0f68) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611352), 'updated_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611363), 'password': '63a9f0ea7bb98050796b649e85481845', 'email': 'airbnb@mail.com', 'id': '246c227a-d5c1-403d-9bc7-6a47bb9f0f68'}, [User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848291), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}]
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
12. Count instances
#advanced
Update your command interpreter (console.py) to retrieve the number of instances of a class: <class name>.count().

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.count()
2
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
13. Show
#advanced
Update your command interpreter (console.py) to retrieve an instance based on its ID: <class name>.show(<id>).

Errors management must be the same as previously.

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.show("246c227a-d5c1-403d-9bc7-6a47bb9f0f68")
[User] (246c227a-d5c1-403d-9bc7-6a47bb9f0f68) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611352), 'updated_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611363), 'password': '63a9f0ea7bb98050796b649e85481845', 'email': 'airbnb@mail.com', 'id': '246c227a-d5c1-403d-9bc7-6a47bb9f0f68'}
(hbnb) User.show("Bar")
** no instance found **
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
14. Destroy
#advanced
Update your command interpreter (console.py) to destroy an instance based on his ID: <class name>.destroy(<id>).

Errors management must be the same as previously.

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.count()
2
(hbnb) User.destroy("246c227a-d5c1-403d-9bc7-6a47bb9f0f68")
(hbnb) User.count()
1
(hbnb) User.destroy("Bar")
** no instance found **
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
15. Update
#advanced
Update your command interpreter (console.py) to update an instance based on his ID: <class name>.update(<id>, <attribute name>, <attribute value>).

Errors management must be the same as previously.

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848291), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb)
(hbnb) User.update("38f22813-2753-4d42-b37c-57a17f1e4f88", "first_name", "John")
(hbnb) User.update("38f22813-2753-4d42-b37c-57a17f1e4f88", "age", 89)
(hbnb)
(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'age': 89, 'first_name': 'John', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 15, 32, 299055), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
16. Update from dictionary
#advanced
Update your command interpreter (console.py) to update an instance based on his ID with a dictionary: <class name>.update(<id>, <dictionary representation>).

Errors management must be the same as previously.

guillaume@ubuntu:~/AirBnB$ ./console.py
(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'age': 23, 'first_name': 'Bob', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 15, 32, 299055), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb) 
(hbnb) User.update("38f22813-2753-4d42-b37c-57a17f1e4f88", {'first_name': "John", "age": 89})
(hbnb) 
(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'age': 89, 'first_name': 'John', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 17, 10, 788143), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb) 
No unittests needed

Repo:

GitHub repository: AirBnB_clone
File: console.py
  
17. Unittests for the Console!
#advanced
Write all unittests for console.py, all features!

For testing the console, you should “intercept” STDOUT of it, we highly recommend you to use:

with patch('sys.stdout', new=StringIO()) as f:
    HBNBCommand().onecmd("help show")
Otherwise, you will have to re-write the console by replacing precmd by default.

Repo:

GitHub repository: AirBnB_clone
File: tests/test_console.py
  
# File @generated by hack/generate-authors.sh. DO NOT EDIT.
# This file lists all contributors to the repository.
# See hack/generate-authors.sh to make modifications.

Aanand Prasad <aanand.prasad@gmail.com>
Aaron Davidson <aaron@databricks.com>
Aaron Feng <aaron.feng@gmail.com>
Aaron Hnatiw <aaron@griddio.com>
Aaron Huslage <huslage@gmail.com>
Aaron L. Xu <liker.xu@foxmail.com>
Aaron Lehmann <alehmann@netflix.com>
Aaron Welch <welch@packet.net>
Abel Muiño <amuino@gmail.com>
Abhijeet Kasurde <akasurde@redhat.com>
Abhinandan Prativadi <aprativadi@gmail.com>
Abhinav Ajgaonkar <abhinav316@gmail.com>
Abhishek Chanda <abhishek.becs@gmail.com>
Abhishek Sharma <abhishek@asharma.me>
Abin Shahab <ashahab@altiscale.com>
Abirdcfly <fp544037857@gmail.com>
Ada Mancini <ada@docker.com>
Adam Avilla <aavilla@yp.com>
Adam Dobrawy <naczelnik@jawnosc.tk>
Adam Eijdenberg <adam.eijdenberg@gmail.com>
Adam Kunk <adam.kunk@tiaa-cref.org>
Adam Miller <admiller@redhat.com>
Adam Mills <adam@armills.info>
Adam Pointer <adam.pointer@skybettingandgaming.com>
Adam Singer <financeCoding@gmail.com>
Adam Walz <adam@adamwalz.net>
Adam Williams <awilliams@mirantis.com>
Addam Hardy <addam.hardy@gmail.com>
Aditi Rajagopal <arajagopal@us.ibm.com>
Aditya <aditya@netroy.in>
Adnan Khan <adnkha@amazon.com>
Adolfo Ochagavía <aochagavia92@gmail.com>
Adria Casas <adriacasas88@gmail.com>
Adrian Moisey <adrian@changeover.za.net>
Adrian Mouat <adrian.mouat@gmail.com>
Adrian Oprea <adrian@codesi.nz>
Adrien Folie <folie.adrien@gmail.com>
Adrien Gallouët <adrien@gallouet.fr>
Ahmed Kamal <email.ahmedkamal@googlemail.com>
Ahmet Alp Balkan <ahmetb@microsoft.com>
Aidan Feldman <aidan.feldman@gmail.com>
Aidan Hobson Sayers <aidanhs@cantab.net>
AJ Bowen <aj@soulshake.net>
Ajey Charantimath <ajey.charantimath@gmail.com>
ajneu <ajneu@users.noreply.github.com>
Akash Gupta <akagup@microsoft.com>
Akhil Mohan <akhil.mohan@mayadata.io>
Akihiro Matsushima <amatsusbit@gmail.com>
Akihiro Suda <akihiro.suda.cz@hco.ntt.co.jp>
Akim Demaille <akim.demaille@docker.com>
Akira Koyasu <mail@akirakoyasu.net>
Akshay Karle <akshay.a.karle@gmail.com>
Akshay Moghe <akshay.moghe@gmail.com>
Al Tobey <al@ooyala.com>
alambike <alambike@gmail.com>
Alan Hoyle <alan@alanhoyle.com>
Alan Scherger <flyinprogrammer@gmail.com>
Alan Thompson <cloojure@gmail.com>
Albert Callarisa <shark234@gmail.com>
Albert Zhang <zhgwenming@gmail.com>
Albin Kerouanton <albinker@gmail.com>
Alec Benson <albenson@redhat.com>
Alejandro González Hevia <alejandrgh11@gmail.com>
Aleksa Sarai <asarai@suse.de>
Aleksandr Chebotov <v-aleche@microsoft.com>
Aleksandrs Fadins <aleks@s-ko.net>
Alena Prokharchyk <alena@rancher.com>
Alessandro Boch <aboch@tetrationanalytics.com>
Alessio Biancalana <dottorblaster@gmail.com>
Alex Chan <alex@alexwlchan.net>
Alex Chen <alexchenunix@gmail.com>
Alex Coventry <alx@empirical.com>
Alex Crawford <alex.crawford@coreos.com>
Alex Ellis <alexellis2@gmail.com>
Alex Gaynor <alex.gaynor@gmail.com>
Alex Goodman <wagoodman@gmail.com>
Alex Nordlund <alexander.nordlund@nasdaq.com>
Alex Olshansky <i@creagenics.com>
Alex Samorukov <samm@os2.kiev.ua>
Alex Warhawk <ax.warhawk@gmail.com>
Alexander Artemenko <svetlyak.40wt@gmail.com>
Alexander Boyd <alex@opengroove.org>
Alexander Larsson <alexl@redhat.com>
Alexander Midlash <amidlash@docker.com>
Alexander Morozov <lk4d4math@gmail.com>
Alexander Polakov <plhk@sdf.org>
Alexander Shopov <ash@kambanaria.org>
Alexandre Beslic <alexandre.beslic@gmail.com>
Alexandre Garnier <zigarn@gmail.com>
Alexandre González <agonzalezro@gmail.com>
Alexandre Jomin <alexandrejomin@gmail.com>
Alexandru Sfirlogea <alexandru.sfirlogea@gmail.com>
Alexei Margasov <alexei38@yandex.ru>
Alexey Guskov <lexag@mail.ru>
Alexey Kotlyarov <alexey@infoxchange.net.au>
Alexey Shamrin <shamrin@gmail.com>
Alexis Ries <ries.alexis@gmail.com>
Alexis Thomas <fr.alexisthomas@gmail.com>
Alfred Landrum <alfred.landrum@docker.com>
Ali Dehghani <ali.dehghani.g@gmail.com>
Alicia Lauerman <alicia@eta.im>
Alihan Demir <alihan_6153@hotmail.com>
Allen Madsen <blatyo@gmail.com>
Allen Sun <allensun.shl@alibaba-inc.com>
almoehi <almoehi@users.noreply.github.com>
Alvaro Saurin <alvaro.saurin@gmail.com>
Alvin Deng <alvin.q.deng@utexas.edu>
Alvin Richards <alvin.richards@docker.com>
amangoel <amangoel@gmail.com>
Amen Belayneh <amenbelayneh@gmail.com>
Ameya Gawde <agawde@mirantis.com>
Amir Goldstein <amir73il@aquasec.com>
Amit Bakshi <ambakshi@gmail.com>
Amit Krishnan <amit.krishnan@oracle.com>
Amit Shukla <amit.shukla@docker.com>
Amr Gawish <amr.gawish@gmail.com>
Amy Lindburg <amy.lindburg@docker.com>
Anand Patil <anand.prabhakar.patil@gmail.com>
AnandkumarPatel <anandkumarpatel@gmail.com>
Anatoly Borodin <anatoly.borodin@gmail.com>
Anca Iordache <anca.iordache@docker.com>
Anchal Agrawal <aagrawa4@illinois.edu>
Anda Xu <anda.xu@docker.com>
Anders Janmyr <anders@janmyr.com>
Andre Dublin <81dublin@gmail.com>
Andre Granovsky <robotciti@live.com>
Andrea Denisse Gómez <crypto.andrea@protonmail.ch>
Andrea Luzzardi <aluzzardi@gmail.com>
Andrea Turli <andrea.turli@gmail.com>
Andreas Elvers <andreas@work.de>
Andreas Köhler <andi5.py@gmx.net>
Andreas Savvides <andreas@editd.com>
Andreas Tiefenthaler <at@an-ti.eu>
Andrei Gherzan <andrei@resin.io>
Andrei Ushakov <aushakov@netflix.com>
Andrei Vagin <avagin@gmail.com>
Andrew C. Bodine <acbodine@us.ibm.com>
Andrew Clay Shafer <andrewcshafer@gmail.com>
Andrew Duckworth <grillopress@gmail.com>
Andrew France <andrew@avito.co.uk>
Andrew Gerrand <adg@golang.org>
Andrew Guenther <guenther.andrew.j@gmail.com>
Andrew He <he.andrew.mail@gmail.com>
Andrew Hsu <andrewhsu@docker.com>
Andrew Kim <taeyeonkim90@gmail.com>
Andrew Kuklewicz <kookster@gmail.com>
Andrew Macgregor <andrew.macgregor@agworld.com.au>
Andrew Macpherson <hopscotch23@gmail.com>
Andrew Martin <sublimino@gmail.com>
Andrew McDonnell <bugs@andrewmcdonnell.net>
Andrew Munsell <andrew@wizardapps.net>
Andrew Pennebaker <andrew.pennebaker@gmail.com>
Andrew Po <absourd.noise@gmail.com>
Andrew Weiss <andrew.weiss@docker.com>
Andrew Williams <williams.andrew@gmail.com>
Andrews Medina <andrewsmedina@gmail.com>
Andrey Kolomentsev <andrey.kolomentsev@docker.com>
Andrey Petrov <andrey.petrov@shazow.net>
Andrey Stolbovsky <andrey.stolbovsky@gmail.com>
André Martins <aanm90@gmail.com>
Andy Chambers <anchambers@paypal.com>
andy diller <dillera@gmail.com>
Andy Goldstein <agoldste@redhat.com>
Andy Kipp <andy@rstudio.com>
Andy Lindeman <alindeman@salesforce.com>
Andy Rothfusz <github@developersupport.net>
Andy Smith <github@anarkystic.com>
Andy Wilson <wilson.andrew.j+github@gmail.com>
Andy Zhang <andy.zhangtao@hotmail.com>
Anes Hasicic <anes.hasicic@gmail.com>
Angel Velazquez <angelcar@amazon.com>
Anil Belur <askb23@gmail.com>
Anil Madhavapeddy <anil@recoil.org>
Ankit Jain <ajatkj@yahoo.co.in>
Ankush Agarwal <ankushagarwal11@gmail.com>
Anonmily <michelle@michelleliu.io>
Anran Qiao <anran.qiao@daocloud.io>
Anshul Pundir <anshul.pundir@docker.com>
Anthon van der Neut <anthon@mnt.org>
Anthony Baire <Anthony.Baire@irisa.fr>
Anthony Bishopric <git@anthonybishopric.com>
Anthony Dahanne <anthony.dahanne@gmail.com>
Anthony Sottile <asottile@umich.edu>
Anton Löfgren <anton.lofgren@gmail.com>
Anton Nikitin <anton.k.nikitin@gmail.com>
Anton Polonskiy <anton.polonskiy@gmail.com>
Anton Tiurin <noxiouz@yandex.ru>
Antonio Murdaca <antonio.murdaca@gmail.com>
Antonis Kalipetis <akalipetis@gmail.com>
Antony Messerli <amesserl@rackspace.com>
Anuj Bahuguna <anujbahuguna.dev@gmail.com>
Anuj Varma <anujvarma@thumbtack.com>
Anusha Ragunathan <anusha.ragunathan@docker.com>
Anyu Wang <wanganyu@outlook.com>
apocas <petermdias@gmail.com>
Arash Deshmeh <adeshmeh@ca.ibm.com>
ArikaChen <eaglesora@gmail.com>
Arko Dasgupta <arko@tetrate.io>
Arnaud Lefebvre <a.lefebvre@outlook.fr>
Arnaud Porterie <icecrime@gmail.com>
Arnaud Rebillout <arnaud.rebillout@collabora.com>
Artem Khramov <akhramov@pm.me>
Arthur Barr <arthur.barr@uk.ibm.com>
Arthur Gautier <baloo@gandi.net>
Artur Meyster <arthurfbi@yahoo.com>
Arun Gupta <arun.gupta@gmail.com>
Asad Saeeduddin <masaeedu@gmail.com>
Asbjørn Enge <asbjorn@hanafjedle.net>
Austin Vazquez <macedonv@amazon.com>
averagehuman <averagehuman@users.noreply.github.com>
Avi Das <andas222@gmail.com>
Avi Kivity <avi@scylladb.com>
Avi Miller <avi.miller@oracle.com>
Avi Vaid <avaid1996@gmail.com>
ayoshitake <airandfingers@gmail.com>
Azat Khuyiyakhmetov <shadow_uz@mail.ru>
Bao Yonglei <baoyonglei@huawei.com>
Bardia Keyoumarsi <bkeyouma@ucsc.edu>
Barnaby Gray <barnaby@pickle.me.uk>
Barry Allard <barry.allard@gmail.com>
Bartłomiej Piotrowski <b@bpiotrowski.pl>
Bastiaan Bakker <bbakker@xebia.com>
Bastien Pascard <bpascard@hotmail.com>
bdevloed <boris.de.vloed@gmail.com>
Bearice Ren <bearice@gmail.com>
Ben Bonnefoy <frenchben@docker.com>
Ben Firshman <ben@firshman.co.uk>
Ben Golub <ben.golub@dotcloud.com>
Ben Gould <ben@bengould.co.uk>
Ben Hall <ben@benhall.me.uk>
Ben Langfeld <ben@langfeld.me>
Ben Sargent <ben@brokendigits.com>
Ben Severson <BenSeverson@users.noreply.github.com>
Ben Toews <mastahyeti@gmail.com>
Ben Wiklund <ben@daisyowl.com>
Benjamin Atkin <ben@benatkin.com>
Benjamin Baker <Benjamin.baker@utexas.edu>
Benjamin Boudreau <boudreau.benjamin@gmail.com>
Benjamin Böhmke <benjamin@boehmke.net>
Benjamin Yolken <yolken@stripe.com>
Benny Ng <benny.tpng@gmail.com>
Benoit Chesneau <bchesneau@gmail.com>
Bernerd Schaefer <bj.schaefer@gmail.com>
Bernhard M. Wiedemann <bwiedemann@suse.de>
Bert Goethals <bert@bertg.be>
Bertrand Roussel <broussel@sierrawireless.com>
Bevisy Zhang <binbin36520@gmail.com>
Bharath Thiruveedula <bharath_ves@hotmail.com>
Bhiraj Butala <abhiraj.butala@gmail.com>
Bhumika Bayani <bhumikabayani@gmail.com>
Bilal Amarni <bilal.amarni@gmail.com>
Bill Wang <ozbillwang@gmail.com>
Billy Ridgway <wrridgwa@us.ibm.com>
Bily Zhang <xcoder@tenxcloud.com>
Bin Liu <liubin0329@gmail.com>
Bingshen Wang <bingshen.wbs@alibaba-inc.com>
Bjorn Neergaard <bneergaard@mirantis.com>
Blake Geno <blakegeno@gmail.com>
Boaz Shuster <ripcurld.github@gmail.com>
bobby abbott <ttobbaybbob@gmail.com>
Bojun Zhu <bojun.zhu@foxmail.com>
Boqin Qin <bobbqqin@gmail.com>
Boris Pruessmann <boris@pruessmann.org>
Boshi Lian <farmer1992@gmail.com>
Bouke Haarsma <bouke@webatoom.nl>
Boyd Hemphill <boyd@feedmagnet.com>
boynux <boynux@gmail.com>
Bradley Cicenas <bradley.cicenas@gmail.com>
Bradley Wright <brad@intranation.com>
Brandon Liu <bdon@bdon.org>
Brandon Philips <brandon.philips@coreos.com>
Brandon Rhodes <brandon@rhodesmill.org>
Brendan Dixon <brendand@microsoft.com>
Brent Salisbury <brent.salisbury@docker.com>
Brett Higgins <brhiggins@arbor.net>
Brett Kochendorfer <brett.kochendorfer@gmail.com>
Brett Milford <brettmilford@gmail.com>
Brett Randall <javabrett@gmail.com>
Brian (bex) Exelbierd <bexelbie@redhat.com>
Brian Bland <brian.bland@docker.com>
Brian DeHamer <brian@dehamer.com>
Brian Dorsey <brian@dorseys.org>
Brian Flad <bflad417@gmail.com>
Brian Goff <cpuguy83@gmail.com>
Brian McCallister <brianm@skife.org>
Brian Olsen <brian@maven-group.org>
Brian Schwind <brianmschwind@gmail.com>
Brian Shumate <brian@couchbase.com>
Brian Torres-Gil <brian@dralth.com>
Brian Trump <btrump@yelp.com>
Brice Jaglin <bjaglin@teads.tv>
Briehan Lombaard <briehan.lombaard@gmail.com>
Brielle Broder <bbroder@google.com>
Bruno Bigras <bigras.bruno@gmail.com>
Bruno Binet <bruno.binet@gmail.com>
Bruno Gazzera <bgazzera@paginar.com>
Bruno Renié <brutasse@gmail.com>
Bruno Tavares <btavare@thoughtworks.com>
Bryan Bess <squarejaw@bsbess.com>
Bryan Boreham <bjboreham@gmail.com>
Bryan Matsuo <bryan.matsuo@gmail.com>
Bryan Murphy <bmurphy1976@gmail.com>
Burke Libbey <burke@libbey.me>
Byung Kang <byung.kang.ctr@amrdec.army.mil>
Caleb Spare <cespare@gmail.com>
Calen Pennington <cale@edx.org>
Cameron Boehmer <cameron.boehmer@gmail.com>
Cameron Sparr <gh@sparr.email>
Cameron Spear <cameronspear@gmail.com>
Campbell Allen <campbell.allen@gmail.com>
Candid Dauth <cdauth@cdauth.eu>
Cao Weiwei <cao.weiwei30@zte.com.cn>
Carl Henrik Lunde <chlunde@ping.uio.no>
Carl Loa Odin <carlodin@gmail.com>
Carl X. Su <bcbcarl@gmail.com>
Carlo Mion <mion00@gmail.com>
Carlos Alexandro Becker <caarlos0@gmail.com>
Carlos de Paula <me@carlosedp.com>
Carlos Sanchez <carlos@apache.org>
Carol Fager-Higgins <carol.fager-higgins@docker.com>
Cary <caryhartline@users.noreply.github.com>
Casey Bisson <casey.bisson@joyent.com>
Catalin Pirvu <pirvu.catalin94@gmail.com>
Ce Gao <ce.gao@outlook.com>
Cedric Davies <cedricda@microsoft.com>
Cezar Sa Espinola <cezarsa@gmail.com>
Chad Swenson <chadswen@gmail.com>
Chance Zibolski <chance.zibolski@gmail.com>
Chander Govindarajan <chandergovind@gmail.com>
Chanhun Jeong <keyolk@gmail.com>
Chao Wang <wangchao.fnst@cn.fujitsu.com>
Charles Chan <charleswhchan@users.noreply.github.com>
Charles Hooper <charles.hooper@dotcloud.com>
Charles Law <claw@conduce.com>
Charles Lindsay <chaz@chazomatic.us>
Charles Merriam <charles.merriam@gmail.com>
Charles Sarrazin <charles@sarraz.in>
Charles Smith <charles.smith@docker.com>
Charlie Drage <charlie@charliedrage.com>
Charlie Lewis <charliel@lab41.org>
Chase Bolt <chase.bolt@gmail.com>
ChaYoung You <yousbe@gmail.com>
Chee Hau Lim <ch33hau@gmail.com>
Chen Chao <cc272309126@gmail.com>
Chen Chuanliang <chen.chuanliang@zte.com.cn>
Chen Hanxiao <chenhanxiao@cn.fujitsu.com>
Chen Min <chenmin46@huawei.com>
Chen Mingjie <chenmingjie0828@163.com>
Chen Qiu <cheney-90@hotmail.com>
Cheng-mean Liu <soccerl@microsoft.com>
Chengfei Shang <cfshang@alauda.io>
Chengguang Xu <cgxu519@gmx.com>
Chenyang Yan <memory.yancy@gmail.com>
chenyuzhu <chenyuzhi@oschina.cn>
Chetan Birajdar <birajdar.chetan@gmail.com>
Chewey <prosto-chewey@users.noreply.github.com>
Chia-liang Kao <clkao@clkao.org>
chli <chli@freewheel.tv>
Cholerae Hu <choleraehyq@gmail.com>
Chris Alfonso <calfonso@redhat.com>
Chris Armstrong <chris@opdemand.com>
Chris Dias <cdias@microsoft.com>
Chris Dituri <csdituri@gmail.com>
Chris Fordham <chris@fordham-nagy.id.au>
Chris Gavin <chris@chrisgavin.me>
Chris Gibson <chris@chrisg.io>
Chris Khoo <chris.khoo@gmail.com>
Chris Kreussling (Flatbush Gardener) <xrisfg@gmail.com>
Chris McKinnel <chris.mckinnel@tangentlabs.co.uk>
Chris McKinnel <chrismckinnel@gmail.com>
Chris Price <cprice@mirantis.com>
Chris Seto <chriskseto@gmail.com>
Chris Snow <chsnow123@gmail.com>
Chris St. Pierre <chris.a.st.pierre@gmail.com>
Chris Stivers <chris@stivers.us>
Chris Swan <chris.swan@iee.org>
Chris Telfer <ctelfer@docker.com>
Chris Wahl <github@wahlnetwork.com>
Chris Weyl <cweyl@alumni.drew.edu>
Chris White <me@cwprogram.com>
Christian Becker <christian.becker@sixt.com>
Christian Berendt <berendt@b1-systems.de>
Christian Brauner <christian.brauner@ubuntu.com>
Christian Böhme <developement@boehme3d.de>
Christian Muehlhaeuser <muesli@gmail.com>
Christian Persson <saser@live.se>
Christian Rotzoll <ch.rotzoll@gmail.com>
Christian Simon <simon@swine.de>
Christian Stefanescu <st.chris@gmail.com>
Christoph Ziebuhr <chris@codefrickler.de>
Christophe Mehay <cmehay@online.net>
Christophe Troestler <christophe.Troestler@umons.ac.be>
Christophe Vidal <kriss@krizalys.com>
Christopher Biscardi <biscarch@sketcht.com>
Christopher Crone <christopher.crone@docker.com>
Christopher Currie <codemonkey+github@gmail.com>
Christopher Jones <tophj@linux.vnet.ibm.com>
Christopher Latham <sudosurootdev@gmail.com>
Christopher Rigor <crigor@gmail.com>
Christy Norman <christy@linux.vnet.ibm.com>
Chun Chen <ramichen@tencent.com>
Ciro S. Costa <ciro.costa@usp.br>
Clayton Coleman <ccoleman@redhat.com>
Clint Armstrong <clint@clintarmstrong.net>
Clinton Kitson <clintonskitson@gmail.com>
clubby789 <jamie@hill-daniel.co.uk>
Cody Roseborough <crrosebo@amazon.com>
Coenraad Loubser <coenraad@wish.org.za>
Colin Dunklau <colin.dunklau@gmail.com>
Colin Hebert <hebert.colin@gmail.com>
Colin Panisset <github@clabber.com>
Colin Rice <colin@daedrum.net>
Colin Walters <walters@verbum.org>
Collin Guarino <collin.guarino@gmail.com>
Colm Hally <colmhally@gmail.com>
companycy <companycy@gmail.com>
Conor Evans <coevans@tcd.ie>
Corbin Coleman <corbin.coleman@docker.com>
Corey Farrell <git@cfware.com>
Cory Forsyth <cory.forsyth@gmail.com>
Cory Snider <csnider@mirantis.com>
cressie176 <github@stephen-cresswell.net>
Cristian Ariza <dev@cristianrz.com>
Cristian Staretu <cristian.staretu@gmail.com>
cristiano balducci <cristiano.balducci@gmail.com>
Cristina Yenyxe Gonzalez Garcia <cristina.yenyxe@gmail.com>
Cruceru Calin-Cristian <crucerucalincristian@gmail.com>
CUI Wei <ghostplant@qq.com>
cuishuang <imcusg@gmail.com>
Cuong Manh Le <cuong.manhle.vn@gmail.com>
Cyprian Gracz <cyprian.gracz@micro-jumbo.eu>
Cyril F <cyrilf7x@gmail.com>
Da McGrady <dabkb@aol.com>
Daan van Berkel <daan.v.berkel.1980@gmail.com>
Daehyeok Mun <daehyeok@gmail.com>
Dafydd Crosby <dtcrsby@gmail.com>
dalanlan <dalanlan925@gmail.com>
Damian Smyth <damian@dsau.co>
Damien Nadé <github@livna.org>
Damien Nozay <damien.nozay@gmail.com>
Damjan Georgievski <gdamjan@gmail.com>
Dan Anolik <dan@anolik.net>
Dan Buch <d.buch@modcloth.com>
Dan Cotora <dan@bluevision.ro>
Dan Feldman <danf@jfrog.com>
Dan Griffin <dgriffin@peer1.com>
Dan Hirsch <thequux@upstandinghackers.com>
Dan Keder <dan.keder@gmail.com>
Dan Levy <dan@danlevy.net>
Dan McPherson <dmcphers@redhat.com>
Dan Plamadeala <cornul11@gmail.com>
Dan Stine <sw@stinemail.com>
Dan Williams <me@deedubs.com>
Dani Hodovic <dani.hodovic@gmail.com>
Dani Louca <dani.louca@docker.com>
Daniel Antlinger <d.antlinger@gmx.at>
Daniel Black <daniel@linux.ibm.com>
Daniel Dao <dqminh@cloudflare.com>
Daniel Exner <dex@dragonslave.de>
Daniel Farrell <dfarrell@redhat.com>
Daniel Garcia <daniel@danielgarcia.info>
Daniel Gasienica <daniel@gasienica.ch>
Daniel Grunwell <mwgrunny@gmail.com>
Daniel Helfand <helfand.4@gmail.com>
Daniel Hiltgen <daniel.hiltgen@docker.com>
Daniel J Walsh <dwalsh@redhat.com>
Daniel Menet <membership@sontags.ch>
Daniel Mizyrycki <daniel.mizyrycki@dotcloud.com>
Daniel Nephin <dnephin@docker.com>
Daniel Norberg <dano@spotify.com>
Daniel Nordberg <dnordberg@gmail.com>
Daniel P. Berrangé <berrange@redhat.com>
Daniel Robinson <gottagetmac@gmail.com>
Daniel S <dan.streby@gmail.com>
Daniel Sweet <danieljsweet@icloud.com>
Daniel Von Fange <daniel@leancoder.com>
Daniel Watkins <daniel@daniel-watkins.co.uk>
Daniel X Moore <yahivin@gmail.com>
Daniel YC Lin <dlin.tw@gmail.com>
Daniel Zhang <jmzwcn@gmail.com>
Daniele Rondina <geaaru@sabayonlinux.org>
Danny Berger <dpb587@gmail.com>
Danny Milosavljevic <dannym@scratchpost.org>
Danny Yates <danny@codeaholics.org>
Danyal Khaliq <danyal.khaliq@tenpearls.com>
Darren Coxall <darren@darrencoxall.com>
Darren Shepherd <darren.s.shepherd@gmail.com>
Darren Stahl <darst@microsoft.com>
Dattatraya Kumbhar <dattatraya.kumbhar@gslab.com>
Davanum Srinivas <davanum@gmail.com>
Dave Barboza <dbarboza@datto.com>
Dave Goodchild <buddhamagnet@gmail.com>
Dave Henderson <dhenderson@gmail.com>
Dave MacDonald <mindlapse@gmail.com>
Dave Tucker <dt@docker.com>
David Anderson <dave@natulte.net>
David Bellotti <dbellotti@pivotal.io>
David Calavera <david.calavera@gmail.com>
David Chung <david.chung@docker.com>
David Corking <dmc-source@dcorking.com>
David Cramer <davcrame@cisco.com>
David Currie <david_currie@uk.ibm.com>
David Davis <daviddavis@redhat.com>
David Dooling <dooling@gmail.com>
David Gageot <david@gageot.net>
David Gebler <davidgebler@gmail.com>
David Glasser <glasser@davidglasser.net>
David Lawrence <david.lawrence@docker.com>
David Lechner <david@lechnology.com>
David M. Karr <davidmichaelkarr@gmail.com>
David Mackey <tdmackey@booleanhaiku.com>
David Manouchehri <manouchehri@riseup.net>
David Mat <david@davidmat.com>
David Mcanulty <github@hellspark.com>
David McKay <david@rawkode.com>
David O'Rourke <david@scalefactory.com>
David P Hilton <david.hilton.p@gmail.com>
David Pelaez <pelaez89@gmail.com>
David R. Jenni <david.r.jenni@gmail.com>
David Röthlisberger <david@rothlis.net>
David Sheets <dsheets@docker.com>
David Sissitka <me@dsissitka.com>
David Trott <github@davidtrott.com>
David Wang <00107082@163.com>
David Williamson <david.williamson@docker.com>
David Xia <dxia@spotify.com>
David Young <yangboh@cn.ibm.com>
Davide Ceretti <davide.ceretti@hogarthww.com>
Dawn Chen <dawnchen@google.com>
dbdd <wangtong2712@gmail.com>
dcylabs <dcylabs@gmail.com>
Debayan De <debayande@users.noreply.github.com>
Deborah Gertrude Digges <deborah.gertrude.digges@gmail.com>
deed02392 <georgehafiz@gmail.com>
Deep Debroy <ddebroy@docker.com>
Deng Guangxing <dengguangxing@huawei.com>
Deni Bertovic <deni@kset.org>
Denis Defreyne <denis@soundcloud.com>
Denis Gladkikh <denis@gladkikh.email>
Denis Ollier <larchunix@users.noreply.github.com>
Dennis Chen <barracks510@gmail.com>
Dennis Chen <dennis.chen@arm.com>
Dennis Docter <dennis@d23.nl>
Derek <crq@kernel.org>
Derek <crquan@gmail.com>
Derek Ch <denc716@gmail.com>
Derek McGowan <derek@mcg.dev>
Deric Crago <deric.crago@gmail.com>
Deshi Xiao <dxiao@redhat.com>
Devon Estes <devon.estes@klarna.com>
Devvyn Murphy <devvyn@devvyn.com>
Dharmit Shah <shahdharmit@gmail.com>
Dhawal Yogesh Bhanushali <dbhanushali@vmware.com>
Dhilip Kumars <dhilip.kumar.s@huawei.com>
Diego Romero <idiegoromero@gmail.com>
Diego Siqueira <dieg0@live.com>
Dieter Reuter <dieter.reuter@me.com>
Dillon Dixon <dillondixon@gmail.com>
Dima Stopel <dima@twistlock.com>
Dimitri John Ledkov <dimitri.j.ledkov@intel.com>
Dimitris Mandalidis <dimitris.mandalidis@gmail.com>
Dimitris Rozakis <dimrozakis@gmail.com>
Dimitry Andric <d.andric@activevideo.com>
Dinesh Subhraveti <dineshs@altiscale.com>
Ding Fei <dingfei@stars.org.cn>
dingwei <dingwei@cmss.chinamobile.com>
Diogo Monica <diogo@docker.com>
DiuDiugirl <sophia.wang@pku.edu.cn>
Djibril Koné <kone.djibril@gmail.com>
Djordje Lukic <djordje.lukic@docker.com>
dkumor <daniel@dkumor.com>
Dmitri Logvinenko <dmitri.logvinenko@gmail.com>
Dmitri Shuralyov <shurcooL@gmail.com>
Dmitry Demeshchuk <demeshchuk@gmail.com>
Dmitry Gusev <dmitry.gusev@gmail.com>
Dmitry Kononenko <d@dm42.ru>
Dmitry Sharshakov <d3dx12.xx@gmail.com>
Dmitry Shyshkin <dmitry@shyshkin.org.ua>
Dmitry Smirnov <onlyjob@member.fsf.org>
Dmitry V. Krivenok <krivenok.dmitry@gmail.com>
Dmitry Vorobev <dimahabr@gmail.com>
Dmytro Iakovliev <dmytro.iakovliev@zodiacsystems.com>
docker-unir[bot] <docker-unir[bot]@users.noreply.github.com>
Dolph Mathews <dolph.mathews@gmail.com>
Dominic Tubach <dominic.tubach@to.com>
Dominic Yin <yindongchao@inspur.com>
Dominik Dingel <dingel@linux.vnet.ibm.com>
Dominik Finkbeiner <finkes93@gmail.com>
Dominik Honnef <dominik@honnef.co>
Don Kirkby <donkirkby@users.noreply.github.com>
Don Kjer <don.kjer@gmail.com>
Don Spaulding <donspauldingii@gmail.com>
Donald Huang <don.hcd@gmail.com>
Dong Chen <dongluo.chen@docker.com>
Donghwa Kim <shanytt@gmail.com>
Donovan Jones <git@gamma.net.nz>
Doron Podoleanu <doronp@il.ibm.com>
Doug Davis <dug@us.ibm.com>
Doug MacEachern <dougm@vmware.com>
Doug Tangren <d.tangren@gmail.com>
Douglas Curtis <dougcurtis1@gmail.com>
Dr Nic Williams <drnicwilliams@gmail.com>
dragon788 <dragon788@users.noreply.github.com>
Dražen Lučanin <kermit666@gmail.com>
Drew Erny <derny@mirantis.com>
Drew Hubl <drew.hubl@gmail.com>
Dustin Sallings <dustin@spy.net>
Ed Costello <epc@epcostello.com>
Edmund Wagner <edmund-wagner@web.de>
Eiichi Tsukata <devel@etsukata.com>
Eike Herzbach <eike@herzbach.net>
Eivin Giske Skaaren <eivinsn@axis.com>
Eivind Uggedal <eivind@uggedal.com>
Elan Ruusamäe <glen@pld-linux.org>
Elango Sivanandam <elango.siva@docker.com>
Elena Morozova <lelenanam@gmail.com>
Eli Uriegas <seemethere101@gmail.com>
Elias Faxö <elias.faxo@tre.se>
Elias Koromilas <elias.koromilas@gmail.com>
Elias Probst <mail@eliasprobst.eu>
Elijah Zupancic <elijah@zupancic.name>
eluck <mail@eluck.me>
Elvir Kuric <elvirkuric@gmail.com>
Emil Davtyan <emil2k@gmail.com>
Emil Hernvall <emil@quench.at>
Emily Maier <emily@emilymaier.net>
Emily Rose <emily@contactvibe.com>
Emir Ozer <emirozer@yandex.com>
Eng Zer Jun <engzerjun@gmail.com>
Enguerran <engcolson@gmail.com>
Eohyung Lee <liquidnuker@gmail.com>
epeterso <epeterson@breakpoint-labs.com>
Eric Barch <barch@tomesoftware.com>
Eric Curtin <ericcurtin17@gmail.com>
Eric G. Noriega <enoriega@vizuri.com>
Eric Hanchrow <ehanchrow@ine.com>
Eric Lee <thenorthsecedes@gmail.com>
Eric Mountain <eric.mountain@datadoghq.com>
Eric Myhre <hash@exultant.us>
Eric Paris <eparis@redhat.com>
Eric Rafaloff <erafaloff@gmail.com>
Eric Rosenberg <ehaydenr@gmail.com>
Eric Sage <eric.david.sage@gmail.com>
Eric Soderstrom <ericsoderstrom@gmail.com>
Eric Yang <windfarer@gmail.com>
Eric-Olivier Lamey <eo@lamey.me>
Erica Windisch <erica@windisch.us>
Erich Cordoba <erich.cm@yandex.com>
Erik Bray <erik.m.bray@gmail.com>
Erik Dubbelboer <erik@dubbelboer.com>
Erik Hollensbe <github@hollensbe.org>
Erik Inge Bolsø <knan@redpill-linpro.com>
Erik Kristensen <erik@erikkristensen.com>
Erik Sipsma <erik@sipsma.dev>
Erik St. Martin <alakriti@gmail.com>
Erik Weathers <erikdw@gmail.com>
Erno Hopearuoho <erno.hopearuoho@gmail.com>
Erwin van der Koogh <info@erronis.nl>
Espen Suenson <mail@espensuenson.dk>
Ethan Bell <ebgamer29@gmail.com>
Ethan Mosbaugh <ethan@replicated.com>
Euan Harris <euan.harris@docker.com>
Euan Kemp <euan.kemp@coreos.com>
Eugen Krizo <eugen.krizo@gmail.com>
Eugene Yakubovich <eugene.yakubovich@coreos.com>
Evan Allrich <evan@unguku.com>
Evan Carmi <carmi@users.noreply.github.com>
Evan Hazlett <ejhazlett@gmail.com>
Evan Krall <krall@yelp.com>
Evan Phoenix <evan@fallingsnow.net>
Evan Wies <evan@neomantra.net>
Evelyn Xu <evelynhsu21@gmail.com>
Everett Toews <everett.toews@rackspace.com>
Evgeniy Makhrov <e.makhrov@corp.badoo.com>
Evgeny Shmarnev <shmarnev@gmail.com>
Evgeny Vereshchagin <evvers@ya.ru>
Ewa Czechowska <ewa@ai-traders.com>
Eystein Måløy Stenberg <eystein.maloy.stenberg@cfengine.com>
ezbercih <cem.ezberci@gmail.com>
Ezra Silvera <ezra@il.ibm.com>
Fabian Kramm <kramm@covexo.com>
Fabian Lauer <kontakt@softwareschmiede-saar.de>
Fabian Raetz <fabian.raetz@gmail.com>
Fabiano Rosas <farosas@br.ibm.com>
Fabio Falci <fabiofalci@gmail.com>
Fabio Kung <fabio.kung@gmail.com>
Fabio Rapposelli <fabio@vmware.com>
Fabio Rehm <fgrehm@gmail.com>
Fabrizio Regini <freegenie@gmail.com>
Fabrizio Soppelsa <fsoppelsa@mirantis.com>
Faiz Khan <faizkhan00@gmail.com>
falmp <chico.lopes@gmail.com>
Fangming Fang <fangming.fang@arm.com>
Fangyuan Gao <21551127@zju.edu.cn>
fanjiyun <fan.jiyun@zte.com.cn>
Fareed Dudhia <fareeddudhia@googlemail.com>
Fathi Boudra <fathi.boudra@linaro.org>
Federico Gimenez <fgimenez@coit.es>
Felipe Oliveira <felipeweb.programador@gmail.com>
Felipe Ruhland <felipe.ruhland@gmail.com>
Felix Abecassis <fabecassis@nvidia.com>
Felix Geisendörfer <felix@debuggable.com>
Felix Hupfeld <felix@quobyte.com>
Felix Rabe <felix@rabe.io>
Felix Ruess <felix.ruess@gmail.com>
Felix Schindler <fschindler@weluse.de>
Feng Yan <fy2462@gmail.com>
Fengtu Wang <wangfengtu@huawei.com>
Ferenc Szabo <pragmaticfrank@gmail.com>
Fernando <fermayo@gmail.com>
Fero Volar <alian@alian.info>
Feroz Salam <feroz.salam@sourcegraph.com>
Ferran Rodenas <frodenas@gmail.com>
Filipe Brandenburger <filbranden@google.com>
Filipe Oliveira <contato@fmoliveira.com.br>
Flavio Castelli <fcastelli@suse.com>
Flavio Crisciani <flavio.crisciani@docker.com>
Florian <FWirtz@users.noreply.github.com>
Florian Klein <florian.klein@free.fr>
Florian Maier <marsmensch@users.noreply.github.com>
Florian Noeding <noeding@adobe.com>
Florian Schmaus <flo@geekplace.eu>
Florian Weingarten <flo@hackvalue.de>
Florin Asavoaie <florin.asavoaie@gmail.com>
Florin Patan <florinpatan@gmail.com>
fonglh <fonglh@gmail.com>
Foysal Iqbal <foysal.iqbal.fb@gmail.com>
Francesc Campoy <campoy@google.com>
Francesco Degrassi <francesco.degrassi@optionfactory.net>
Francesco Mari <mari.francesco@gmail.com>
Francis Chuang <francis.chuang@boostport.com>
Francisco Carriedo <fcarriedo@gmail.com>
Francisco Souza <f@souza.cc>
Frank Groeneveld <frank@ivaldi.nl>
Frank Herrmann <fgh@4gh.tv>
Frank Macreery <frank@macreery.com>
Frank Rosquin <frank.rosquin+github@gmail.com>
Frank Yang <yyb196@gmail.com>
Fred Lifton <fred.lifton@docker.com>
Frederick F. Kautz IV <fkautz@redhat.com>
Frederico F. de Oliveira <FreddieOliveira@users.noreply.github.com>
Frederik Loeffert <frederik@zitrusmedia.de>
Frederik Nordahl Jul Sabroe <frederikns@gmail.com>
Freek Kalter <freek@kalteronline.org>
Frieder Bluemle <frieder.bluemle@gmail.com>
frobnicaty <92033765+frobnicaty@users.noreply.github.com>
Frédéric Dalleau <frederic.dalleau@docker.com>
Fu JinLin <withlin@yeah.net>
Félix Baylac-Jacqué <baylac.felix@gmail.com>
Félix Cantournet <felix.cantournet@cloudwatt.com>
Gabe Rosenhouse <gabe@missionst.com>
Gabor Nagy <mail@aigeruth.hu>
Gabriel Goller <gabrielgoller123@gmail.com>
Gabriel L. Somlo <gsomlo@gmail.com>
Gabriel Linder <linder.gabriel@gmail.com>
Gabriel Monroy <gabriel@opdemand.com>
Gabriel Nicolas Avellaneda <avellaneda.gabriel@gmail.com>
Gaetan de Villele <gdevillele@gmail.com>
Galen Sampson <galen.sampson@gmail.com>
Gang Qiao <qiaohai8866@gmail.com>
Gareth Rushgrove <gareth@morethanseven.net>
Garrett Barboza <garrett@garrettbarboza.com>
Gary Schaetz <gary@schaetzkc.com>
Gaurav <gaurav.gosec@gmail.com>
Gaurav Singh <gaurav1086@gmail.com>
Gaël PORTAY <gael.portay@savoirfairelinux.com>
Genki Takiuchi <genki@s21g.com>
GennadySpb <lipenkov@gmail.com>
Geoff Levand <geoff@infradead.org>
Geoffrey Bachelet <grosfrais@gmail.com>
Geon Kim <geon0250@gmail.com>
George Kontridze <george@bugsnag.com>
George MacRorie <gmacr31@gmail.com>
George Xie <georgexsh@gmail.com>
Georgi Hristozov <georgi@forkbomb.nl>
Georgy Yakovlev <gyakovlev@gentoo.org>
Gereon Frey <gereon.frey@dynport.de>
German DZ <germ@ndz.com.ar>
Gert van Valkenhoef <g.h.m.van.valkenhoef@rug.nl>
Gerwim Feiken <g.feiken@tfe.nl>
Ghislain Bourgeois <ghislain.bourgeois@gmail.com>
Giampaolo Mancini <giampaolo@trampolineup.com>
Gianluca Borello <g.borello@gmail.com>
Gildas Cuisinier <gildas.cuisinier@gcuisinier.net>
Giovan Isa Musthofa <giovanism@outlook.co.id>
gissehel <public-devgit-dantus@gissehel.org>
Giuseppe Mazzotta <gdm85@users.noreply.github.com>
Giuseppe Scrivano <gscrivan@redhat.com>
Gleb Fotengauer-Malinovskiy <glebfm@altlinux.org>
Gleb M Borisov <borisov.gleb@gmail.com>
Glyn Normington <gnormington@gopivotal.com>
GoBella <caili_welcome@163.com>
Goffert van Gool <goffert@phusion.nl>
Goldwyn Rodrigues <rgoldwyn@suse.com>
Gopikannan Venugopalsamy <gopikannan.venugopalsamy@gmail.com>
Gosuke Miyashita <gosukenator@gmail.com>
Gou Rao <gou@portworx.com>
Govinda Fichtner <govinda.fichtner@googlemail.com>
Grant Millar <rid@cylo.io>
Grant Reaber <grant.reaber@gmail.com>
Graydon Hoare <graydon@pobox.com>
Greg Fausak <greg@tacodata.com>
Greg Pflaum <gpflaum@users.noreply.github.com>
Greg Stephens <greg@udon.org>
Greg Thornton <xdissent@me.com>
Grzegorz Jaśkiewicz <gj.jaskiewicz@gmail.com>
Guilhem Lettron <guilhem+github@lettron.fr>
Guilherme Salgado <gsalgado@gmail.com>
Guillaume Dufour <gdufour.prestataire@voyages-sncf.com>
Guillaume J. Charmes <guillaume.charmes@docker.com>
Gunadhya S. <6939749+gunadhya@users.noreply.github.com>
Guoqiang QI <guoqiang.qi1@gmail.com>
guoxiuyan <guoxiuyan@huawei.com>
Guri <odg0318@gmail.com>
Gurjeet Singh <gurjeet@singh.im>
Guruprasad <lgp171188@gmail.com>
Gustav Sinder <gustav.sinder@gmail.com>
gwx296173 <gaojing3@huawei.com>
Günter Zöchbauer <guenter@gzoechbauer.com>
Haichao Yang <yang.haichao@zte.com.cn>
haikuoliu <haikuo@amazon.com>
haining.cao <haining.cao@daocloud.io>
Hakan Özler <hakan.ozler@kodcu.com>
Hamish Hutchings <moredhel@aoeu.me>
Hannes Ljungberg <hannes@5monkeys.se>
Hans Kristian Flaatten <hans@starefossen.com>
Hans Rødtang <hansrodtang@gmail.com>
Hao Shu Wei <haoshuwei24@gmail.com>
Hao Zhang <21521210@zju.edu.cn>
Harald Albers <github@albersweb.de>
Harald Niesche <harald@niesche.de>
Harley Laue <losinggeneration@gmail.com>
Harold Cooper <hrldcpr@gmail.com>
Harrison Turton <harrisonturton@gmail.com>
Harry Zhang <harryz@hyper.sh>
Harshal Patil <harshal.patil@in.ibm.com>
Harshal Patil <harshalp@linux.vnet.ibm.com>
He Simei <hesimei@zju.edu.cn>
He Xiaoxi <tossmilestone@gmail.com>
He Xin <he_xinworld@126.com>
heartlock <21521209@zju.edu.cn>
Hector Castro <hectcastro@gmail.com>
Helen Xie <chenjg@harmonycloud.cn>
Henning Sprang <henning.sprang@gmail.com>
Hiroshi Hatake <hatake@clear-code.com>
Hiroyuki Sasagawa <hs19870702@gmail.com>
Hobofan <goisser94@gmail.com>
Hollie Teal <hollie@docker.com>
Hong Xu <hong@topbug.net>
Hongbin Lu <hongbin034@gmail.com>
Hongxu Jia <hongxu.jia@windriver.com>
Honza Pokorny <me@honza.ca>
Hsing-Hui Hsu <hsinghui@amazon.com>
hsinko <21551195@zju.edu.cn>
Hu Keping <hukeping@huawei.com>
Hu Tao <hutao@cn.fujitsu.com>
HuanHuan Ye <logindaveye@gmail.com>
Huanzhong Zhang <zhanghuanzhong90@gmail.com>
Huayi Zhang <irachex@gmail.com>
Hugo Barrera <hugo@barrera.io>
Hugo Duncan <hugo@hugoduncan.org>
Hugo Marisco <0x6875676f@gmail.com>
Hui Kang <hkang.sunysb@gmail.com>
Hunter Blanks <hunter@twilio.com>
huqun <huqun@zju.edu.cn>
Huu Nguyen <huu@prismskylabs.com>
Hyeongkyu Lee <hyeongkyu.lee@navercorp.com>
Hyzhou Zhy <hyzhou.zhy@alibaba-inc.com>
Iago López Galeiras <iago@kinvolk.io>
Ian Bishop <ianbishop@pace7.com>
Ian Bull <irbull@gmail.com>
Ian Calvert <ianjcalvert@gmail.com>
Ian Campbell <ian.campbell@docker.com>
Ian Chen <ianre657@gmail.com>
Ian Lee <IanLee1521@gmail.com>
Ian Main <imain@redhat.com>
Ian Philpot <ian.philpot@microsoft.com>
Ian Truslove <ian.truslove@gmail.com>
Iavael <iavaelooeyt@gmail.com>
Icaro Seara <icaro.seara@gmail.com>
Ignacio Capurro <icapurrofagian@gmail.com>
Igor Dolzhikov <bluesriverz@gmail.com>
Igor Karpovich <i.karpovich@currencysolutions.com>
Iliana Weller <iweller@amazon.com>
Ilkka Laukkanen <ilkka@ilkka.io>
Illo Abdulrahim <abdulrahim.illo@nokia.com>
Ilya Dmitrichenko <errordeveloper@gmail.com>
Ilya Gusev <mail@igusev.ru>
Ilya Khlopotov <ilya.khlopotov@gmail.com>
imre Fitos <imre.fitos+github@gmail.com>
inglesp <peter.inglesby@gmail.com>
Ingo Gottwald <in.gottwald@gmail.com>
Innovimax <innovimax@gmail.com>
Isaac Dupree <antispam@idupree.com>
Isabel Jimenez <contact.isabeljimenez@gmail.com>
Isaiah Grace <irgkenya4@gmail.com>
Isao Jonas <isao.jonas@gmail.com>
Iskander Sharipov <quasilyte@gmail.com>
Ivan Babrou <ibobrik@gmail.com>
Ivan Fraixedes <ifcdev@gmail.com>
Ivan Grcic <igrcic@gmail.com>
Ivan Markin <sw@nogoegst.net>
J Bruni <joaohbruni@yahoo.com.br>
J. Nunn <jbnunn@gmail.com>
Jack Danger Canty <jackdanger@squareup.com>
Jack Laxson <jackjrabbit@gmail.com>
Jacob Atzen <jacob@jacobatzen.dk>
Jacob Edelman <edelman.jd@gmail.com>
Jacob Tomlinson <jacob@tom.linson.uk>
Jacob Vallejo <jakeev@amazon.com>
Jacob Wen <jian.w.wen@oracle.com>
Jaime Cepeda <jcepedavillamayor@gmail.com>
Jaivish Kothari <janonymous.codevulture@gmail.com>
Jake Champlin <jake.champlin.27@gmail.com>
Jake Moshenko <jake@devtable.com>
Jake Sanders <jsand@google.com>
Jakub Drahos <jdrahos@pulsepoint.com>
Jakub Guzik <jakubmguzik@gmail.com>
James Allen <jamesallen0108@gmail.com>
James Carey <jecarey@us.ibm.com>
James Carr <james.r.carr@gmail.com>
James DeFelice <james.defelice@ishisystems.com>
James Harrison Fisher <jameshfisher@gmail.com>
James Kyburz <james.kyburz@gmail.com>
James Kyle <james@jameskyle.org>
James Lal <james@lightsofapollo.com>
James Mills <prologic@shortcircuit.net.au>
James Nesbitt <jnesbitt@mirantis.com>
James Nugent <james@jen20.com>
James Sanders <james3sanders@gmail.com>
James Turnbull <james@lovedthanlost.net>
James Watkins-Harvey <jwatkins@progi-media.com>
Jamie Hannaford <jamie@limetree.org>
Jamshid Afshar <jafshar@yahoo.com>
Jan Breig <git@pygos.space>
Jan Chren <dev.rindeal@gmail.com>
Jan Götte <jaseg@jaseg.net>
Jan Keromnes <janx@linux.com>
Jan Koprowski <jan.koprowski@gmail.com>
Jan Pazdziora <jpazdziora@redhat.com>
Jan Toebes <jan@toebes.info>
Jan-Gerd Tenberge <janten@gmail.com>
Jan-Jaap Driessen <janjaapdriessen@gmail.com>
Jana Radhakrishnan <mrjana@docker.com>
Jannick Fahlbusch <git@jf-projects.de>
Januar Wayong <januar@gmail.com>
Jared Biel <jared.biel@bolderthinking.com>
Jared Hocutt <jaredh@netapp.com>
Jaroslaw Zabiello <hipertracker@gmail.com>
Jasmine Hegman <jasmine@jhegman.com>
Jason A. Donenfeld <Jason@zx2c4.com>
Jason Divock <jdivock@gmail.com>
Jason Giedymin <jasong@apache.org>
Jason Green <Jason.Green@AverInformatics.Com>
Jason Hall <imjasonh@gmail.com>
Jason Heiss <jheiss@aput.net>
Jason Livesay <ithkuil@gmail.com>
Jason McVetta <jason.mcvetta@gmail.com>
Jason Plum <jplum@devonit.com>
Jason Shepherd <jason@jasonshepherd.net>
Jason Smith <jasonrichardsmith@gmail.com>
Jason Sommer <jsdirv@gmail.com>
Jason Stangroome <jason@codeassassin.com>
Javier Bassi <javierbassi@gmail.com>
jaxgeller <jacksongeller@gmail.com>
Jay <teguhwpurwanto@gmail.com>
Jay Kamat <github@jgkamat.33mail.com>
Jay Lim <jay@imjching.com>
Jean Rouge <rougej+github@gmail.com>
Jean-Baptiste Barth <jeanbaptiste.barth@gmail.com>
Jean-Baptiste Dalido <jeanbaptiste@appgratis.com>
Jean-Christophe Berthon <huygens@berthon.eu>
Jean-Paul Calderone <exarkun@twistedmatrix.com>
Jean-Pierre Huynh <jean-pierre.huynh@ounet.fr>
Jean-Tiare Le Bigot <jt@yadutaf.fr>
Jeeva S. Chelladhurai <sjeeva@gmail.com>
Jeff Anderson <jeff@docker.com>
Jeff Hajewski <jeff.hajewski@gmail.com>
Jeff Johnston <jeff.johnston.mn@gmail.com>
Jeff Lindsay <progrium@gmail.com>
Jeff Mickey <j@codemac.net>
Jeff Minard <jeff@creditkarma.com>
Jeff Nickoloff <jeff.nickoloff@gmail.com>
Jeff Silberman <jsilberm@gmail.com>
Jeff Welch <whatthejeff@gmail.com>
Jeff Zvier <zvier20@gmail.com>
Jeffrey Bolle <jeffreybolle@gmail.com>
Jeffrey Morgan <jmorganca@gmail.com>
Jeffrey van Gogh <jvg@google.com>
Jenny Gebske <jennifer@gebske.de>
Jeremy Chambers <jeremy@thehipbot.com>
Jeremy Grosser <jeremy@synack.me>
Jeremy Huntwork <jhuntwork@lightcubesolutions.com>
Jeremy Price <jprice.rhit@gmail.com>
Jeremy Qian <vanpire110@163.com>
Jeremy Unruh <jeremybunruh@gmail.com>
Jeremy Yallop <yallop@docker.com>
Jeroen Franse <jeroenfranse@gmail.com>
Jeroen Jacobs <github@jeroenj.be>
Jesse Dearing <jesse.dearing@gmail.com>
Jesse Dubay <jesse@thefortytwo.net>
Jessica Frazelle <jess@oxide.computer>
Jezeniel Zapanta <jpzapanta22@gmail.com>
Jhon Honce <jhonce@redhat.com>
Ji.Zhilong <zhilongji@gmail.com>
Jian Liao <jliao@alauda.io>
Jian Zhang <zhangjian.fnst@cn.fujitsu.com>
Jiang Jinyang <jjyruby@gmail.com>
Jianyong Wu <jianyong.wu@arm.com>
Jie Luo <luo612@zju.edu.cn>
Jie Ma <jienius@outlook.com>
Jihyun Hwang <jhhwang@telcoware.com>
Jilles Oldenbeuving <ojilles@gmail.com>
Jim Alateras <jima@comware.com.au>
Jim Carroll <jim.carroll@docker.com>
Jim Ehrismann <jim.ehrismann@docker.com>
Jim Galasyn <jim.galasyn@docker.com>
Jim Lin <b04705003@ntu.edu.tw>
Jim Minter <jminter@redhat.com>
Jim Perrin <jperrin@centos.org>
Jimmy Cuadra <jimmy@jimmycuadra.com>
Jimmy Puckett <jimmy.puckett@spinen.com>
Jimmy Song <rootsongjc@gmail.com>
Jinsoo Park <cellpjs@gmail.com>
Jintao Zhang <zhangjintao9020@gmail.com>
Jiri Appl <jiria@microsoft.com>
Jiri Popelka <jpopelka@redhat.com>
Jiuyue Ma <majiuyue@huawei.com>
Jiří Župka <jzupka@redhat.com>
Joakim Roubert <joakim.roubert@axis.com>
Joao Fernandes <joao.fernandes@docker.com>
Joao Trindade <trindade.joao@gmail.com>
Joe Beda <joe.github@bedafamily.com>
Joe Doliner <jdoliner@pachyderm.io>
Joe Ferguson <joe@infosiftr.com>
Joe Gordon <joe.gordon0@gmail.com>
Joe Shaw <joe@joeshaw.org>
Joe Van Dyk <joe@tanga.com>
Joel Friedly <joelfriedly@gmail.com>
Joel Handwell <joelhandwell@gmail.com>
Joel Hansson <joel.hansson@ecraft.com>
Joel Wurtz <jwurtz@jolicode.com>
Joey Geiger <jgeiger@gmail.com>
Joey Geiger <jgeiger@users.noreply.github.com>
Joey Gibson <joey@joeygibson.com>
Joffrey F <joffrey@docker.com>
Johan Euphrosine <proppy@google.com>
Johan Rydberg <johan.rydberg@gmail.com>
Johanan Lieberman <johanan.lieberman@gmail.com>
Johannes 'fish' Ziemke <github@freigeist.org>
John Costa <john.costa@gmail.com>
John Feminella <jxf@jxf.me>
John Gardiner Myers <jgmyers@proofpoint.com>
John Gossman <johngos@microsoft.com>
John Harris <john@johnharris.io>
John Howard <github@lowenna.com>
John Laswell <john.n.laswell@gmail.com>
John Maguire <jmaguire@duosecurity.com>
John Mulhausen <john@docker.com>
John OBrien III <jobrieniii@yahoo.com>
John Starks <jostarks@microsoft.com>
John Stephens <johnstep@docker.com>
John Tims <john.k.tims@gmail.com>
John V. Martinez <jvmatl@gmail.com>
John Warwick <jwarwick@gmail.com>
John Willis <john.willis@docker.com>
Jon Johnson <jonjohnson@google.com>
Jon Surrell <jon.surrell@gmail.com>
Jon Wedaman <jweede@gmail.com>
Jonas Dohse <jonas@dohse.ch>
Jonas Heinrich <Jonas@JonasHeinrich.com>
Jonas Pfenniger <jonas@pfenniger.name>
Jonathan A. Schweder <jonathanschweder@gmail.com>
Jonathan A. Sternberg <jonathansternberg@gmail.com>
Jonathan Boulle <jonathanboulle@gmail.com>
Jonathan Camp <jonathan@irondojo.com>
Jonathan Choy <jonathan.j.choy@gmail.com>
Jonathan Dowland <jon+github@alcopop.org>
Jonathan Lebon <jlebon@redhat.com>
Jonathan Lomas <jonathan@floatinglomas.ca>
Jonathan McCrohan <jmccrohan@gmail.com>
Jonathan Mueller <j.mueller@apoveda.ch>
Jonathan Pares <jonathanpa@users.noreply.github.com>
Jonathan Rudenberg <jonathan@titanous.com>
Jonathan Stoppani <jonathan.stoppani@divio.com>
Jonh Wendell <jonh.wendell@redhat.com>
Joni Sar <yoni@cocycles.com>
Joost Cassee <joost@cassee.net>
Jordan Arentsen <blissdev@gmail.com>
Jordan Jennings <jjn2009@gmail.com>
Jordan Sissel <jls@semicomplete.com>
Jordi Massaguer Pla <jmassaguerpla@suse.de>
Jorge Marin <chipironcin@users.noreply.github.com>
Jorit Kleine-Möllhoff <joppich@bricknet.de>
Jose Diaz-Gonzalez <email@josediazgonzalez.com>
Joseph Anthony Pasquale Holsten <joseph@josephholsten.com>
Joseph Hager <ajhager@gmail.com>
Joseph Kern <jkern@semafour.net>
Joseph Rothrock <rothrock@rothrock.org>
Josh <jokajak@gmail.com>
Josh Bodah <jb3689@yahoo.com>
Josh Bonczkowski <josh.bonczkowski@gmail.com>
Josh Chorlton <jchorlton@gmail.com>
Josh Eveleth <joshe@opendns.com>
Josh Hawn <josh.hawn@docker.com>
Josh Horwitz <horwitz@addthis.com>
Josh Poimboeuf <jpoimboe@redhat.com>
Josh Soref <jsoref@gmail.com>
Josh Wilson <josh.wilson@fivestars.com>
Josiah Kiehl <jkiehl@riotgames.com>
José Tomás Albornoz <jojo@eljojo.net>
Joyce Jang <mail@joycejang.com>
JP <jpellerin@leapfrogonline.com>
Julian Taylor <jtaylor.debian@googlemail.com>
Julien Barbier <write0@gmail.com>
Julien Bisconti <veggiemonk@users.noreply.github.com>
Julien Bordellier <julienbordellier@gmail.com>
Julien Dubois <julien.dubois@gmail.com>
Julien Kassar <github@kassisol.com>
Julien Maitrehenry <julien.maitrehenry@me.com>
Julien Pervillé <julien.perville@perfect-memory.com>
Julien Pivotto <roidelapluie@inuits.eu>
Julio Guerra <julio@sqreen.com>
Julio Montes <imc.coder@gmail.com>
Jun Du <dujun5@huawei.com>
Jun-Ru Chang <jrjang@gmail.com>
junxu <xujun@cmss.chinamobile.com>
Jussi Nummelin <jussi.nummelin@gmail.com>
Justas Brazauskas <brazauskasjustas@gmail.com>
Justen Martin <jmart@the-coder.com>
Justin Cormack <justin.cormack@docker.com>
Justin Force <justin.force@gmail.com>
Justin Keller <85903732+jk-vb@users.noreply.github.com>
Justin Menga <justin.menga@gmail.com>
Justin Plock <jplock@users.noreply.github.com>
Justin Simonelis <justin.p.simonelis@gmail.com>
Justin Terry <juterry@microsoft.com>
Justyn Temme <justyntemme@gmail.com>
Jyrki Puttonen <jyrkiput@gmail.com>
Jérémy Leherpeur <amenophis@leherpeur.net>
Jérôme Petazzoni <jerome.petazzoni@docker.com>
Jörg Thalheim <joerg@higgsboson.tk>
K. Heller <pestophagous@gmail.com>
Kai Blin <kai@samba.org>
Kai Qiang Wu (Kennan) <wkq5325@gmail.com>
Kaijie Chen <chen@kaijie.org>
Kamil Domański <kamil@domanski.co>
Kamjar Gerami <kami.gerami@gmail.com>
Kanstantsin Shautsou <kanstantsin.sha@gmail.com>
Kara Alexandra <kalexandra@us.ibm.com>
Karan Lyons <karan@karanlyons.com>
Kareem Khazem <karkhaz@karkhaz.com>
kargakis <kargakis@users.noreply.github.com>
Karl Grzeszczak <karlgrz@gmail.com>
Karol Duleba <mr.fuxi@gmail.com>
Karthik Karanth <karanth.karthik@gmail.com>
Karthik Nayak <karthik.188@gmail.com>
Kasper Fabæch Brandt <poizan@poizan.dk>
Kate Heddleston <kate.heddleston@gmail.com>
Katie McLaughlin <katie@glasnt.com>
Kato Kazuyoshi <kato.kazuyoshi@gmail.com>
Katrina Owen <katrina.owen@gmail.com>
Kawsar Saiyeed <kawsar.saiyeed@projiris.com>
Kay Yan <kay.yan@daocloud.io>
kayrus <kay.diam@gmail.com>
Kazuhiro Sera <seratch@gmail.com>
Kazuyoshi Kato <katokazu@amazon.com>
Ke Li <kel@splunk.com>
Ke Xu <leonhartx.k@gmail.com>
Kei Ohmura <ohmura.kei@gmail.com>
Keith Hudgins <greenman@greenman.org>
Keli Hu <dev@keli.hu>
Ken Cochrane <kencochrane@gmail.com>
Ken Herner <kherner@progress.com>
Ken ICHIKAWA <ichikawa.ken@jp.fujitsu.com>
Ken Reese <krrgithub@gmail.com>
Kenfe-Mickaël Laventure <mickael.laventure@gmail.com>
Kenjiro Nakayama <nakayamakenjiro@gmail.com>
Kent Johnson <kentoj@gmail.com>
Kenta Tada <Kenta.Tada@sony.com>
Kevin "qwazerty" Houdebert <kevin.houdebert@gmail.com>
Kevin Alvarez <crazy-max@users.noreply.github.com>
Kevin Burke <kev@inburke.com>
Kevin Clark <kevin.clark@gmail.com>
Kevin Feyrer <kevin.feyrer@btinternet.com>
Kevin J. Lynagh <kevin@keminglabs.com>
Kevin Jing Qiu <kevin@idempotent.ca>
Kevin Kern <kaiwentan@harmonycloud.cn>
Kevin Menard <kevin@nirvdrum.com>
Kevin Meredith <kevin.m.meredith@gmail.com>
Kevin P. Kucharczyk <kevinkucharczyk@gmail.com>
Kevin Parsons <kevpar@microsoft.com>
Kevin Richardson <kevin@kevinrichardson.co>
Kevin Shi <kshi@andrew.cmu.edu>
Kevin Wallace <kevin@pentabarf.net>
Kevin Yap <me@kevinyap.ca>
Keyvan Fatehi <keyvanfatehi@gmail.com>
kies <lleelm@gmail.com>
Kim BKC Carlbacker <kim.carlbacker@gmail.com>
Kim Eik <kim@heldig.org>
Kimbro Staken <kstaken@kstaken.com>
Kir Kolyshkin <kolyshkin@gmail.com>
Kiran Gangadharan <kiran.daredevil@gmail.com>
Kirill SIbirev <l0kix2@gmail.com>
knappe <tyler.knappe@gmail.com>
Kohei Tsuruta <coheyxyz@gmail.com>
Koichi Shiraishi <k@zchee.io>
Konrad Kleine <konrad.wilhelm.kleine@gmail.com>
Konrad Ponichtera <konpon96@gmail.com>
Konstantin Gribov <grossws@gmail.com>
Konstantin L <sw.double@gmail.com>
Konstantin Pelykh <kpelykh@zettaset.com>
Kostadin Plachkov <k.n.plachkov@gmail.com>
Krasi Georgiev <krasi@vip-consult.solutions>
Krasimir Georgiev <support@vip-consult.co.uk>
Kris-Mikael Krister <krismikael@protonmail.com>
Kristian Haugene <kristian.haugene@capgemini.com>
Kristina Zabunova <triara.xiii@gmail.com>
Krystian Wojcicki <kwojcicki@sympatico.ca>
Kunal Kushwaha <kushwaha_kunal_v7@lab.ntt.co.jp>
Kunal Tyagi <tyagi.kunal@live.com>
Kyle Conroy <kyle.j.conroy@gmail.com>
Kyle Linden <linden.kyle@gmail.com>
Kyle Squizzato <ksquizz@gmail.com>
Kyle Wuolle <kyle.wuolle@gmail.com>
kyu <leehk1227@gmail.com>
Lachlan Coote <lcoote@vmware.com>
Lai Jiangshan <jiangshanlai@gmail.com>
Lajos Papp <lajos.papp@sequenceiq.com>
Lakshan Perera <lakshan@laktek.com>
Lalatendu Mohanty <lmohanty@redhat.com>
Lance Chen <cyen0312@gmail.com>
Lance Kinley <lkinley@loyaltymethods.com>
Lars Butler <Lars.Butler@gmail.com>
Lars Kellogg-Stedman <lars@redhat.com>
Lars R. Damerow <lars@pixar.com>
Lars-Magnus Skog <ralphtheninja@riseup.net>
Laszlo Meszaros <lacienator@gmail.com>
Laura Frank <ljfrank@gmail.com>
Laurent Bernaille <laurent.bernaille@datadoghq.com>
Laurent Erignoux <lerignoux@gmail.com>
Laurie Voss <github@seldo.com>
Leandro Siqueira <leandro.siqueira@gmail.com>
Lee Calcote <leecalcote@gmail.com>
Lee Chao <932819864@qq.com>
Lee, Meng-Han <sunrisedm4@gmail.com>
Lei Gong <lgong@alauda.io>
Lei Jitang <leijitang@huawei.com>
Leiiwang <u2takey@gmail.com>
Len Weincier <len@cloudafrica.net>
Lennie <github@consolejunkie.net>
Leo Gallucci <elgalu3@gmail.com>
Leonardo Nodari <me@leonardonodari.it>
Leonardo Taccari <leot@NetBSD.org>
Leszek Kowalski <github@leszekkowalski.pl>
Levi Blackstone <levi.blackstone@rackspace.com>
Levi Gross <levi@levigross.com>
Levi Harrison <levisamuelharrison@gmail.com>
Lewis Daly <lewisdaly@me.com>
Lewis Marshall <lewis@lmars.net>
Lewis Peckover <lew+github@lew.io>
Li Yi <denverdino@gmail.com>
Liam Macgillavry <liam@kumina.nl>
Liana Lo <liana.lixia@gmail.com>
Liang Mingqiang <mqliang.zju@gmail.com>
Liang-Chi Hsieh <viirya@gmail.com>
liangwei <liangwei14@huawei.com>
Liao Qingwei <liaoqingwei@huawei.com>
Lifubang <lifubang@acmcoder.com>
Lihua Tang <lhtang@alauda.io>
Lily Guo <lily.guo@docker.com>
limeidan <limeidan@loongson.cn>
Lin Lu <doraalin@163.com>
LingFaKe <lingfake@huawei.com>
Linus Heckemann <lheckemann@twig-world.com>
Liran Tal <liran.tal@gmail.com>
Liron Levin <liron@twistlock.com>
Liu Bo <bo.li.liu@oracle.com>
Liu Hua <sdu.liu@huawei.com>
liwenqi <vikilwq@zju.edu.cn>
lixiaobing10051267 <li.xiaobing1@zte.com.cn>
Liz Zhang <lizzha@microsoft.com>
LIZAO LI <lzlarryli@gmail.com>
Lizzie Dixon <_@lizzie.io>
Lloyd Dewolf <foolswisdom@gmail.com>
Lokesh Mandvekar <lsm5@fedoraproject.org>
longliqiang88 <394564827@qq.com>
Lorenz Leutgeb <lorenz.leutgeb@gmail.com>
Lorenzo Fontana <fontanalorenz@gmail.com>
Lotus Fenn <fenn.lotus@gmail.com>
Louis Delossantos <ldelossa.ld@gmail.com>
Louis Opter <kalessin@kalessin.fr>
Luca Favatella <luca.favatella@erlang-solutions.com>
Luca Marturana <lucamarturana@gmail.com>
Luca Orlandi <luca.orlandi@gmail.com>
Luca-Bogdan Grigorescu <Luca-Bogdan Grigorescu>
Lucas Chan <lucas-github@lucaschan.com>
Lucas Chi <lucas@teacherspayteachers.com>
Lucas Molas <lmolas@fundacionsadosky.org.ar>
Lucas Silvestre <lukas.silvestre@gmail.com>
Luciano Mores <leslau@gmail.com>
Luis Henrique Mulinari <luis.mulinari@gmail.com>
Luis Martínez de Bartolomé Izquierdo <lmartinez@biicode.com>
Luiz Svoboda <luizek@gmail.com>
Lukas Heeren <lukas-heeren@hotmail.com>
Lukas Waslowski <cr7pt0gr4ph7@gmail.com>
lukaspustina <lukas.pustina@centerdevice.com>
Lukasz Zajaczkowski <Lukasz.Zajaczkowski@ts.fujitsu.com>
Luke Marsden <me@lukemarsden.net>
Lyn <energylyn@zju.edu.cn>
Lynda O'Leary <lyndaoleary29@gmail.com>
Lénaïc Huard <lhuard@amadeus.com>
Ma Müller <mueller-ma@users.noreply.github.com>
Ma Shimiao <mashimiao.fnst@cn.fujitsu.com>
Mabin <bin.ma@huawei.com>
Madhan Raj Mookkandy <MadhanRaj.Mookkandy@microsoft.com>
Madhav Puri <madhav.puri@gmail.com>
Madhu Venugopal <mavenugo@gmail.com>
Mageee <fangpuyi@foxmail.com>
Mahesh Tiyyagura <tmahesh@gmail.com>
malnick <malnick@gmail..com>
Malte Janduda <mail@janduda.net>
Manfred Touron <m@42.am>
Manfred Zabarauskas <manfredas@zabarauskas.com>
Manjunath A Kumatagi <mkumatag@in.ibm.com>
Mansi Nahar <mmn4185@rit.edu>
Manuel Meurer <manuel@krautcomputing.com>
Manuel Rüger <manuel@rueg.eu>
Manuel Woelker <github@manuel.woelker.org>
mapk0y <mapk0y@gmail.com>
Marc Abramowitz <marc@marc-abramowitz.com>
Marc Kuo <kuomarc2@gmail.com>
Marc Tamsky <mtamsky@gmail.com>
Marcel Edmund Franke <marcel.edmund.franke@gmail.com>
Marcelo Horacio Fortino <info@fortinux.com>
Marcelo Salazar <chelosalazar@gmail.com>
Marco Hennings <marco.hennings@freiheit.com>
Marcus Cobden <mcobden@cisco.com>
Marcus Farkas <toothlessgear@finitebox.com>
Marcus Linke <marcus.linke@gmx.de>
Marcus Martins <marcus@docker.com>
Marcus Ramberg <marcus@nordaaker.com>
Marek Goldmann <marek.goldmann@gmail.com>
Marian Marinov <mm@yuhu.biz>
Marianna Tessel <mtesselh@gmail.com>
Mario Loriedo <mario.loriedo@gmail.com>
Marius Gundersen <me@mariusgundersen.net>
Marius Sturm <marius@graylog.com>
Marius Voila <marius.voila@gmail.com>
Mark Allen <mrallen1@yahoo.com>
Mark Feit <mfeit@internet2.edu>
Mark Jeromin <mark.jeromin@sysfrog.net>
Mark McGranaghan <mmcgrana@gmail.com>
Mark McKinstry <mmckinst@umich.edu>
Mark Milstein <mark@epiloque.com>
Mark Oates <fl0yd@me.com>
Mark Parker <godefroi@users.noreply.github.com>
Mark Vainomaa <mikroskeem@mikroskeem.eu>
Mark West <markewest@gmail.com>
Markan Patel <mpatel678@gmail.com>
Marko Mikulicic <mmikulicic@gmail.com>
Marko Tibold <marko@tibold.nl>
Markus Fix <lispmeister@gmail.com>
Markus Kortlang <hyp3rdino@googlemail.com>
Martijn Dwars <ikben@martijndwars.nl>
Martijn van Oosterhout <kleptog@svana.org>
Martin Braun <braun@neuroforge.de>
Martin Dojcak <martin.dojcak@lablabs.io>
Martin Honermeyer <maze@strahlungsfrei.de>
Martin Kelly <martin@surround.io>
Martin Mosegaard Amdisen <martin.amdisen@praqma.com>
Martin Muzatko <martin@happy-css.com>
Martin Redmond <redmond.martin@gmail.com>
Maru Newby <mnewby@thesprawl.net>
Mary Anthony <mary.anthony@docker.com>
Masahito Zembutsu <zembutsu@users.noreply.github.com>
Masato Ohba <over.rye@gmail.com>
Masayuki Morita <minamijoyo@gmail.com>
Mason Malone <mason.malone@gmail.com>
Mateusz Sulima <sulima.mateusz@gmail.com>
Mathias Monnerville <mathias@monnerville.com>
Mathieu Champlon <mathieu.champlon@docker.com>
Mathieu Le Marec - Pasquet <kiorky@cryptelium.net>
Mathieu Parent <math.parent@gmail.com>
Mathieu Paturel <mathieu.paturel@gmail.com>
Matt Apperson <me@mattapperson.com>
Matt Bachmann <bachmann.matt@gmail.com>
Matt Bajor <matt@notevenremotelydorky.com>
Matt Bentley <matt.bentley@docker.com>
Matt Haggard <haggardii@gmail.com>
Matt Hoyle <matt@deployable.co>
Matt McCormick <matt.mccormick@kitware.com>
Matt Moore <mattmoor@google.com>
Matt Morrison <3maven@gmail.com>
Matt Richardson <matt@redgumtech.com.au>
Matt Rickard <mrick@google.com>
Matt Robenolt <matt@ydekproductions.com>
Matt Schurenko <matt.schurenko@gmail.com>
Matt Williams <mattyw@me.com>
Matthew Heon <mheon@redhat.com>
Matthew Lapworth <matthewl@bit-shift.net>
Matthew Mayer <matthewkmayer@gmail.com>
Matthew Mosesohn <raytrac3r@gmail.com>
Matthew Mueller <mattmuelle@gmail.com>
Matthew Riley <mattdr@google.com>
Matthias Klumpp <matthias@tenstral.net>
Matthias Kühnle <git.nivoc@neverbox.com>
Matthias Rampke <mr@soundcloud.com>
Matthieu Fronton <m@tthieu.fr>
Matthieu Hauglustaine <matt.hauglustaine@gmail.com>
Mattias Jernberg <nostrad@gmail.com>
Mauricio Garavaglia <mauricio@medallia.com>
mauriyouth <mauriyouth@gmail.com>
Max Harmathy <max.harmathy@web.de>
Max Shytikov <mshytikov@gmail.com>
Max Timchenko <maxvt@pagerduty.com>
Maxim Fedchyshyn <sevmax@gmail.com>
Maxim Ivanov <ivanov.maxim@gmail.com>
Maxim Kulkin <mkulkin@mirantis.com>
Maxim Treskin <zerthurd@gmail.com>
Maxime Petazzoni <max@signalfuse.com>
Maximiliano Maccanti <maccanti@amazon.com>
Maxwell <csuhp007@gmail.com>
Meaglith Ma <genedna@gmail.com>
meejah <meejah@meejah.ca>
Megan Kostick <mkostick@us.ibm.com>
Mehul Kar <mehul.kar@gmail.com>
Mei ChunTao <mei.chuntao@zte.com.cn>
Mengdi Gao <usrgdd@gmail.com>
Menghui Chen <menghui.chen@alibaba-inc.com>
Mert Yazıcıoğlu <merty@users.noreply.github.com>
mgniu <mgniu@dataman-inc.com>
Micah Zoltu <micah@newrelic.com>
Michael A. Smith <michael@smith-li.com>
Michael Beskin <mrbeskin@gmail.com>
Michael Bridgen <mikeb@squaremobius.net>
Michael Brown <michael@netdirect.ca>
Michael Chiang <mchiang@docker.com>
Michael Crosby <crosbymichael@gmail.com>
Michael Currie <mcurrie@bruceforceresearch.com>
Michael Friis <friism@gmail.com>
Michael Gorsuch <gorsuch@github.com>
Michael Grauer <michael.grauer@kitware.com>
Michael Holzheu <holzheu@linux.vnet.ibm.com>
Michael Hudson-Doyle <michael.hudson@canonical.com>
Michael Huettermann <michael@huettermann.net>
Michael Irwin <mikesir87@gmail.com>
Michael Kuehn <micha@kuehn.io>
Michael Käufl <docker@c.michael-kaeufl.de>
Michael Neale <michael.neale@gmail.com>
Michael Nussbaum <michael.nussbaum@getbraintree.com>
Michael Prokop <github@michael-prokop.at>
Michael Scharf <github@scharf.gr>
Michael Spetsiotis <michael_spets@hotmail.com>
Michael Stapelberg <michael+gh@stapelberg.de>
Michael Steinert <mike.steinert@gmail.com>
Michael Thies <michaelthies78@gmail.com>
Michael Weidmann <michaelweidmann@web.de>
Michael West <mwest@mdsol.com>
Michael Zhao <michael.zhao@arm.com>
Michal Fojtik <mfojtik@redhat.com>
Michal Gebauer <mishak@mishak.net>
Michal Jemala <michal.jemala@gmail.com>
Michal Kostrzewa <michal.kostrzewa@codilime.com>
Michal Minář <miminar@redhat.com>
Michal Rostecki <mrostecki@opensuse.org>
Michal Wieczorek <wieczorek-michal@wp.pl>
Michaël Pailloncy <mpapo.dev@gmail.com>
Michał Czeraszkiewicz <czerasz@gmail.com>
Michał Gryko <github@odkurzacz.org>
Michał Kosek <mihao@users.noreply.github.com>
Michiel de Jong <michiel@unhosted.org>
Mickaël Fortunato <morsi.morsicus@gmail.com>
Mickaël Remars <mickael@remars.com>
Miguel Angel Fernández <elmendalerenda@gmail.com>
Miguel Morales <mimoralea@gmail.com>
Miguel Perez <miguel@voyat.com>
Mihai Borobocea <MihaiBorob@gmail.com>
Mihuleacc Sergiu <mihuleac.sergiu@gmail.com>
Mikael Davranche <mikael.davranche@corp.ovh.com>
Mike Brown <brownwm@us.ibm.com>
Mike Bush <mpbush@gmail.com>
Mike Casas <mkcsas0@gmail.com>
Mike Chelen <michael.chelen@gmail.com>
Mike Danese <mikedanese@google.com>
Mike Dillon <mike@embody.org>
Mike Dougherty <mike.dougherty@docker.com>
Mike Estes <mike.estes@logos.com>
Mike Gaffney <mike@uberu.com>
Mike Goelzer <mike.goelzer@docker.com>
Mike Leone <mleone896@gmail.com>
Mike Lundy <mike@fluffypenguin.org>
Mike MacCana <mike.maccana@gmail.com>
Mike Naberezny <mike@naberezny.com>
Mike Snitzer <snitzer@redhat.com>
mikelinjie <294893458@qq.com>
Mikhail Sobolev <mss@mawhrin.net>
Miklos Szegedi <miklos.szegedi@cloudera.com>
Milas Bowman <milasb@gmail.com>
Milind Chawre <milindchawre@gmail.com>
Miloslav Trmač <mitr@redhat.com>
mingqing <limingqing@cyou-inc.com>
Mingzhen Feng <fmzhen@zju.edu.cn>
Misty Stanley-Jones <misty@docker.com>
Mitch Capper <mitch.capper@gmail.com>
Mizuki Urushida <z11111001011@gmail.com>
mlarcher <github@ringabell.org>
Mohammad Banikazemi <MBanikazemi@gmail.com>
Mohammad Nasirifar <farnasirim@gmail.com>
Mohammed Aaqib Ansari <maaquib@gmail.com>
Mohit Soni <mosoni@ebay.com>
Moorthy RS <rsmoorthy@gmail.com>
Morgan Bauer <mbauer@us.ibm.com>
Morgante Pell <morgante.pell@morgante.net>
Morgy93 <thomas@ulfertsprygoda.de>
Morten Siebuhr <sbhr@sbhr.dk>
Morton Fox <github@qslw.com>
Moysés Borges <moysesb@gmail.com>
mrfly <mr.wrfly@gmail.com>
Mrunal Patel <mrunalp@gmail.com>
Muayyad Alsadi <alsadi@gmail.com>
Muhammad Zohaib Aslam <zohaibse011@gmail.com>
Mustafa Akın <mustafa91@gmail.com>
Muthukumar R <muthur@gmail.com>
Máximo Cuadros <mcuadros@gmail.com>
Médi-Rémi Hashim <medimatrix@users.noreply.github.com>
Nace Oroz <orkica@gmail.com>
Nahum Shalman <nshalman@omniti.com>
Nakul Pathak <nakulpathak3@hotmail.com>
Nalin Dahyabhai <nalin@redhat.com>
Nan Monnand Deng <monnand@gmail.com>
Naoki Orii <norii@cs.cmu.edu>
Natalie Parker <nparker@omnifone.com>
Natanael Copa <natanael.copa@docker.com>
Natasha Jarus <linuxmercedes@gmail.com>
Nate Brennand <nate.brennand@clever.com>
Nate Eagleson <nate@nateeag.com>
Nate Jones <nate@endot.org>
Nathan Carlson <carl4403@umn.edu>
Nathan Herald <me@nathanherald.com>
Nathan Hsieh <hsieh.nathan@gmail.com>
Nathan Kleyn <nathan@nathankleyn.com>
Nathan LeClaire <nathan.leclaire@docker.com>
Nathan McCauley <nathan.mccauley@docker.com>
Nathan Williams <nathan@teamtreehouse.com>
Naveed Jamil <naveed.jamil@tenpearls.com>
Neal McBurnett <neal@mcburnett.org>
Neil Horman <nhorman@tuxdriver.com>
Neil Peterson <neilpeterson@outlook.com>
Nelson Chen <crazysim@gmail.com>
Neyazul Haque <nuhaque@gmail.com>
Nghia Tran <nghia@google.com>
Niall O'Higgins <niallo@unworkable.org>
Nicholas E. Rabenau <nerab@gmx.at>
Nick Adcock <nick.adcock@docker.com>
Nick DeCoursin <n.decoursin@foodpanda.com>
Nick Irvine <nfirvine@nfirvine.com>
Nick Neisen <nwneisen@gmail.com>
Nick Parker <nikaios@gmail.com>
Nick Payne <nick@kurai.co.uk>
Nick Russo <nicholasjamesrusso@gmail.com>
Nick Stenning <nick.stenning@digital.cabinet-office.gov.uk>
Nick Stinemates <nick@stinemates.org>
Nick Wood <nwood@microsoft.com>
NickrenREN <yuquan.ren@easystack.cn>
Nicola Kabar <nicolaka@gmail.com>
Nicolas Borboën <ponsfrilus@gmail.com>
Nicolas De Loof <nicolas.deloof@gmail.com>
Nicolas Dudebout <nicolas.dudebout@gatech.edu>
Nicolas Goy <kuon@goyman.com>
Nicolas Kaiser <nikai@nikai.net>
Nicolas Sterchele <sterchele.nicolas@gmail.com>
Nicolas V Castet <nvcastet@us.ibm.com>
Nicolás Hock Isaza <nhocki@gmail.com>
Niel Drummond <niel@drummond.lu>
Nigel Poulton <nigelpoulton@hotmail.com>
Nik Nyby <nikolas@gnu.org>
Nikhil Chawla <chawlanikhil24@gmail.com>
NikolaMandic <mn080202@gmail.com>
Nikolas Garofil <nikolas.garofil@uantwerpen.be>
Nikolay Edigaryev <edigaryev@gmail.com>
Nikolay Milovanov <nmil@itransformers.net>
Nirmal Mehta <nirmalkmehta@gmail.com>
Nishant Totla <nishanttotla@gmail.com>
NIWA Hideyuki <niwa.niwa@nifty.ne.jp>
Noah Meyerhans <nmeyerha@amazon.com>
Noah Treuhaft <noah.treuhaft@docker.com>
NobodyOnSE <ich@sektor.selfip.com>
noducks <onemannoducks@gmail.com>
Nolan Darilek <nolan@thewordnerd.info>
Noriki Nakamura <noriki.nakamura@miraclelinux.com>
nponeccop <andy.melnikov@gmail.com>
Nurahmadie <nurahmadie@gmail.com>
Nuutti Kotivuori <naked@iki.fi>
nzwsch <hi@nzwsch.com>
O.S. Tezer <ostezer@gmail.com>
objectified <objectified@gmail.com>
Odin Ugedal <odin@ugedal.com>
Oguz Bilgic <fisyonet@gmail.com>
Oh Jinkyun <tintypemolly@gmail.com>
Ohad Schneider <ohadschn@users.noreply.github.com>
ohmystack <jun.jiang02@ele.me>
Ole Reifschneider <mail@ole-reifschneider.de>
Oliver Neal <ItsVeryWindy@users.noreply.github.com>
Oliver Reason <oli@overrateddev.co>
Olivier Gambier <dmp42@users.noreply.github.com>
Olle Jonsson <olle.jonsson@gmail.com>
Olli Janatuinen <olli.janatuinen@gmail.com>
Olly Pomeroy <oppomeroy@gmail.com>
Omri Shiv <Omri.Shiv@teradata.com>
Onur Filiz <onur.filiz@microsoft.com>
Oriol Francès <oriolfa@gmail.com>
Oscar Bonilla <6f6231@gmail.com>
Oskar Niburski <oskarniburski@gmail.com>
Otto Kekäläinen <otto@seravo.fi>
Ouyang Liduo <oyld0210@163.com>
Ovidio Mallo <ovidio.mallo@gmail.com>
Panagiotis Moustafellos <pmoust@elastic.co>
Paolo G. Giarrusso <p.giarrusso@gmail.com>
Pascal <pascalgn@users.noreply.github.com>
Pascal Bach <pascal.bach@siemens.com>
Pascal Borreli <pascal@borreli.com>
Pascal Hartig <phartig@rdrei.net>
Patrick Böänziger <patrick.baenziger@bsi-software.com>
Patrick Devine <patrick.devine@docker.com>
Patrick Haas <patrickhaas@google.com>
Patrick Hemmer <patrick.hemmer@gmail.com>
Patrick Stapleton <github@gdi2290.com>
Patrik Cyvoct <patrik@ptrk.io>
pattichen <craftsbear@gmail.com>
Paul "TBBle" Hampson <Paul.Hampson@Pobox.com>
Paul <paul9869@gmail.com>
paul <paul@inkling.com>
Paul Annesley <paul@annesley.cc>
Paul Bellamy <paul.a.bellamy@gmail.com>
Paul Bowsher <pbowsher@globalpersonals.co.uk>
Paul Furtado <pfurtado@hubspot.com>
Paul Hammond <paul@paulhammond.org>
Paul Jimenez <pj@place.org>
Paul Kehrer <paul.l.kehrer@gmail.com>
Paul Lietar <paul@lietar.net>
Paul Liljenberg <liljenberg.paul@gmail.com>
Paul Morie <pmorie@gmail.com>
Paul Nasrat <pnasrat@gmail.com>
Paul Weaver <pauweave@cisco.com>
Paulo Gomes <pjbgf@linux.com>
Paulo Ribeiro <paigr.io@gmail.com>
Pavel Lobashov <ShockwaveNN@gmail.com>
Pavel Matěja <pavel@verotel.cz>
Pavel Pletenev <cpp.create@gmail.com>
Pavel Pospisil <pospispa@gmail.com>
Pavel Sutyrin <pavel.sutyrin@gmail.com>
Pavel Tikhomirov <ptikhomirov@virtuozzo.com>
Pavlos Ratis <dastergon@gentoo.org>
Pavol Vargovcik <pallly.vargovcik@gmail.com>
Pawel Konczalski <mail@konczalski.de>
Paweł Gronowski <pawel.gronowski@docker.com>
Peeyush Gupta <gpeeyush@linux.vnet.ibm.com>
Peggy Li <peggyli.224@gmail.com>
Pei Su <sillyousu@gmail.com>
Peng Tao <bergwolf@gmail.com>
Penghan Wang <ph.wang@daocloud.io>
Per Weijnitz <per.weijnitz@gmail.com>
perhapszzy@sina.com <perhapszzy@sina.com>
Pete Woods <pete.woods@circleci.com>
Peter Bourgon <peter@bourgon.org>
Peter Braden <peterbraden@peterbraden.co.uk>
Peter Bücker <peter.buecker@pressrelations.de>
Peter Choi <phkchoi89@gmail.com>
Peter Dave Hello <hsu@peterdavehello.org>
Peter Edge <peter.edge@gmail.com>
Peter Ericson <pdericson@gmail.com>
Peter Esbensen <pkesbensen@gmail.com>
Peter Jaffe <pjaffe@nevo.com>
Peter Kang <peter@spell.run>
Peter Malmgren <ptmalmgren@gmail.com>
Peter Salvatore <peter@psftw.com>
Peter Volpe <petervo@redhat.com>
Peter Waller <p@pwaller.net>
Petr Švihlík <svihlik.petr@gmail.com>
Petros Angelatos <petrosagg@gmail.com>
Phil <underscorephil@gmail.com>
Phil Estes <estesp@gmail.com>
Phil Sphicas <phil.sphicas@att.com>
Phil Spitler <pspitler@gmail.com>
Philip Alexander Etling <paetling@gmail.com>
Philip Monroe <phil@philmonroe.com>
Philipp Gillé <philipp.gille@gmail.com>
Philipp Wahala <philipp.wahala@gmail.com>
Philipp Weissensteiner <mail@philippweissensteiner.com>
Phillip Alexander <git@phillipalexander.io>
phineas <phin@phineas.io>
pidster <pid@pidster.com>
Piergiuliano Bossi <pgbossi@gmail.com>
Pierre <py@poujade.org>
Pierre Carrier <pierre@meteor.com>
Pierre Dal-Pra <dalpra.pierre@gmail.com>
Pierre Wacrenier <pierre.wacrenier@gmail.com>
Pierre-Alain RIVIERE <pariviere@ippon.fr>
Piotr Bogdan <ppbogdan@gmail.com>
Piotr Karbowski <piotr.karbowski@protonmail.ch>
Porjo <porjo38@yahoo.com.au>
Poul Kjeldager Sørensen <pks@s-innovations.net>
Pradeep Chhetri <pradeep@indix.com>
Pradip Dhara <pradipd@microsoft.com>
Pradipta Kr. Banerjee <bpradip@in.ibm.com>
Prasanna Gautam <prasannagautam@gmail.com>
Pratik Karki <prertik@outlook.com>
Prayag Verma <prayag.verma@gmail.com>
Priya Wadhwa <priyawadhwa@google.com>
Projjol Banerji <probaner23@gmail.com>
Przemek Hejman <przemyslaw.hejman@gmail.com>
Puneet Pruthi <puneet.pruthi@oracle.com>
Pure White <daniel48@126.com>
pysqz <randomq@126.com>
Qiang Huang <h.huangqiang@huawei.com>
Qin TianHuan <tianhuan@bingotree.cn>
Qinglan Peng <qinglanpeng@zju.edu.cn>
Quan Tian <tianquan@cloudin.cn>
qudongfang <qudongfang@gmail.com>
Quentin Brossard <qbrossard@gmail.com>
Quentin Perez <qperez@ocs.online.net>
Quentin Tayssier <qtayssier@gmail.com>
r0n22 <cameron.regan@gmail.com>
Radostin Stoyanov <rstoyanov1@gmail.com>
Rafal Jeczalik <rjeczalik@gmail.com>
Rafe Colton <rafael.colton@gmail.com>
Raghavendra K T <raghavendra.kt@linux.vnet.ibm.com>
Raghuram Devarakonda <draghuram@gmail.com>
Raja Sami <raja.sami@tenpearls.com>
Rajat Pandit <rp@rajatpandit.com>
Rajdeep Dua <dua_rajdeep@yahoo.com>
Ralf Sippl <ralf.sippl@gmail.com>
Ralle <spam@rasmusa.net>
Ralph Bean <rbean@redhat.com>
Ramkumar Ramachandra <artagnon@gmail.com>
Ramon Brooker <rbrooker@aetherealmind.com>
Ramon van Alteren <ramon@vanalteren.nl>
RaviTeja Pothana <ravi-teja@live.com>
Ray Tsang <rayt@google.com>
ReadmeCritic <frankensteinbot@gmail.com>
realityone <realityone@me.com>
Recursive Madman <recursive.madman@gmx.de>
Reficul <xuzhenglun@gmail.com>
Regan McCooey <rmccooey27@aol.com>
Remi Rampin <remirampin@gmail.com>
Remy Suen <remy.suen@gmail.com>
Renato Riccieri Santos Zannon <renato.riccieri@gmail.com>
Renaud Gaubert <rgaubert@nvidia.com>
Rhys Hiltner <rhys@twitch.tv>
Ri Xu <xuri.me@gmail.com>
Ricardo N Feliciano <FelicianoTech@gmail.com>
Rich Horwood <rjhorwood@apple.com>
Rich Moyse <rich@moyse.us>
Rich Seymour <rseymour@gmail.com>
Richard Burnison <rburnison@ebay.com>
Richard Harvey <richard@squarecows.com>
Richard Mathie <richard.mathie@amey.co.uk>
Richard Metzler <richard@paadee.com>
Richard Scothern <richard.scothern@gmail.com>
Richo Healey <richo@psych0tik.net>
Rick Bradley <rick@users.noreply.github.com>
Rick van de Loo <rickvandeloo@gmail.com>
Rick Wieman <git@rickw.nl>
Rik Nijessen <rik@keefo.nl>
Riku Voipio <riku.voipio@linaro.org>
Riley Guerin <rileytg.dev@gmail.com>
Ritesh H Shukla <sritesh@vmware.com>
Riyaz Faizullabhoy <riyaz.faizullabhoy@docker.com>
Rob Cowsill <42620235+rcowsill@users.noreply.github.com>
Rob Gulewich <rgulewich@netflix.com>
Rob Vesse <rvesse@dotnetrdf.org>
Robert Bachmann <rb@robertbachmann.at>
Robert Bittle <guywithnose@gmail.com>
Robert Obryk <robryk@gmail.com>
Robert Schneider <mail@shakeme.info>
Robert Shade <robert.shade@gmail.com>
Robert Stern <lexandro2000@gmail.com>
Robert Terhaar <rterhaar@atlanticdynamic.com>
Robert Wallis <smilingrob@gmail.com>
Robert Wang <robert@arctic.tw>
Roberto G. Hashioka <roberto.hashioka@docker.com>
Roberto Muñoz Fernández <robertomf@gmail.com>
Robin Naundorf <r.naundorf@fh-muenster.de>
Robin Schneider <ypid@riseup.net>
Robin Speekenbrink <robin@kingsquare.nl>
Robin Thoni <robin@rthoni.com>
robpc <rpcann@gmail.com>
Rodolfo Carvalho <rhcarvalho@gmail.com>
Rodrigo Campos <rodrigo@kinvolk.io>
Rodrigo Vaz <rodrigo.vaz@gmail.com>
Roel Van Nyen <roel.vannyen@gmail.com>
Roger Peppe <rogpeppe@gmail.com>
Rohit Jnagal <jnagal@google.com>
Rohit Kadam <rohit.d.kadam@gmail.com>
Rohit Kapur <rkapur@flatiron.com>
Rojin George <rojingeorge@huawei.com>
Roland Huß <roland@jolokia.org>
Roland Kammerer <roland.kammerer@linbit.com>
Roland Moriz <rmoriz@users.noreply.github.com>
Roma Sokolov <sokolov.r.v@gmail.com>
Roman Dudin <katrmr@gmail.com>
Roman Mazur <roman@balena.io>
Roman Strashkin <roman.strashkin@gmail.com>
Roman Volosatovs <roman.volosatovs@docker.com>
Roman Zabaluev <gpg@haarolean.dev>
Ron Smits <ron.smits@gmail.com>
Ron Williams <ron.a.williams@gmail.com>
Rong Gao <gaoronggood@163.com>
Rong Zhang <rongzhang@alauda.io>
Rongxiang Song <tinysong1226@gmail.com>
Rony Weng <ronyweng@synology.com>
root <docker-dummy@example.com>
root <root@lxdebmas.marist.edu>
root <root@ubuntu-14.04-amd64-vbox>
root <root@webm215.cluster016.ha.ovh.net>
Rory Hunter <roryhunter2@gmail.com>
Rory McCune <raesene@gmail.com>
Ross Boucher <rboucher@gmail.com>
Rovanion Luckey <rovanion.luckey@gmail.com>
Royce Remer <royceremer@gmail.com>
Rozhnov Alexandr <nox73@ya.ru>
Rudolph Gottesheim <r.gottesheim@loot.at>
Rui Cao <ruicao@alauda.io>
Rui Lopes <rgl@ruilopes.com>
Ruilin Li <liruilin4@huawei.com>
Runshen Zhu <runshen.zhu@gmail.com>
Russ Magee <rmagee@gmail.com>
Ryan Abrams <rdabrams@gmail.com>
Ryan Anderson <anderson.ryanc@gmail.com>
Ryan Aslett <github@mixologic.com>
Ryan Barry <rbarry@mirantis.com>
Ryan Belgrave <rmb1993@gmail.com>
Ryan Campbell <campbellr@gmail.com>
Ryan Detzel <ryan.detzel@gmail.com>
Ryan Fowler <rwfowler@gmail.com>
Ryan Liu <ryanlyy@me.com>
Ryan McLaughlin <rmclaughlin@insidesales.com>
Ryan O'Donnell <odonnellryanc@gmail.com>
Ryan Seto <ryanseto@yak.net>
Ryan Shea <sheabot03@gmail.com>
Ryan Simmen <ryan.simmen@gmail.com>
Ryan Stelly <ryan.stelly@live.com>
Ryan Thomas <rthomas@atlassian.com>
Ryan Trauntvein <rtrauntvein@novacoast.com>
Ryan Wallner <ryan.wallner@clusterhq.com>
Ryan Zhang <ryan.zhang@docker.com>
ryancooper7 <ryan.cooper7@gmail.com>
RyanDeng <sheldon.d1018@gmail.com>
Ryo Nakao <nakabonne@gmail.com>
Ryoga Saito <contact@proelbtn.com>
Rémy Greinhofer <remy.greinhofer@livelovely.com>
s. rannou <mxs@sbrk.org>
Sabin Basyal <sabin.basyal@gmail.com>
Sachin Joshi <sachin_jayant_joshi@hotmail.com>
Sagar Hani <sagarhani33@gmail.com>
Sainath Grandhi <sainath.grandhi@intel.com>
Sakeven Jiang <jc5930@sina.cn>
Salahuddin Khan <salah@docker.com>
Sally O'Malley <somalley@redhat.com>
Sam Abed <sam.abed@gmail.com>
Sam Alba <sam.alba@gmail.com>
Sam Bailey <cyprix@cyprix.com.au>
Sam J Sharpe <sam.sharpe@digital.cabinet-office.gov.uk>
Sam Neirinck <sam@samneirinck.com>
Sam Reis <sreis@atlassian.com>
Sam Rijs <srijs@airpost.net>
Sam Whited <sam@samwhited.com>
Sambuddha Basu <sambuddhabasu1@gmail.com>
Sami Wagiaalla <swagiaal@redhat.com>
Samuel Andaya <samuel@andaya.net>
Samuel Dion-Girardeau <samuel.diongirardeau@gmail.com>
Samuel Karp <me@samuelkarp.com>
Samuel PHAN <samuel-phan@users.noreply.github.com>
sanchayanghosh <sanchayanghosh@outlook.com>
Sandeep Bansal <sabansal@microsoft.com>
Sankar சங்கர் <sankar.curiosity@gmail.com>
Sanket Saurav <sanketsaurav@gmail.com>
Santhosh Manohar <santhosh@docker.com>
sapphiredev <se.imas.kr@gmail.com>
Sargun Dhillon <sargun@netflix.com>
Sascha Andres <sascha.andres@outlook.com>
Sascha Grunert <sgrunert@suse.com>
SataQiu <qiushida@beyondcent.com>
Satnam Singh <satnam@raintown.org>
Satoshi Amemiya <satoshi_amemiya@voyagegroup.com>
Satoshi Tagomori <tagomoris@gmail.com>
Scott Bessler <scottbessler@gmail.com>
Scott Collier <emailscottcollier@gmail.com>
Scott Johnston <scott@docker.com>
Scott Percival <scottp@lastyard.com>
Scott Stamp <scottstamp851@gmail.com>
Scott Walls <sawalls@umich.edu>
sdreyesg <sdreyesg@gmail.com>
Sean Christopherson <sean.j.christopherson@intel.com>
Sean Cronin <seancron@gmail.com>
Sean Lee <seanlee@tw.ibm.com>
Sean McIntyre <s.mcintyre@xverba.ca>
Sean OMeara <sean@chef.io>
Sean P. Kane <skane@newrelic.com>
Sean Rodman <srodman7689@gmail.com>
Sebastiaan van Steenis <mail@superseb.nl>
Sebastiaan van Stijn <github@gone.nl>
Sebastian Höffner <sebastian.hoeffner@mevis.fraunhofer.de>
Sebastian Radloff <sradloff23@gmail.com>
Sebastien Goasguen <runseb@gmail.com>
Senthil Kumar Selvaraj <senthil.thecoder@gmail.com>
Senthil Kumaran <senthil@uthcode.com>
SeongJae Park <sj38.park@gmail.com>
Seongyeol Lim <seongyeol37@gmail.com>
Serge Hallyn <serge.hallyn@ubuntu.com>
Sergey Alekseev <sergey.alekseev.minsk@gmail.com>
Sergey Evstifeev <sergey.evstifeev@gmail.com>
Sergii Kabashniuk <skabashnyuk@codenvy.com>
Sergio Lopez <slp@redhat.com>
Serhat Gülçiçek <serhat25@gmail.com>
SeungUkLee <lsy931106@gmail.com>
Sevki Hasirci <s@sevki.org>
Shane Canon <scanon@lbl.gov>
Shane da Silva <shane@dasilva.io>
Shaun Kaasten <shaunk@gmail.com>
shaunol <shaunol@gmail.com>
Shawn Landden <shawn@churchofgit.com>
Shawn Siefkas <shawn.siefkas@meredith.com>
shawnhe <shawnhe@shawnhedeMacBook-Pro.local>
Shayan Pooya <shayan@liveve.org>
Shayne Wang <shaynexwang@gmail.com>
Shekhar Gulati <shekhargulati84@gmail.com>
Sheng Yang <sheng@yasker.org>
Shengbo Song <thomassong@tencent.com>
Shengjing Zhu <zhsj@debian.org>
Shev Yan <yandong_8212@163.com>
Shih-Yuan Lee <fourdollars@gmail.com>
Shihao Xia <charlesxsh@hotmail.com>
Shijiang Wei <mountkin@gmail.com>
Shijun Qin <qinshijun16@mails.ucas.ac.cn>
Shishir Mahajan <shishir.mahajan@redhat.com>
Shoubhik Bose <sbose78@gmail.com>
Shourya Sarcar <shourya.sarcar@gmail.com>
Shu-Wai Chow <shu-wai.chow@seattlechildrens.org>
shuai-z <zs.broccoli@gmail.com>
Shukui Yang <yangshukui@huawei.com>
Sian Lerk Lau <kiawin@gmail.com>
Siarhei Rasiukevich <s_rasiukevich@wargaming.net>
Sidhartha Mani <sidharthamn@gmail.com>
sidharthamani <sid@rancher.com>
Silas Sewell <silas@sewell.org>
Silvan Jegen <s.jegen@gmail.com>
Simão Reis <smnrsti@gmail.com>
Simon Barendse <simon.barendse@gmail.com>
Simon Eskildsen <sirup@sirupsen.com>
Simon Ferquel <simon.ferquel@docker.com>
Simon Leinen <simon.leinen@gmail.com>
Simon Menke <simon.menke@gmail.com>
Simon Taranto <simon.taranto@gmail.com>
Simon Vikstrom <pullreq@devsn.se>
Sindhu S <sindhus@live.in>
Sjoerd Langkemper <sjoerd-github@linuxonly.nl>
skanehira <sho19921005@gmail.com>
Smark Meng <smark@freecoop.net>
Solganik Alexander <solganik@gmail.com>
Solomon Hykes <solomon@docker.com>
Song Gao <song@gao.io>
Soshi Katsuta <soshi.katsuta@gmail.com>
Sotiris Salloumis <sotiris.salloumis@gmail.com>
Soulou <leo@unbekandt.eu>
Spencer Brown <spencer@spencerbrown.org>
Spencer Smith <robertspencersmith@gmail.com>
Spike Curtis <spike.curtis@metaswitch.com>
Sridatta Thatipamala <sthatipamala@gmail.com>
Sridhar Ratnakumar <sridharr@activestate.com>
Srini Brahmaroutu <srbrahma@us.ibm.com>
Srinivasan Srivatsan <srinivasan.srivatsan@hpe.com>
Staf Wagemakers <staf@wagemakers.be>
Stanislav Bondarenko <stanislav.bondarenko@gmail.com>
Stanislav Levin <slev@altlinux.org>
Steeve Morin <steeve.morin@gmail.com>
Stefan Berger <stefanb@linux.vnet.ibm.com>
Stefan J. Wernli <swernli@microsoft.com>
Stefan Praszalowicz <stefan@greplin.com>
Stefan S. <tronicum@user.github.com>
Stefan Scherer <stefan.scherer@docker.com>
Stefan Staudenmeyer <doerte@instana.com>
Stefan Weil <sw@weilnetz.de>
Steffen Butzer <steffen.butzer@outlook.com>
Stephan Spindler <shutefan@gmail.com>
Stephen Benjamin <stephen@redhat.com>
Stephen Crosby <stevecrozz@gmail.com>
Stephen Day <stevvooe@gmail.com>
Stephen Drake <stephen@xenolith.net>
Stephen Rust <srust@blockbridge.com>
Steve Desmond <steve@vtsv.ca>
Steve Dougherty <steve@asksteved.com>
Steve Durrheimer <s.durrheimer@gmail.com>
Steve Francia <steve.francia@gmail.com>
Steve Koch <stevekochscience@gmail.com>
Steven Burgess <steven.a.burgess@hotmail.com>
Steven Erenst <stevenerenst@gmail.com>
Steven Hartland <steven.hartland@multiplay.co.uk>
Steven Iveson <sjiveson@outlook.com>
Steven Merrill <steven.merrill@gmail.com>
Steven Richards <steven@axiomzen.co>
Steven Taylor <steven.taylor@me.com>
Stéphane Este-Gracias <sestegra@gmail.com>
Stig Larsson <stig@larsson.dev>
Su Wang <su.wang@docker.com>
Subhajit Ghosh <isubuz.g@gmail.com>
Sujith Haridasan <sujith.h@gmail.com>
Sun Gengze <690388648@qq.com>
Sun Jianbo <wonderflow.sun@gmail.com>
Sune Keller <sune.keller@gmail.com>
Sunny Gogoi <indiasuny000@gmail.com>
Suryakumar Sudar <surya.trunks@gmail.com>
Sven Dowideit <SvenDowideit@home.org.au>
Swapnil Daingade <swapnil.daingade@gmail.com>
Sylvain Baubeau <lebauce@gmail.com>
Sylvain Bellemare <sylvain@ascribe.io>
Sébastien <sebastien@yoozio.com>
Sébastien HOUZÉ <cto@verylastroom.com>
Sébastien Luttringer <seblu@seblu.net>
Sébastien Stormacq <sebsto@users.noreply.github.com>
Sören Tempel <soeren+git@soeren-tempel.net>
Tabakhase <mail@tabakhase.com>
Tadej Janež <tadej.j@nez.si>
Takuto Sato <tockn.jp@gmail.com>
tang0th <tang0th@gmx.com>
Tangi Colin <tangicolin@gmail.com>
Tatsuki Sugiura <sugi@nemui.org>
Tatsushi Inagaki <e29253@jp.ibm.com>
Taylan Isikdemir <taylani@google.com>
Taylor Jones <monitorjbl@gmail.com>
Ted M. Young <tedyoung@gmail.com>
Tehmasp Chaudhri <tehmasp@gmail.com>
Tejaswini Duggaraju <naduggar@microsoft.com>
Tejesh Mehta <tejesh.mehta@gmail.com>
Terry Chu <zue.hterry@gmail.com>
terryding77 <550147740@qq.com>
Thatcher Peskens <thatcher@docker.com>
theadactyl <thea.lamkin@gmail.com>
Thell 'Bo' Fowler <thell@tbfowler.name>
Thermionix <bond711@gmail.com>
Thiago Alves Silva <thiago.alves@aurea.com>
Thijs Terlouw <thijsterlouw@gmail.com>
Thomas Bikeev <thomas.bikeev@mac.com>
Thomas Frössman <thomasf@jossystem.se>
Thomas Gazagnaire <thomas@gazagnaire.org>
Thomas Graf <tgraf@suug.ch>
Thomas Grainger <tagrain@gmail.com>
Thomas Hansen <thomas.hansen@gmail.com>
Thomas Ledos <thomas.ledos92@gmail.com>
Thomas Leonard <thomas.leonard@docker.com>
Thomas Léveil <thomasleveil@gmail.com>
Thomas Orozco <thomas@orozco.fr>
Thomas Riccardi <riccardi@systran.fr>
Thomas Schroeter <thomas@cliqz.com>
Thomas Sjögren <konstruktoid@users.noreply.github.com>
Thomas Swift <tgs242@gmail.com>
Thomas Tanaka <thomas.tanaka@oracle.com>
Thomas Texier <sharkone@en-mousse.org>
Ti Zhou <tizhou1986@gmail.com>
Tiago Seabra <tlgs@users.noreply.github.com>
Tianon Gravi <admwiggin@gmail.com>
Tianyi Wang <capkurmagati@gmail.com>
Tibor Vass <teabee89@gmail.com>
Tiffany Jernigan <tiffany.f.j@gmail.com>
Tiffany Low <tiffany@box.com>
Till Claassen <pixelistik@users.noreply.github.com>
Till Wegmüller <toasterson@gmail.com>
Tim <elatllat@gmail.com>
Tim Bart <tim@fewagainstmany.com>
Tim Bosse <taim@bosboot.org>
Tim Dettrick <t.dettrick@uq.edu.au>
Tim Düsterhus <tim@bastelstu.be>
Tim Hockin <thockin@google.com>
Tim Potter <tpot@hpe.com>
Tim Ruffles <oi@truffles.me.uk>
Tim Smith <timbot@google.com>
Tim Terhorst <mynamewastaken+git@gmail.com>
Tim Wagner <tim.wagner@freenet.ag>
Tim Wang <timwangdev@gmail.com>
Tim Waugh <twaugh@redhat.com>
Tim Wraight <tim.wraight@tangentlabs.co.uk>
Tim Zju <21651152@zju.edu.cn>
timchenxiaoyu <837829664@qq.com>
timfeirg <kkcocogogo@gmail.com>
Timo Rothenpieler <timo@rothenpieler.org>
Timothy Hobbs <timothyhobbs@seznam.cz>
tjwebb123 <tjwebb123@users.noreply.github.com>
tobe <tobegit3hub@gmail.com>
Tobias Bieniek <Tobias.Bieniek@gmx.de>
Tobias Bradtke <webwurst@gmail.com>
Tobias Gesellchen <tobias@gesellix.de>
Tobias Klauser <tklauser@distanz.ch>
Tobias Munk <schmunk@usrbin.de>
Tobias Pfandzelter <tobias@pfandzelter.com>
Tobias Schmidt <ts@soundcloud.com>
Tobias Schwab <tobias.schwab@dynport.de>
Todd Crane <todd@toddcrane.com>
Todd Lunter <tlunter@gmail.com>
Todd Whiteman <todd.whiteman@joyent.com>
Toli Kuznets <toli@docker.com>
Tom Barlow <tomwbarlow@gmail.com>
Tom Booth <tombooth@gmail.com>
Tom Denham <tom@tomdee.co.uk>
Tom Fotherby <tom+github@peopleperhour.com>
Tom Howe <tom.howe@enstratius.com>
Tom Hulihan <hulihan.tom159@gmail.com>
Tom Maaswinkel <tom.maaswinkel@12wiki.eu>
Tom Parker <palfrey@tevp.net>
Tom Sweeney <tsweeney@redhat.com>
Tom Wilkie <tom.wilkie@gmail.com>
Tom X. Tobin <tomxtobin@tomxtobin.com>
Tom Zhao <zlwangel@gmail.com>
Tomas Janousek <tomi@nomi.cz>
Tomas Kral <tomas.kral@gmail.com>
Tomas Tomecek <ttomecek@redhat.com>
Tomasz Kopczynski <tomek@kopczynski.net.pl>
Tomasz Lipinski <tlipinski@users.noreply.github.com>
Tomasz Nurkiewicz <nurkiewicz@gmail.com>
Tomek Mańko <tomek.manko@railgun-solutions.com>
Tommaso Visconti <tommaso.visconti@gmail.com>
Tomoya Tabuchi <t@tomoyat1.com>
Tomáš Hrčka <thrcka@redhat.com>
tonic <tonicbupt@gmail.com>
Tonny Xu <tonny.xu@gmail.com>
Tony Abboud <tdabboud@hotmail.com>
Tony Daws <tony@daws.ca>
Tony Miller <mcfiredrill@gmail.com>
toogley <toogley@mailbox.org>
Torstein Husebø <torstein@huseboe.net>
Toshiaki Makita <makita.toshiaki@lab.ntt.co.jp>
Tõnis Tiigi <tonistiigi@gmail.com>
Trace Andreason <tandreason@gmail.com>
tracylihui <793912329@qq.com>
Trapier Marshall <tmarshall@mirantis.com>
Travis Cline <travis.cline@gmail.com>
Travis Thieman <travis.thieman@gmail.com>
Trent Ogren <tedwardo2@gmail.com>
Trevor <trevinwoodstock@gmail.com>
Trevor Pounds <trevor.pounds@gmail.com>
Trevor Sullivan <pcgeek86@gmail.com>
Trishna Guha <trishnaguha17@gmail.com>
Tristan Carel <tristan@cogniteev.com>
Troy Denton <trdenton@gmail.com>
Tudor Brindus <me@tbrindus.ca>
Ty Alexander <ty.alexander@sendgrid.com>
Tycho Andersen <tycho@docker.com>
Tyler Brock <tyler.brock@gmail.com>
Tyler Brown <tylers.pile@gmail.com>
Tzu-Jung Lee <roylee17@gmail.com>
uhayate <uhayate.gong@daocloud.io>
Ulysse Carion <ulyssecarion@gmail.com>
Umesh Yadav <umesh4257@gmail.com>
Utz Bacher <utz.bacher@de.ibm.com>
vagrant <vagrant@ubuntu-14.04-amd64-vbox>
Vaidas Jablonskis <jablonskis@gmail.com>
Valentin Kulesh <valentin.kulesh@virtuozzo.com>
vanderliang <lansheng@meili-inc.com>
Velko Ivanov <vivanov@deeperplane.com>
Veres Lajos <vlajos@gmail.com>
Victor Algaze <valgaze@gmail.com>
Victor Coisne <victor.coisne@dotcloud.com>
Victor Costan <costan@gmail.com>
Victor I. Wood <viw@t2am.com>
Victor Lyuboslavsky <victor@victoreda.com>
Victor Marmol <vmarmol@google.com>
Victor Palma <palma.victor@gmail.com>
Victor Vieux <victor.vieux@docker.com>
Victoria Bialas <victoria.bialas@docker.com>
Vijaya Kumar K <vijayak@caviumnetworks.com>
Vikas Choudhary <choudharyvikas16@gmail.com>
Vikram bir Singh <vsingh@mirantis.com>
Viktor Stanchev <me@viktorstanchev.com>
Viktor Vojnovski <viktor.vojnovski@amadeus.com>
VinayRaghavanKS <raghavan.vinay@gmail.com>
Vincent Batts <vbatts@redhat.com>
Vincent Bernat <vincent@bernat.ch>
Vincent Boulineau <vincent.boulineau@datadoghq.com>
Vincent Demeester <vincent.demeester@docker.com>
Vincent Giersch <vincent.giersch@ovh.net>
Vincent Mayers <vincent.mayers@inbloom.org>
Vincent Woo <me@vincentwoo.com>
Vinod Kulkarni <vinod.kulkarni@gmail.com>
Vishal Doshi <vishal.doshi@gmail.com>
Vishnu Kannan <vishnuk@google.com>
Vitaly Ostrosablin <vostrosablin@virtuozzo.com>
Vitor Monteiro <vmrmonteiro@gmail.com>
Vivek Agarwal <me@vivek.im>
Vivek Dasgupta <vdasgupt@redhat.com>
Vivek Goyal <vgoyal@redhat.com>
Vladimir Bulyga <xx@ccxx.cc>
Vladimir Kirillov <proger@wilab.org.ua>
Vladimir Pouzanov <farcaller@google.com>
Vladimir Rutsky <altsysrq@gmail.com>
Vladimir Varankin <nek.narqo+git@gmail.com>
VladimirAus <v_roudakov@yahoo.com>
Vladislav Kolesnikov <vkolesnikov@beget.ru>
Vlastimil Zeman <vlastimil.zeman@diffblue.com>
Vojtech Vitek (V-Teq) <vvitek@redhat.com>
Walter Leibbrandt <github@wrl.co.za>
Walter Stanish <walter@pratyeka.org>
Wang Chao <chao.wang@ucloud.cn>
Wang Guoliang <liangcszzu@163.com>
Wang Jie <wangjie5@chinaskycloud.com>
Wang Long <long.wanglong@huawei.com>
Wang Ping <present.wp@icloud.com>
Wang Xing <hzwangxing@corp.netease.com>
Wang Yuexiao <wang.yuexiao@zte.com.cn>
Wang Yumu <37442693@qq.com>
wanghuaiqing <wanghuaiqing@loongson.cn>
Ward Vandewege <ward@jhvc.com>
WarheadsSE <max@warheads.net>
Wassim Dhif <wassimdhif@gmail.com>
Wataru Ishida <ishida.wataru@lab.ntt.co.jp>
Wayne Chang <wayne@neverfear.org>
Wayne Song <wsong@docker.com>
Weerasak Chongnguluam <singpor@gmail.com>
Wei Fu <fuweid89@gmail.com>
Wei Wu <wuwei4455@gmail.com>
Wei-Ting Kuo <waitingkuo0527@gmail.com>
weipeng <weipeng@tuscloud.io>
weiyan <weiyan3@huawei.com>
Weiyang Zhu <cnresonant@gmail.com>
Wen Cheng Ma <wenchma@cn.ibm.com>
Wendel Fleming <wfleming@usc.edu>
Wenjun Tang <tangwj2@lenovo.com>
Wenkai Yin <yinw@vmware.com>
wenlxie <wenlxie@ebay.com>
Wenxuan Zhao <viz@linux.com>
Wenyu You <21551128@zju.edu.cn>
Wenzhi Liang <wenzhi.liang@gmail.com>
Wes Morgan <cap10morgan@gmail.com>
Wewang Xiaorenfine <wang.xiaoren@zte.com.cn>
Wiktor Kwapisiewicz <wiktor@metacode.biz>
Will Dietz <w@wdtz.org>
Will Rouesnel <w.rouesnel@gmail.com>
Will Weaver <monkey@buildingbananas.com>
willhf <willhf@gmail.com>
William Delanoue <william.delanoue@gmail.com>
William Henry <whenry@redhat.com>
William Hubbs <w.d.hubbs@gmail.com>
William Martin <wmartin@pivotal.io>
William Riancho <wr.wllm@gmail.com>
William Thurston <thurstw@amazon.com>
Wilson Júnior <wilsonpjunior@gmail.com>
Wing-Kam Wong <wingkwong.code@gmail.com>
WiseTrem <shepelyov.g@gmail.com>
Wolfgang Nagele <mail@wnagele.com>
Wolfgang Powisch <powo@powo.priv.at>
Wonjun Kim <wonjun.kim@navercorp.com>
WuLonghui <wlh6666@qq.com>
xamyzhao <x.amy.zhao@gmail.com>
Xia Wu <xwumzn@amazon.com>
Xian Chaobo <xianchaobo@huawei.com>
Xianglin Gao <xlgao@zju.edu.cn>
Xianjie <guxianjie@gmail.com>
Xianlu Bird <xianlubird@gmail.com>
Xiao YongBiao <xyb4638@gmail.com>
Xiao Zhang <xiaozhang0210@hotmail.com>
XiaoBing Jiang <s7v7nislands@gmail.com>
Xiaodong Liu <liuxiaodong@loongson.cn>
Xiaodong Zhang <a4012017@sina.com>
Xiaohua Ding <xiao_hua_ding@sina.cn>
Xiaoxi He <xxhe@alauda.io>
Xiaoxu Chen <chenxiaoxu14@otcaix.iscas.ac.cn>
Xiaoyu Zhang <zhang.xiaoyu33@zte.com.cn>
xichengliudui <1693291525@qq.com>
xiekeyang <xiekeyang@huawei.com>
Ximo Guanter Gonzálbez <joaquin.guantergonzalbez@telefonica.com>
Xinbo Weng <xihuanbo_0521@zju.edu.cn>
Xinfeng Liu <xinfeng.liu@gmail.com>
Xinzi Zhou <imdreamrunner@gmail.com>
Xiuming Chen <cc@cxm.cc>
Xuecong Liao <satorulogic@gmail.com>
xuzhaokui <cynicholas@gmail.com>
Yadnyawalkya Tale <ytale@redhat.com>
Yahya <ya7yaz@gmail.com>
yalpul <yalpul@gmail.com>
YAMADA Tsuyoshi <tyamada@minimum2scp.org>
Yamasaki Masahide <masahide.y@gmail.com>
Yan Feng <yanfeng2@huawei.com>
Yan Zhu <yanzhu@alauda.io>
Yang Bai <hamo.by@gmail.com>
Yang Li <idealhack@gmail.com>
Yang Pengfei <yangpengfei4@huawei.com>
yangchenliang <yangchenliang@huawei.com>
Yann Autissier <yann.autissier@gmail.com>
Yanqiang Miao <miao.yanqiang@zte.com.cn>
Yao Zaiyong <yaozaiyong@hotmail.com>
Yash Murty <yashmurty@gmail.com>
Yassine Tijani <yasstij11@gmail.com>
Yasunori Mahata <nori@mahata.net>
Yazhong Liu <yorkiefixer@gmail.com>
Yestin Sun <sunyi0804@gmail.com>
Yi EungJun <eungjun.yi@navercorp.com>
Yibai Zhang <xm1994@gmail.com>
Yihang Ho <hoyihang5@gmail.com>
Ying Li <ying.li@docker.com>
Yohei Ueda <yohei@jp.ibm.com>
Yong Tang <yong.tang.github@outlook.com>
Yongxin Li <yxli@alauda.io>
Yongzhi Pan <panyongzhi@gmail.com>
Yosef Fertel <yfertel@gmail.com>
You-Sheng Yang (楊有勝) <vicamo@gmail.com>
youcai <omegacoleman@gmail.com>
Youcef YEKHLEF <yyekhlef@gmail.com>
Youfu Zhang <zhangyoufu@gmail.com>
Yu Changchun <yuchangchun1@huawei.com>
Yu Chengxia <yuchengxia@huawei.com>
Yu Peng <yu.peng36@zte.com.cn>
Yu-Ju Hong <yjhong@google.com>
Yuan Sun <sunyuan3@huawei.com>
Yuanhong Peng <pengyuanhong@huawei.com>
Yue Zhang <zy675793960@yeah.net>
Yufei Xiong <yufei.xiong@qq.com>
Yuhao Fang <fangyuhao@gmail.com>
Yuichiro Kaneko <spiketeika@gmail.com>
YujiOshima <yuji.oshima0x3fd@gmail.com>
Yunxiang Huang <hyxqshk@vip.qq.com>
Yurii Rashkovskii <yrashk@gmail.com>
Yusuf Tarık Günaydın <yusuf_tarik@hotmail.com>
Yves Blusseau <90z7oey02@sneakemail.com>
Yves Junqueira <yves.junqueira@gmail.com>
Zac Dover <zdover@redhat.com>
Zach Borboa <zachborboa@gmail.com>
Zach Gershman <zachgersh@gmail.com>
Zachary Jaffee <zjaffee@us.ibm.com>
Zain Memon <zain@inzain.net>
Zaiste! <oh@zaiste.net>
Zane DeGraffenried <zane.deg@gmail.com>
Zefan Li <lizefan@huawei.com>
Zen Lin(Zhinan Lin) <linzhinan@huawei.com>
Zhang Kun <zkazure@gmail.com>
Zhang Wei <zhangwei555@huawei.com>
Zhang Wentao <zhangwentao234@huawei.com>
ZhangHang <stevezhang2014@gmail.com>
zhangxianwei <xianwei.zw@alibaba-inc.com>
Zhenan Ye <21551168@zju.edu.cn>
zhenghenghuo <zhenghenghuo@zju.edu.cn>
Zhenhai Gao <gaozh1988@live.com>
Zhenkun Bi <bi.zhenkun@zte.com.cn>
ZhiPeng Lu <lu.zhipeng@zte.com.cn>
zhipengzuo <zuozhipeng@baidu.com>
Zhou Hao <zhouhao@cn.fujitsu.com>
Zhoulin Xie <zhoulin.xie@daocloud.io>
Zhu Guihua <zhugh.fnst@cn.fujitsu.com>
Zhu Kunjia <zhu.kunjia@zte.com.cn>
Zhuoyun Wei <wzyboy@wzyboy.org>
Ziheng Liu <lzhfromustc@gmail.com>
Zilin Du <zilin.du@gmail.com>
zimbatm <zimbatm@zimbatm.com>
Ziming Dong <bnudzm@foxmail.com>
ZJUshuaizhou <21551191@zju.edu.cn>
zmarouf <zeid.marouf@gmail.com>
Zoltan Tombol <zoltan.tombol@gmail.com>
Zou Yu <zouyu7@huawei.com>
zqh <zqhxuyuan@gmail.com>
Zuhayr Elahi <zuhayr.elahi@docker.com>
Zunayed Ali <zunayed@gmail.com>
Álvaro Lázaro <alvaro.lazaro.g@gmail.com>
Átila Camurça Alves <camurca.home@gmail.com>
尹吉峰 <jifeng.yin@gmail.com>
屈骏 <qujun@tiduyun.com>
徐俊杰 <paco.xu@daocloud.io>
慕陶 <jihui.xjh@alibaba-inc.com>
搏通 <yufeng.pyf@alibaba-inc.com>
黄艳红00139573 <huang.yanhong@zte.com.cn>
정재영 <jjy600901@gmail.com>