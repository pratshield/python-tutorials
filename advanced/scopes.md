# Scopes in Python

When a Python interpreter is trying to look up a name, it uses the **LEGB** rule to resolve names. It checks the the existence of name in the L, E, G, B scopes in order below:

## Local scope
The area within the function body or a lambda expression

```
def local_func():
  x = 100 # local variable
  return x
```

## Enclosing scope
Assume we have a function called **outer** which has a nested function. Enclosing scope(nonlocal scope) is the area within the body of outer function

```
def outer():
  x = 100
  def local_func():
    nonlocal x # Use to override the nonlocal variable
    x = 200
    return x
  local_func()
```

## Global scope
The name in this scope are visible to all code in one Python script(in one file having a .py extension)

```
x = 100
def func1():
  global x # Use to override global variable
  x = 300
  return x
```

## Built-in scope
The names that exist in this scope are loaded when we run Python shell/script

Keywords like **in, as, and, def, class etc.** and expressions like **__main__, __file__, etc.** are some examples
