Summary
-------

(to be added soon)

Instance
--------

A `Badguy` is instantiated by placing a definition inside a level. It can then be accessed by its `name` from a script or via <code>sector.<var>name</var></code> from the console.

### Example

In the level file:

    (particles-custom
      (texture
        (surface "/images/engine/editor/sparkle.png")
        (color_r 1)
        (color_g 1)
        (color_b 1)
        (color_a 1)
        (likeliness 1)
        (scale_x 1)
        (scale_y 1)
      )
      (main-texture "/images/engine/editor/sparkle.png")
      (birth-time 0)
      (death-time 0)
    )
In a script:

    Jeff.set_action("left", -1)

In the console:

    sector.Jeff.kill()

Methods
-------

| Method                      | Explanation                             |
|---------------------------- |---------------------------------------- |
| `kill()`                    | Kills the enemy.                        |
| `ignite()`                  | Kills the enemy with fire, playing iether the melting or burning animation. |
| `set_action(string action, int loops)` | Sets the action of the enemy. (defined in the enemies `.sprite` file) |
| `set_sprite(sprite)`        | Sets the enemies `.sprite` file.        |

Constants
---------

-   *None*
