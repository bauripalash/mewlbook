# Identifiers and Assignment

In mewl, identifiers just look like mew numbers, so be careful when reading/writing mewl programs.

> **Some backstory**:
> 
> While I was designing mewl identifiers, I was confused about identifiers, I wanted something crazy but usable. So I just decided to go with `mew`, but to distinguish numbers from identifiers, I needed something *special* .  Now, please continue.

### Identifiers/Variables

In mewl, identifiers look something like this -> `~mew` , `~mewmew` etc.

So basically, Identifiers follow the same syntax as mew numbers but with a leading `~` (tilde) character.

`~mew` , `~mewmew` , `~mewmewmewmewmew` , these all are identifiers.

## Assignment

Assignments are little awkward, it'd be easy to understand with examples:

```
[=mew [+ mew mew]]
```

This expression assigns 2 to the variable `~mew` and this expression `[:: ~mew]` would print the value of variable `~mew` (which is 2 )

If you want to assign something to variable, write the identifier with a leading `=` (equal sign) without any space(s).

**In short**, `=mew` tells the interpreter to evaluate the following expression(s) and store it in variable `~mew`. 

For example,

`[=mewmew [* mewmew mewmew]]` would store 9 in a variable which can be accessed via `~mewmew`.

I know, it is confusing. 

## More examples:

* `[=mewmewmew [+ mew mew [* mewmew mewmew]]]` would store 6 to a variable which to be accessed via `~mewmewmew`

* Another one
  
  ```lisp
  [=mewmewmewmewmew [' mew mew mewmew]]
  [:: ~mewmewmewmewmew]
  ```
  
  it would print 112 to stdout

**[Info Note]**: Assiging something using `=mewmewmewmewmew` wouldn't change the meaning of `mewmewmewmewmew` as a mew number which still is `5`
