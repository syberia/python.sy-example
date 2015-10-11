# Example of Python Modules for R

Python is known for a stellar [module and import system](https://docs.python.org/2/tutorial/modules.html)
that makes it incredibly easy to manage dependencies and track the
etiology of local variables and functions.

This is an example [python.sy](https://github.com/robertzk/python.sy) project
that demonstrates an example of Python's module system ported to R using
[syberia](https://github.com/robertzk/syberia).

Example
-------
Opening the R console from the root of the project, we notice

```r
syberia_engine(".")$resource("toplevel")
# $chocolate
# [1] "Chocolate makes me happy!"
# 
# $coconut
# [1] "Eating coconut leaves one feeling delighted."
```

If you inspect [toplevel.R](toplevel.R), you will see it contains a "from-import" like
syntax:

```r
from(first.second.third) %import% c("chocolate", "coconut")

list(
  chocolate = chocolate("happy"),
  coconut   = coconut("delighted")
)
```

