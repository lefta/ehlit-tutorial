# Conditions

In their basics and like lots of other things in ehlit, conditions have quite the same syntax than
in C. However, there are still some differences : `else if` have been shortened to `elif`, and the
parenthesis required around the condition have been dropped.

```
age = 25
if age < 18 {
	puts("You are young !")
} elif age < 60 {
	puts("You are an adult !")
} else {
	puts("You are old !")
}
```

Like in C, curly braces are optional, this would produce the same output :

```
age = 25
if age < 18
	puts("You are young !")
elif age < 60
	puts("You are an adult !")
else
	puts("You are old !")
```

## Condition operators

The same operators than in C are available : `&&` (logical and), `||` (logical or) and `^`
(logical exclusive or), `==` (equals), `!=` (not equals), `>` (greater than), `<` (lesser than),
`>=` (greater or equal), `<=` (lesser or equal).

```
age = 25
if age > 18 && age < 65
	puts("You are in age to work !")
```

There are shorteners for multiple standard conditions. A range check may be shortened to

```
if 18 <= age < 65
	puts(...)
```

`<` and `<=` may be used together, as well as `>` and `>=`. However, both sides of comparison may
not be used together

```
if 19 < age > 18  // Error
```

Several values may be compared for equality or inequality at once. To check if `i`, `j` and `k` are
equal to 5 :

```
if i == j == k == 5
```

Equality or inequality may be chained to will, but may not be mixed together

```
if i == j != 5 == k  # Error. Anyway, what should it mean ?
```

---

* [Home](../Readme.md)
* Basics
  1. [Functions](01_functions.md)
  1. Conditions
  1. [Loops](03_loops.md)
  1. [References](04_references.md)
  1. [Switches](05_switches.md)
