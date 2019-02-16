# Switches

## Basics

Like most languages, Ehlit supports comparison of a variable against multiple values at once :

```
switch status_code {
case 0
  everything_went_well()
case 1
  an_error_arised()
}
```

Nothing very new here, we use `switch` to specify the variable to check against, `case` to specify each test case, and the actions to perform after the case. The sequence of actions parsing stops at the next `case`.

## Fallback

If you really need it to keep going into the next `case`, you may use the `fallthrough` keyword :

```
switch status_code {
case 0
  everything_went_well()
case -1
  a_serious_error_arised()
  fallthrough
case 1
  an_error_arised()
}
```

Here, `an_error_arised` will be called both if `status_code` is equal to `-1` or `1`.

## Default

Now what if you want to handle all unhandled values ?

```
switch status_code {
case 0
  everything_went_well()
case -1
  a_serious_error_arised()
  fallthrough
case 1
  an_error_arised()
default
  something_really_serious_happened()
```

Just use `default` in place of `case`. It will handle all cases not handled previously.

## Chaining

One last question, what if you want to handle multiple cases the same way ?

```
switch status_code {
case 0
  everything_went_well()
case -1
  a_serious_error_arised()
  fallthrough
case 1
case 2
  an_error_arised()
default
  something_really_serious_happened()
```

Specify them one after the other, Ehlit is smart enough to handle them the same way

---

* [Home](../Readme.md)
* Basics
  1. [Functions](01_functions.md)
  1. [Conditions](02_conditions.md)
  1. [Loops](03_loops.md)
  1. [References](04_references.md)
  1. Switches
