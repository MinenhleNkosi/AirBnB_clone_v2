# 0x02. AirBnB clone - MySQL

-----
## Background Context.
Environment variables will be your best friend for this project!
* `HBNB_ENV`: running environment. It can be “dev” or “test” for the moment (“production” soon!)
* `HBNB_MYSQL_USER`: the username of your MySQL
* `HBNB_MYSQL_PWD`: the password of your MySQL
* `HBNB_MYSQL_HOST`: the hostname of your MySQL
* `HBNB_MYSQL_DB`: the database name of your MySQL
* `HBNB_TYPE_STORAGE`: the type of storage used. It can be “file” (using `FileStorage`) or `db` (using `DBStorage`)

## Resources.
**Read or watch**:
* [cmd module](https://intranet.alxswe.com/rltoken/OG2OW5Pbjs-ds3ZHT0ow4g)
* **packages** concept page
* [unittest module](https://intranet.alxswe.com/rltoken/g0tzN6ea1hWCj5OF99HB9w)
* [args/kwargs](https://intranet.alxswe.com/rltoken/F6YRBSrkkkTTMVc66iaMgA)
* [SQLAlchemy tutorial](https://intranet.alxswe.com/rltoken/GYWCmxokUZKAr-T93iQPcQ)
* [How To Create a New User and Grant Permissions in MySQL](https://intranet.alxswe.com/rltoken/m4ogDCoKVm3Us0FybYh1tA)
* [Python3 and environment variables](https://intranet.alxswe.com/rltoken/FJCSaX1TCf0HAOzhsH_eWA)
* [SQLAlchemy](https://intranet.alxswe.com/rltoken/bWxESLJVYGNonjOYg8fOVg)
* [MySQL 8.0 SQL Statement Syntax](https://intranet.alxswe.com/rltoken/n6ePnCDwnbQMbxGgeoe1VA)

## Learning Objectives.
At the end of this project, you are expected to be able to [explain to anyone](https://intranet.alxswe.com/rltoken/3nWKduPHOPRUFGNEtT-SMw), **without the help of Google**:

### General.
* What is Unit testing and how to implement it in a large project
* What is `*args` and how to use it
* What is `**kwargs` and how to use it
* How to handle named arguments in a function
* How to create a MySQL database
* How to create a MySQL user and grant it privileges
* What ORM means
* How to map a Python Class to a MySQL table
* How to handle 2 different storage engines with the same codebase
* How to use environment variables

### Copyright - Plagiarism.
* You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
* You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
* You are not allowed to publish any content of this project.
* Any form of plagiarism is strictly forbidden and will result in removal from the program.

## Requirements.
### Python Scripts.
* Allowed editors: `vi`, `vim`, `emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
* All your files should end with a new line
* The first line of all your files should be exactly `#!/usr/bin/python3`
* A `README.md` file, at the root of the folder of the project, is mandatory
* Your code should use the pycodestyle (version `2.8.*`)
* All your files must be executable
* The length of your files will be tested using `wc`
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

### Python Unit Tests.
* Allowed editors: `vi`, `vim`, `emacs`
* All your files should end with a new line
* All your test files should be inside a folder `tests`
* You have to use the [unittest module](https://intranet.alxswe.com/rltoken/g0tzN6ea1hWCj5OF99HB9w)
* All your test files should be python files (extension: `.py`)
* All your test files and folders should start by `test_`
* Your file organization in the tests folder should be the same as your project: ex: for `models/base_model.py`, unit tests must be in: `tests/test_models/test_base_model.py`
* All your tests should be executed by using this command: `python3 -m unittest discover tests`
* You can also test file by file by using this command: `python3 -m unittest tests/test_models/test_base_model.py`
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'` and `python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* We strongly encourage you to work together on test cases, so that you don’t miss any edge cases.

### SQL Scripts.
* Allowed editors: `vi`, `vim`, `emacs`
* All your files will be executed on Ubuntu 20.04 LTS using `MySQL 8.0`
* Your files will be executed with `SQLAlchemy` version `1.4.x`
* All your files should end with a new line
* All your SQL queries should have a comment just before (i.e. syntax above)
* All your files should start by a comment describing the task
* All SQL keywords should be in uppercase (`SELECT`, `WHERE…`)
* A `README.md` file, at the root of the folder of the project, is mandatory
* The length of your files will be tested using `wc`

### GitHub.
**There should be one project repository per group. If you clone/fork/whatever a partner’s project repository with the same name before the second deadline, you risk a 0% score.**

## More Info.

<kbd>
<a href="url"><img src="https://s3.amazonaws.com/intranet-projects-files/concepts/74/hbnb_step2.png" alt="your-image-description" height="auto" width="600" style="border-radius: 50%"></a>
</kbd>

### Comments for your SQL file:

```sql
$ cat my_script.sql
-- first 3 students in the Batch ID=3
-- because Batch 3 is the best!
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;
$
```
------

## General Use

1. First clone this repository.

3. Once the repository is cloned locate the "console.py" file and run it as follows:
```bash
/AirBnB_clone$ ./console.py
```

4. The following prompt should appear:
```
(hbnb)
```

5. This prompt signifies that  you are in the "HBnB" console.

### Commands Used:
* **create** - Creates an instance based on given class
* **destroy** - Destroys an object based on class and UUID
* **show** - Shows an object based on class and UUID
* **all** - Shows all objects the program has access to, or all objects of a given class
* **update** - Updates existing attributes an object based on class name and UUID
* **quit** - Exits the program (EOF will as well)


## Examples
### Primary Command Syntax

###### Example 0: Create an object
Usage: create <class_name>
```
(hbnb) create BaseModel
```

```
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb)                   
```
###### Example 1: Show an object
Usage: show <class_name> <_id>

```
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96971)}
(hbnb)  
```

###### Example 2: Destroy an object
Usage: destroy <class_name> <_id>
```
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
(hbnb)   
```

###### Example 3: Update an object
Usage: update <class_name> <_id>
```
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889), 
'updated_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729907), 'first_name': 'person'}
(hbnb)
```
