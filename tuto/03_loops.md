# Loops

Like in C, there are multiple loop types. The `while` loop repeat an action as long as a condition
is true and has the same syntax than conditions:

```
while i < 5
	i++
```

If you need to perform the loop body at least once, the `do while` loop is for you:

```
do
	prompt_for_password()
while !password_match()
```

Last but not least, you may combine initialization, condition check and end-of-loop-action in a
`for do` loop. Let's add some security to the previous example :

```
for int failures = 0 do failures++ while !password_match() && failures < 5
	prompt_for_password()

// This is roughly the equivalent to :
int failures = 0
while !password_match() && failures < 5 {
	prompt_for_password()
	failures++
}
```

---

* [Home](../Readme.md)
* Basics
  1. [Functions](01_functions.md)
  1. [Conditions](02_conditions.md)
  1. Loops
  1. [References](04_references.md)
  1. [Switches](05_switches.md)
