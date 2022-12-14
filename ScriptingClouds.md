Summary
-------

Some clouds that were given a name can be controlled by scripts.

Instance
--------

`Clouds` are instantiated by placing a definition inside a level. It can then be accessed by its `name` from a script or via <code>sector.<var>name</var></code> from the console.

### Example

In the level file:

    (particles-clouds
      (z-pos -200)
      (intensity 15)
      (enabled #t)
      (name "Clouds")
    )
In a script:

    Clouds.set_enabled(true)

In the console:

    sector.Clouds.fade_speed(2, 3)

Methods
-------

| Method                      | Explanation                             |
|---------------------------- |---------------------------------------- |
| `set_enabled(bool enable)`  | Turns on or off the clouds.             |
| `bool get_enabled`          | Returns whether the clouds are visible. |
| `fade_speed(float speed, float time)` | Smoothly changes the speed of the clouds. |
| `fade_amount(int amount, float time)` | Smoothly changes the amount of clouds. |
| `set_amount(int amount, float time)` | Smoothly changes the amount of clouds? |

Constants
---------

-   *None*
