Summary
-------

A decal that was given a name can be controlled by scripts.

Instance
--------

A `Decal` is instantiated by placing a definition inside a level. It can then be accessed by its `name` from a script or via <code>sector.<var>name</var></code> from the console.

### Example

In the level file:

    (decal
      (action "default")
      (sprite "/images/decal/explanations/billboard-bigtux.png")
      (name "decalio")
      (x 976)
      (y 192)
    )
In a script:

    decalio.fade_in(1.7)

In the console:

    sector.decalio.change_sprite("images/decal/retro/copter.png")

Methods
-------

| Method                      | Explanation                             |
|---------------------------- |---------------------------------------- |
| `fade_sprite(string new_sprite_name, float fade_time)` | Smoothly fades from one image to another. |
| `change_sprite(string new_sprite_name)` | Changes the image. (Drastic counterpart to `fade_sprite()`) |
| `fade_in(float fade_time)` | Fades in the sprite.                     |
| `fade_out(float fade_time)` | Fades out the sprite.                   |

Constants
---------

-   *None*
