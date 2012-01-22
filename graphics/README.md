Simple graphic functions
========================

It is all about the paths. Make a path and stroke it. Then go to the next path.

Define a path with

        newpath

and close it with

        closepath

Then stroke it, e. g.

        newpath
            % some magic graphic definitions
        closepath
        stroke

Path manipulators
-----------------

Be aware of newpath. It empties the current path and declares a new path. Thus stroke the paths before you define a new one.

+ moveto

    Moves the pen to these absolute position.

    Syntax:

        % put the coordinates on the stack
        x y

        moveto

    Stack transformation:

        obj_1...obj_i-2 obj_i-1 obj_i => obj_1...obj_i-2

+ lineto

    Draws a line from last moveto position to these absolute coordinates.

    Syntax:

        % put the coordinates on the stack
        x y

        lineto

    Stack transformation:

        obj_1...obj_i-2 obj_i-1 obj_i => obj_1...obj_i-2

+ rlineto

    Draws a line from last moveto position relativ to these coordinates.

    Syntax:

        % put the coordinates on the stack
        x y

        rlineto

    Stack transformation:

        obj_1...obj_i-2 obj_i-1 obj_i => obj_1...obj_i-2


+ rmoveto

    Moves the pen from last (r)moveto position relative to a new position.

    Syntax:

        % put the coordinates on the stack
        x y

        rmoveto

    Stack transformation:

        obj_1...obj_i-2 obj_i-1 obj_i => obj_1...obj_i-2

+ setlinewidth

    Set the width of the line

    Syntax:

        % put the width on the stack
        width

        setlinewidth

    Stack transformation:

        obj_1...obj_i => obj_1...obj_i-1

+ fill

    Fills the current path with ink.

    Syntax:

        fill

    Stack transformation:

        obj => obj

+ setgray

    Defines the shade of gray (0-1, float) in which the pen draws.

    Syntax

        % put the shade on the stack
        shade

        setgray

    Stack transformation:

        obj_1...obj_i => obj_1...obj_i-1

