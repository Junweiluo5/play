# play
play around: pratice of developing python package

objective: develop a toy python package

参考文献：
part 1: https://dagster.io/blog/python-packages-primer-1

part 2: https://dagster.io/blog/python-packages-primer-2

**Note**

1. Modules

**Modules** are the building blocks of Python packages. A module is a single ``Python file (.py)`` that contains definitions and statements. They provide a way to structure your code into logical units and reuse code across multiple projects.

2. Package

As your code grows, it can become difficult to manage and maintain all the code in a single module. **Packages** provide a way to organize and split your code into multiple **modules**, while still keeping everything organized and accessible.

steps to create a package
a. create a root directory (a python package is a folder(directory) on github)

b. create a __init__.py file under the root directory
    the __init__.py file can be empty 

3. __init__.py

__init__.py is a special file in Python packages that serves as an entry point for the package. It is executed when the package is imported, and its code can be used to initialize the package or set up any necessary components.

Prat 2: Python Package Index (PyPI/pip)

1. setup.py

setup.py is a file that you include in the root of your project, which contains information about your package and its dependencies. The file is used by pip, the package installer for Python, to install your package and its dependencies.

Template:
```
from setuptools import setup, find_packages

setup(
    name='your-package-name',
    version='0.0.1',
    description='A brief description of your package',
    author='Your Name',
    author_email='your.email@example.com',
    packages=find_packages(),
    install_requires=[
        'dependency1',
        'dependency2',
    ],
)
```

p.s. new way pyproject.toml

``pyproject.toml`` is a new file format introduced to replace setup.py for managing dependencies in Python projects. It was introduced as part of PEP 518 and PEP 621.

Template:

```
[project]
name = "your-package-name"
version = "0.0.1"
description = "A brief description of your package"
authors = ["Your Name <your.email@example.com>"]

[project.dependencies]
dependency1 = "^1.0"
dependency2 = "^2.0"
```