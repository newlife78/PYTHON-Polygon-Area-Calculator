Program Description:

This program create a Rectangle class and a Square class.
The Square class will be a subclass of Rectangle and inherit methods and attributes.


Rectangle class:
When a Rectangle object is created, it will be initialized with width and height attributes.
The class will also contain the following methods:

    . set_width
    . set_height
    . get_area: Returns area
    . get_perimeter: returns perimeter
    . get_diagonal: returns diagonal
    . get_picture: returns a string that represents the shape using lines of "*".
                   The number of lines are equal to the height and the number of "*" in each line are equal
                   to the width.
                   If the width or height is larger than 50, this will return the string:
                   "Too big for picture.".
    . get_amount_inside: takes another shape (square or rectangle) as an argument.
                         Returns the number of times the passed in shape can fit inside the shape (with no
                         rotations).
                         For instance, a rectangle with a width of 4 and a height of 8 can fit in two squares
                         with sides of 4.

Additionally, if an instance of a Rectangle is represented as a string, it should look like:
Rectangle(width=5, height=10)


Square class:
The Square class will be a subclass of Rectangle.
When a Square object is created, a single side length is passed in.
The __init__ method should store the side length in both the width and height attributes from the
Rectangle class.
The Square class will be able to access the Rectangle class methods but will also contain a set_side method.
If an instance of a Square is represented as a string, it should look like:
Square(side=9)

Additionally, the set_width and set_height methods on the Square class will set both the width and height.


Examples:
    . Code:
        rect = shape_calculator.Rectangle(10, 5)
        print(rect.get_area())
        rect.set_height(3)
        print(rect.get_perimeter())
        print(rect)
        print(rect.get_picture())

        sq = shape_calculator.Square(9)
        print(sq.get_area())
        sq.set_side(4)
        print(sq.get_diagonal())
        print(sq)
        print(sq.get_picture())

        rect.set_height(8)
        rect.set_width(16)
        print(rect.get_amount_inside(sq))

    . Code will return:
        50
        26
        Rectangle(width=10, height=3)
        **********
        **********
        **********

        81
        5.656854249492381
        Square(side=4)
        ****
        ****
        ****
        ****

        8


The unit tests for this project are in test_module.py.
