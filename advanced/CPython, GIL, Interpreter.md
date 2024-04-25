## What is CPython
Python is interpreted language. Its code is first interpreted by another program(interpreter) and then compiled into bytecode which represents machine's instructions.

**CPython** is the implementation of Python whose bytecode is in C programming language.

**Jython** is the implementation of Python whose bytecode is in Java.

We also have **Cython** which is a compiled language used to create CPython extensions. **Cython** is a superset of Python that supports several C programming language features

## What is GIL
**GIL(Global Interpreter Lock)** is the most controversial and important feature of **CPython** based implementation of Python.

GIL is a tool that makes sure that only one thread at a time can execute a Python program.

For example, threat T1 acquires GIL and does its job. While the Python interpreter is using GIL to lock T1, all other threads have to wait.
After T1 finishes, it releases GIL and pass it to another thread T2 that needs it. This makes the the CPython thread-safe
