Summary
-------

`Camera` is an interface to manipulate the camera.

Instances
---------

An instance named `Camera` (`sector.Camera` in the console) is available. *(Note: doesn't having a class and an eponymous instance create a potential for conflicts? We should probably rename the instance or the class.)*

The *mode* of the camera is either **normal** (the camera is following the player) or **autoscroll**. In the latter mode the camera is forced along a specified [path](ScriptingPath "wikilink").

### Example

    (camera
      (mode "autoscroll")
      (path
        (node
          (x 0)
          (y 0)
          (time 250)
        )
        (node
          (x 19072)
          (y 0)
        )
      )
    )

Methods
-------

Method                                            | Explanation
--------------------------------------|-------------------------------------
`shake(float time, float x, float y)` | Moves camera to the given coordinates in <var>time</var> seconds returning quickly to the original position after that.
`set_pos(float x, float y)`           | Moves the camera to the specified absolute position. The origin is at the top left.
`set_mode(string modestring)`         | This function sets the camera mode. Valid values for <var>modestring</var> are “normal” and “manual”.
`scroll_to(float x, float y, float time)` | Scrolls the camera to the given coordinates within <var>time</var> seconds.
`float get_current_scale()`           | Get the curent scale factor of the camera.
`float get_target_scale()`            | Get the scale factor the camera is fading towards.
`set_scale(float scale)`              | Set the scale factor.
`scale(float scale, float time)`      | Fade the scale factor to <var>scale</var> over time.
`ease_scale(float scale, float time, string ease)` | Fade the scale factor to <var>scale</var> over time with <var>ease</var> easing (smooth movement).


Constants
---------

None
