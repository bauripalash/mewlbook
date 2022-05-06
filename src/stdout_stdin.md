# Reading from Stdin and Writing to Stdout

## Writing to Stdout

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

## Reading From Stdin

| Symbol | What?                                                                 | Notes                                                                                |
| ------ | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| `\|>`  | Read a mew number or normal number from Stdin and store to a variable | Trailing whitespace gets trimmed                                                     |
| `\|    | >`                                                                    | Read a string from stdin, calculate the length of the string and store to a variable |

#### Read Mew/Normal Number from Stdin

Syntax of reading mew/normal number from stdin is:

```
[|> Variable_To_Store_Number]
```

Here's a simple example,

```lisp
[|> =mew]
[:: ~mew]
```

This example, reads a number/mewnum from stdin and prints it to stdout.

* Learn about [Identifiers/Assignment](./id_assign.md)

#### Read a String from Stdin and store the length

Syntax is just like reading number from stdin,

```
[||> =mew]
[:: ~mew]
```

Just like before, read a string from stdin and print the length of the string.

## Example/Usage

##### a. Count the character of a file using mewl

First, let's create a simple script (it is just the above example code)

```lisp
[||> =mew]
[:: ~mew]
```

save it with filename `char_len.mew.txt`

Now, we need the target file, from which we will count characters from, for this example we will create a file,

```bash
$ echo "Foo bar" >foobar.txt
```

Now, run

```shell
$ cat foobar.txt | mewl char_len.mew.txt
```

If everything is right, you'll see `7` in the terminal!
