# how to use trimesh to create a line with selected color.



 when i use the `trimesh==3.20.0` to draw the symmetry axis of a model by following code, i meet some error.

```python
line = trimesh.load_path(np.array([point_start, point_end],
                         colors=[255, 0, 0, 255]))
scene.add_geometry(line)
```

```shell
ValueError('colors must be per-entity!')
```

It is beacause the keyparameter colors need the input dimension of (len(entities), 4) in the official package, but in fact, if we want to create a line, we can't get the number of the rendering points. So it has to visualize it with default color **black**.

If you want to use other color, you can try to change the following code in ` your\env\site-packages\trimesh\path\path.py` row 157.

the official function is 

```python
    @colors.setter
    def colors(self, values):
        """
        Set the color for every entity in the Path.

        Parameters
        ------------
        values : (len(entities), 4) uint8
          Color of each entity
        """
        # if not set return
        if values is None:
            return
        # make sure colors are RGBA
        colors = to_rgba(values)
        if len(colors) != len(self.entities):
            raise ValueError('colors must be per-entity!')
        # otherwise assign each color to the entity
        for c, e in zip(colors, self.entities):
            e.color = c
```

 than fix it with

```python
    @colors.setter
    def colors(self, values):
        """
        Set the color for every entity in the Path.

        Parameters
        ------------
        values : (len(entities), 4) uint8
          Color of each entity
        """
        # if not set return
        if values is None:
            return
        # make sure colors are RGBA
        colors = to_rgba(values)
        # otherwise assign each color to the entity
        for e in self.entities:
            e.color = colors
```

Than, you can use the `colors=` to definite your own color.




