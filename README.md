# Overview

This is a demonstration of the concepts I discuss in my OSDC 2010 presentation,
"Hugging Abstract Syntax Trees: A Pythonic Love Story".

Viking is a programming language compiler front end written in Python
for the Python VM. Viking programs can call Python code and vice versa
(the latter currently requires the use of the --compile flag).

The language itself resembles Python with curly braces.

Viking has been implemented as a poorly-written recursive descent parser.
It is half-baked, unsupported and very, very dirty. *Not for production use!*

# Usage

    #
    # Run a Viking source file
    #
    $ ./viking helloworld.vk

    #
    # Compile a Viking source file to a .pyc,
    # then run it using Python.
    #
    $ ./viking --compile helloworld.vk
    $ python helloworld.pyc

    #
    # Alternatively, you can import compiled
    # viking programs in Python.
    #
    $ python
    # ... snip ...
    >>> import helloworld
    Hello, World!
    >>>

