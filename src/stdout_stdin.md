# Reading from Stdin and Writing to Stdout

## Stdout

To print something on the stdout we have two options, first we can print the expression or atom as is or we can convert the expression values to ASCII characters and print them to stdout.

| Symbol | What                                                                     | Notes                                                                 |
|:------:|:------------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| `::`   | Print the expression or atom to stdout as-is                             | `[:: mew mew]` will print `1 1` to stdout                             |
| `:::`  | Convert the next atom/expression to ASCII characters and print to stdout | `[:::['[+[* mewmewmew mewmew] mew] mewmew]]` will print `H` to stdout |
|        |                                                                          |                                                                       |

#### Examples

Here's a overly complicated `Hello World` program in mewl

```lisp
[=mew [[+[* mewmewmew mewmew] mew] mewmew] ] //H
[=mewmew [mew [- mew mew] mew]] //e
[=mewmewmew [mew [- mew mew] [* mewmewmewmew mewmew]]] //l
[=mewmewmewmew [mew mew mew]] //o
[=mewmewmewmewmew [mewmewmew mewmew]] //SPACE
[=mewmewmewmewmewmew [[* mewmewmewmew mewmew] mewmewmewmewmewmewmew]] //W
[=mewmewmewmewmewmewmew [mew mew mewmewmewmew]] //r
[=mewmewmewmewmewmewmewmew [mew [- mew mew] [- mew mew]]] //d
[=mewmewmewmewmewmewmewmewmew [mewmewmew mewmewmew]] //!

[::: ~mew //H
~mewmew //e
~mewmewmew //l
~mewmewmew //l
~mewmewmewmew //o
~mewmewmewmewmew //SPACE 
~mewmewmewmewmewmew //W
~mewmewmewmew //o
~mewmewmewmewmewmewmew //r
~mewmewmew //l
~mewmewmewmewmewmewmewmew //d
~mewmewmewmewmewmewmewmewmew //!
]
```



## Stdin
