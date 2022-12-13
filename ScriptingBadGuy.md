Summary
-------

An background that was given a name can be controlled by scripts.

Instance
--------

A `Badguy` is instantiated by placing a definition inside a level. It can then be accessed by its `name` from a script or via <code>sector.<var>name</var></code> from the console.

### Example

In the level file:

    (background
      (color 1 1 1)
      (speed 0.5)
      (name "mountains")
      (image "images/background/antarctic/arctis2.png")
    )

In a script:

    mountain.set_color(0.6, 0.5, 0.1, 1)

In the console:

    sector.mountain.fade_color(0.6, 0.5, 0.1, 1, 0.5)

Methods
-------

| Method                      | Explanation                             |
|---------------------------- |---------------------------------------- |
| `float get_color_red()`     | gets the amount of red in the image     |
| `float get_color_green()`   | gets the amount of green in the image   |
| `float get_color_blue()`    | gets the amount of blue in the image    |
| `float get_color_alpha()`   | gets the amount of alpha in the image   |
| `set_color(float red, float green, float blue, float alpha)` | Instantly sets the color to the given values. |
| `fade_color(float red, float green, float blue, float alpha, float time)` | Fades from the current color to the new color in <var>time</var> seconds. |

Constants
---------

-   *None*
