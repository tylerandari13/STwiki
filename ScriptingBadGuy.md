Summary
-------

A badguy that was given a name can be controlled by scripts.

Instance
--------

A `Badguy` is instantiated by placing a definition inside a level. It can then be accessed by its `name` from a script or via <code>sector.<var>name</var></code> from the console.

### Example

In the level file:

    (snowball
      ;the name and contents of the enemy may be different
      (name "Jeff")
      (direction "left")
      (x 640)
      (y 480)
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
