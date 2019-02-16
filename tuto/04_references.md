# References

You may change the value of a variable from another scope with references. Lots of languages do it
transparently; in Ehlit this is explicit.

```
void setNumberTo42(ref int param) {
  param = 42
}

[...]

int nb
setNumberTo42(nb)
// nb == 42
```

You may have noted two things here. First, if you are familiar with the C pointers syntax, you may
notice that param have not been de-referenced. In Ehlit, when you use a reference as is, you are
using the deepest underlying variable. If you really need to manipulate the reference itself, you
may use the `ref` keyword :

```
str choice1 = "Choice 1"
str choice2 = "Choice 2"
str choice3 = "Choice 3"
ref str chosen

if choice == 1
  ref chosen = choice1
elif choice == 2
  ref chosen = choice2
elif choice == 3
  ref chosen = choice3
```

This may look strange if you are coming from a pointer based language like C, but with OO languages
like Ehlit you will find yourself using more often underlying values rather than references
themselves.

The second thing to note in the first example is that nb is not explicitely converted to a
reference. The compiler does it automatically, in most cases, you don't need to care about. The only
moment Ehlit may not infer it exactly is when converting the variable to the `any` type. In this
case, you may help the compiler with the `ref` keyword:

```
ref ref int deep = malloc([...])
free(ref ref deep)
```

---

* [Home](../Readme.md)
* Basics
  1. [Functions](01_functions.md)
  1. [Conditions](02_conditions.md)
  1. [Loops](03_loops.md)
  1. References
  1. [Switches](05_switches.md)
