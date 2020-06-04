# lgtm-exercises
LGTM exercises

## Exercise 1

* Write a query which returns the length of the string "lgtm".
(Hint: here is the list of the functions that can be applied to strings.)
https://help.semmle.com/QL/ql-spec/language.html#built-ins-for-string

```lgtm
import cpp

from string str
where str = "lgtm"
select str.length()
```

## Exercise 2

Write a query which returns the sine of the minimum of 3^5 (3 raised to the power 5) and 245.6.

```
import cpp

from float val1, float val2, float val3, float res
where
  val1 = (3.0).pow(5.0)
  and val2 = 245.6
  and val3 = val1.minimum(val2)
  and res = val3.sin()
select res
```

* Result: __-0.8900093488562771__
