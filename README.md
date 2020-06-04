# lgtm-exercises
LGTM exercises


* Write a query which returns the length of the string "lgtm".
(Hint: here is the list of the functions that can be applied to strings.)
https://help.semmle.com/QL/ql-spec/language.html#built-ins-for-string

```lgtm
import cpp

from string str
where str = "lgtm"
select str.length()
```
