ghostscript-fu
==============

Some ghostscript base knowledge.

Index
-----

1. math

Contains some simple math operations.

2. graphics

Contains some simple graphics operations.

Must-Knows
----------

+ Standard unit is inch.
+ All widths and coordinates are in inch
+ You have a unvisible pen, which you can control with path operations.

Base operators
--------------

The stacktransformation shows what the stack is before the command and what it is after the command is executed. An - signals an empty stack.

### Output operators

+ showpage

    Transfers the curent page to output device.

    Syntax:

        showpage

    Stacktransformation:

        obj_1...obj_i => obj_1...obj_i

### Stack operators

+ clear

    Removes all stack contents.

    Syntax:

        clear

    Stacktransformation:

        obj_1...obj_i => -

+ dup

    Duplicates top of the stack

    Syntax:

        dup

    Stacktransformation:

        ob => ob ob

+ exch

    Changes the two top level elements of the stack.

    Syntax:

        exch

    Stacktransformation:

        ob_1 ob_2 => ob_2 ob_1

+ pop

    Removes the first element of the stack.

    Syntax:

        pop

    Stacktransformation:

        ob_1 ob_2 => ob_1

### Interactive operators

+ ==

    Prints the first element of the stack and removes it.

    Syntax:

        ==

    Stacktransformation:

        ob => -

+ pstack

    Prints the content of the stack.

    Syntax:

        pstack

    Stacktransformation:

        ob_1...ob_i => ob_1...ob_i
