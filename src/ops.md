# Basic Operations

## Binary Operations

Mewl supports few commonly used binary operators such as addition, subtraction, division, multiplication etc.

| Operation      | Symbol | Notes                        |
|:--------------:|:------:|:----------------------------:|
| Addition       | +      | -                            |
| Subtraction    | -      | -                            |
| Multiplication | *      | -                            |
| Division       | /      | [/ m1 m2 m3] -> m1 ÷ m2 ÷ m3 |
| Power          | **     | Evaluates just like division |
| Remainder      | %      | evaluates just like division |

## Unary Minus Operation

There're not specific way to use unary minus Operations in mewl, for example, [+ mew -mew]
This should've been evaluated like this , (+1 -1) = 0. But mewl will throw an error if you do something like that. If we want to get -1, we have to do something like this

```lisp
[- [- mew mew] mew]
```

It's basically, \\\(0-x = -x\\) 

## Bitwise Operations

⚠️ Important Reminder : As Bitwise operations cannot be applied on floating point numbers; and in mewl all numbers are 64bit floats, so before doing any bitwise operation numbers are converted to 64bit signed integers and the answer returned is converted to float from signed integer

| Operation   | Symbol | Notes                           |
|:-----------:|:------:|:-------------------------------:|
| Shift right | >>     | [>> m1 m2 m3] -> m1 >> m2 >> m3 |
| Shift Left  | <<     | Same as above                   |
| XOR         | ^      | "                               |
| AND         | &&     | "                               |
| OR          | ##     | "                               |
| NOT         | !!     | [Note1]                         |

🙀 [Note1] : As bitwise not `!!` Is an unary operation there can be unexpected behaviors if applied to an expression list, for that it will only be applied on the first element of an expression.

## Comparisons (Boolean Operations)

Important Note: In mewl `True = 1.0` (mew) and `False = 0.0` ([- mew mew])

| Operation             | Symbol | Note                                                                                       |
|:---------------------:|:------:|:------------------------------------------------------------------------------------------:|
| Is equal              | ==     | [== m1 m2 m3] -> m1== m2==m3                                                               |
| Not equal             | !=     | similar to previous                                                                        |
| Less than             | <      | "                                                                                          |
| Less than or equal    | <=     | "                                                                                          |
| Greater than          | >      | "                                                                                          |
| Greater than or equal | >=     | "                                                                                          |
| Or                    | #      | "                                                                                          |
| And                   | &      | "                                                                                          |
| Not                   | !      | As this is an unary operation so it's applied on the first element of the given expression |

# 
