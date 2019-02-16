# Functions

Functions have quite the same syntax than in the C family of languages. Here is an example:

```
int multiply(int a, int b) {
  return a * b
}
```

Arguments may be made optional. In this case, when it is omitted, it will be replaced by its default
value at compilation time.

```
void scale(float factor = 1.0)
```

Order of functions doesn't matter, you may call a function declared later in the same file.

```
void caller() {
  callee()
}

void callee() {
  // Do something
}
```

---

* [Home](../Readme.md)
* Basics
  1. Functions
  1. [Conditions](02_conditions.md)
  1. [Loops](03_loops.md)
  1. [References](04_references.md)
  1. [Switches](05_switches.md)
